---
title: Mensaje (disponibilidad)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Message
api_type:
- schema
ms.assetid: 1eec24dd-c981-41f4-a2f0-c51d43f1d7c0
description: El elemento de mensaje contiene la espera de respuesta de la oficina (OOF).
ms.openlocfilehash: 9facd04767fdcc0fd9dfd84fc6badb1a7633d2b5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836452"
---
# <a name="message-availability"></a><span data-ttu-id="eb393-103">Mensaje (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="eb393-103">Message (Availability)</span></span>

<span data-ttu-id="eb393-104">El elemento de **mensaje** contiene la espera de respuesta de la oficina (OOF).</span><span class="sxs-lookup"><span data-stu-id="eb393-104">The **Message** element contains the out of Office (OOF) response.</span></span> 
  
```xml
<Message/> 
```

 <span data-ttu-id="eb393-105">**string**</span><span class="sxs-lookup"><span data-stu-id="eb393-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb393-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eb393-106">Attributes and elements</span></span>

<span data-ttu-id="eb393-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eb393-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb393-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="eb393-108">Attributes</span></span>

<span data-ttu-id="eb393-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eb393-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb393-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eb393-110">Child elements</span></span>

<span data-ttu-id="eb393-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eb393-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eb393-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eb393-112">Parent elements</span></span>

|<span data-ttu-id="eb393-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="eb393-113">**Element**</span></span>|<span data-ttu-id="eb393-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eb393-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb393-115">InternalReply</span><span class="sxs-lookup"><span data-stu-id="eb393-115">InternalReply</span></span>](internalreply.md) <br/> | <span data-ttu-id="eb393-116">Contiene el mensaje OOF enviado a otros usuarios en el dominio del remitente.</span><span class="sxs-lookup"><span data-stu-id="eb393-116">Contains the OOF message sent to other users in the sender's domain.</span></span> <br/> <br/>  <span data-ttu-id="eb393-117">Los siguientes son las expresiones de XPath posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="eb393-117">The following are the possible XPath expressions to this element:</span></span> <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/InternalReply` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/InternalReply` <br/> |
|[<span data-ttu-id="eb393-118">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="eb393-118">ExternalReply</span></span>](externalreply.md) <br/> | <span data-ttu-id="eb393-119">Contiene el mensaje de fuera de la oficina que se envía a direcciones fuera del dominio de la dirección del remitente.</span><span class="sxs-lookup"><span data-stu-id="eb393-119">Contains the OOF message that is sent to addresses outside the sender's domain.</span></span>  <br/> <br/> <span data-ttu-id="eb393-120">Los siguientes son las expresiones de XPath posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="eb393-120">The following are the possible XPath expressions to this element:</span></span>  <br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/ExternalReply` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/ExternalReply` <br/> |
|[<span data-ttu-id="eb393-121">ReplyBody</span><span class="sxs-lookup"><span data-stu-id="eb393-121">ReplyBody</span></span>](replybody.md) <br/> |<span data-ttu-id="eb393-122">Contiene un mensaje de fuera de la oficina y el idioma utilizado para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="eb393-122">Contains an OOF message and the language used for the message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="eb393-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="eb393-123">Text value</span></span>

<span data-ttu-id="eb393-124">Se requiere un valor de texto para establecer el mensaje de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="eb393-124">A text value is required to set the OOF message.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb393-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eb393-125">Remarks</span></span>

<span data-ttu-id="eb393-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="eb393-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="eb393-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eb393-127">Example</span></span>

<span data-ttu-id="eb393-128">El siguiente ejemplo de una solicitud de [operación de SetUserOofSettings](setuseroofsettings-operation.md) el [OofState](oofstate.md) establece en **habilitado**, Establece la duración de OOF a 10 días y establece los mensajes de fuera de la oficina internos y externos.</span><span class="sxs-lookup"><span data-stu-id="eb393-128">The following example of a [SetUserOofSettings operation](setuseroofsettings-operation.md) request sets the [OofState](oofstate.md) to **Enabled**, sets the duration of OOF to 10 days, and sets the internal and external OOF messages.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2005-10-05T00:00:00</StartTime>
          <EndTime>2005-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="eb393-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eb393-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb393-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eb393-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eb393-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="eb393-131">Schema Name</span></span>  <br/> |<span data-ttu-id="eb393-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="eb393-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="eb393-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="eb393-133">Validation File</span></span>  <br/> |<span data-ttu-id="eb393-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eb393-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="eb393-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="eb393-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb393-136">False</span><span class="sxs-lookup"><span data-stu-id="eb393-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb393-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb393-137">See also</span></span>

- [<span data-ttu-id="eb393-138">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="eb393-138">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)
- [<span data-ttu-id="eb393-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="eb393-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

