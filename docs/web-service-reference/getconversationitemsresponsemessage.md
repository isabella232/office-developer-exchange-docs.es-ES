---
title: GetConversationItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e930650-7848-4bf2-a975-026309b3ea02
description: El elemento GetConversationItemsResponseMessage especifica el mensaje de respuesta para una solicitud de GetConversationItems.
ms.openlocfilehash: b38bca60bb51c24a7635391c4e23e5426366cd72
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461075"
---
# <a name="getconversationitemsresponsemessage"></a><span data-ttu-id="6ccbf-103">GetConversationItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6ccbf-103">GetConversationItemsResponseMessage</span></span>

<span data-ttu-id="6ccbf-104">El elemento **GetConversationItemsResponseMessage** especifica el mensaje de respuesta para una solicitud de **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="6ccbf-104">The **GetConversationItemsResponseMessage** element specifies the response message for a **GetConversationItems** request.</span></span> 
  
```XML
<GetConversationItemsResponseMessage ResponseClass="Success | Warning | Error">
    <Conversation/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetConversationItemsResponseMessage>
```

 <span data-ttu-id="6ccbf-105">**GetConversationItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="6ccbf-105">**GetConversationItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6ccbf-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6ccbf-106">Attributes and elements</span></span>

<span data-ttu-id="6ccbf-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ccbf-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6ccbf-108">Attributes</span></span>

|<span data-ttu-id="6ccbf-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6ccbf-109">**Attribute**</span></span>|<span data-ttu-id="6ccbf-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ccbf-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ccbf-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="6ccbf-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="6ccbf-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="6ccbf-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="6ccbf-113">ResponseClass</span></span>

|<span data-ttu-id="6ccbf-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6ccbf-114">**Value**</span></span>|<span data-ttu-id="6ccbf-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ccbf-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ccbf-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="6ccbf-116">Success</span></span>  <br/> |<span data-ttu-id="6ccbf-117">Indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="6ccbf-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="6ccbf-118">Warning</span></span>  <br/> |<span data-ttu-id="6ccbf-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="6ccbf-120">Error</span><span class="sxs-lookup"><span data-stu-id="6ccbf-120">Error</span></span>  <br/> |<span data-ttu-id="6ccbf-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6ccbf-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6ccbf-122">Child elements</span></span>

|<span data-ttu-id="6ccbf-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6ccbf-123">**Element**</span></span>|<span data-ttu-id="6ccbf-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ccbf-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ccbf-125">Conversación (ConversationResponseType)</span><span class="sxs-lookup"><span data-stu-id="6ccbf-125">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md) <br/> |<span data-ttu-id="6ccbf-126">Representa una única conversación devuelta en una respuesta **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="6ccbf-126">Represents a single conversation returned in a **GetConversationItems** response.</span></span>  <br/> |
|[<span data-ttu-id="6ccbf-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="6ccbf-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="6ccbf-128">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="6ccbf-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="6ccbf-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="6ccbf-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="6ccbf-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="6ccbf-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="6ccbf-132">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="6ccbf-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6ccbf-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="6ccbf-134">Proporciona información de estado sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6ccbf-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6ccbf-135">Parent elements</span></span>

|<span data-ttu-id="6ccbf-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6ccbf-136">**Element**</span></span>|<span data-ttu-id="6ccbf-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ccbf-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ccbf-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6ccbf-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="6ccbf-139">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="6ccbf-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ccbf-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ccbf-140">Remarks</span></span>

<span data-ttu-id="6ccbf-141">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6ccbf-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6ccbf-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ccbf-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6ccbf-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ccbf-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ccbf-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6ccbf-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6ccbf-145">Schema Name</span></span>  <br/> |<span data-ttu-id="6ccbf-146">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6ccbf-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="6ccbf-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6ccbf-147">Validation File</span></span>  <br/> |<span data-ttu-id="6ccbf-148">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6ccbf-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6ccbf-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6ccbf-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="6ccbf-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ccbf-150">See also</span></span>



- [<span data-ttu-id="6ccbf-151">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6ccbf-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

