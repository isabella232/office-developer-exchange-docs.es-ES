---
title: CreateFolderPathResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f7b3507-713d-4ccf-8518-75fa6f967d6d
description: El elemento CreateFolderPathResponseMessage especifica el mensaje de respuesta para una solicitud de CreateFolderPath.
ms.openlocfilehash: 3c0c4e98b568a6398dcd0e71a6e6931a3f47e3da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458890"
---
# <a name="createfolderpathresponsemessage"></a><span data-ttu-id="fa498-103">CreateFolderPathResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fa498-103">CreateFolderPathResponseMessage</span></span>

<span data-ttu-id="fa498-104">El elemento **CreateFolderPathResponseMessage** especifica el mensaje de respuesta para una solicitud de **CreateFolderPath** .</span><span class="sxs-lookup"><span data-stu-id="fa498-104">The **CreateFolderPathResponseMessage** element specifies the response message for a **CreateFolderPath** request.</span></span> 
  
```XML
<CreateFolderPathResponseMessage ResponseClass="">
    <Folders></Folders>
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</CreateFolderPathResponseMessage>
```

 <span data-ttu-id="fa498-105">**FolderInfoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="fa498-105">**FolderInfoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa498-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fa498-106">Attributes and elements</span></span>

<span data-ttu-id="fa498-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fa498-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa498-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fa498-108">Attributes</span></span>

|<span data-ttu-id="fa498-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="fa498-109">**Attribute**</span></span>|<span data-ttu-id="fa498-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa498-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fa498-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="fa498-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="fa498-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fa498-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="fa498-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="fa498-113">ResponseClass</span></span>

|<span data-ttu-id="fa498-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fa498-114">**Value**</span></span>|<span data-ttu-id="fa498-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa498-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fa498-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="fa498-116">Success</span></span>  <br/> |<span data-ttu-id="fa498-117">Indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="fa498-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="fa498-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="fa498-118">Warning</span></span>  <br/> |<span data-ttu-id="fa498-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="fa498-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="fa498-120">Error</span><span class="sxs-lookup"><span data-stu-id="fa498-120">Error</span></span>  <br/> |<span data-ttu-id="fa498-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="fa498-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fa498-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fa498-122">Child elements</span></span>

|<span data-ttu-id="fa498-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fa498-123">**Element**</span></span>|<span data-ttu-id="fa498-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa498-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa498-125">Folders</span><span class="sxs-lookup"><span data-stu-id="fa498-125">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="fa498-126">Contiene una matriz de carpetas que se usan en las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="fa498-126">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
|[<span data-ttu-id="fa498-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="fa498-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="fa498-128">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="fa498-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="fa498-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="fa498-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="fa498-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fa498-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="fa498-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="fa498-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="fa498-132">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="fa498-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="fa498-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="fa498-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="fa498-134">Proporciona información de estado sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fa498-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fa498-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fa498-135">Parent elements</span></span>

|<span data-ttu-id="fa498-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fa498-136">**Element**</span></span>|<span data-ttu-id="fa498-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa498-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa498-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="fa498-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="fa498-139">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa498-139">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa498-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa498-140">Remarks</span></span>

<span data-ttu-id="fa498-141">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fa498-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fa498-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa498-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa498-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fa498-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa498-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa498-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fa498-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fa498-145">Schema Name</span></span>  <br/> |<span data-ttu-id="fa498-146">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="fa498-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="fa498-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fa498-147">Validation File</span></span>  <br/> |<span data-ttu-id="fa498-148">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="fa498-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fa498-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fa498-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="fa498-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa498-150">See also</span></span>

- [<span data-ttu-id="fa498-151">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fa498-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

