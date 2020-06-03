---
title: FindPeopleResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 95f016a9-002f-4be3-abd6-f5e3528afd44
description: El elemento FindPeopleResponse especifica la respuesta a una solicitud FindPeople.
ms.openlocfilehash: b969ac3f7bc2bbd3fc77bf753a15696c3b6d8216
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466405"
---
# <a name="findpeopleresponse"></a><span data-ttu-id="5f2bf-103">FindPeopleResponse</span><span class="sxs-lookup"><span data-stu-id="5f2bf-103">FindPeopleResponse</span></span>

<span data-ttu-id="5f2bf-104">El elemento **FindPeopleResponse** especifica la respuesta a una solicitud **FindPeople** .</span><span class="sxs-lookup"><span data-stu-id="5f2bf-104">The **FindPeopleResponse** element specifies the response to a **FindPeople** request.</span></span> 
  
```XML
<FindPeopleResponse ResponseClass=" Success | Warning | Error ">
    <People/>
    <TotalNumberOfPeopleInView/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</FindPeopleResponse>
```

 <span data-ttu-id="5f2bf-105">**FindPeopleResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="5f2bf-105">**FindPeopleResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5f2bf-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5f2bf-106">Attributes and elements</span></span>

<span data-ttu-id="5f2bf-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5f2bf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f2bf-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5f2bf-108">Attributes</span></span>

|<span data-ttu-id="5f2bf-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="5f2bf-109">**Attribute**</span></span>|<span data-ttu-id="5f2bf-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f2bf-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5f2bf-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="5f2bf-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="5f2bf-112">Especifica la clase de respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f2bf-112">Specifies the response class.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="5f2bf-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="5f2bf-113">ResponseClass</span></span>

|<span data-ttu-id="5f2bf-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5f2bf-114">**Value**</span></span>|<span data-ttu-id="5f2bf-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f2bf-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5f2bf-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="5f2bf-116">Success</span></span>  <br/> |<span data-ttu-id="5f2bf-117">Indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5f2bf-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="5f2bf-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="5f2bf-118">Warning</span></span>  <br/> |<span data-ttu-id="5f2bf-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="5f2bf-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="5f2bf-120">Error</span><span class="sxs-lookup"><span data-stu-id="5f2bf-120">Error</span></span>  <br/> |<span data-ttu-id="5f2bf-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="5f2bf-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5f2bf-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5f2bf-122">Child elements</span></span>

|<span data-ttu-id="5f2bf-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5f2bf-123">**Element**</span></span>|<span data-ttu-id="5f2bf-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f2bf-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f2bf-125">Personas</span><span class="sxs-lookup"><span data-stu-id="5f2bf-125">People</span></span>](people.md) <br/> |<span data-ttu-id="5f2bf-126">Especifica una matriz de datos de rol devueltos como resultado de una solicitud **FindPeople** .</span><span class="sxs-lookup"><span data-stu-id="5f2bf-126">Specifies an array of persona data returned as the result of a **FindPeople** request.</span></span>  <br/> |
|[<span data-ttu-id="5f2bf-127">TotalNumberOfPeopleInView</span><span class="sxs-lookup"><span data-stu-id="5f2bf-127">TotalNumberOfPeopleInView</span></span>](totalnumberofpeopleinview.md) <br/> |<span data-ttu-id="5f2bf-128">Especifica el número total de roles almacenados en un servidor devueltos por una solicitud **FindPeople** .</span><span class="sxs-lookup"><span data-stu-id="5f2bf-128">Specifies the total number of personas stored on a server that are returned by a **FindPeople** request.</span></span>  <br/> |
|[<span data-ttu-id="5f2bf-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="5f2bf-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="5f2bf-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f2bf-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="5f2bf-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5f2bf-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="5f2bf-132">Proporciona información de estado sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5f2bf-132">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="5f2bf-133">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5f2bf-133">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="5f2bf-134">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5f2bf-134">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="5f2bf-135">MessageXml</span><span class="sxs-lookup"><span data-stu-id="5f2bf-135">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="5f2bf-136">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="5f2bf-136">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5f2bf-137">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5f2bf-137">Parent elements</span></span>

|<span data-ttu-id="5f2bf-138">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5f2bf-138">**Element**</span></span>|<span data-ttu-id="5f2bf-139">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f2bf-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f2bf-140">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5f2bf-140">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="5f2bf-141">Especifica una matriz de mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f2bf-141">Specifies an array of response messages.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f2bf-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f2bf-142">Remarks</span></span>

<span data-ttu-id="5f2bf-143">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5f2bf-143">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5f2bf-144">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5f2bf-144">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5f2bf-145">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5f2bf-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f2bf-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f2bf-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5f2bf-147">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5f2bf-147">Schema Name</span></span>  <br/> |<span data-ttu-id="5f2bf-148">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5f2bf-148">Message schema</span></span>  <br/> |
|<span data-ttu-id="5f2bf-149">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5f2bf-149">Validation File</span></span>  <br/> |<span data-ttu-id="5f2bf-150">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5f2bf-150">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5f2bf-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5f2bf-151">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="5f2bf-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f2bf-152">See also</span></span>



- [<span data-ttu-id="5f2bf-153">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5f2bf-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

