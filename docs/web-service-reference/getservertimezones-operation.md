---
title: Operación GetServerTimeZones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServerTimeZones
api_type:
- schema
ms.assetid: 680173e1-e916-466b-b573-5a3182316345
description: La operación GetServerTimeZones devuelve información de las definiciones de zona horaria que están disponibles en un servidor de Exchange.
ms.openlocfilehash: 1afe7fe13501af4a14f72c731703fe41e1f33049
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460543"
---
# <a name="getservertimezones-operation"></a><span data-ttu-id="9d303-103">Operación GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="9d303-103">GetServerTimeZones operation</span></span>

<span data-ttu-id="9d303-104">La operación **GetServerTimeZones** devuelve información de las definiciones de zona horaria que están disponibles en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9d303-104">The **GetServerTimeZones** operation returns information from time zone definitions that are available on an Exchange server.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="9d303-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="9d303-105">SOAP Headers</span></span>

<span data-ttu-id="9d303-106">La operación **GetServerTimeZones** puede usar los encabezados SOAP que se enumeran y describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="9d303-106">The **GetServerTimeZones** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="9d303-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="9d303-107">**Header**</span></span>|<span data-ttu-id="9d303-108">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9d303-108">**Element**</span></span>|<span data-ttu-id="9d303-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d303-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9d303-110">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="9d303-110">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="9d303-111">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="9d303-111">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="9d303-112">Identifica la referencia cultural RFC3066 que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="9d303-112">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="9d303-113">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="9d303-113">RequestVersion</span></span>  <br/> |[<span data-ttu-id="9d303-114">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="9d303-114">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="9d303-115">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="9d303-115">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="9d303-116">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="9d303-116">ServerVersion</span></span>  <br/> |[<span data-ttu-id="9d303-117">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="9d303-117">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="9d303-118">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9d303-118">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getservertimezones-request-examples"></a><span data-ttu-id="9d303-119">Ejemplos de solicitudes de GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="9d303-119">GetServerTimeZones request examples</span></span>

### <a name="getting-the-name-and-identifier-of-each-time-zone"></a><span data-ttu-id="9d303-120">Obtener el nombre y el identificador de cada zona horaria</span><span class="sxs-lookup"><span data-stu-id="9d303-120">Getting the Name and Identifier of Each Time Zone</span></span>

<span data-ttu-id="9d303-121">En el ejemplo de código siguiente se muestra cómo recuperar el nombre y el identificador de la hora estándar del este y las zonas horarias horarias estándar del Pacífico.</span><span class="sxs-lookup"><span data-stu-id="9d303-121">The following code example shows how to retrieve the name and identifier for the Eastern Standard Time and Pacific Standard Time time zones.</span></span>
  
### <a name="code"></a><span data-ttu-id="9d303-122">Código</span><span class="sxs-lookup"><span data-stu-id="9d303-122">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <m:GetServerTimeZones ReturnFullTimeZoneData="false">
      <m:Ids>
        <t:Id>Eastern Standard Time</Id>
        <t:Id>Pacific Standard Time</Id>
      </m:Ids>
    </m:GetServerTimeZones>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="9d303-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9d303-123">Comments</span></span>

<span data-ttu-id="9d303-124">Cada elemento de [identificador (TimeZone)](id-timezone.md) contiene el identificador de una definición de zona horaria que se está solicitando.</span><span class="sxs-lookup"><span data-stu-id="9d303-124">Each [Id (TimeZone)](id-timezone.md) element contains the identifier of a time zone definition that is being requested.</span></span> <span data-ttu-id="9d303-125">Para solicitar información de todas las zonas horarias, omita el elemento [IDS](ids.md) de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9d303-125">To request information for all time zones, omit the [Ids](ids.md) element from the request.</span></span> 
  
### <a name="getting-the-full-definition-of-each-time-zone"></a><span data-ttu-id="9d303-126">Obtención de la definición completa de cada zona horaria</span><span class="sxs-lookup"><span data-stu-id="9d303-126">Getting the Full Definition of Each Time Zone</span></span>

<span data-ttu-id="9d303-127">En el ejemplo de código siguiente se muestra cómo recuperar la definición de la zona horaria completa para la zona horaria estándar del este.</span><span class="sxs-lookup"><span data-stu-id="9d303-127">The following code example shows how to retrieve the full time zone definition for the Eastern Standard Time time zone.</span></span>
  
### <a name="code"></a><span data-ttu-id="9d303-128">Código</span><span class="sxs-lookup"><span data-stu-id="9d303-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <m:GetServerTimeZones ReturnFullTimeZoneData="true">
      <m:Ids>
        <t:Id>Eastern Standard Time</Id>
      </m:Ids>
    </m:GetServerTimeZones>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="9d303-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9d303-129">Comments</span></span>

<span data-ttu-id="9d303-130">Cada elemento de [identificador (TimeZone)](id-timezone.md) contiene el identificador de una definición de zona horaria que se está solicitando.</span><span class="sxs-lookup"><span data-stu-id="9d303-130">Each [Id (TimeZone)](id-timezone.md) element contains the identifier of a time zone definition that is being requested.</span></span> <span data-ttu-id="9d303-131">Para solicitar información de todas las zonas horarias, omita el elemento [IDS](ids.md) de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9d303-131">To request information for all time zones, omit the [Ids](ids.md) element from the request.</span></span> 
  
## <a name="getservertimezones-response-examples"></a><span data-ttu-id="9d303-132">Ejemplos de respuesta de GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="9d303-132">GetServerTimeZones response examples</span></span>

### <a name="receiving-the-time-zone-name-and-identifier-only"></a><span data-ttu-id="9d303-133">Recepción del nombre y el identificador de la zona horaria solamente</span><span class="sxs-lookup"><span data-stu-id="9d303-133">Receiving the Time Zone Name and Identifier Only</span></span>

<span data-ttu-id="9d303-134">El siguiente ejemplo de una respuesta de **GetServerTimeZones** muestra una respuesta correcta a una solicitud de **GetServerTimeZones** en la que el atributo **ReturnFullTimeZoneData** se estableció en **false**.</span><span class="sxs-lookup"><span data-stu-id="9d303-134">The following example of a **GetServerTimeZones** response shows a successful response to a **GetServerTimeZones** request in which the **ReturnFullTimeZoneData** attribute was set to **false**.</span></span> <span data-ttu-id="9d303-135">La respuesta contiene el nombre y el identificador de la hora estándar del este y las zonas horarias horarias estándar.</span><span class="sxs-lookup"><span data-stu-id="9d303-135">The response contains the name and identifier for the Eastern Standard Time and Pacific Standard Time time zones.</span></span>
  
### <a name="code"></a><span data-ttu-id="9d303-136">Código</span><span class="sxs-lookup"><span data-stu-id="9d303-136">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetServerTimeZonesResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetServerTimeZonesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</ResponseCode>
          <m:TimeZoneDefinitions>
            <t:TimeZoneDefinition Id="Eastern Standard Time" Name="(GMT-05:00) Eastern Time (US &amp;amp; Canada)" />
            <t:TimeZoneDefinition Id="Pacific Standard Time" Name="(GMT-08:00) Pacific Time (US &amp;amp; Canada)" />
          </m:TimeZoneDefinitions>
        </m:GetServerTimeZonesResponseMessage>
      </m:ResponseMessages>
    </m:GetServerTimeZonesResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="receiving-a-full-time-zone-definition"></a><span data-ttu-id="9d303-137">Recibir una definición de zona horaria completa</span><span class="sxs-lookup"><span data-stu-id="9d303-137">Receiving a Full Time Zone Definition</span></span>

<span data-ttu-id="9d303-138">El siguiente ejemplo de una respuesta de **GetServerTimeZones** muestra una respuesta correcta a una solicitud de **GetServerTimeZones** en la que el atributo **ReturnFullTimeZoneData** se estableció en **true**.</span><span class="sxs-lookup"><span data-stu-id="9d303-138">The following example of a **GetServerTimeZones** response shows a successful response to a **GetServerTimeZones** request in which the **ReturnFullTimeZoneData** attribute was set to **true**.</span></span> <span data-ttu-id="9d303-139">La respuesta contiene la definición de la zona horaria completa para la zona horaria estándar del este.</span><span class="sxs-lookup"><span data-stu-id="9d303-139">The response contains the full time zone definition for the Eastern Standard Time time zone.</span></span>
  
### <a name="code"></a><span data-ttu-id="9d303-140">Código</span><span class="sxs-lookup"><span data-stu-id="9d303-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetServerTimeZonesResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetServerTimeZonesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</ResponseCode>
          <m:TimeZoneDefinitions>
            <t:TimeZoneDefinition Id="Eastern Standard Time" Name="(GMT-05:00) Eastern Time (US &amp;amp; Canada)">
              <t:Periods>
                <t:Period Bias="PT5H" Name="Standard" Id="trule:Microsoft/Registry/EasternStandardTime/2006-Standard" />
                <t:Period Bias="PT4H" Name="Daylight" Id="trule:Microsoft/Registry/EasternStandardTime/2006-Daylight" />
                <t:Period Bias="PT5H" Name="Standard" Id="trule:Microsoft/Registry/EasternStandardTime/2007-Standard" />
                <t:Period Bias="PT4H" Name="Daylight" Id="trule:Microsoft/Registry/EasternStandardTime/2007-Daylight" />
              </t:Periods>
              <t:TransitionsGroups>
                <t:TransitionsGroup Id="0">
                  <t:RecurringDayTransition>
                    <t:To Kind="Period">trule:Microsoft/Registry/EasternStandardTime/2006-Daylight</t:To>
                    <t:TimeOffset>PT2H</t:TimeOffset>
                    <t:Month>4</t:Month>
                    <t:DayOfWeek>Sunday</t:DayOfWeek>
                    <t:Occurrence>1</t:Occurrence>
                  </t:RecurringDayTransition>
                  <t:RecurringDayTransition>
                    <t:To Kind="Period">trule:Microsoft/Registry/EasternStandardTime/2006-Standard</t:To>
                    <t:TimeOffset>PT2H</t:TimeOffset>
                    <t:Month>10</t:Month>
                    <t:DayOfWeek>Sunday</t:DayOfWeek>
                    <t:Occurrence>-1</t:Occurrence>
                  </t:RecurringDayTransition>
                </t:TransitionsGroup>
                <t:TransitionsGroup Id="1">
                  <t:RecurringDayTransition>
                    <t:To Kind="Period">trule:Microsoft/Registry/EasternStandardTime/2007-Daylight</t:To>
                    <t:TimeOffset>PT2H</t:TimeOffset>
                    <t:Month>3</t:Month>
                    <t:DayOfWeek>Sunday</t:DayOfWeek>
                    <t:Occurrence>2</t:Occurrence>
                  </t:RecurringDayTransition>
                  <t:RecurringDayTransition>
                    <t:To Kind="Period">trule:Microsoft/Registry/EasternStandardTime/2007-Standard</t:To>
                    <t:TimeOffset>PT2H</t:TimeOffset>
                    <t:Month>11</t:Month>
                    <t:DayOfWeek>Sunday</t:DayOfWeek>
                    <t:Occurrence>1</t:Occurrence>
                  </t:RecurringDayTransition>
                </t:TransitionsGroup>
              </t:TransitionsGroups>
              <t:Transitions>
                <t:Transition>
                  <t:To Kind="Group">0</t:To>
                </t:Transition>
                <t:AbsoluteDateTransition>
                  <t:To Kind="Group">1</t:To>
                  <t:DateTime>2007-01-01T00:00:00</t:DateTime>
                </t:AbsoluteDateTransition>
              </t:Transitions>
            </t:TimeZoneDefinition>
          </m:TimeZoneDefinitions>
        </m:GetServerTimeZonesResponseMessage>
      </m:ResponseMessages>
    </m:GetServerTimeZonesResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="9d303-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d303-141">See also</span></span>



[<span data-ttu-id="9d303-142">GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="9d303-142">GetServerTimeZones</span></span>](getservertimezones.md)
  
[<span data-ttu-id="9d303-143">GetServerTimeZonesResponse</span><span class="sxs-lookup"><span data-stu-id="9d303-143">GetServerTimeZonesResponse</span></span>](getservertimezonesresponse.md)
  
 <span data-ttu-id="9d303-144">**GetServerTimeZonesType**</span><span class="sxs-lookup"><span data-stu-id="9d303-144">**GetServerTimeZonesType**</span></span>


[<span data-ttu-id="9d303-145">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="9d303-145">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="9d303-146">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="9d303-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

