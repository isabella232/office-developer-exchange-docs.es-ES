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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764866"
---
# <a name="getholdonmailboxesresponsemessage"></a><span data-ttu-id="2a894-103">GetHoldOnMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2a894-103">GetHoldOnMailboxesResponseMessage</span></span>

<span data-ttu-id="2a894-104">El elemento **GetHoldOnMailboxesResponseMessage** especifica el mensaje de respuesta de una solicitud de **GetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="2a894-104">The **GetHoldOnMailboxesResponseMessage** element specifies the response message for a **GetHoldOnMailboxes** request.</span></span> 
  
```XML
<GetHoldOnMailboxesResponseMessage ResponseClass=" Success | Warning | Error ">
    <MailboxHoldResult/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetHoldOnMailboxesResponseMessage>
```

 <span data-ttu-id="2a894-105">**GetHoldOnMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2a894-105">**GetHoldOnMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2a894-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2a894-106">Attributes and elements</span></span>

<span data-ttu-id="2a894-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2a894-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a894-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2a894-108">Attributes</span></span>

|<span data-ttu-id="2a894-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="2a894-109">**Attribute**</span></span>|<span data-ttu-id="2a894-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a894-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2a894-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="2a894-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="2a894-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a894-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="2a894-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="2a894-113">ResponseClass</span></span>

|<span data-ttu-id="2a894-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2a894-114">**Value**</span></span>|<span data-ttu-id="2a894-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a894-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2a894-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="2a894-116">Success</span></span>  <br/> |<span data-ttu-id="2a894-117">Indica éxito.</span><span class="sxs-lookup"><span data-stu-id="2a894-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="2a894-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="2a894-118">Warning</span></span>  <br/> |<span data-ttu-id="2a894-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="2a894-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="2a894-120">Error</span><span class="sxs-lookup"><span data-stu-id="2a894-120">Error</span></span>  <br/> |<span data-ttu-id="2a894-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="2a894-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2a894-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2a894-122">Child elements</span></span>

|<span data-ttu-id="2a894-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="2a894-123">**Element**</span></span>|<span data-ttu-id="2a894-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a894-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a894-125">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="2a894-125">MailboxHoldResult</span></span>](mailboxholdresult.md) <br/> |<span data-ttu-id="2a894-126">Contiene el resultado de la solicitud de **GetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="2a894-126">Contains the result of the **GetHoldOnMailboxes** request.</span></span>  <br/> |
|[<span data-ttu-id="2a894-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2a894-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="2a894-128">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2a894-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="2a894-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="2a894-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="2a894-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a894-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="2a894-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="2a894-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="2a894-132">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="2a894-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="2a894-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2a894-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="2a894-134">Proporciona información de estado acerca de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2a894-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2a894-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2a894-135">Parent elements</span></span>

|<span data-ttu-id="2a894-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="2a894-136">**Element**</span></span>|<span data-ttu-id="2a894-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a894-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a894-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2a894-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="2a894-139">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="2a894-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a894-140">Notas</span><span class="sxs-lookup"><span data-stu-id="2a894-140">Remarks</span></span>

<span data-ttu-id="2a894-141">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2a894-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2a894-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2a894-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a894-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2a894-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a894-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2a894-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2a894-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2a894-145">Schema Name</span></span>  <br/> |<span data-ttu-id="2a894-146">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="2a894-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="2a894-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2a894-147">Validation File</span></span>  <br/> |<span data-ttu-id="2a894-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2a894-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2a894-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2a894-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2a894-150">Ver también</span><span class="sxs-lookup"><span data-stu-id="2a894-150">See also</span></span>



- [<span data-ttu-id="2a894-151">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2a894-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

