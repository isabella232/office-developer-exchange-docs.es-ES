---
title: GetHoldOnMailboxesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f7d0d90-d418-4ce9-8cea-afe8f14728c3
description: El elemento GetHoldOnMailboxesResponseMessage especifica el mensaje de respuesta de una solicitud de GetHoldOnMailboxes.
ms.openlocfilehash: e1c43f75bfa62b20de9248546e71c92ae5998ed9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764866"
---
# <a name="getholdonmailboxesresponsemessage"></a><span data-ttu-id="07733-103">GetHoldOnMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="07733-103">GetHoldOnMailboxesResponseMessage</span></span>

<span data-ttu-id="07733-104">El elemento **GetHoldOnMailboxesResponseMessage** especifica el mensaje de respuesta de una solicitud de **GetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="07733-104">The **GetHoldOnMailboxesResponseMessage** element specifies the response message for a **GetHoldOnMailboxes** request.</span></span> 
  
```XML
<GetHoldOnMailboxesResponseMessage ResponseClass=" Success | Warning | Error ">
    <MailboxHoldResult/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetHoldOnMailboxesResponseMessage>
```

 <span data-ttu-id="07733-105">**GetHoldOnMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="07733-105">**GetHoldOnMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07733-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="07733-106">Attributes and elements</span></span>

<span data-ttu-id="07733-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="07733-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07733-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="07733-108">Attributes</span></span>

|<span data-ttu-id="07733-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="07733-109">**Attribute**</span></span>|<span data-ttu-id="07733-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07733-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07733-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="07733-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="07733-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="07733-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="07733-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="07733-113">ResponseClass</span></span>

|<span data-ttu-id="07733-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="07733-114">**Value**</span></span>|<span data-ttu-id="07733-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07733-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07733-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="07733-116">Success</span></span>  <br/> |<span data-ttu-id="07733-117">Indica éxito.</span><span class="sxs-lookup"><span data-stu-id="07733-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="07733-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="07733-118">Warning</span></span>  <br/> |<span data-ttu-id="07733-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="07733-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="07733-120">Error</span><span class="sxs-lookup"><span data-stu-id="07733-120">Error</span></span>  <br/> |<span data-ttu-id="07733-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="07733-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="07733-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="07733-122">Child elements</span></span>

|<span data-ttu-id="07733-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="07733-123">**Element**</span></span>|<span data-ttu-id="07733-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07733-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07733-125">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="07733-125">MailboxHoldResult</span></span>](mailboxholdresult.md) <br/> |<span data-ttu-id="07733-126">Contiene el resultado de la solicitud de **GetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="07733-126">Contains the result of the **GetHoldOnMailboxes** request.</span></span>  <br/> |
|[<span data-ttu-id="07733-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="07733-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="07733-128">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="07733-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="07733-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="07733-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="07733-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="07733-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="07733-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="07733-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="07733-132">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="07733-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="07733-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="07733-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="07733-134">Proporciona información de estado acerca de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="07733-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="07733-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="07733-135">Parent elements</span></span>

|<span data-ttu-id="07733-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="07733-136">**Element**</span></span>|<span data-ttu-id="07733-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07733-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07733-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="07733-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="07733-139">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="07733-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07733-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07733-140">Remarks</span></span>

<span data-ttu-id="07733-141">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="07733-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="07733-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="07733-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07733-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="07733-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07733-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="07733-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="07733-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="07733-145">Schema Name</span></span>  <br/> |<span data-ttu-id="07733-146">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="07733-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="07733-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="07733-147">Validation File</span></span>  <br/> |<span data-ttu-id="07733-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="07733-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="07733-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="07733-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="07733-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="07733-150">See also</span></span>



- [<span data-ttu-id="07733-151">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="07733-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

