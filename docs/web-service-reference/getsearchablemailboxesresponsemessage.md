---
title: GetSearchableMailboxesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f45865fd-4626-4d80-84f6-7989339fdd85
description: El elemento GetSearchableMailboxesResponseMessage especifica el mensaje de respuesta para una solicitud de GetSearchableMailboxes.
ms.openlocfilehash: 69f45d87cfbd398013d021cdd39b55497d78ae04
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458260"
---
# <a name="getsearchablemailboxesresponsemessage"></a><span data-ttu-id="ca434-103">GetSearchableMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ca434-103">GetSearchableMailboxesResponseMessage</span></span>

<span data-ttu-id="ca434-104">El elemento **GetSearchableMailboxesResponseMessage** especifica el mensaje de respuesta para una solicitud de **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="ca434-104">The **GetSearchableMailboxesResponseMessage** element specifies the response message for a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<GetSearchableMailboxesResponseMessage ResponseClass=" Success | Warning | Error ">
    <SearchableMailboxes/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetSearchablemailboxesResponseMessage>
```

 <span data-ttu-id="ca434-105">**GetSearchableMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ca434-105">**GetSearchableMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ca434-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ca434-106">Attributes and elements</span></span>

<span data-ttu-id="ca434-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ca434-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca434-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ca434-108">Attributes</span></span>

|<span data-ttu-id="ca434-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ca434-109">**Attribute**</span></span>|<span data-ttu-id="ca434-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ca434-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ca434-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="ca434-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="ca434-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ca434-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="ca434-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="ca434-113">ResponseClass</span></span>

|<span data-ttu-id="ca434-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ca434-114">**Value**</span></span>|<span data-ttu-id="ca434-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ca434-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ca434-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="ca434-116">Success</span></span>  <br/> |<span data-ttu-id="ca434-117">Indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ca434-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="ca434-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="ca434-118">Warning</span></span>  <br/> |<span data-ttu-id="ca434-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="ca434-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="ca434-120">Error</span><span class="sxs-lookup"><span data-stu-id="ca434-120">Error</span></span>  <br/> |<span data-ttu-id="ca434-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="ca434-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ca434-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ca434-122">Child elements</span></span>

|<span data-ttu-id="ca434-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ca434-123">**Element**</span></span>|<span data-ttu-id="ca434-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ca434-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca434-125">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="ca434-125">SearchableMailboxes</span></span>](searchablemailboxes.md) <br/> |<span data-ttu-id="ca434-126">Contiene una matriz de los buzones devueltos por una solicitud **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="ca434-126">Contains an array of the mailboxes returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
|[<span data-ttu-id="ca434-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ca434-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ca434-128">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="ca434-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="ca434-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="ca434-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ca434-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ca434-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ca434-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="ca434-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ca434-132">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="ca434-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="ca434-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ca434-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ca434-134">Proporciona información de estado sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ca434-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ca434-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ca434-135">Parent elements</span></span>

|<span data-ttu-id="ca434-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ca434-136">**Element**</span></span>|<span data-ttu-id="ca434-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ca434-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca434-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ca434-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="ca434-139">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ca434-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca434-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ca434-140">Remarks</span></span>

<span data-ttu-id="ca434-141">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ca434-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ca434-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ca434-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ca434-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ca434-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca434-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca434-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ca434-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ca434-145">Schema Name</span></span>  <br/> |<span data-ttu-id="ca434-146">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ca434-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="ca434-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ca434-147">Validation File</span></span>  <br/> |<span data-ttu-id="ca434-148">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ca434-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ca434-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ca434-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ca434-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca434-150">See also</span></span>



- [<span data-ttu-id="ca434-151">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ca434-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

