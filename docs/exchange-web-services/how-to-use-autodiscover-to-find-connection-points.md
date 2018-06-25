---
title: Usar detección automática para buscar puntos de conexión
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03896542-549b-4c45-973c-98f9025ea26c
description: Descubra cómo usar el servicio Detección automática para indicar a su aplicación de cliente al servidor de Exchange correcto.
ms.openlocfilehash: 653fcd1c094c23c3e89e903b7194b96720802b51
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763185"
---
# <a name="use-autodiscover-to-find-connection-points"></a><span data-ttu-id="49df3-103">Usar detección automática para buscar puntos de conexión</span><span class="sxs-lookup"><span data-stu-id="49df3-103">Use Autodiscover to find connection points</span></span>

<span data-ttu-id="49df3-104">Descubra cómo usar el servicio Detección automática para indicar a su aplicación de cliente al servidor de Exchange correcto.</span><span class="sxs-lookup"><span data-stu-id="49df3-104">Find out how to use the Autodiscover service to direct your client application to the correct Exchange server.</span></span>
  
<span data-ttu-id="49df3-105">El servicio de detección automática de Exchange proporciona la aplicación de cliente con opciones de configuración para las cuentas de correo electrónico que se hospedan en Exchange Online, Exchange Online como parte de Office 365 o un servidor de Exchange que ejecuta una versión de Exchange a partir de Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="49df3-105">The Exchange Autodiscover service provides your client application with configuration settings for email accounts that are hosted on Exchange Online, Exchange Online as part of Office 365, or an Exchange server running a version of Exchange starting with Exchange 2013.</span></span> <span data-ttu-id="49df3-106">El servicio Detección automática es un servicio web que proporciona opciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="49df3-106">The Autodiscover service is a web service that provides configuration settings.</span></span> <span data-ttu-id="49df3-107">El servicio Detección automática es un servicio web que proporciona información de configuración de Exchange server a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="49df3-107">The Autodiscover service is a web service that provides Exchange server configuration information to your client application.</span></span> <span data-ttu-id="49df3-108">Las aplicaciones cliente usan la detección automática para determinar el extremo del servicio de detección automática para un buzón específico.</span><span class="sxs-lookup"><span data-stu-id="49df3-108">Client applications use Autodiscover to determine the endpoint of the Autodiscover service for a specific mailbox.</span></span> <span data-ttu-id="49df3-109">En este artículo se explica cómo debe seguir las respuestas de un servidor de Exchange para buscar el extremo correcto.</span><span class="sxs-lookup"><span data-stu-id="49df3-109">This article explains how to follow the responses from an Exchange server to find the correct endpoint.</span></span> 
  
<span data-ttu-id="49df3-110">Para obtener información acerca de cómo obtener los valores de configuración de dirección de correo electrónico, vea [obtener la configuración de usuario de Exchange mediante el uso de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) y [obtendrá la configuración de dominio de un servidor de Exchange](how-to-get-domain-settings-from-an-exchange-server.md).</span><span class="sxs-lookup"><span data-stu-id="49df3-110">For information about how to get email address configuration settings, see [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) and [Get domain settings from an Exchange server](how-to-get-domain-settings-from-an-exchange-server.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="49df3-111">El proceso para buscar el extremo correcto es parte de la solicitud de configuración de usuario o dominio.</span><span class="sxs-lookup"><span data-stu-id="49df3-111">The process for finding the correct endpoint is part of the request for user or domain settings.</span></span> <span data-ttu-id="49df3-112">El servicio Detección automática usa una serie de respuestas de redirección para enviar la aplicación cliente en el extremo correcto para una dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="49df3-112">The Autodiscover service uses a series of redirect responses to send the client application to the correct endpoint for an email address.</span></span> 
  
<span data-ttu-id="49df3-113">Puede usar una de las siguientes tecnologías de desarrollo de Exchange para tener acceso al servicio de detección automática:</span><span class="sxs-lookup"><span data-stu-id="49df3-113">You can use one of the following Exchange development technologies to access the Autodiscover service:</span></span>
  
> [!NOTE]
> <span data-ttu-id="49df3-114">Para obtener más información acerca de estas tecnologías de desarrollo de Exchange, vea [Explorar la API administrada de EWS, EWS y web de servicios de Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="49df3-114">For more information about these Exchange development technologies, see [Explore the EWS Managed API, EWS, and web services in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md).</span></span> 
  
- <span data-ttu-id="49df3-115">La API administrada de servicios Web Exchange (EWS)</span><span class="sxs-lookup"><span data-stu-id="49df3-115">The Exchange Web Services (EWS) Managed API</span></span>
    
- <span data-ttu-id="49df3-116">EWS</span><span class="sxs-lookup"><span data-stu-id="49df3-116">EWS</span></span>
    
    <span data-ttu-id="49df3-117">Si usa EWS, puede usar los métodos siguientes para recuperar la configuración de usuario:</span><span class="sxs-lookup"><span data-stu-id="49df3-117">If you are using EWS, you can use the following methods to retrieve user settings:</span></span>
    
  - <span data-ttu-id="49df3-118">El servicio Detección automática basado en SOAP</span><span class="sxs-lookup"><span data-stu-id="49df3-118">The SOAP-based Autodiscover service</span></span>
    
  - <span data-ttu-id="49df3-119">El servicio Detección automática XML (POX)</span><span class="sxs-lookup"><span data-stu-id="49df3-119">The XML (POX) Autodiscover service</span></span>
    
  - <span data-ttu-id="49df3-120">Un proxy generado automáticamente se ha generado del servicio Detección automática de XML o SOAP</span><span class="sxs-lookup"><span data-stu-id="49df3-120">An autogenerated proxy generated from the SOAP or XML Autodiscover service</span></span>
    
    <span data-ttu-id="49df3-121">Para obtener más información acerca de estos métodos, vea [detección automática de Exchange](autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="49df3-121">For more information about these methods, see [Autodiscover for Exchange](autodiscover-for-exchange.md).</span></span>
    
<span data-ttu-id="49df3-p103">La API administrada de EWS proporciona una interfaz basada en objetos para recuperar la configuración de usuario. Si su aplicación cliente usa un código administrado, le recomendamos que use la API administrada de EWS. La interfaz de la API administrada de EWS está mejor optimizada para un modelo de objetos simples que el típico proxy de servicio web generado automáticamente. </span><span class="sxs-lookup"><span data-stu-id="49df3-p103">The EWS Managed API provides an object-based interface for retrieving user settings. If your client application uses managed code, we recommend that you use the EWS Managed API. The EWS Managed API interface is better optimized for a simple object model than the typical autogenerated web service proxy.</span></span> 
  
<span data-ttu-id="49df3-125">Si está usando EWS, le sugerimos que use el servicio Detección automática de SOAP, ya que admite un conjunto superior de características que el servicio Detección automática de POX.</span><span class="sxs-lookup"><span data-stu-id="49df3-125">If you are using EWS, we suggest that you use the SOAP Autodiscover service, because it supports a richer set of features than the POX Autodiscover service.</span></span>
  
## <a name="prerequisites-for-finding-an-endpoint"></a><span data-ttu-id="49df3-126">Requisitos previos de la búsqueda de un extremo</span><span class="sxs-lookup"><span data-stu-id="49df3-126">Prerequisites for finding an endpoint</span></span>
<span data-ttu-id="49df3-127"><a name="bk_Prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="49df3-127"></span></span>

<span data-ttu-id="49df3-128">Antes de poder crear una aplicación cliente que usa el servicio de detección automática, necesita tener acceso a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="49df3-128">Before you can create a client application that uses the Autodiscover service, you need to have access to the following:</span></span>
  
- <span data-ttu-id="49df3-129">Exchange Online o un servidor que está ejecutando una versión de Exchange a partir de Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="49df3-129">Exchange Online or a server that is running a version of Exchange starting with Exchange 2007 SP1.</span></span> <span data-ttu-id="49df3-130">Si está usando el servicio Detección automática basada en SOAP, Exchange Online o una versión de Exchange a partir de Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="49df3-130">If you are using the SOAP-based Autodiscover service, Exchange Online or a version of Exchange starting with Exchange 2010.</span></span>
    
- <span data-ttu-id="49df3-131">Un servidor de Exchange que está configurado para aceptar conexiones desde la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="49df3-131">An Exchange server that is configured to accept connections from your client application.</span></span> <span data-ttu-id="49df3-132">Para obtener información acerca de cómo configurar el servidor de Exchange, vea [controlar el acceso de la aplicación de cliente para EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="49df3-132">For information about how to configure your Exchange server, see [Controlling client application access to EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).</span></span>
    
- <span data-ttu-id="49df3-133">Una cuenta que está autorizada para uso de EWS.</span><span class="sxs-lookup"><span data-stu-id="49df3-133">An account that is authorized to use EWS.</span></span> <span data-ttu-id="49df3-134">Para obtener información acerca de cómo configurar una cuenta, vea [controlar el acceso de la aplicación de cliente para EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="49df3-134">For information about how to configure an account, see [Controlling client application access to EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="49df3-135">Si está utilizando la API administrada de EWS, debe proporcionar una devolución de llamada de validación de certificado en algunas circunstancias.</span><span class="sxs-lookup"><span data-stu-id="49df3-135">If you are using the EWS Managed API, you must provide a certificate validation callback in some circumstances.</span></span> <span data-ttu-id="49df3-136">También es posible que deba una devolución de llamada de validación de certificado con algunas bibliotecas proxy generado, como las creadas por Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="49df3-136">You may also need a certificate validation callback with some generated proxy libraries, such as those created by Visual Studio.</span></span> <span data-ttu-id="49df3-137">Para obtener más información, vea [validar un certificado de servidor para la API administrada de EWS](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span><span class="sxs-lookup"><span data-stu-id="49df3-137">For more information, see [Validate a server certificate for the EWS Managed API](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span></span> 
  
### <a name="core-concepts-for-finding-an-endpoint"></a><span data-ttu-id="49df3-138">Conceptos básicos de la búsqueda de un extremo</span><span class="sxs-lookup"><span data-stu-id="49df3-138">Core concepts for finding an endpoint</span></span>
<span data-ttu-id="49df3-139"><a name="bk_Core"> </a></span><span class="sxs-lookup"><span data-stu-id="49df3-139"></span></span>

<span data-ttu-id="49df3-140">Antes de usar detección automática para encontrar un extremo, debe estar familiarizado con los conceptos que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="49df3-140">Before you use Autodiscover to find an endpoint, you should be familiar with the concepts listed in the following table.</span></span>
  
|<span data-ttu-id="49df3-141">**Concepto**</span><span class="sxs-lookup"><span data-stu-id="49df3-141">**Concept**</span></span>|<span data-ttu-id="49df3-142">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="49df3-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49df3-143">Detección automática de Exchange</span><span class="sxs-lookup"><span data-stu-id="49df3-143">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md) <br/> |<span data-ttu-id="49df3-144">Proporciona información general del funcionamiento del servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="49df3-144">Provides an overview of how the Autodiscover service works.</span></span>  <br/> |
   
<span data-ttu-id="49df3-145">Si está utilizando la API administrada de EWS, use la clase [Microsoft.Exchange.WebServices.Data.ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) en el espacio de nombres [Microsoft.Exchange.WebServices.Data](http://msdn.microsoft.com/en-us/library/dd633907%28v=exchg.80%29.aspx) para administrar la conexión a EWS.</span><span class="sxs-lookup"><span data-stu-id="49df3-145">If you are using the EWS Managed API, you use the [Microsoft.Exchange.WebServices.Data.ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) class in the [Microsoft.Exchange.WebServices.Data](http://msdn.microsoft.com/en-us/library/dd633907%28v=exchg.80%29.aspx) namespace to manage your connection to EWS.</span></span> <span data-ttu-id="49df3-146">Para usar los ejemplos de código de API administrada de EWS en este artículo, debe hacer referencia a los siguientes espacios de nombres en el código:</span><span class="sxs-lookup"><span data-stu-id="49df3-146">To use the EWS Managed API code samples in this article, you need to reference the following namespaces in your code:</span></span> 
  
- <span data-ttu-id="49df3-147">**System.Net**</span><span class="sxs-lookup"><span data-stu-id="49df3-147">**System.Net**</span></span>
    
- <span data-ttu-id="49df3-148">**Microsoft.Exchange.WebServices.Data.ExchangeService**</span><span class="sxs-lookup"><span data-stu-id="49df3-148">**Microsoft.Exchange.WebServices.Data.ExchangeService**</span></span>
    
## <a name="find-the-correct-endpoint-by-using-the-ews-managed-api"></a><span data-ttu-id="49df3-149">Buscar el extremo correcto mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="49df3-149">Find the correct endpoint by using the EWS Managed API</span></span>
<span data-ttu-id="49df3-150"><a name="bk_Managed"> </a></span><span class="sxs-lookup"><span data-stu-id="49df3-150"></span></span>

<span data-ttu-id="49df3-151">Si está utilizando la API administrada de EWS, llamadas al servicio de detección automática se controlan mediante la clase **ExchangeService** .</span><span class="sxs-lookup"><span data-stu-id="49df3-151">If you are using the EWS Managed API, calls to the Autodiscover service are handled by the **ExchangeService** class.</span></span> <span data-ttu-id="49df3-152">Para determinar el extremo correcto para una cuenta de correo electrónico, llama al método **AutodiscoverUrl** en un objeto **[ExchangeService]** .</span><span class="sxs-lookup"><span data-stu-id="49df3-152">To determine the correct endpoint for an email account, you call the **AutodiscoverUrl** method on an **[ExchangeService]** object.</span></span> <span data-ttu-id="49df3-153">En el ejemplo de código siguiente se muestra cómo establecer el extremo de servicio web EWS para una dirección de correo electrónico en el archivo Exchange.asmx en el servidor de acceso de cliente correcto mediante el uso de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="49df3-153">The following code example shows how to set the EWS web service endpoint for an email address to the Exchange.asmx file on the correct Client Access server by using the EWS Managed API.</span></span> 
  
```cs
NetworkCredential credentials = new NetworkCredential(securelyStoredEmail, securelyStoredPassword);
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2013);
service.Credentials = credentials;
service.AutodiscoverUrl("User1@contoso.com");
```

## <a name="find-the-correct-endpoint-by-using-ews"></a><span data-ttu-id="49df3-154">Buscar el extremo correcto mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="49df3-154">Find the correct endpoint by using EWS</span></span>
<span data-ttu-id="49df3-155"><a name="bk_SOAP"> </a></span><span class="sxs-lookup"><span data-stu-id="49df3-155"></span></span>

<span data-ttu-id="49df3-156">El servicio de detección automática de SOAP puede utilizar una serie de solicitudes y respuestas para dirigir la aplicación para el extremo correcto para EWS.</span><span class="sxs-lookup"><span data-stu-id="49df3-156">The SOAP Autodiscover service may use a series of requests and responses to direct your application to the correct endpoint for EWS.</span></span> <span data-ttu-id="49df3-157">Para obtener información acerca del proceso para determinar el extremo correcto para una cuenta de correo electrónico, vea [detección automática de Exchange](autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="49df3-157">For information about the process for determining the correct endpoint for an email account, see [Autodiscover for Exchange](autodiscover-for-exchange.md).</span></span> <span data-ttu-id="49df3-158">Los siguientes ejemplos XML muestran la serie de solicitudes y respuestas que puede esperar cuando se realiza una solicitud de detección automática de SOAP para encontrar el extremo correcto.</span><span class="sxs-lookup"><span data-stu-id="49df3-158">The following XML examples show the series of requests and responses that you can expect when making a SOAP Autodiscover request to find the correct endpoint.</span></span>
  
### <a name="soap-autodiscover-endpoint-request"></a><span data-ttu-id="49df3-159">Solicitud de extremo de detección automática SOAP</span><span class="sxs-lookup"><span data-stu-id="49df3-159">SOAP Autodiscover endpoint request</span></span>

<span data-ttu-id="49df3-160">En el ejemplo siguiente se muestra una solicitud XML que se envía al servicio de detección automática para buscar el extremo correcto.</span><span class="sxs-lookup"><span data-stu-id="49df3-160">The following example shows an XML request that is sent to the Autodiscover service to find the correct endpoint.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://mail.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>User1@Contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>InternalEwsUrl</a:Setting>
          <a:Setting>ExternalEwsUrl</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>

```

### <a name="soap-autodiscover-redirection-response"></a><span data-ttu-id="49df3-161">Respuesta de redirección de detección automática SOAP</span><span class="sxs-lookup"><span data-stu-id="49df3-161">SOAP Autodiscover redirection response</span></span>

<span data-ttu-id="49df3-162">El servicio Detección automática puede responder con una de las dos respuestas de redirección: una redirección HTTP 302 o una respuesta de redirección de SOAP.</span><span class="sxs-lookup"><span data-stu-id="49df3-162">The Autodiscover service may respond with one of two redirection responses: an HTTP 302 redirect, or a SOAP redirection response.</span></span> <span data-ttu-id="49df3-163">Si la respuesta del servidor de Exchange es un redireccionamiento 302 de HTTP, la aplicación cliente debe validar que la dirección de redireccionamiento es aceptable y, a continuación, siga la respuesta de redirección.</span><span class="sxs-lookup"><span data-stu-id="49df3-163">If the response from the Exchange server is an HTTP 302 redirect, the client application should validate that the redirection address is acceptable and then follow the redirection response.</span></span>
  
> [! Nota de seguridad]<span data-ttu-id="49df3-164"> para criterios para validar una respuesta de redirección, vea [detección automática de Exchange](autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="49df3-164"> For criteria for validating a redirection response, see [Autodiscover for Exchange](autodiscover-for-exchange.md).</span></span> 
  
<span data-ttu-id="49df3-165">Si el servicio Detección automática devuelve una respuesta de redirección, indicada por el elemento [ErrorCode](http://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) del elemento **UserResponse** , la aplicación cliente debe usar el elemento **RedirectTarget** para crear una nueva solicitud de configuración que es se envían al servidor especificado en la respuesta de redirección.</span><span class="sxs-lookup"><span data-stu-id="49df3-165">If the Autodiscover service returns a redirection response, indicated by the [ErrorCode](http://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) element of the **UserResponse** element, your client application should use the **RedirectTarget** element to construct a new settings request that is sent to the server specified in the redirection response.</span></span> <span data-ttu-id="49df3-166">En el ejemplo siguiente se muestra una respuesta de redirección desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="49df3-166">The following example shows a redirection response from the server.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>682</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>RedirectAddress</ErrorCode>
            <ErrorMessage>Redirection address.</ErrorMessage>
            <RedirectTarget>User1@mail.Contoso.com</RedirectTarget>
            <UserSettingErrors />
            <UserSettings />
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="49df3-167">Después de una redirección, el cliente utiliza la dirección URL de redirección para preparar otra solicitud.</span><span class="sxs-lookup"><span data-stu-id="49df3-167">After a redirection, the client uses the redirection URL to prepare another request.</span></span> <span data-ttu-id="49df3-168">El código siguiente muestra un ejemplo de la solicitud que cree a partir de la respuesta de redirección.</span><span class="sxs-lookup"><span data-stu-id="49df3-168">The following code shows an example of the request that you create from the redirection response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>User1@mail.Contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>InternalEwsUrl</a:Setting>
          <a:Setting>ExternalEwsUrl</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="49df3-169">Cuando haya se ha indicado a la aplicación cliente para el extremo correcto para el servicio Detección automática, el servidor enviará una respuesta con el elemento [ErrorCode](http://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) del elemento **UserResponse** establecida en **NoError** y que contiene la información solicitada configuración del usuario.</span><span class="sxs-lookup"><span data-stu-id="49df3-169">When the client application has been directed to the correct endpoint for the Autodiscover service, the server will send a response with the [ErrorCode](http://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) element of the **UserResponse** element set to **NoError** and containing the requested user settings.</span></span> <span data-ttu-id="49df3-170">Sólo la configuración de usuario solicitado, **InternalEwsUrl** y **ExternalEwsUrl**, se devuelve.</span><span class="sxs-lookup"><span data-stu-id="49df3-170">Only the requested user settings, **InternalEwsUrl** and **ExternalEwsUrl**, are returned.</span></span> <span data-ttu-id="49df3-171">En el ejemplo siguiente se muestra la respuesta del servidor.</span><span class="sxs-lookup"><span data-stu-id="49df3-171">The following example shows the response from the server.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>160</h:MajorBuildNumber>
      <h:MinorBuildNumber>4</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>NoError</ErrorCode>
            <ErrorMessage>No error.</ErrorMessage>
            <RedirectTarget i:nil="true" />
            <UserSettingErrors />
            <UserSettings>
              <UserSetting i:type="StringSetting">
                <Name>InternalEwsUrl</Name>
                <Value>https://server.Contoso.com/ews/exchange.asmx</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ExternalEwsUrl</Name>
                <Value>https://server.Contoso.com/ews/exchange.asmx</Value>
              </UserSetting>
            </UserSettings>
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

## <a name="next-steps"></a><span data-ttu-id="49df3-172">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="49df3-172">Next steps</span></span>
<span data-ttu-id="49df3-173"><a name="bk_Next"> </a></span><span class="sxs-lookup"><span data-stu-id="49df3-173"></span></span>

<span data-ttu-id="49df3-174">Buscar el extremo siguiendo el proceso de detección automática devuelve el dominio solicitado o la configuración del usuario.</span><span class="sxs-lookup"><span data-stu-id="49df3-174">Finding the endpoint by following the Autodiscover process returns the requested domain or user settings.</span></span> <span data-ttu-id="49df3-175">Para obtener información acerca de cómo realizar una solicitud para configuraciones específicas, vea los siguientes artículos:</span><span class="sxs-lookup"><span data-stu-id="49df3-175">For information about making a request for specific settings, see the following articles:</span></span>
  
- [<span data-ttu-id="49df3-176">Obtener la configuración de dominio de un servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="49df3-176">Get domain settings from an Exchange server</span></span>](how-to-get-domain-settings-from-an-exchange-server.md)
    
- [<span data-ttu-id="49df3-177">Obtener la configuración de usuario de Exchange mediante el uso de detección automática</span><span class="sxs-lookup"><span data-stu-id="49df3-177">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
## <a name="see-also"></a><span data-ttu-id="49df3-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="49df3-178">See also</span></span>


- [<span data-ttu-id="49df3-179">Configurar una aplicación de EWS</span><span class="sxs-lookup"><span data-stu-id="49df3-179">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)
    
- [<span data-ttu-id="49df3-180">Detección automática de Exchange</span><span class="sxs-lookup"><span data-stu-id="49df3-180">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)
    
- [<span data-ttu-id="49df3-181">Referencia de servicio web de detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="49df3-181">Autodiscover web service reference for Exchange</span></span>](http://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)
    
- [<span data-ttu-id="49df3-182">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="49df3-182">EWS reference for Exchange</span></span>](http://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)
    

