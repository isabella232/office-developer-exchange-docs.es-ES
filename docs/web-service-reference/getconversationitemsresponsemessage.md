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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764791"
---
# <a name="getconversationitemsresponsemessage"></a><span data-ttu-id="69a13-103">GetConversationItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="69a13-103">GetConversationItemsResponseMessage</span></span>

<span data-ttu-id="69a13-104">El elemento **GetConversationItemsResponseMessage** especifica el mensaje de respuesta de una solicitud de **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="69a13-104">The **GetConversationItemsResponseMessage** element specifies the response message for a **GetConversationItems** request.</span></span> 
  
```XML
<GetConversationItemsResponseMessage ResponseClass="Success | Warning | Error">
    <Conversation/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetConversationItemsResponseMessage>
```

 <span data-ttu-id="69a13-105">**GetConversationItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="69a13-105">**GetConversationItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69a13-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="69a13-106">Attributes and elements</span></span>

<span data-ttu-id="69a13-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="69a13-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69a13-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="69a13-108">Attributes</span></span>

|<span data-ttu-id="69a13-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="69a13-109">**Attribute**</span></span>|<span data-ttu-id="69a13-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69a13-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="69a13-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="69a13-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="69a13-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="69a13-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="69a13-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="69a13-113">ResponseClass</span></span>

|<span data-ttu-id="69a13-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="69a13-114">**Value**</span></span>|<span data-ttu-id="69a13-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69a13-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="69a13-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="69a13-116">Success</span></span>  <br/> |<span data-ttu-id="69a13-117">Indica éxito.</span><span class="sxs-lookup"><span data-stu-id="69a13-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="69a13-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="69a13-118">Warning</span></span>  <br/> |<span data-ttu-id="69a13-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="69a13-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="69a13-120">Error</span><span class="sxs-lookup"><span data-stu-id="69a13-120">Error</span></span>  <br/> |<span data-ttu-id="69a13-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="69a13-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="69a13-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="69a13-122">Child elements</span></span>

|<span data-ttu-id="69a13-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="69a13-123">**Element**</span></span>|<span data-ttu-id="69a13-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69a13-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69a13-125">Conversación (ConversationResponseType)</span><span class="sxs-lookup"><span data-stu-id="69a13-125">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md) <br/> |<span data-ttu-id="69a13-126">Representa una sola conversación devuelta en una respuesta de **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="69a13-126">Represents a single conversation returned in a **GetConversationItems** response.</span></span>  <br/> |
|[<span data-ttu-id="69a13-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="69a13-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="69a13-128">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="69a13-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="69a13-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="69a13-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="69a13-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="69a13-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="69a13-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="69a13-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="69a13-132">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="69a13-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="69a13-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="69a13-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="69a13-134">Proporciona información de estado acerca de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="69a13-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="69a13-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="69a13-135">Parent elements</span></span>

|<span data-ttu-id="69a13-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="69a13-136">**Element**</span></span>|<span data-ttu-id="69a13-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69a13-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69a13-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="69a13-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="69a13-139">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="69a13-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69a13-140">Notas</span><span class="sxs-lookup"><span data-stu-id="69a13-140">Remarks</span></span>

<span data-ttu-id="69a13-141">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="69a13-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="69a13-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="69a13-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69a13-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="69a13-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69a13-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="69a13-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="69a13-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="69a13-145">Schema Name</span></span>  <br/> |<span data-ttu-id="69a13-146">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="69a13-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="69a13-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="69a13-147">Validation File</span></span>  <br/> |<span data-ttu-id="69a13-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="69a13-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="69a13-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="69a13-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="69a13-150">Ver también</span><span class="sxs-lookup"><span data-stu-id="69a13-150">See also</span></span>



- [<span data-ttu-id="69a13-151">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="69a13-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

