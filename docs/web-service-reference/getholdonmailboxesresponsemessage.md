---
title: GetHoldOnMailboxesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f7d0d90-d418-4ce9-8cea-afe8f14728c3
description: El elemento GetHoldOnMailboxesResponseMessage especifica el mensaje de respuesta para una solicitud de GetHoldOnMailboxes.
ms.openlocfilehash: 31832c11181bdca482e88419dd46ff1eacf77ea6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462953"
---
# <a name="getholdonmailboxesresponsemessage"></a><span data-ttu-id="0752c-103">GetHoldOnMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0752c-103">GetHoldOnMailboxesResponseMessage</span></span>

<span data-ttu-id="0752c-104">El elemento **GetHoldOnMailboxesResponseMessage** especifica el mensaje de respuesta para una solicitud de **GetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="0752c-104">The **GetHoldOnMailboxesResponseMessage** element specifies the response message for a **GetHoldOnMailboxes** request.</span></span> 
  
```XML
<GetHoldOnMailboxesResponseMessage ResponseClass=" Success | Warning | Error ">
    <MailboxHoldResult/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetHoldOnMailboxesResponseMessage>
```

 <span data-ttu-id="0752c-105">**GetHoldOnMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0752c-105">**GetHoldOnMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0752c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0752c-106">Attributes and elements</span></span>

<span data-ttu-id="0752c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0752c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0752c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0752c-108">Attributes</span></span>

|<span data-ttu-id="0752c-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="0752c-109">**Attribute**</span></span>|<span data-ttu-id="0752c-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0752c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0752c-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="0752c-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="0752c-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0752c-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="0752c-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="0752c-113">ResponseClass</span></span>

|<span data-ttu-id="0752c-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0752c-114">**Value**</span></span>|<span data-ttu-id="0752c-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0752c-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0752c-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="0752c-116">Success</span></span>  <br/> |<span data-ttu-id="0752c-117">Indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0752c-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="0752c-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="0752c-118">Warning</span></span>  <br/> |<span data-ttu-id="0752c-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="0752c-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="0752c-120">Error</span><span class="sxs-lookup"><span data-stu-id="0752c-120">Error</span></span>  <br/> |<span data-ttu-id="0752c-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="0752c-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0752c-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0752c-122">Child elements</span></span>

|<span data-ttu-id="0752c-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0752c-123">**Element**</span></span>|<span data-ttu-id="0752c-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0752c-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0752c-125">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="0752c-125">MailboxHoldResult</span></span>](mailboxholdresult.md) <br/> |<span data-ttu-id="0752c-126">Contiene el resultado de la solicitud **GetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="0752c-126">Contains the result of the **GetHoldOnMailboxes** request.</span></span>  <br/> |
|[<span data-ttu-id="0752c-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0752c-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0752c-128">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0752c-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="0752c-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="0752c-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0752c-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0752c-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0752c-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0752c-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0752c-132">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="0752c-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="0752c-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0752c-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0752c-134">Proporciona información de estado sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0752c-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0752c-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0752c-135">Parent elements</span></span>

|<span data-ttu-id="0752c-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0752c-136">**Element**</span></span>|<span data-ttu-id="0752c-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0752c-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0752c-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0752c-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="0752c-139">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="0752c-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0752c-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0752c-140">Remarks</span></span>

<span data-ttu-id="0752c-141">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0752c-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0752c-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0752c-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0752c-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0752c-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0752c-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="0752c-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0752c-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0752c-145">Schema Name</span></span>  <br/> |<span data-ttu-id="0752c-146">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0752c-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="0752c-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0752c-147">Validation File</span></span>  <br/> |<span data-ttu-id="0752c-148">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0752c-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0752c-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0752c-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0752c-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="0752c-150">See also</span></span>



- [<span data-ttu-id="0752c-151">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0752c-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

