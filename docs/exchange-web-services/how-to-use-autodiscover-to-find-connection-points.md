---
title: Usar autodetección para buscar puntos de conexión
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 03896542-549b-4c45-973c-98f9025ea26c
description: Descubra cómo usar el servicio de detección automática para dirigir la aplicación cliente al servidor Exchange correcto.
localization_priority: Priority
ms.openlocfilehash: c1895fa0d2cce489467a726614e9457052624ef6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527596"
---
# <a name="use-autodiscover-to-find-connection-points"></a><span data-ttu-id="31172-103">Usar autodetección para buscar puntos de conexión</span><span class="sxs-lookup"><span data-stu-id="31172-103">Use Autodiscover to find connection points</span></span>

<span data-ttu-id="31172-104">Descubra cómo usar el servicio de detección automática para dirigir la aplicación cliente al servidor Exchange correcto.</span><span class="sxs-lookup"><span data-stu-id="31172-104">Find out how to use the Autodiscover service to direct your client application to the correct Exchange server.</span></span>
  
<span data-ttu-id="31172-105">El servicio Detección automática de Exchange proporciona a la aplicación cliente opciones de configuración para las cuentas de correo electrónico que se hospedan en Exchange Online, Exchange online como parte de Office 365, o un servidor de Exchange que ejecuta una versión de Exchange que empieza por Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="31172-105">The Exchange Autodiscover service provides your client application with configuration settings for email accounts that are hosted on Exchange Online, Exchange Online as part of Office 365, or an Exchange server running a version of Exchange starting with Exchange 2013.</span></span> <span data-ttu-id="31172-106">El servicio de detección automática es un servicio Web que proporciona opciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="31172-106">The Autodiscover service is a web service that provides configuration settings.</span></span> <span data-ttu-id="31172-107">El servicio de detección automática es un servicio Web que proporciona información de configuración de Exchange Server a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="31172-107">The Autodiscover service is a web service that provides Exchange server configuration information to your client application.</span></span> <span data-ttu-id="31172-108">Las aplicaciones cliente usan detección automática para determinar el punto final del servicio Detección automática para un buzón específico.</span><span class="sxs-lookup"><span data-stu-id="31172-108">Client applications use Autodiscover to determine the endpoint of the Autodiscover service for a specific mailbox.</span></span> <span data-ttu-id="31172-109">En este artículo se explica cómo seguir las respuestas de un servidor de Exchange para encontrar el punto de conexión correcto.</span><span class="sxs-lookup"><span data-stu-id="31172-109">This article explains how to follow the responses from an Exchange server to find the correct endpoint.</span></span> 
  
<span data-ttu-id="31172-110">Para obtener información sobre cómo obtener las opciones de configuración de direcciones de correo electrónico, consulte [obtener configuración de usuario de Exchange mediante la detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) y [obtener la configuración de dominio de un servidor de Exchange](how-to-get-domain-settings-from-an-exchange-server.md).</span><span class="sxs-lookup"><span data-stu-id="31172-110">For information about how to get email address configuration settings, see [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) and [Get domain settings from an Exchange server](how-to-get-domain-settings-from-an-exchange-server.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="31172-111">El proceso para buscar el punto de conexión correcto forma parte de la solicitud de configuración de usuario o dominio.</span><span class="sxs-lookup"><span data-stu-id="31172-111">The process for finding the correct endpoint is part of the request for user or domain settings.</span></span> <span data-ttu-id="31172-112">El servicio Detección automática usa una serie de respuestas de redirección para enviar la aplicación cliente al punto de conexión correcto para una dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="31172-112">The Autodiscover service uses a series of redirect responses to send the client application to the correct endpoint for an email address.</span></span> 
  
<span data-ttu-id="31172-113">Puede usar una de las siguientes tecnologías de desarrollo de Exchange para tener acceso al servicio de detección automática:</span><span class="sxs-lookup"><span data-stu-id="31172-113">You can use one of the following Exchange development technologies to access the Autodiscover service:</span></span>

- <span data-ttu-id="31172-114">La API administrada de servicios Web Exchange (EWS)</span><span class="sxs-lookup"><span data-stu-id="31172-114">The Exchange Web Services (EWS) Managed API</span></span>
    
- <span data-ttu-id="31172-115">EWS</span><span class="sxs-lookup"><span data-stu-id="31172-115">EWS</span></span>
    
<span data-ttu-id="31172-116">Si usa EWS, puede usar los métodos siguientes para recuperar la configuración de usuario:</span><span class="sxs-lookup"><span data-stu-id="31172-116">If you are using EWS, you can use the following methods to retrieve user settings:</span></span>
    
- <span data-ttu-id="31172-117">El servicio Detección automática basado en SOAP</span><span class="sxs-lookup"><span data-stu-id="31172-117">The SOAP-based Autodiscover service</span></span>
    
- <span data-ttu-id="31172-118">El servicio Detección automática XML (POX)</span><span class="sxs-lookup"><span data-stu-id="31172-118">The XML (POX) Autodiscover service</span></span>
    
- <span data-ttu-id="31172-119">Un proxy generado automáticamente se ha generado del servicio Detección automática de XML o SOAP</span><span class="sxs-lookup"><span data-stu-id="31172-119">An autogenerated proxy generated from the SOAP or XML Autodiscover service</span></span>
    
<span data-ttu-id="31172-120">Para obtener más información sobre estos métodos, vea [Detección automática en Exchange](autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="31172-120">For more information about these methods, see [Autodiscover for Exchange](autodiscover-for-exchange.md).</span></span>

<span data-ttu-id="31172-121">Para obtener más información sobre estas tecnologías de desarrollo de Exchange, vea [explorar la API administrada de EWS, EWS y servicios Web de Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="31172-121">For more information about these Exchange development technologies, see [Explore the EWS Managed API, EWS, and web services in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md).</span></span> 

<span data-ttu-id="31172-p103">La API administrada de EWS proporciona una interfaz basada en objetos para recuperar la configuración de usuario. Si su aplicación cliente usa un código administrado, le recomendamos que use la API administrada de EWS. La interfaz de la API administrada de EWS está mejor optimizada para un modelo de objetos simples que el típico proxy de servicio web generado automáticamente. </span><span class="sxs-lookup"><span data-stu-id="31172-p103">The EWS Managed API provides an object-based interface for retrieving user settings. If your client application uses managed code, we recommend that you use the EWS Managed API. The EWS Managed API interface is better optimized for a simple object model than the typical autogenerated web service proxy.</span></span> 
  
<span data-ttu-id="31172-125">Si está usando EWS, le sugerimos que use el servicio Detección automática de SOAP, ya que admite un conjunto superior de características que el servicio Detección automática de POX.</span><span class="sxs-lookup"><span data-stu-id="31172-125">If you are using EWS, we suggest that you use the SOAP Autodiscover service, because it supports a richer set of features than the POX Autodiscover service.</span></span>
  
## <a name="prerequisites-for-finding-an-endpoint"></a><span data-ttu-id="31172-126">Requisitos previos para buscar un extremo</span><span class="sxs-lookup"><span data-stu-id="31172-126">Prerequisites for finding an endpoint</span></span>
<span data-ttu-id="31172-127"><a name="bk_Prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="31172-127"><a name="bk_Prereq"> </a></span></span>

<span data-ttu-id="31172-128">Antes de crear una aplicación cliente que use el servicio de detección automática, debe tener acceso a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="31172-128">Before you can create a client application that uses the Autodiscover service, you need to have access to the following:</span></span>
  
- <span data-ttu-id="31172-129">Exchange online o un servidor que ejecute una versión de Exchange a partir de Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="31172-129">Exchange Online or a server that is running a version of Exchange starting with Exchange 2007 SP1.</span></span> <span data-ttu-id="31172-130">Si usa el servicio de detección automática basado en SOAP, Exchange online o una versión de Exchange que empiece por Exchange 2010.</span><span class="sxs-lookup"><span data-stu-id="31172-130">If you are using the SOAP-based Autodiscover service, Exchange Online or a version of Exchange starting with Exchange 2010.</span></span>
    
- <span data-ttu-id="31172-131">Un servidor Exchange que está configurado para aceptar conexiones de su aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="31172-131">An Exchange server that is configured to accept connections from your client application.</span></span> <span data-ttu-id="31172-132">Para obtener información sobre cómo configurar su servidor de Exchange, vea [Controlar el acceso de la aplicación de cliente a EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="31172-132">For information about how to configure your Exchange server, see [Controlling client application access to EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).</span></span>
    
- <span data-ttu-id="31172-133">Una cuenta que esté autorizada para usar EWS.</span><span class="sxs-lookup"><span data-stu-id="31172-133">An account that is authorized to use EWS.</span></span> <span data-ttu-id="31172-134">Para obtener información sobre cómo configurar una cuenta, vea [Controlar el acceso de la aplicación de cliente a EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="31172-134">For information about how to configure an account, see [Controlling client application access to EWS in Exchange](controlling-client-application-access-to-ews-in-exchange.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="31172-135">Si está usando la API administrada de EWS, debe proporcionar una devolución de llamada de validación de certificado en algunas circunstancias.</span><span class="sxs-lookup"><span data-stu-id="31172-135">If you are using the EWS Managed API, you must provide a certificate validation callback in some circumstances.</span></span> <span data-ttu-id="31172-136">También puede necesitar una devolución de llamada de validación de certificado con algunas bibliotecas de proxy generadas, como las que se han creado mediante Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="31172-136">You may also need a certificate validation callback with some generated proxy libraries, such as those created by Visual Studio.</span></span> <span data-ttu-id="31172-137">Para obtener más información, vea [Validar un certificado de servidor de la API de administración de EWS](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span><span class="sxs-lookup"><span data-stu-id="31172-137">For more information, see [Validate a server certificate for the EWS Managed API](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span></span> 
  
### <a name="core-concepts-for-finding-an-endpoint"></a><span data-ttu-id="31172-138">Conceptos básicos para buscar un extremo</span><span class="sxs-lookup"><span data-stu-id="31172-138">Core concepts for finding an endpoint</span></span>
<span data-ttu-id="31172-139"><a name="bk_Core"> </a></span><span class="sxs-lookup"><span data-stu-id="31172-139"><a name="bk_Core"> </a></span></span>

<span data-ttu-id="31172-140">Antes de usar la detección automática para buscar un extremo, debe estar familiarizado con los conceptos que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="31172-140">Before you use Autodiscover to find an endpoint, you should be familiar with the concepts listed in the following table.</span></span>
  
|<span data-ttu-id="31172-141">**Concepto**</span><span class="sxs-lookup"><span data-stu-id="31172-141">**Concept**</span></span>|<span data-ttu-id="31172-142">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="31172-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31172-143">Detección automática en Exchange</span><span class="sxs-lookup"><span data-stu-id="31172-143">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md) <br/> |<span data-ttu-id="31172-144">Proporciona información general del funcionamiento del servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="31172-144">Provides an overview of how the Autodiscover service works.</span></span>  <br/> |
   
<span data-ttu-id="31172-145">Si usa la API administrada de EWS, usa la clase [Microsoft.Exchange.WebServices.Data.ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) del espacio de nombres [Microsoft.Exchange.WebServices.Data](https://msdn.microsoft.com/library/dd633907%28v=exchg.80%29.aspx) para administrar la conexión con EWS.</span><span class="sxs-lookup"><span data-stu-id="31172-145">If you are using the EWS Managed API, you use the [Microsoft.Exchange.WebServices.Data.ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) class in the [Microsoft.Exchange.WebServices.Data](https://msdn.microsoft.com/library/dd633907%28v=exchg.80%29.aspx) namespace to manage your connection to EWS.</span></span> <span data-ttu-id="31172-146">Para usar los ejemplos de código de la API administrada de EWS de este artículo, debe hacer referencia a los siguientes espacios de nombres en el código:</span><span class="sxs-lookup"><span data-stu-id="31172-146">To use the EWS Managed API code samples in this article, you need to reference the following namespaces in your code:</span></span> 
  
- <span data-ttu-id="31172-147">**System.Net**</span><span class="sxs-lookup"><span data-stu-id="31172-147">**System.Net**</span></span>
    
- <span data-ttu-id="31172-148">**Microsoft.Exchange.WebServices.Data.ExchangeService**</span><span class="sxs-lookup"><span data-stu-id="31172-148">**Microsoft.Exchange.WebServices.Data.ExchangeService**</span></span>
    
## <a name="find-the-correct-endpoint-by-using-the-ews-managed-api"></a><span data-ttu-id="31172-149">Buscar el punto de conexión correcto mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="31172-149">Find the correct endpoint by using the EWS Managed API</span></span>
<span data-ttu-id="31172-150"><a name="bk_Managed"> </a></span><span class="sxs-lookup"><span data-stu-id="31172-150"><a name="bk_Managed"> </a></span></span>

<span data-ttu-id="31172-151">Si usa la API administrada de EWS, las llamadas al servicio Detección automática se administran mediante la clase **ExchangeService** .</span><span class="sxs-lookup"><span data-stu-id="31172-151">If you are using the EWS Managed API, calls to the Autodiscover service are handled by the **ExchangeService** class.</span></span> <span data-ttu-id="31172-152">Para determinar el punto de conexión correcto de una cuenta de correo electrónico, llame al método **AutodiscoverUrl** en un objeto **[ExchangeService]** .</span><span class="sxs-lookup"><span data-stu-id="31172-152">To determine the correct endpoint for an email account, you call the **AutodiscoverUrl** method on an **[ExchangeService]** object.</span></span> <span data-ttu-id="31172-153">En el siguiente ejemplo de código se muestra cómo establecer el extremo del servicio Web EWS para una dirección de correo electrónico en el archivo Exchange. asmx en el servidor de acceso de cliente correcto mediante la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="31172-153">The following code example shows how to set the EWS web service endpoint for an email address to the Exchange.asmx file on the correct Client Access server by using the EWS Managed API.</span></span> 
  
```cs
NetworkCredential credentials = new NetworkCredential(securelyStoredEmail, securelyStoredPassword);
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2013);
service.Credentials = credentials;
service.AutodiscoverUrl("User1@contoso.com");
```

## <a name="find-the-correct-endpoint-by-using-ews"></a><span data-ttu-id="31172-154">Buscar el punto de conexión correcto mediante EWS</span><span class="sxs-lookup"><span data-stu-id="31172-154">Find the correct endpoint by using EWS</span></span>
<span data-ttu-id="31172-155"><a name="bk_SOAP"> </a></span><span class="sxs-lookup"><span data-stu-id="31172-155"><a name="bk_SOAP"> </a></span></span>

<span data-ttu-id="31172-156">El servicio Detección automática de SOAP puede usar una serie de solicitudes y respuestas para dirigir la aplicación al punto de conexión correcto de EWS.</span><span class="sxs-lookup"><span data-stu-id="31172-156">The SOAP Autodiscover service may use a series of requests and responses to direct your application to the correct endpoint for EWS.</span></span> <span data-ttu-id="31172-157">Para obtener información acerca del proceso para determinar el punto de conexión correcto para una cuenta de correo electrónico, consulte [detección automática de Exchange](autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="31172-157">For information about the process for determining the correct endpoint for an email account, see [Autodiscover for Exchange](autodiscover-for-exchange.md).</span></span> <span data-ttu-id="31172-158">Los siguientes ejemplos de XML muestran la serie de solicitudes y respuestas que puede esperar al realizar una solicitud de detección automática de SOAP para encontrar el punto de conexión correcto.</span><span class="sxs-lookup"><span data-stu-id="31172-158">The following XML examples show the series of requests and responses that you can expect when making a SOAP Autodiscover request to find the correct endpoint.</span></span>
  
### <a name="soap-autodiscover-endpoint-request"></a><span data-ttu-id="31172-159">Solicitud de extremo de detección automática de SOAP</span><span class="sxs-lookup"><span data-stu-id="31172-159">SOAP Autodiscover endpoint request</span></span>

<span data-ttu-id="31172-160">En el ejemplo siguiente se muestra una solicitud XML que se envía al servicio de detección automática para encontrar el punto de conexión correcto.</span><span class="sxs-lookup"><span data-stu-id="31172-160">The following example shows an XML request that is sent to the Autodiscover service to find the correct endpoint.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://mail.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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

### <a name="soap-autodiscover-redirection-response"></a><span data-ttu-id="31172-161">Respuesta de redireccionamiento de detección automática de SOAP</span><span class="sxs-lookup"><span data-stu-id="31172-161">SOAP Autodiscover redirection response</span></span>

<span data-ttu-id="31172-162">El servicio Detección automática puede responder con una de dos respuestas de redirección: una redirección HTTP 302 o una respuesta de redireccionamiento SOAP.</span><span class="sxs-lookup"><span data-stu-id="31172-162">The Autodiscover service may respond with one of two redirection responses: an HTTP 302 redirect, or a SOAP redirection response.</span></span> <span data-ttu-id="31172-163">Si la respuesta del servidor de Exchange es una redirección HTTP 302, la aplicación cliente debe validar que la dirección de redireccionamiento es aceptable y, a continuación, seguir la respuesta de redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="31172-163">If the response from the Exchange server is an HTTP 302 redirect, the client application should validate that the redirection address is acceptable and then follow the redirection response.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="31172-164">Para consultar los criterios para validar una respuesta de redireccionamiento, consulte [detección automática de Exchange](autodiscover-for-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="31172-164">For criteria for validating a redirection response, see [Autodiscover for Exchange](autodiscover-for-exchange.md).</span></span> 
  
<span data-ttu-id="31172-165">Si el servicio Detección automática devuelve una respuesta de redirección, indicada por el elemento [ErrorCode](https://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) del elemento **UserResponse** , la aplicación cliente debe usar el elemento **RedirectTarget** para construir una nueva solicitud de configuración que se envía al servidor especificado en la respuesta de redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="31172-165">If the Autodiscover service returns a redirection response, indicated by the [ErrorCode](https://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) element of the **UserResponse** element, your client application should use the **RedirectTarget** element to construct a new settings request that is sent to the server specified in the redirection response.</span></span> <span data-ttu-id="31172-166">En el ejemplo siguiente se muestra una respuesta de redirección del servidor.</span><span class="sxs-lookup"><span data-stu-id="31172-166">The following example shows a redirection response from the server.</span></span> 
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>682</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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

<span data-ttu-id="31172-167">Después de una redirección, el cliente usa la dirección URL de redireccionamiento para preparar otra solicitud.</span><span class="sxs-lookup"><span data-stu-id="31172-167">After a redirection, the client uses the redirection URL to prepare another request.</span></span> <span data-ttu-id="31172-168">El siguiente código muestra un ejemplo de la solicitud que ha creado a partir de la respuesta de redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="31172-168">The following code shows an example of the request that you create from the redirection response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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

<span data-ttu-id="31172-169">Cuando la aplicación cliente se haya redirigido al punto de conexión correcto del servicio Detección automática, el servidor enviará una respuesta con el elemento [ErrorCode](https://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) del elemento **UserResponse** establecido en **NoError** y que contenga la configuración de usuario solicitada.</span><span class="sxs-lookup"><span data-stu-id="31172-169">When the client application has been directed to the correct endpoint for the Autodiscover service, the server will send a response with the [ErrorCode](https://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx) element of the **UserResponse** element set to **NoError** and containing the requested user settings.</span></span> <span data-ttu-id="31172-170">Solo se devuelven las configuraciones de usuario solicitadas, **InternalEwsUrl** y **ExternalEwsUrl**.</span><span class="sxs-lookup"><span data-stu-id="31172-170">Only the requested user settings, **InternalEwsUrl** and **ExternalEwsUrl**, are returned.</span></span> <span data-ttu-id="31172-171">En el ejemplo siguiente se muestra la respuesta del servidor.</span><span class="sxs-lookup"><span data-stu-id="31172-171">The following example shows the response from the server.</span></span> 
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>160</h:MajorBuildNumber>
      <h:MinorBuildNumber>4</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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

## <a name="next-steps"></a><span data-ttu-id="31172-172">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="31172-172">Next steps</span></span>
<span data-ttu-id="31172-173"><a name="bk_Next"> </a></span><span class="sxs-lookup"><span data-stu-id="31172-173"><a name="bk_Next"> </a></span></span>

<span data-ttu-id="31172-174">La búsqueda del extremo siguiendo el proceso de detección automática devuelve la configuración de dominio o usuario solicitada.</span><span class="sxs-lookup"><span data-stu-id="31172-174">Finding the endpoint by following the Autodiscover process returns the requested domain or user settings.</span></span> <span data-ttu-id="31172-175">Para obtener información sobre cómo realizar una solicitud para una configuración específica, vea los siguientes artículos:</span><span class="sxs-lookup"><span data-stu-id="31172-175">For information about making a request for specific settings, see the following articles:</span></span>
  
- [<span data-ttu-id="31172-176">Obtener la configuración de dominio de un servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="31172-176">Get domain settings from an Exchange server</span></span>](how-to-get-domain-settings-from-an-exchange-server.md)    
- [<span data-ttu-id="31172-177">Obtener la configuración de usuario de Exchange mediante el uso de detección automática</span><span class="sxs-lookup"><span data-stu-id="31172-177">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
## <a name="see-also"></a><span data-ttu-id="31172-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="31172-178">See also</span></span>

- [<span data-ttu-id="31172-179">Configurar la aplicación EWS</span><span class="sxs-lookup"><span data-stu-id="31172-179">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)   
- [<span data-ttu-id="31172-180">Detección automática en Exchange</span><span class="sxs-lookup"><span data-stu-id="31172-180">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)    
- [<span data-ttu-id="31172-181">Referencia del servicio web de Detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="31172-181">Autodiscover web service reference for Exchange</span></span>](https://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)    
- [<span data-ttu-id="31172-182">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="31172-182">EWS reference for Exchange</span></span>](https://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)
    

