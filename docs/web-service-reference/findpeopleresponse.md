---
title: FindPeopleResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 95f016a9-002f-4be3-abd6-f5e3528afd44
description: El elemento FindPeopleResponse especifica la respuesta a una solicitud de FindPeople.
ms.openlocfilehash: 4f2c2f6069a515d5153ea488b35182d8b35f029f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764649"
---
# <a name="findpeopleresponse"></a><span data-ttu-id="74c2f-103">FindPeopleResponse</span><span class="sxs-lookup"><span data-stu-id="74c2f-103">FindPeopleResponse</span></span>

<span data-ttu-id="74c2f-104">El elemento **FindPeopleResponse** especifica la respuesta a una solicitud de **FindPeople** .</span><span class="sxs-lookup"><span data-stu-id="74c2f-104">The **FindPeopleResponse** element specifies the response to a **FindPeople** request.</span></span> 
  
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

 <span data-ttu-id="74c2f-105">**FindPeopleResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="74c2f-105">**FindPeopleResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="74c2f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="74c2f-106">Attributes and elements</span></span>

<span data-ttu-id="74c2f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="74c2f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="74c2f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="74c2f-108">Attributes</span></span>

|<span data-ttu-id="74c2f-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="74c2f-109">**Attribute**</span></span>|<span data-ttu-id="74c2f-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="74c2f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="74c2f-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="74c2f-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="74c2f-112">Especifica la clase de respuesta.</span><span class="sxs-lookup"><span data-stu-id="74c2f-112">Specifies the response class.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="74c2f-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="74c2f-113">ResponseClass</span></span>

|<span data-ttu-id="74c2f-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="74c2f-114">**Value**</span></span>|<span data-ttu-id="74c2f-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="74c2f-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="74c2f-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="74c2f-116">Success</span></span>  <br/> |<span data-ttu-id="74c2f-117">Indica éxito.</span><span class="sxs-lookup"><span data-stu-id="74c2f-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="74c2f-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="74c2f-118">Warning</span></span>  <br/> |<span data-ttu-id="74c2f-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="74c2f-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="74c2f-120">Error</span><span class="sxs-lookup"><span data-stu-id="74c2f-120">Error</span></span>  <br/> |<span data-ttu-id="74c2f-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="74c2f-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="74c2f-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="74c2f-122">Child elements</span></span>

|<span data-ttu-id="74c2f-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="74c2f-123">**Element**</span></span>|<span data-ttu-id="74c2f-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="74c2f-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="74c2f-125">Personas</span><span class="sxs-lookup"><span data-stu-id="74c2f-125">People</span></span>](people.md) <br/> |<span data-ttu-id="74c2f-126">Especifica una matriz de datos de rol devueltos como resultado de una solicitud de **FindPeople** .</span><span class="sxs-lookup"><span data-stu-id="74c2f-126">Specifies an array of persona data returned as the result of a **FindPeople** request.</span></span>  <br/> |
|[<span data-ttu-id="74c2f-127">TotalNumberOfPeopleInView</span><span class="sxs-lookup"><span data-stu-id="74c2f-127">TotalNumberOfPeopleInView</span></span>](totalnumberofpeopleinview.md) <br/> |<span data-ttu-id="74c2f-128">Especifica el número total de roles almacenados en un servidor que se devuelven por una solicitud de **FindPeople** .</span><span class="sxs-lookup"><span data-stu-id="74c2f-128">Specifies the total number of personas stored on a server that are returned by a **FindPeople** request.</span></span>  <br/> |
|[<span data-ttu-id="74c2f-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="74c2f-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="74c2f-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74c2f-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="74c2f-131">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="74c2f-131">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="74c2f-132">Proporciona información de estado acerca de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="74c2f-132">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="74c2f-133">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="74c2f-133">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="74c2f-134">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="74c2f-134">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="74c2f-135">MessageXml</span><span class="sxs-lookup"><span data-stu-id="74c2f-135">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="74c2f-136">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="74c2f-136">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="74c2f-137">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="74c2f-137">Parent elements</span></span>

|<span data-ttu-id="74c2f-138">**Element**</span><span class="sxs-lookup"><span data-stu-id="74c2f-138">**Element**</span></span>|<span data-ttu-id="74c2f-139">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="74c2f-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="74c2f-140">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="74c2f-140">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="74c2f-141">Especifica una matriz de los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="74c2f-141">Specifies an array of response messages.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74c2f-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74c2f-142">Remarks</span></span>

<span data-ttu-id="74c2f-143">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="74c2f-143">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="74c2f-144">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="74c2f-144">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="74c2f-145">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="74c2f-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="74c2f-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="74c2f-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="74c2f-147">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="74c2f-147">Schema Name</span></span>  <br/> |<span data-ttu-id="74c2f-148">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="74c2f-148">Message schema</span></span>  <br/> |
|<span data-ttu-id="74c2f-149">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="74c2f-149">Validation File</span></span>  <br/> |<span data-ttu-id="74c2f-150">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="74c2f-150">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="74c2f-151">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="74c2f-151">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="74c2f-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="74c2f-152">See also</span></span>



- [<span data-ttu-id="74c2f-153">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="74c2f-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

