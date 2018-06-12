---
title: GetSearchableMailboxesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f45865fd-4626-4d80-84f6-7989339fdd85
description: El elemento GetSearchableMailboxesResponseMessage especifica el mensaje de respuesta de una solicitud de GetSearchableMailboxes.
ms.openlocfilehash: 2a4d1fe357656fe29d8572e7f32a4bc2e4a6131e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764974"
---
# <a name="getsearchablemailboxesresponsemessage"></a><span data-ttu-id="3c9ba-103">GetSearchableMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3c9ba-103">GetSearchableMailboxesResponseMessage</span></span>

<span data-ttu-id="3c9ba-104">El elemento **GetSearchableMailboxesResponseMessage** especifica el mensaje de respuesta de una solicitud de **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="3c9ba-104">The **GetSearchableMailboxesResponseMessage** element specifies the response message for a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<GetSearchableMailboxesResponseMessage ResponseClass=" Success | Warning | Error ">
    <SearchableMailboxes/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetSearchablemailboxesResponseMessage>
```

 <span data-ttu-id="3c9ba-105">**GetSearchableMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="3c9ba-105">**GetSearchableMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3c9ba-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3c9ba-106">Attributes and elements</span></span>

<span data-ttu-id="3c9ba-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3c9ba-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c9ba-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3c9ba-108">Attributes</span></span>

|<span data-ttu-id="3c9ba-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="3c9ba-109">**Attribute**</span></span>|<span data-ttu-id="3c9ba-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3c9ba-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3c9ba-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="3c9ba-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="3c9ba-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3c9ba-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="3c9ba-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="3c9ba-113">ResponseClass</span></span>

|<span data-ttu-id="3c9ba-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3c9ba-114">**Value**</span></span>|<span data-ttu-id="3c9ba-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3c9ba-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3c9ba-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="3c9ba-116">Success</span></span>  <br/> |<span data-ttu-id="3c9ba-117">Indica éxito.</span><span class="sxs-lookup"><span data-stu-id="3c9ba-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="3c9ba-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="3c9ba-118">Warning</span></span>  <br/> |<span data-ttu-id="3c9ba-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="3c9ba-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="3c9ba-120">Error</span><span class="sxs-lookup"><span data-stu-id="3c9ba-120">Error</span></span>  <br/> |<span data-ttu-id="3c9ba-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="3c9ba-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3c9ba-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3c9ba-122">Child elements</span></span>

|<span data-ttu-id="3c9ba-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c9ba-123">**Element**</span></span>|<span data-ttu-id="3c9ba-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3c9ba-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c9ba-125">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="3c9ba-125">SearchableMailboxes</span></span>](searchablemailboxes.md) <br/> |<span data-ttu-id="3c9ba-126">Contiene una matriz de los buzones de correo devuelto desde una solicitud de **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="3c9ba-126">Contains an array of the mailboxes returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
|[<span data-ttu-id="3c9ba-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="3c9ba-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="3c9ba-128">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="3c9ba-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="3c9ba-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="3c9ba-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="3c9ba-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3c9ba-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="3c9ba-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="3c9ba-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="3c9ba-132">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="3c9ba-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="3c9ba-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3c9ba-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="3c9ba-134">Proporciona información de estado acerca de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3c9ba-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3c9ba-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3c9ba-135">Parent elements</span></span>

|<span data-ttu-id="3c9ba-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c9ba-136">**Element**</span></span>|<span data-ttu-id="3c9ba-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3c9ba-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c9ba-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3c9ba-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="3c9ba-139">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3c9ba-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c9ba-140">Notas</span><span class="sxs-lookup"><span data-stu-id="3c9ba-140">Remarks</span></span>

<span data-ttu-id="3c9ba-141">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3c9ba-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3c9ba-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3c9ba-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c9ba-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3c9ba-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c9ba-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3c9ba-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3c9ba-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3c9ba-145">Schema Name</span></span>  <br/> |<span data-ttu-id="3c9ba-146">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="3c9ba-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="3c9ba-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3c9ba-147">Validation File</span></span>  <br/> |<span data-ttu-id="3c9ba-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3c9ba-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3c9ba-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3c9ba-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3c9ba-150">Ver también</span><span class="sxs-lookup"><span data-stu-id="3c9ba-150">See also</span></span>



- [<span data-ttu-id="3c9ba-151">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3c9ba-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

