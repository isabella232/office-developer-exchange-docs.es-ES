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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456783"
---
# <a name="validate-a-server-certificate-for-the-ews-managed-api"></a><span data-ttu-id="c857d-103">Validar un certificado de servidor para la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="c857d-103">Validate a server certificate for the EWS Managed API</span></span>

<span data-ttu-id="c857d-104">Obtenga información sobre cómo crear y hacer referencia a un método de devolución de llamada de validación de certificados para que pueda realizar solicitudes de la API administrada de EWS a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c857d-104">Learn how to create and reference a certificate validation callback method so that you can make EWS Managed API requests to an Exchange server.</span></span>
  
<span data-ttu-id="c857d-105">De forma predeterminada, las versiones de Exchange que comienzan con Exchange 2007 SP1 usan certificados X509 autofirmados para autenticar llamadas de EWS.</span><span class="sxs-lookup"><span data-stu-id="c857d-105">By default, versions of Exchange starting with Exchange 2007 SP1 use self-signed X509 certificates to authenticate calls from EWS.</span></span> <span data-ttu-id="c857d-106">Cuando se usa la API administrada de EWS, es necesario crear un método de devolución de llamada de validación de certificados; de lo contrario, se producirá un error en las solicitudes de API administrada EWS.</span><span class="sxs-lookup"><span data-stu-id="c857d-106">When you are using the EWS Managed API, you need to create a certificate validation callback method; otherwise, EWS Managed API requests will fail.</span></span> <span data-ttu-id="c857d-107">Si usa el servicio Detección automática, se producirá un error **AutodiscoverLocalException** en la llamada al método detección automática de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="c857d-107">If you are using the Autodiscover service, the call to the EWS Managed API Autodiscover method will fail with an **AutodiscoverLocalException** error.</span></span> <span data-ttu-id="c857d-108">Si usa un proxy de servicio Web generado por Web, es posible que también tenga que crear un método de devolución de llamada de validación, en función de cómo se cree el proxy.</span><span class="sxs-lookup"><span data-stu-id="c857d-108">If you are using a web-generated web service proxy, you might also have to create a validation callback method, depending on how the proxy is created.</span></span> 
  
## <a name="prerequisites-for-creating-a-validation-callback-method"></a><span data-ttu-id="c857d-109">Requisitos previos para crear un método de devolución de llamada de validación</span><span class="sxs-lookup"><span data-stu-id="c857d-109">Prerequisites for creating a validation callback method</span></span>
<span data-ttu-id="c857d-110"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="c857d-110"><a name="bk_prereq"> </a></span></span>

<span data-ttu-id="c857d-111">Para configurar la validación de un certificado de servidor, asegúrese de que se cumplen las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="c857d-111">To set up to validate a server certificate, ensure that the following are true:</span></span> 
  
- <span data-ttu-id="c857d-112">El servidor de Exchange usa un certificado autofirmado para EWS.</span><span class="sxs-lookup"><span data-stu-id="c857d-112">Your Exchange server is using a self-signed certificate for EWS.</span></span> <span data-ttu-id="c857d-113">Si el administrador ha instalado un certificado válido que realiza el seguimiento de un certificado raíz, no es necesario crear un método de devolución de llamada de validación.</span><span class="sxs-lookup"><span data-stu-id="c857d-113">If the administrator has installed a valid certificate that traces to a root certificate, you do not need to create a validation callback method.</span></span> 
    
- <span data-ttu-id="c857d-114">Está creando una aplicación administrada que incluye una referencia a los siguientes espacios de nombres de .NET Framework necesarios:</span><span class="sxs-lookup"><span data-stu-id="c857d-114">You are creating a managed application that includes a reference to the following required .NET Framework namespaces:</span></span> 
    
  - <span data-ttu-id="c857d-115">**System.Net**</span><span class="sxs-lookup"><span data-stu-id="c857d-115">**System.Net**</span></span>
  - <span data-ttu-id="c857d-116">**System .net. Security**</span><span class="sxs-lookup"><span data-stu-id="c857d-116">**System.Net.Security**</span></span>  
  - <span data-ttu-id="c857d-117">**System. Security. Cryptography. X509Certificates**</span><span class="sxs-lookup"><span data-stu-id="c857d-117">**System.Security.Cryptography.X509Certificates**</span></span>
    
## <a name="example-callback-method-to-validate-a-server-certificate-for-the-ews-managed-api"></a><span data-ttu-id="c857d-118">Ejemplo: método de devolución de llamada para validar un certificado de servidor para la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="c857d-118">Example: Callback method to validate a server certificate for the EWS Managed API</span></span>
<span data-ttu-id="c857d-119"><a name="bk_example"> </a></span><span class="sxs-lookup"><span data-stu-id="c857d-119"><a name="bk_example"> </a></span></span>

<span data-ttu-id="c857d-120">En el siguiente ejemplo de código se muestra cómo crear un método de devolución de llamada de validación de certificado X509 para la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="c857d-120">The following code example shows how to create an X509 certificate validation callback method for the EWS Managed API.</span></span> <span data-ttu-id="c857d-121">Este método validará un certificado X509 y solo devolverá True cuando se cumpla cualquiera de los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="c857d-121">This method will validate an X509 certificate and only return true when either of the following criteria are met:</span></span> 
  
- <span data-ttu-id="c857d-122">El certificado es válido y se vuelve a trazar a un certificado raíz válido.</span><span class="sxs-lookup"><span data-stu-id="c857d-122">The certificate is valid and traces back to a valid root certificate.</span></span>    
- <span data-ttu-id="c857d-123">El certificado es válido y está autofirmado por el servidor que lo devolvió.</span><span class="sxs-lookup"><span data-stu-id="c857d-123">The certificate is valid and is self-signed by the server that returned it.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="c857d-124">El método de devolución de llamada de validación de certificados en este ejemplo proporciona la seguridad suficiente para el desarrollo y las pruebas de las aplicaciones de API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="c857d-124">The certificate validation callback method in this example provides sufficient security for development and testing of EWS Managed API applications.</span></span> <span data-ttu-id="c857d-125">Sin embargo, es posible que no proporcione suficiente seguridad para la aplicación implementada.</span><span class="sxs-lookup"><span data-stu-id="c857d-125">However, it might not provide sufficient security for your deployed application.</span></span> <span data-ttu-id="c857d-126">Siempre debe asegurarse de que el método de devolución de llamada de validación de certificados que use cumple con los requisitos de seguridad de su organización.</span><span class="sxs-lookup"><span data-stu-id="c857d-126">You should always make sure that the certificate validation callback method that you use meets the security requirements of your organization.</span></span> 
  
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

<span data-ttu-id="c857d-127">La clase **ServicePointManager** se usa en el espacio de nombres de .net **System.net** para enlazar un método de devolución de llamada de validación mediante la configuración de la propiedad **ServerCertificateValidationCallback** .</span><span class="sxs-lookup"><span data-stu-id="c857d-127">You use the **ServicePointManager** class in the .NET **System.Net** namespace to hook up a validation callback method by setting the **ServerCertificateValidationCallback** property.</span></span> <span data-ttu-id="c857d-128">Puede usar código similar al siguiente ejemplo de código para establecer la propiedad **ServerCertificateValidationCallback** .</span><span class="sxs-lookup"><span data-stu-id="c857d-128">You can use code similar to the following code example to set the **ServerCertificateValidationCallback** property.</span></span> 
  
```cs
ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;

```

## <a name="next-steps"></a><span data-ttu-id="c857d-129">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="c857d-129">Next steps</span></span>
<span data-ttu-id="c857d-130"><a name="bk_example"> </a></span><span class="sxs-lookup"><span data-stu-id="c857d-130"><a name="bk_example"> </a></span></span>

<span data-ttu-id="c857d-131">Una vez que haya creado el método de devolución de llamada de validación para la API administrada de EWS, puede usar el servicio de detección automática para obtener puntos de conexión y la configuración de usuario y dominio de un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c857d-131">After you have created the validation callback method for the EWS Managed API, you can use the Autodiscover service to get connection points and user and domain settings from an Exchange server.</span></span> <span data-ttu-id="c857d-132">Para obtener más información, consulte los siguientes artículos:</span><span class="sxs-lookup"><span data-stu-id="c857d-132">For more information, see the following articles:</span></span>
  
- [<span data-ttu-id="c857d-133">Usar autodetección para buscar puntos de conexión</span><span class="sxs-lookup"><span data-stu-id="c857d-133">Use Autodiscover to find connection points</span></span>](how-to-use-autodiscover-to-find-connection-points.md)
    
- [<span data-ttu-id="c857d-134">Obtener la configuración de usuario de Exchange mediante el uso de detección automática</span><span class="sxs-lookup"><span data-stu-id="c857d-134">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [<span data-ttu-id="c857d-135">Obtener la configuración de dominio de un servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="c857d-135">Get domain settings from an Exchange server</span></span>](how-to-get-domain-settings-from-an-exchange-server.md)
    
## <a name="see-also"></a><span data-ttu-id="c857d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="c857d-136">See also</span></span>

- [<span data-ttu-id="c857d-137">Configurar la aplicación EWS</span><span class="sxs-lookup"><span data-stu-id="c857d-137">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)  
- [<span data-ttu-id="c857d-138">Empezar a usar los servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="c857d-138">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    

