---
title: Operación GetUMProperties (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetUMProperties
api_type:
- schema
ms.assetid: 301fb9a3-67df-44c4-8ffe-0600237fc344
description: La operación GetUMProperties obtiene todas las propiedades de mensajería unificada del buzón de correo del usuario que realiza la solicitud.
ms.openlocfilehash: 42176d9cd0288af6515aeea616a4f216a419410c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462475"
---
# <a name="getumproperties-operation-um-web-service"></a><span data-ttu-id="2ab86-103">Operación GetUMProperties (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="2ab86-103">GetUMProperties operation (UM web service)</span></span>

<span data-ttu-id="2ab86-104">La operación GetUMProperties obtiene todas las propiedades de mensajería unificada del buzón de correo del usuario que realiza la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2ab86-104">The GetUMProperties operation gets all the Unified Messaging properties for the mailbox of the user who is making the request.</span></span>
  
## <a name="getumproperties-request-example"></a><span data-ttu-id="2ab86-105">Ejemplo de solicitud GetUMProperties</span><span class="sxs-lookup"><span data-stu-id="2ab86-105">GetUMProperties request example</span></span>

### <a name="description"></a><span data-ttu-id="2ab86-106">Description</span><span class="sxs-lookup"><span data-stu-id="2ab86-106">Description</span></span>

<span data-ttu-id="2ab86-107">El siguiente ejemplo de una solicitud GetUMProperties muestra cómo crear una solicitud para obtener las propiedades de mensajería unificada de un buzón.</span><span class="sxs-lookup"><span data-stu-id="2ab86-107">The following example of a GetUMProperties request shows how to form a request to get the Unified Messaging properties of a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="2ab86-108">Código</span><span class="sxs-lookup"><span data-stu-id="2ab86-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUMProperties xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getumproperties-response-example"></a><span data-ttu-id="2ab86-109">Ejemplo de respuesta GetUMProperties correcta</span><span class="sxs-lookup"><span data-stu-id="2ab86-109">Successful GetUMProperties response example</span></span>

### <a name="description"></a><span data-ttu-id="2ab86-110">Description</span><span class="sxs-lookup"><span data-stu-id="2ab86-110">Description</span></span>

<span data-ttu-id="2ab86-111">El siguiente ejemplo de una respuesta de GetUMProperties muestra una respuesta a la solicitud GetUMProperties.</span><span class="sxs-lookup"><span data-stu-id="2ab86-111">The following example of a GetUMProperties response shows a response to the GetUMProperties request.</span></span>
  
### <a name="code"></a><span data-ttu-id="2ab86-112">Código</span><span class="sxs-lookup"><span data-stu-id="2ab86-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <GetUMPropertiesResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <GetUMPropertiesResponse>
        <OofStatus>false</OofStatus> 
        <MissedCallNotificationEnabled>true</MissedCallNotificationEnabled> 
        <PlayOnPhoneDialString>12345</PlayOnPhoneDialString> 
        <TelephoneAccessNumbers>54321</TelephoneAccessNumbers> 
        <TelephoneAccessFolderEmail>AAAAAGsd2rbQLVtLobUGbrq/9IUBAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAAA==</TelephoneAccessFolderEmail> 
      </GetUMPropertiesResponse>
    </GetUMPropertiesResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="2ab86-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ab86-113">See also</span></span>



[<span data-ttu-id="2ab86-114">GetUMProperties (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="2ab86-114">GetUMProperties (UM web service)</span></span>](getumproperties-um-web-service.md)
  
[<span data-ttu-id="2ab86-115">GetUMPropertiesResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="2ab86-115">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)

