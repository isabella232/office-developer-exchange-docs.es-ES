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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763183"
---
# <a name="validate-a-server-certificate-for-the-ews-managed-api"></a><span data-ttu-id="30c30-103">Validar un certificado de servidor para la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="30c30-103">Validate a server certificate for the EWS Managed API</span></span>

<span data-ttu-id="30c30-104">Obtenga información sobre cómo crear y hacer referencia a un método de devolución de llamada de validación de certificados para que pueda realizar las solicitudes de la API administrada de EWS para un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="30c30-104">Learn how to create and reference a certificate validation callback method so that you can make EWS Managed API requests to an Exchange server.</span></span>
  
<span data-ttu-id="30c30-105">De forma predeterminada, las versiones de Exchange a partir de Exchange 2007 SP1 utilizan autofirmados X509 certificados para autenticar las llamadas de EWS.</span><span class="sxs-lookup"><span data-stu-id="30c30-105">By default, versions of Exchange starting with Exchange 2007 SP1 use self-signed X509 certificates to authenticate calls from EWS.</span></span> <span data-ttu-id="30c30-106">Cuando se usa la API administrada de EWS, debe crear un método de devolución de llamada de validación de certificado; de lo contrario, se producirá un error en las solicitudes de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="30c30-106">When you are using the EWS Managed API, you need to create a certificate validation callback method; otherwise, EWS Managed API requests will fail.</span></span> <span data-ttu-id="30c30-107">Si se usa el servicio de detección automática, se producirá un error en la llamada al método de detección automática de EWS Managed API con un error de **AutodiscoverLocalException** .</span><span class="sxs-lookup"><span data-stu-id="30c30-107">If you are using the Autodiscover service, the call to the EWS Managed API Autodiscover method will fail with an **AutodiscoverLocalException** error.</span></span> <span data-ttu-id="30c30-108">Si usa a un proxy de servicio web generado por el web, también es posible que tener que crear un método de devolución de llamada de validación, dependiendo de cómo se creó el proxy.</span><span class="sxs-lookup"><span data-stu-id="30c30-108">If you are using a web-generated web service proxy, you might also have to create a validation callback method, depending on how the proxy is created.</span></span> 
  
## <a name="prerequisites-for-creating-a-validation-callback-method"></a><span data-ttu-id="30c30-109">Requisitos previos para crear un método de devolución de llamada de validación</span><span class="sxs-lookup"><span data-stu-id="30c30-109">Prerequisites for creating a validation callback method</span></span>
<span data-ttu-id="30c30-110"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="30c30-110"></span></span>

<span data-ttu-id="30c30-111">Para configurar para validar un certificado de servidor, asegúrese de que los siguientes sean verdaderas:</span><span class="sxs-lookup"><span data-stu-id="30c30-111">To set up to validate a server certificate, ensure that the following are true:</span></span> 
  
- <span data-ttu-id="30c30-112">El servidor de Exchange está usando un certificado autofirmado de EWS.</span><span class="sxs-lookup"><span data-stu-id="30c30-112">Your Exchange server is using a self-signed certificate for EWS.</span></span> <span data-ttu-id="30c30-113">Si el administrador ha instalado un certificado válido que hace un seguimiento para un certificado raíz, no es necesario crear un método de devolución de llamada de validación.</span><span class="sxs-lookup"><span data-stu-id="30c30-113">If the administrator has installed a valid certificate that traces to a root certificate, you do not need to create a validation callback method.</span></span> 
    
- <span data-ttu-id="30c30-114">Va a crear una aplicación administrada que incluye una referencia a los siguientes espacios de nombres de .NET Framework necesarias:</span><span class="sxs-lookup"><span data-stu-id="30c30-114">You are creating a managed application that includes a reference to the following required .NET Framework namespaces:</span></span> 
    
  - <span data-ttu-id="30c30-115">**System.Net**</span><span class="sxs-lookup"><span data-stu-id="30c30-115">**System.Net**</span></span>
  - <span data-ttu-id="30c30-116">**System.Net.Security**</span><span class="sxs-lookup"><span data-stu-id="30c30-116">**System.Net.Security**</span></span>  
  - <span data-ttu-id="30c30-117">**System.Security.Cryptography.X509Certificates**</span><span class="sxs-lookup"><span data-stu-id="30c30-117">**System.Security.Cryptography.X509Certificates**</span></span>
    
## <a name="example-callback-method-to-validate-a-server-certificate-for-the-ews-managed-api"></a><span data-ttu-id="30c30-118">Ejemplo: El método de devolución de llamada para validar un certificado de servidor para la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="30c30-118">Example: Callback method to validate a server certificate for the EWS Managed API</span></span>
<span data-ttu-id="30c30-119"><a name="bk_example"> </a></span><span class="sxs-lookup"><span data-stu-id="30c30-119"></span></span>

<span data-ttu-id="30c30-120">En el ejemplo de código siguiente se muestra cómo crear un X509 método de devolución de llamada de validación de certificados para la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="30c30-120">The following code example shows how to create an X509 certificate validation callback method for the EWS Managed API.</span></span> <span data-ttu-id="30c30-121">Este método valida un X509 de certificados y sólo devuelve true cuando se cumplen cualquiera de los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="30c30-121">This method will validate an X509 certificate and only return true when either of the following criteria are met:</span></span> 
  
- <span data-ttu-id="30c30-122">El certificado es válido y realiza un seguimiento de vuelta a un certificado raíz válido.</span><span class="sxs-lookup"><span data-stu-id="30c30-122">The certificate is valid and traces back to a valid root certificate.</span></span>    
- <span data-ttu-id="30c30-123">El certificado es válido y autofirmado por el servidor que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="30c30-123">The certificate is valid and is self-signed by the server that returned it.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="30c30-124">El método de devolución de llamada de validación de certificados en este ejemplo, proporciona seguridad suficiente para el desarrollo y prueba de aplicaciones de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="30c30-124">The certificate validation callback method in this example provides sufficient security for development and testing of EWS Managed API applications.</span></span> <span data-ttu-id="30c30-125">Sin embargo, es posible que proporcionar seguridad suficiente para la aplicación implementada.</span><span class="sxs-lookup"><span data-stu-id="30c30-125">However, it might not provide sufficient security for your deployed application.</span></span> <span data-ttu-id="30c30-126">Siempre debe asegurarse de que el método de devolución de llamada de validación de certificado que usar cumple los requisitos de seguridad de la organización.</span><span class="sxs-lookup"><span data-stu-id="30c30-126">You should always make sure that the certificate validation callback method that you use meets the security requirements of your organization.</span></span> 
  
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

<span data-ttu-id="30c30-127">Utilice la clase **ServicePointManager** en el espacio de nombres .NET **System.Net** para enlazar un método de devolución de llamada de validación estableciendo la propiedad **ServerCertificateValidationCallback** .</span><span class="sxs-lookup"><span data-stu-id="30c30-127">You use the **ServicePointManager** class in the .NET **System.Net** namespace to hook up a validation callback method by setting the **ServerCertificateValidationCallback** property.</span></span> <span data-ttu-id="30c30-128">Puede utilizar código similar al siguiente ejemplo de código para establecer la propiedad **ServerCertificateValidationCallback** .</span><span class="sxs-lookup"><span data-stu-id="30c30-128">You can use code similar to the following code example to set the **ServerCertificateValidationCallback** property.</span></span> 
  
```cs
ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;

```

## <a name="next-steps"></a><span data-ttu-id="30c30-129">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="30c30-129">Next steps</span></span>
<span data-ttu-id="30c30-130"><a name="bk_example"> </a></span><span class="sxs-lookup"><span data-stu-id="30c30-130"></span></span>

<span data-ttu-id="30c30-131">Después de haber creado el método de devolución de llamada de validación para la API administrada de EWS, puede usar el servicio Detección automática para obtener los puntos de conexión y la configuración de dominio y usuario desde un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="30c30-131">After you have created the validation callback method for the EWS Managed API, you can use the Autodiscover service to get connection points and user and domain settings from an Exchange server.</span></span> <span data-ttu-id="30c30-132">Para obtener más información, vea los siguientes artículos:</span><span class="sxs-lookup"><span data-stu-id="30c30-132">For more information, see the following articles:</span></span>
  
- [<span data-ttu-id="30c30-133">Usar detección automática para buscar puntos de conexión</span><span class="sxs-lookup"><span data-stu-id="30c30-133">Use Autodiscover to find connection points</span></span>](how-to-use-autodiscover-to-find-connection-points.md)
    
- [<span data-ttu-id="30c30-134">Obtener la configuración de usuario de Exchange mediante el uso de detección automática</span><span class="sxs-lookup"><span data-stu-id="30c30-134">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [<span data-ttu-id="30c30-135">Obtener la configuración de dominio de un servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="30c30-135">Get domain settings from an Exchange server</span></span>](how-to-get-domain-settings-from-an-exchange-server.md)
    
## <a name="see-also"></a><span data-ttu-id="30c30-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="30c30-136">See also</span></span>

- [<span data-ttu-id="30c30-137">Configurar una aplicación de EWS</span><span class="sxs-lookup"><span data-stu-id="30c30-137">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)  
- [<span data-ttu-id="30c30-138">Empezar a utilizar servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="30c30-138">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    

