---
title: FindMailboxStatisticsByKeywordsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d3835800-8887-43db-9a8a-fe3cfea7a863
description: El elemento FindMailboxStatisticsByKeywordsResponseMessage especifica el mensaje de respuesta para una solicitud de FindMailboxStatisticsByKeywords.
ms.openlocfilehash: 704eebbf82db2871ab36be8e5b30c88c6959baa5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44525979"
---
# <a name="findmailboxstatisticsbykeywordsresponsemessage"></a><span data-ttu-id="53368-103">FindMailboxStatisticsByKeywordsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="53368-103">FindMailboxStatisticsByKeywordsResponseMessage</span></span>

<span data-ttu-id="53368-104">El elemento **FindMailboxStatisticsByKeywordsResponseMessage** especifica el mensaje de respuesta para una solicitud de **FindMailboxStatisticsByKeywords** .</span><span class="sxs-lookup"><span data-stu-id="53368-104">The **FindMailboxStatisticsByKeywordsResponseMessage** element specifies the response message for a **FindMailboxStatisticsByKeywords** request.</span></span> 
  
```XML
<FindMailboxStatisticsByKeywordsResponseMessage ResponseClass=" Success | Warning | Error ">
    <MailboxStatisticsSearchResult/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</FindMailboxStatisticsByKeywordsResponseMessage>
```

 <span data-ttu-id="53368-105">**FindMailboxStatisticsByKeywordsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="53368-105">**FindMailboxStatisticsByKeywordsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="53368-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="53368-106">Attributes and elements</span></span>

<span data-ttu-id="53368-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="53368-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53368-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="53368-108">Attributes</span></span>

|<span data-ttu-id="53368-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="53368-109">**Attribute**</span></span>|<span data-ttu-id="53368-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53368-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53368-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="53368-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="53368-112">Especifica la clase de respuesta.</span><span class="sxs-lookup"><span data-stu-id="53368-112">Specifies the response class.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="53368-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="53368-113">ResponseClass</span></span>

|<span data-ttu-id="53368-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="53368-114">**Value**</span></span>|<span data-ttu-id="53368-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53368-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53368-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="53368-116">Success</span></span>  <br/> |<span data-ttu-id="53368-117">Indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="53368-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="53368-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="53368-118">Warning</span></span>  <br/> |<span data-ttu-id="53368-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="53368-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="53368-120">Error</span><span class="sxs-lookup"><span data-stu-id="53368-120">Error</span></span>  <br/> |<span data-ttu-id="53368-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="53368-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="53368-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="53368-122">Child elements</span></span>

|<span data-ttu-id="53368-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="53368-123">**Element**</span></span>|<span data-ttu-id="53368-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53368-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53368-125">MailboxStatisticsSearchResult</span><span class="sxs-lookup"><span data-stu-id="53368-125">MailboxStatisticsSearchResult</span></span>](mailboxstatisticssearchresult.md) <br/> |<span data-ttu-id="53368-126">Especifica el resultado de una búsqueda de buzones.</span><span class="sxs-lookup"><span data-stu-id="53368-126">Specifies the result of a mailbox search.</span></span>  <br/> |
|[<span data-ttu-id="53368-127">MessageText</span><span class="sxs-lookup"><span data-stu-id="53368-127">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="53368-128">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="53368-128">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="53368-129">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="53368-129">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="53368-130">Proporciona información de estado sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="53368-130">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="53368-131">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="53368-131">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="53368-132">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="53368-132">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="53368-133">MessageXml</span><span class="sxs-lookup"><span data-stu-id="53368-133">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="53368-134">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="53368-134">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="53368-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="53368-135">Parent elements</span></span>

|<span data-ttu-id="53368-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="53368-136">**Element**</span></span>|<span data-ttu-id="53368-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53368-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53368-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="53368-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="53368-139">Especifica una matriz de mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="53368-139">Specifies an array of response messages.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53368-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53368-140">Remarks</span></span>

<span data-ttu-id="53368-141">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="53368-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="53368-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="53368-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="53368-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="53368-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53368-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="53368-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="53368-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="53368-145">Schema Name</span></span>  <br/> |<span data-ttu-id="53368-146">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="53368-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="53368-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="53368-147">Validation File</span></span>  <br/> |<span data-ttu-id="53368-148">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="53368-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="53368-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="53368-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="53368-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="53368-150">See also</span></span>



- [<span data-ttu-id="53368-151">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="53368-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

