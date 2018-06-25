---
title: Validar un certificado de servidor para la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1fe0b215-8340-4bc8-a6ce-4f591ca9e353
description: Obtenga información sobre cómo crear y hacer referencia a un método de devolución de llamada de validación de certificados para que pueda realizar las solicitudes de la API administrada de EWS para un servidor de Exchange.
ms.openlocfilehash: 13d7c51e55308b9e9997697a075c8a9e6b4f10d0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763183"
---
# <a name="validate-a-server-certificate-for-the-ews-managed-api"></a>Validar un certificado de servidor para la API administrada de EWS

Obtenga información sobre cómo crear y hacer referencia a un método de devolución de llamada de validación de certificados para que pueda realizar las solicitudes de la API administrada de EWS para un servidor de Exchange.
  
De forma predeterminada, las versiones de Exchange a partir de Exchange 2007 SP1 utilizan autofirmados X509 certificados para autenticar las llamadas de EWS. Cuando se usa la API administrada de EWS, debe crear un método de devolución de llamada de validación de certificado; de lo contrario, se producirá un error en las solicitudes de la API administrada de EWS. Si se usa el servicio de detección automática, se producirá un error en la llamada al método de detección automática de EWS Managed API con un error de **AutodiscoverLocalException** . Si usa a un proxy de servicio web generado por el web, también es posible que tener que crear un método de devolución de llamada de validación, dependiendo de cómo se creó el proxy. 
  
## <a name="prerequisites-for-creating-a-validation-callback-method"></a>Requisitos previos para crear un método de devolución de llamada de validación
<a name="bk_prereq"> </a>

Para configurar para validar un certificado de servidor, asegúrese de que los siguientes sean verdaderas: 
  
- El servidor de Exchange está usando un certificado autofirmado de EWS. Si el administrador ha instalado un certificado válido que hace un seguimiento para un certificado raíz, no es necesario crear un método de devolución de llamada de validación. 
    
- Va a crear una aplicación administrada que incluye una referencia a los siguientes espacios de nombres de .NET Framework necesarias: 
    
  - **System.Net**
  - **System.Net.Security**  
  - **System.Security.Cryptography.X509Certificates**
    
## <a name="example-callback-method-to-validate-a-server-certificate-for-the-ews-managed-api"></a>Ejemplo: El método de devolución de llamada para validar un certificado de servidor para la API administrada de EWS
<a name="bk_example"> </a>

En el ejemplo de código siguiente se muestra cómo crear un X509 método de devolución de llamada de validación de certificados para la API administrada de EWS. Este método valida un X509 de certificados y sólo devuelve true cuando se cumplen cualquiera de los siguientes criterios: 
  
- El certificado es válido y realiza un seguimiento de vuelta a un certificado raíz válido.    
- El certificado es válido y autofirmado por el servidor que se devuelve. 
    
> [!IMPORTANT]
> El método de devolución de llamada de validación de certificados en este ejemplo, proporciona seguridad suficiente para el desarrollo y prueba de aplicaciones de la API administrada de EWS. Sin embargo, es posible que proporcionar seguridad suficiente para la aplicación implementada. Siempre debe asegurarse de que el método de devolución de llamada de validación de certificado que usar cumple los requisitos de seguridad de la organización. 
  
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

Utilice la clase **ServicePointManager** en el espacio de nombres .NET **System.Net** para enlazar un método de devolución de llamada de validación estableciendo la propiedad **ServerCertificateValidationCallback** . Puede utilizar código similar al siguiente ejemplo de código para establecer la propiedad **ServerCertificateValidationCallback** . 
  
```cs
ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;

```

## <a name="next-steps"></a>Siguientes pasos
<a name="bk_example"> </a>

Después de haber creado el método de devolución de llamada de validación para la API administrada de EWS, puede usar el servicio Detección automática para obtener los puntos de conexión y la configuración de dominio y usuario desde un servidor de Exchange. Para obtener más información, vea los siguientes artículos:
  
- [Usar detección automática para buscar puntos de conexión](how-to-use-autodiscover-to-find-connection-points.md)
    
- [Obtener la configuración de usuario de Exchange mediante el uso de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [Obtener la configuración de dominio de un servidor de Exchange](how-to-get-domain-settings-from-an-exchange-server.md)
    
## <a name="see-also"></a>Vea también

- [Configurar una aplicación de EWS](setting-up-your-ews-application.md)  
- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)
    

