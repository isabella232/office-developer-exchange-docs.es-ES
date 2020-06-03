---
title: Obtener información de configuración de servicio mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9379740a-96e1-490d-a229-0f9937c548d2
description: Descubra cómo obtener información de configuración del servicio para mensajería unificada, zumbidos de la Directiva, sugerencias de correo y reglas de protección de EWS en Exchange.
ms.openlocfilehash: 7546d9524f1e004eda2bdc55687fb44beafa44af
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528009"
---
# <a name="get-service-configuration-information-by-using-ews-in-exchange"></a><span data-ttu-id="3b61a-103">Obtener información de configuración de servicio mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3b61a-103">Get service configuration information by using EWS in Exchange</span></span>

<span data-ttu-id="3b61a-104">Descubra cómo obtener información de configuración del servicio para mensajería unificada, zumbidos de la Directiva, sugerencias de correo y reglas de protección de EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="3b61a-104">Find out how to get service configuration information for UM, policy nudges, mail tips, and protection rules from EWS in Exchange.</span></span>
  
<span data-ttu-id="3b61a-105">¿Funciona la aplicación de EWS con la mensajería unificada, los zumbidos de la Directiva, las sugerencias de correo o las reglas de protección?</span><span class="sxs-lookup"><span data-stu-id="3b61a-105">Does your EWS application work with Unified Messaging (UM), policy nudges, mail tips, or protection rules?</span></span> <span data-ttu-id="3b61a-106">Si es así, la aplicación tendrá que llamar a la [operación GetServiceConfiguration](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) para obtener la información de configuración del servicio que necesita.</span><span class="sxs-lookup"><span data-stu-id="3b61a-106">If so, your application will need to call the [GetServiceConfiguration operation](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) to get the service configuration information that it needs.</span></span> <span data-ttu-id="3b61a-107">La operación **GetServiceConfiguration** devuelve información de configuración específica para cada una de estas características de EWS.</span><span class="sxs-lookup"><span data-stu-id="3b61a-107">The **GetServiceConfiguration** operation returns configuration information that is specific to each of these EWS features.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3b61a-108">La API administrada de EWS no implementa esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="3b61a-108">The EWS Managed API does not implement this functionality.</span></span> 
  
<span data-ttu-id="3b61a-109">**Tabla 1. Información de configuración que devuelve la operación GetServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="3b61a-109">**Table 1. Configuration information that the GetServiceConfiguration operation returns**</span></span>

|<span data-ttu-id="3b61a-110">Característica EWS</span><span class="sxs-lookup"><span data-stu-id="3b61a-110">EWS feature</span></span>|<span data-ttu-id="3b61a-111">La operación GetServiceConfiguration devuelve...</span><span class="sxs-lookup"><span data-stu-id="3b61a-111">GetServiceConfiguration operation returns…</span></span>|
|:-----|:-----|
|<span data-ttu-id="3b61a-112">MU</span><span class="sxs-lookup"><span data-stu-id="3b61a-112">UM</span></span>  <br/> | <ul><li><span data-ttu-id="3b61a-113">Un valor que indica si la mensajería unificada está habilitada.</span><span class="sxs-lookup"><span data-stu-id="3b61a-113">A value that indicates whether UM is enabled.</span></span></li><li><span data-ttu-id="3b61a-114">Un valor que indica si está habilitada la función reproducir en teléfono.</span><span class="sxs-lookup"><span data-stu-id="3b61a-114">A value that indicates whether play on phone is enabled.</span></span></li><li><span data-ttu-id="3b61a-115">La cadena de marcado de reproducir en teléfono.</span><span class="sxs-lookup"><span data-stu-id="3b61a-115">The play on phone dial string.</span></span></li></ul> |
|<span data-ttu-id="3b61a-116">Zumbidos de Directiva</span><span class="sxs-lookup"><span data-stu-id="3b61a-116">Policy nudges</span></span>  <br/> | <ul><li><span data-ttu-id="3b61a-117">La Directiva zumbidos para mostrar en el cliente.</span><span class="sxs-lookup"><span data-stu-id="3b61a-117">Policy nudges for display in your client.</span></span></li></ul> |
|<span data-ttu-id="3b61a-118">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="3b61a-118">Mail tips</span></span>  <br/> | <ul><li><span data-ttu-id="3b61a-119">Un valor que indica si las sugerencias de correo están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="3b61a-119">A value that indicates whether mail tips are enabled.</span></span></li><li><span data-ttu-id="3b61a-120">El número máximo de destinatarios por solicitud.</span><span class="sxs-lookup"><span data-stu-id="3b61a-120">The maximum number of recipients per request.</span></span></li><li><span data-ttu-id="3b61a-121">El tamaño máximo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="3b61a-121">The maximum message size.</span></span></li><li><span data-ttu-id="3b61a-122">El umbral de gran audiencia.</span><span class="sxs-lookup"><span data-stu-id="3b61a-122">The large audience threshold.</span></span></li><li><span data-ttu-id="3b61a-123">Un valor que indica si se muestra el número de destinatarios externos.</span><span class="sxs-lookup"><span data-stu-id="3b61a-123">A value that indicates whether the number of external recipients is shown.</span></span></li><li><span data-ttu-id="3b61a-124">Una lista de dominios internos.</span><span class="sxs-lookup"><span data-stu-id="3b61a-124">A list of internal domains.</span></span></li><li><span data-ttu-id="3b61a-125">Un valor que indica si las sugerencias de directiva están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="3b61a-125">A value that indicates whether policy tips are enabled.</span></span></li><li><span data-ttu-id="3b61a-126">El umbral de la punta de la audiencia grande para indicar si el correo se considera que tiene un gran número de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="3b61a-126">The large audience cap threshold for indicating whether your mail is considered to have a large number of recipients.</span></span>  </li></ul>|
|<span data-ttu-id="3b61a-127">Reglas de protección</span><span class="sxs-lookup"><span data-stu-id="3b61a-127">Protection rules</span></span>  <br/> | <ul><li><span data-ttu-id="3b61a-128">Configuración de reglas de protección para el cliente.</span><span class="sxs-lookup"><span data-stu-id="3b61a-128">Protection rules setup for your client.</span></span></li><li><span data-ttu-id="3b61a-129">Una lista de los dominios internos de la organización.</span><span class="sxs-lookup"><span data-stu-id="3b61a-129">A list of domains that are internal to your organization.</span></span>  </li></ul> |
   
## <a name="code-example-get-service-configuration-information-for-mail-tips-by-using-ews"></a><span data-ttu-id="3b61a-130">Ejemplo de código: obtener información de configuración del servicio para sugerencias de correo mediante EWS</span><span class="sxs-lookup"><span data-stu-id="3b61a-130">Code example: Get service configuration information for mail tips by using EWS</span></span>

<span data-ttu-id="3b61a-131">En el ejemplo de código siguiente se usa la [operación GetServiceConfiguration](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) para solicitar información de configuración del servicio para sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="3b61a-131">The following code example uses the [GetServiceConfiguration operation](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) to request service configuration information for mail tips.</span></span> <span data-ttu-id="3b61a-132">Puede solicitar información de configuración del servicio adicional agregando más elementos [ConfigurationName](https://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) con valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="3b61a-132">You can request additional service configuration information by adding more [ConfigurationName](https://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) elements with different values.</span></span> 
  
```cs
private static void GetServiceConfiguration(ExchangeService service, NetworkCredential creds)
{ 
  // XML for the GetServiceConfiguration request SOAP envelope for mail tips configuration information.
  const string getServiceConfigurationRequest = 
    "<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
    "<soap:Envelope xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\"\n" +
    "               xmlns:m=\"https://schemas.microsoft.com/exchange/services/2006/messages\"\n" +
    "               xmlns:t=\"https://schemas.microsoft.com/exchange/services/2006/types\" \n" +
    "               xmlns:soap=\"https://schemas.xmlsoap.org/soap/envelope/\"\n" +
    "               xmlns:xs=\"http://www.w3.org/2001/XMLSchema\">\n" +
    "  <soap:Header>\n" +
    "    <t:RequestServerVersion Version=\"Exchange2013\" />\n" +
    "  </soap:Header>\n" +
    "  <soap:Body>\n" +
    "    <m:GetServiceConfiguration>\n" +
    "      <m:ActingAs>\n" +
    "        <t:EmailAddress>user1@contoso.com</t:EmailAddress>\n" +
    "        <t:RoutingType>SMTP</t:RoutingType>\n" +
    "      </m:ActingAs>\n" +
    "      <m:RequestedConfiguration>\n" +
    "        <m:ConfigurationName>MailTips</m:ConfigurationName>\n" +
    "      </m:RequestedConfiguration>\n" +
    "    </m:GetServiceConfiguration>\n" +
    "  </soap:Body>\n" +
    "</soap:Envelope>";
  // Encoded GetServiceConfiguration operation request.
  byte[] payload = System.Text.Encoding.UTF8.GetBytes(getServiceConfigurationRequest);
  try
  {
    HttpWebRequest request = (HttpWebRequest)WebRequest.Create(service.Url);
    request.AllowAutoRedirect = false;
    request.Credentials = creds;
    request.Method = "POST";
    request.ContentType = "text/xml";
    Stream requestStream = request.GetRequestStream();
    requestStream.Write(payload, 0, payload.Length);
    requestStream.Close();
    HttpWebResponse response = (HttpWebResponse)request.GetResponse();
    if (response.StatusCode == HttpStatusCode.OK)
    {
      Stream responseStream = response.GetResponseStream();
      StreamReader reader = new StreamReader(responseStream);
      string responseFromServer = reader.ReadToEnd();
      Console.WriteLine("You will need to parse this response to get the configuration information:\n\n" + responseFromServer);
      reader.Close();
      responseStream.Close();
    }
    else
      throw new WebException(response.StatusDescription);
          
  }
  catch (WebException e)
  {
    Console.WriteLine(e.Message);
  }
}

```

## <a name="next-steps"></a><span data-ttu-id="3b61a-133">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="3b61a-133">Next steps</span></span>

<span data-ttu-id="3b61a-134">Una vez solicitada la información de configuración del servicio, use la [clase XmlDocument](https://msdn.microsoft.com/library/system.xml.xmldocument.aspx) para cargar el XML de respuesta para que pueda analizarlo.</span><span class="sxs-lookup"><span data-stu-id="3b61a-134">After you request service configuration information, use the [XmlDocument class](https://msdn.microsoft.com/library/system.xml.xmldocument.aspx) to load the response XML so that you can parse it.</span></span> <span data-ttu-id="3b61a-135">A continuación, según el escenario, puede realizar una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="3b61a-135">Then, depending on your scenario, you can do one of the following:</span></span> 
  
- <span data-ttu-id="3b61a-136">Use la [operación GetMailTips](https://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) para obtener sugerencias de correo para que las aplicaciones cliente se muestren a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="3b61a-136">Use the [GetMailTips operation](https://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) to get mail tips for client applications to display to users.</span></span> 
    
- <span data-ttu-id="3b61a-137">Si la mensajería unificada está habilitada, [obtenga información sobre cómo reproducir elementos de buzón](https://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) a través del teléfono.</span><span class="sxs-lookup"><span data-stu-id="3b61a-137">If UM is enabled, [learn about how to play mailbox items](https://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) over your phone.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3b61a-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b61a-138">See also</span></span>

- [<span data-ttu-id="3b61a-139">Opciones de configuración de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3b61a-139">Configuration options for EWS in Exchange</span></span>](configuration-options-for-ews-in-exchange.md)    
- [<span data-ttu-id="3b61a-140">Configurar la aplicación EWS</span><span class="sxs-lookup"><span data-stu-id="3b61a-140">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)    
- [<span data-ttu-id="3b61a-141">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="3b61a-141">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

