---
title: CreateFolderPathResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f7b3507-713d-4ccf-8518-75fa6f967d6d
description: El elemento CreateFolderPathResponseMessage especifica el mensaje de respuesta de una solicitud de CreateFolderPath.
ms.openlocfilehash: f8f85cc246bb5d5ecd5cb745267d9d373286cf7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763936"
---
# <a name="createfolderpathresponsemessage"></a><span data-ttu-id="b5c1d-103">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b5c1d-103">CreateFolderPathResponseMessage</span></span>

<span data-ttu-id="b5c1d-104">El elemento **CreateFolderPathResponseMessage** especifica el mensaje de respuesta de una solicitud de **CreateFolderPath** .</span><span class="sxs-lookup"><span data-stu-id="b5c1d-104">The **CreateFolderPathResponseMessage** element specifies the response message for a **CreateFolderPath** request.</span></span> 
  
```XML
<CreateFolderPathResponseMessage ResponseClass="">
    <Folders></Folders>
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</CreateFolderPathResponseMessage>
```

 <span data-ttu-id="b5c1d-105">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b5c1d-105">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b5c1d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b5c1d-106">Attributes and elements</span></span>

<span data-ttu-id="b5c1d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5c1d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b5c1d-108">Attributes</span></span>

|<span data-ttu-id="b5c1d-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b5c1d-109">**Attribute**</span></span>|<span data-ttu-id="b5c1d-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5c1d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b5c1d-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="b5c1d-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="b5c1d-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="b5c1d-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="b5c1d-113">ResponseClass</span></span>

|<span data-ttu-id="b5c1d-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b5c1d-114">**Value**</span></span>|<span data-ttu-id="b5c1d-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5c1d-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b5c1d-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="b5c1d-116">Success</span></span>  <br/> |<span data-ttu-id="b5c1d-117">Indica éxito.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="b5c1d-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="b5c1d-118">Warning</span></span>  <br/> |<span data-ttu-id="b5c1d-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="b5c1d-120">Error</span><span class="sxs-lookup"><span data-stu-id="b5c1d-120">Error</span></span>  <br/> |<span data-ttu-id="b5c1d-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b5c1d-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b5c1d-122">Child elements</span></span>

|<span data-ttu-id="b5c1d-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="b5c1d-123">**Element**</span></span>|<span data-ttu-id="b5c1d-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5c1d-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b5c1d-125">Carpetas</span><span class="sxs-lookup"><span data-stu-id="b5c1d-125">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b5c1d-126">Contiene una matriz de las carpetas que se usan en las operaciones de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-126">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
|[<span data-ttu-id="b5c1d-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b5c1d-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="b5c1d-128">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="b5c1d-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="b5c1d-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="b5c1d-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="b5c1d-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="b5c1d-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="b5c1d-132">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="b5c1d-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b5c1d-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="b5c1d-134">Proporciona información de estado acerca de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b5c1d-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b5c1d-135">Parent elements</span></span>

|<span data-ttu-id="b5c1d-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="b5c1d-136">**Element**</span></span>|<span data-ttu-id="b5c1d-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5c1d-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b5c1d-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b5c1d-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="b5c1d-139">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5c1d-140">Notas</span><span class="sxs-lookup"><span data-stu-id="b5c1d-140">Remarks</span></span>

<span data-ttu-id="b5c1d-141">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b5c1d-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5c1d-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b5c1d-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5c1d-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b5c1d-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b5c1d-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b5c1d-145">Schema Name</span></span>  <br/> |<span data-ttu-id="b5c1d-146">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="b5c1d-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="b5c1d-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b5c1d-147">Validation File</span></span>  <br/> |<span data-ttu-id="b5c1d-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b5c1d-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b5c1d-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b5c1d-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b5c1d-150">Ver también</span><span class="sxs-lookup"><span data-stu-id="b5c1d-150">See also</span></span>

- [<span data-ttu-id="b5c1d-151">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b5c1d-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

