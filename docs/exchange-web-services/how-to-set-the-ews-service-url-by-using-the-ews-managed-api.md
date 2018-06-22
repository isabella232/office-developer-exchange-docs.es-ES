---
title: Establecer la dirección URL de servicio EWS mediante el uso de la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cddf6525-1c04-484b-a911-56c2f0f1f7b6
description: Este documento puede incluir contenido relacionado con funciones o productos preliminares que pueden cambiar mucho antes del lanzamiento comercial final. Este documento se proporciona "tal cual" solamente con fines informativos y Microsoft no realiza ninguna garantía, explícita ni implícita, en el documento. Infórmese sobre cómo establecer la dirección URL del servicio EWS en la aplicación de API administrada de EWS.
ms.openlocfilehash: e1a414f7c6f13bd61a58403c9d2be546c0226a69
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763167"
---
# <a name="set-the-ews-service-url-by-using-the-ews-managed-api"></a><span data-ttu-id="efe32-103">Establecer la dirección URL de servicio EWS mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="efe32-103">Set the EWS service URL by using the EWS Managed API</span></span>

<span data-ttu-id="efe32-104">Este documento puede incluir contenido relacionado con funciones o productos preliminares que pueden cambiar mucho antes del lanzamiento comercial final. Este documento se proporciona "tal cual" solamente con fines informativos y Microsoft no realiza ninguna garantía, explícita ni implícita, en el documento. Infórmese sobre cómo establecer la dirección URL del servicio EWS en la aplicación de API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="efe32-104">Find information about how to set the EWS service URL in your EWS Managed API application.</span></span>
  
<span data-ttu-id="efe32-p101">La dirección URL del servicio es la dirección que Exchange usa para comunicarse con los servicios Web Exchange (EWS). Una vez que la aplicación de API administrada de EWS tiene esta dirección y el debido acceso para [comunicarse con EWS](how-to-communicate-with-ews-by-using-the-ews-managed-api.md), puede hacer llamadas a la [clase ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx). La URL del servicio para un servidor de Exchange local puede tener el aspecto siguiente.</span><span class="sxs-lookup"><span data-stu-id="efe32-p101">The service URL is the address that Exchange uses to communicate with Exchange Web Services (EWS). After your EWS Managed API application has this address, and has appropriate access to [communicate with EWS](how-to-communicate-with-ews-by-using-the-ews-managed-api.md), it can make calls to the [ExchangeService class](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx). The service URL for an on-premises Exchange server might look like the following.</span></span> 
  
```HTML
https://computer.domain.contoso.com/EWS/Exchange.asmx
```

<span data-ttu-id="efe32-p102">La dirección URL de EWS se puede establecer en la aplicación de dos formas. Le recomendamos que use el [servicio Detección automática](http://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx) para obtener la dirección URL porque, en un busque grande de servidores, la dirección URL puede cambiar si el buzón de correo se migra a otro servidor. Sin embargo, como la llamada a Detección automática puede tardar y ralentizar la aplicación (en el caso de que tenga que realizar varias llamadas en un breve período de tiempo), conviene almacenar en caché el valor de la URL obtenido de Detección automática y establecer manualmente la dirección URL del servicio EWS con dicho valor. De esta forma se logra mejorar el rendimiento de la aplicación. Debe asegurarse de usar Detección automática para actualizar periódicamente el valor almacenado en caché por si acaso cambia en el servidor.</span><span class="sxs-lookup"><span data-stu-id="efe32-p102">You can set the EWS URL in your application in a couple of ways. We recommend that you use the [Autodiscover service](http://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx) to get the URL because in a large forest of servers, the URL can change if the mailbox is migrated to another server. However, because calling Autodiscover can take some time and can slow down your application if you need to make multiple calls in a short period of time, you might want to cache the URL value you get from Autodiscover and manually set the EWS service URL with this cached value. This will improve the performance of your application; just make sure that you use Autodiscover to update your cached value periodically in case the value changes on the server.</span></span> 
  
## <a name="set-the-ews-service-url-by-using-the-autodiscover-service"></a><span data-ttu-id="efe32-112">Establecer la dirección URL del servicio EWS usando el servicio Detección automática</span><span class="sxs-lookup"><span data-stu-id="efe32-112">Set the EWS service URL by using the Autodiscover service</span></span>
<span data-ttu-id="efe32-113"><a name="bk_SetURLusingAutoDiscover"> </a></span><span class="sxs-lookup"><span data-stu-id="efe32-113"></span></span>

<span data-ttu-id="efe32-p103">El método [AutodiscoverUrl](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.autodiscoverurl%28v=exchg.80%29.aspx) usa la dirección de correo electrónico para establecer el extremo [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) y permite a la aplicación usar los métodos incluidos en las clases proxy **ExchangeService**. El ejemplo siguiente muestra cómo usar el método **AutodiscoverURL**.</span><span class="sxs-lookup"><span data-stu-id="efe32-p103">The [AutodiscoverUrl](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.autodiscoverurl%28v=exchg.80%29.aspx) method uses the email address to set the [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) endpoint and enables your application to use any methods included in the **ExchangeService** proxy classes. The following example shows how to use the **AutodiscoverURL** method.</span></span> 
  
```cs
// Create the binding.
ExchangeService service = new ExchangeService();
// Set the credentials for the on-premises server.
service.Credentials = new WebCredentials("user1@contoso.com", "password");
// Set the URL.
service.AutodiscoverUrl("User1@contoso.com");

```

## <a name="set-the-exchange-service-url-manually"></a><span data-ttu-id="efe32-116">Establecer la dirección URL del servicio de Exchange manualmente</span><span class="sxs-lookup"><span data-stu-id="efe32-116">Set the Exchange service URL manually</span></span>
<span data-ttu-id="efe32-117"><a name="bk_SetURLmanually"> </a></span><span class="sxs-lookup"><span data-stu-id="efe32-117"></span></span>

<span data-ttu-id="efe32-p104">El ejemplo siguiente muestra cómo establecer la dirección URL del servicio EWS mediante un valor almacenado en caché. Antes de hacerlo, use el servicio Detección automática para obtener la dirección URL de EWS.</span><span class="sxs-lookup"><span data-stu-id="efe32-p104">The following example shows you how to set the EWS service URL by using a cached value. Before you do this, make sure to use the Autodiscover service to get the EWS URL.</span></span>
  
```cs
// Create the binding.
ExchangeService service = new ExchangeService();
// Set the credentials for the on-premises server.
service.Credentials = new WebCredentials("user1@contoso.com", "password");
// Set the URL.
service.Url = new Uri("https://computername.domain.contoso.com/EWS/Exchange.asmx");

```

## <a name="see-also"></a><span data-ttu-id="efe32-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="efe32-120">See also</span></span>

- [<span data-ttu-id="efe32-121">Empezar a trabajar con aplicaciones de cliente de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="efe32-121">Get started with EWS Managed API client applications</span></span>](get-started-with-ews-managed-api-client-applications.md)   
- [<span data-ttu-id="efe32-122">Configurar el entorno de desarrollo de aplicación de Exchange</span><span class="sxs-lookup"><span data-stu-id="efe32-122">Setting up your Exchange application development environment</span></span>](setting-up-your-exchange-application-development-environment.md)   
- [<span data-ttu-id="efe32-123">Controlar el acceso a EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="efe32-123">Control access to EWS in Exchange</span></span>](how-to-control-access-to-ews-in-exchange.md) 
- [<span data-ttu-id="efe32-124">Comunicarse con EWS mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="efe32-124">Communicate with EWS by using the EWS Managed API</span></span>](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)  
- [<span data-ttu-id="efe32-125">Usar detección automática para buscar puntos de conexión</span><span class="sxs-lookup"><span data-stu-id="efe32-125">Use Autodiscover to find connection points</span></span>](how-to-use-autodiscover-to-find-connection-points.md)
    

