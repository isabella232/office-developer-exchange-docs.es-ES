---
title: Validar un certificado de servidor para la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 1fe0b215-8340-4bc8-a6ce-4f591ca9e353
description: Obtenga información sobre cómo crear y hacer referencia a un método de devolución de llamada de validación de certificados para que pueda realizar solicitudes de la API administrada de EWS a un servidor de Exchange.
localization_priority: Priority
ms.openlocfilehash: 195c51ca71890d6092e4182d23990bb528d37095
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456783"
---
# <a name="validate-a-server-certificate-for-the-ews-managed-api"></a>Validar un certificado de servidor para la API administrada de EWS

Obtenga información sobre cómo crear y hacer referencia a un método de devolución de llamada de validación de certificados para que pueda realizar solicitudes de la API administrada de EWS a un servidor de Exchange.
  
De forma predeterminada, las versiones de Exchange que comienzan con Exchange 2007 SP1 usan certificados X509 autofirmados para autenticar llamadas de EWS. Cuando se usa la API administrada de EWS, es necesario crear un método de devolución de llamada de validación de certificados; de lo contrario, se producirá un error en las solicitudes de API administrada EWS. Si usa el servicio Detección automática, se producirá un error **AutodiscoverLocalException** en la llamada al método detección automática de la API administrada de EWS. Si usa un proxy de servicio Web generado por Web, es posible que también tenga que crear un método de devolución de llamada de validación, en función de cómo se cree el proxy. 
  
## <a name="prerequisites-for-creating-a-validation-callback-method"></a>Requisitos previos para crear un método de devolución de llamada de validación
<a name="bk_prereq"> </a>

Para configurar la validación de un certificado de servidor, asegúrese de que se cumplen las siguientes condiciones: 
  
- El servidor de Exchange usa un certificado autofirmado para EWS. Si el administrador ha instalado un certificado válido que realiza el seguimiento de un certificado raíz, no es necesario crear un método de devolución de llamada de validación. 
    
- Está creando una aplicación administrada que incluye una referencia a los siguientes espacios de nombres de .NET Framework necesarios: 
    
  - **System.Net**
  - **System .net. Security**  
  - **System. Security. Cryptography. X509Certificates**
    
## <a name="example-callback-method-to-validate-a-server-certificate-for-the-ews-managed-api"></a>Ejemplo: método de devolución de llamada para validar un certificado de servidor para la API administrada de EWS
<a name="bk_example"> </a>

En el siguiente ejemplo de código se muestra cómo crear un método de devolución de llamada de validación de certificado X509 para la API administrada de EWS. Este método validará un certificado X509 y solo devolverá True cuando se cumpla cualquiera de los siguientes criterios: 
  
- El certificado es válido y se vuelve a trazar a un certificado raíz válido.    
- El certificado es válido y está autofirmado por el servidor que lo devolvió. 
    
> [!IMPORTANT]
> El método de devolución de llamada de validación de certificados en este ejemplo proporciona la seguridad suficiente para el desarrollo y las pruebas de las aplicaciones de API administrada de EWS. Sin embargo, es posible que no proporcione suficiente seguridad para la aplicación implementada. Siempre debe asegurarse de que el método de devolución de llamada de validación de certificados que use cumple con los requisitos de seguridad de su organización. 
  
```cs
      private static bool CertificateValidationCallBack(
         object sender,
         System.Security.Cryptography.X509Certificates.X509Certificate certificate,
         System.Security.Cryptography.X509Certificates.X509Chain chain,
         System.Net.Security.SslPolicyErrors sslPolicyErrors)
    {
      // If the certificate is a valid, signed certificate, return true.
      if (sslPolicyErrors == System.Net.Security.SslPolicyErrors.None)
      {
        return true;
      }
      // If there are errors in the certificate chain, look at each error to determine the cause.
      if ((sslPolicyErrors &amp; System.Net.Security.SslPolicyErrors.RemoteCertificateChainErrors) != 0)
      {
        if (chain != null &amp;&amp; chain.ChainStatus != null)
        {
          foreach (System.Security.Cryptography.X509Certificates.X509ChainStatus status in chain.ChainStatus)
          {
            if ((certificate.Subject == certificate.Issuer) &amp;&amp;
               (status.Status == System.Security.Cryptography.X509Certificates.X509ChainStatusFlags.UntrustedRoot))
            {
              // Self-signed certificates with an untrusted root are valid. 
              continue;
            }
            else
            {
              if (status.Status != System.Security.Cryptography.X509Certificates.X509ChainStatusFlags.NoError)
              {
                // If there are any other errors in the certificate chain, the certificate is invalid,
             // so the method returns false.
                return false;
              }
            }
          }
        }
        // When processing reaches this line, the only errors in the certificate chain are 
    // untrusted root errors for self-signed certificates. These certificates are valid
    // for default Exchange server installations, so return true.
        return true;
      }
      else
      {
     // In all other cases, return false.
        return false;
      }
    }

```

La clase **ServicePointManager** se usa en el espacio de nombres de .net **System.net** para enlazar un método de devolución de llamada de validación mediante la configuración de la propiedad **ServerCertificateValidationCallback** . Puede usar código similar al siguiente ejemplo de código para establecer la propiedad **ServerCertificateValidationCallback** . 
  
```cs
ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;

```

## <a name="next-steps"></a>Siguientes pasos
<a name="bk_example"> </a>

Una vez que haya creado el método de devolución de llamada de validación para la API administrada de EWS, puede usar el servicio de detección automática para obtener puntos de conexión y la configuración de usuario y dominio de un servidor de Exchange. Para obtener más información, consulte los siguientes artículos:
  
- [Usar autodetección para buscar puntos de conexión](how-to-use-autodiscover-to-find-connection-points.md)
    
- [Obtener la configuración de usuario de Exchange mediante el uso de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [Obtener la configuración de dominio de un servidor de Exchange](how-to-get-domain-settings-from-an-exchange-server.md)
    
## <a name="see-also"></a>Vea también

- [Configurar la aplicación EWS](setting-up-your-ews-application.md)  
- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)
    

