---
title: Obtener la información de configuración de servicio mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9379740a-96e1-490d-a229-0f9937c548d2
description: Averigüe cómo obtener información de configuración de servicio de mensajería unificada, desplazar de directiva, las sugerencias de correo y las reglas de protección de EWS en Exchange.
ms.openlocfilehash: e84a563bb094a2fe03e08f8e1a81b2b054d45850
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763067"
---
# <a name="get-service-configuration-information-by-using-ews-in-exchange"></a><span data-ttu-id="f2196-103">Obtener la información de configuración de servicio mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f2196-103">Get service configuration information by using EWS in Exchange</span></span>

<span data-ttu-id="f2196-104">Averigüe cómo obtener información de configuración de servicio de mensajería unificada, desplazar de directiva, las sugerencias de correo y las reglas de protección de EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="f2196-104">Find out how to get service configuration information for UM, policy nudges, mail tips, and protection rules from EWS in Exchange.</span></span>
  
<span data-ttu-id="f2196-105">¿La aplicación EWS funciona con mensajería unificada (UM), desplazar de directiva, las sugerencias de correo o las reglas de protección?</span><span class="sxs-lookup"><span data-stu-id="f2196-105">Does your EWS application work with Unified Messaging (UM), policy nudges, mail tips, or protection rules?</span></span> <span data-ttu-id="f2196-106">Si es así, la aplicación deberá llamar a la [operación de GetServiceConfiguration](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) para obtener la información de configuración de servicio que necesita.</span><span class="sxs-lookup"><span data-stu-id="f2196-106">If so, your application will need to call the [GetServiceConfiguration operation](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) to get the service configuration information that it needs.</span></span> <span data-ttu-id="f2196-107">La operación **GetServiceConfiguration** devuelve información de configuración que es específica de cada una de estas características EWS.</span><span class="sxs-lookup"><span data-stu-id="f2196-107">The **GetServiceConfiguration** operation returns configuration information that is specific to each of these EWS features.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f2196-108">La API administrada de EWS no implementa esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="f2196-108">The EWS Managed API does not implement this functionality.</span></span> 
  
<span data-ttu-id="f2196-109">**La tabla 1. Información de configuración que devuelve la operación GetServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="f2196-109">**Table 1. Configuration information that the GetServiceConfiguration operation returns**</span></span>

|<span data-ttu-id="f2196-110">Característica EWS</span><span class="sxs-lookup"><span data-stu-id="f2196-110">EWS feature</span></span>|<span data-ttu-id="f2196-111">Devuelve la operación GetServiceConfiguration...</span><span class="sxs-lookup"><span data-stu-id="f2196-111">GetServiceConfiguration operation returns…</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2196-112">MENSAJERÍA UNIFICADA</span><span class="sxs-lookup"><span data-stu-id="f2196-112">UM</span></span>  <br/> | <ul><li><span data-ttu-id="f2196-113">Un valor que indica si está habilitada la mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="f2196-113">A value that indicates whether UM is enabled.</span></span></li><li><span data-ttu-id="f2196-114">Un valor que indica si está habilitada la reproducir en el teléfono.</span><span class="sxs-lookup"><span data-stu-id="f2196-114">A value that indicates whether play on phone is enabled.</span></span></li><li><span data-ttu-id="f2196-115">Reproducir en la cadena de marcado de teléfono.</span><span class="sxs-lookup"><span data-stu-id="f2196-115">The play on phone dial string.</span></span></li></ul> |
|<span data-ttu-id="f2196-116">Desplazar de directiva</span><span class="sxs-lookup"><span data-stu-id="f2196-116">Policy nudges</span></span>  <br/> | <ul><li><span data-ttu-id="f2196-117">Directiva se desplazará para mostrarla en el cliente.</span><span class="sxs-lookup"><span data-stu-id="f2196-117">Policy nudges for display in your client.</span></span></li></ul> |
|<span data-ttu-id="f2196-118">Sugerencias de correo</span><span class="sxs-lookup"><span data-stu-id="f2196-118">Mail tips</span></span>  <br/> | <ul><li><span data-ttu-id="f2196-119">Un valor que indica si están habilitadas las sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="f2196-119">A value that indicates whether mail tips are enabled.</span></span></li><li><span data-ttu-id="f2196-120">El número máximo de destinatarios por solicitud.</span><span class="sxs-lookup"><span data-stu-id="f2196-120">The maximum number of recipients per request.</span></span></li><li><span data-ttu-id="f2196-121">El tamaño máximo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f2196-121">The maximum message size.</span></span></li><li><span data-ttu-id="f2196-122">Umbral de la audiencia de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="f2196-122">The large audience threshold.</span></span></li><li><span data-ttu-id="f2196-123">Un valor que indica si se muestra el número de destinatarios externos.</span><span class="sxs-lookup"><span data-stu-id="f2196-123">A value that indicates whether the number of external recipients is shown.</span></span></li><li><span data-ttu-id="f2196-124">Una lista de los dominios internos.</span><span class="sxs-lookup"><span data-stu-id="f2196-124">A list of internal domains.</span></span></li><li><span data-ttu-id="f2196-125">Un valor que indica si están habilitadas las sugerencias de directiva.</span><span class="sxs-lookup"><span data-stu-id="f2196-125">A value that indicates whether policy tips are enabled.</span></span></li><li><span data-ttu-id="f2196-126">El umbral del límite audiencia grandes para que indica si el correo se considera que tiene un gran número de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="f2196-126">The large audience cap threshold for indicating whether your mail is considered to have a large number of recipients.</span></span>  </li></ul>|
|<span data-ttu-id="f2196-127">Reglas de protección</span><span class="sxs-lookup"><span data-stu-id="f2196-127">Protection rules</span></span>  <br/> | <ul><li><span data-ttu-id="f2196-128">Configuración de reglas de protección de su cliente.</span><span class="sxs-lookup"><span data-stu-id="f2196-128">Protection rules setup for your client.</span></span></li><li><span data-ttu-id="f2196-129">Una lista de dominios que son internos a la organización.</span><span class="sxs-lookup"><span data-stu-id="f2196-129">A list of domains that are internal to your organization.</span></span>  </li></ul> |
   
## <a name="code-example-get-service-configuration-information-for-mail-tips-by-using-ews"></a><span data-ttu-id="f2196-130">Ejemplo de código: obtener la información de configuración de servicio para las sugerencias de correo mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="f2196-130">Code example: Get service configuration information for mail tips by using EWS</span></span>

<span data-ttu-id="f2196-131">En el ejemplo de código siguiente se usa la [operación de GetServiceConfiguration](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) para solicitar información de configuración de servicio para las sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="f2196-131">The following code example uses the [GetServiceConfiguration operation](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx) to request service configuration information for mail tips.</span></span> <span data-ttu-id="f2196-132">Puede solicitar información de configuración de servicios adicionales mediante la adición de más elementos [ConfigurationName](http://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) con valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="f2196-132">You can request additional service configuration information by adding more [ConfigurationName](http://msdn.microsoft.com/library/3b524a2f-9c6b-4550-9f3d-f78d176b0f7b%28Office.15%29.aspx) elements with different values.</span></span> 
  
```cs
private static void GetServiceConfiguration(ExchangeService service, NetworkCredential creds)
{ 
  // XML for the GetServiceConfiguration request SOAP envelope for mail tips configuration information.
  const string getServiceConfigurationRequest = 
    "<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
    "<soap:Envelope xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\"\n" +
    "               xmlns:m=\"http://schemas.microsoft.com/exchange/services/2006/messages\"\n" +
    "               xmlns:t=\"http://schemas.microsoft.com/exchange/services/2006/types\" \n" +
    "               xmlns:soap=\"http://schemas.xmlsoap.org/soap/envelope/\"\n" +
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

## <a name="next-steps"></a><span data-ttu-id="f2196-133">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="f2196-133">Next steps</span></span>

<span data-ttu-id="f2196-134">Después de solicitar información de configuración de servicio, use la [clase XmlDocument](http://msdn.microsoft.com/en-us/library/system.xml.xmldocument.aspx) para cargar el XML de la respuesta de manera que se puede analizar.</span><span class="sxs-lookup"><span data-stu-id="f2196-134">After you request service configuration information, use the [XmlDocument class](http://msdn.microsoft.com/en-us/library/system.xml.xmldocument.aspx) to load the response XML so that you can parse it.</span></span> <span data-ttu-id="f2196-135">A continuación, dependiendo de su situación, puede hacer una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="f2196-135">Then, depending on your scenario, you can do one of the following:</span></span> 
  
- <span data-ttu-id="f2196-136">Use la [operación de GetMailTips](http://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) para obtener sugerencias de correo para las aplicaciones de cliente mostrar a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="f2196-136">Use the [GetMailTips operation](http://msdn.microsoft.com/library/025483ec-a9f3-4735-8a95-d26e30ea7974%28Office.15%29.aspx) to get mail tips for client applications to display to users.</span></span> 
    
- <span data-ttu-id="f2196-137">Si está habilitada la mensajería unificada, [Obtenga información sobre cómo reproducir los elementos del buzón](http://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) a través de su teléfono.</span><span class="sxs-lookup"><span data-stu-id="f2196-137">If UM is enabled, [learn about how to play mailbox items](http://blogs.msdn.com/b/exchangedev/archive/2009/11/05/play-exchange-2010-mailbox-items-on-your-phone-by-using-the-ews-managed-api.aspx) over your phone.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f2196-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="f2196-138">See also</span></span>

- [<span data-ttu-id="f2196-139">Opciones de configuración para EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f2196-139">Configuration options for EWS in Exchange</span></span>](configuration-options-for-ews-in-exchange.md)    
- [<span data-ttu-id="f2196-140">Configurar una aplicación de EWS</span><span class="sxs-lookup"><span data-stu-id="f2196-140">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)    
- [<span data-ttu-id="f2196-141">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="f2196-141">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

