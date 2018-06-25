---
title: GetConversationItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e930650-7848-4bf2-a975-026309b3ea02
description: El elemento GetConversationItemsResponseMessage especifica el mensaje de respuesta de una solicitud de GetConversationItems.
ms.openlocfilehash: 997319193311ef9267d8f6ff14c70bfe40e2634b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764791"
---
# <a name="getconversationitemsresponsemessage"></a><span data-ttu-id="b9929-103">GetConversationItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b9929-103">GetConversationItemsResponseMessage</span></span>

<span data-ttu-id="b9929-104">El elemento **GetConversationItemsResponseMessage** especifica el mensaje de respuesta de una solicitud de **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="b9929-104">The **GetConversationItemsResponseMessage** element specifies the response message for a **GetConversationItems** request.</span></span> 
  
```XML
<GetConversationItemsResponseMessage ResponseClass="Success | Warning | Error">
    <Conversation/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetConversationItemsResponseMessage>
```

 <span data-ttu-id="b9929-105">**GetConversationItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b9929-105">**GetConversationItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b9929-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b9929-106">Attributes and elements</span></span>

<span data-ttu-id="b9929-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b9929-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b9929-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b9929-108">Attributes</span></span>

|<span data-ttu-id="b9929-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b9929-109">**Attribute**</span></span>|<span data-ttu-id="b9929-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9929-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9929-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="b9929-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="b9929-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b9929-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="b9929-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="b9929-113">ResponseClass</span></span>

|<span data-ttu-id="b9929-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b9929-114">**Value**</span></span>|<span data-ttu-id="b9929-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9929-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9929-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="b9929-116">Success</span></span>  <br/> |<span data-ttu-id="b9929-117">Indica éxito.</span><span class="sxs-lookup"><span data-stu-id="b9929-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="b9929-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="b9929-118">Warning</span></span>  <br/> |<span data-ttu-id="b9929-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="b9929-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="b9929-120">Error</span><span class="sxs-lookup"><span data-stu-id="b9929-120">Error</span></span>  <br/> |<span data-ttu-id="b9929-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="b9929-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b9929-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b9929-122">Child elements</span></span>

|<span data-ttu-id="b9929-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="b9929-123">**Element**</span></span>|<span data-ttu-id="b9929-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9929-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b9929-125">Conversación (ConversationResponseType)</span><span class="sxs-lookup"><span data-stu-id="b9929-125">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md) <br/> |<span data-ttu-id="b9929-126">Representa una sola conversación devuelta en una respuesta de **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="b9929-126">Represents a single conversation returned in a **GetConversationItems** response.</span></span>  <br/> |
|[<span data-ttu-id="b9929-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b9929-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="b9929-128">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="b9929-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="b9929-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="b9929-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="b9929-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b9929-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="b9929-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="b9929-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="b9929-132">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="b9929-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="b9929-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b9929-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="b9929-134">Proporciona información de estado acerca de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b9929-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b9929-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b9929-135">Parent elements</span></span>

|<span data-ttu-id="b9929-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="b9929-136">**Element**</span></span>|<span data-ttu-id="b9929-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9929-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b9929-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b9929-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="b9929-139">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="b9929-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9929-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b9929-140">Remarks</span></span>

<span data-ttu-id="b9929-141">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b9929-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b9929-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b9929-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b9929-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b9929-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9929-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b9929-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b9929-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b9929-145">Schema Name</span></span>  <br/> |<span data-ttu-id="b9929-146">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="b9929-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="b9929-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b9929-147">Validation File</span></span>  <br/> |<span data-ttu-id="b9929-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b9929-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b9929-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b9929-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b9929-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9929-150">See also</span></span>



- [<span data-ttu-id="b9929-151">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b9929-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

