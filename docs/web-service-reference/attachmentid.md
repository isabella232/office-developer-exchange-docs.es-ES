---
title: AttachmentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentId
api_type:
- schema
ms.assetid: 55a5fd77-60d1-40fa-8144-770600cedc6a
description: El elemento AttachmentId identifica un elemento o archivo de datos adjuntos. Este elemento se usa en las respuestas CreateAttachment.
ms.openlocfilehash: 2910503d1661ca3aaeeb4e319deb39f6b57c5c0a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763567"
---
# <a name="attachmentid"></a><span data-ttu-id="b7d10-104">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="b7d10-104">AttachmentId</span></span>

<span data-ttu-id="b7d10-105">El elemento **AttachmentId** identifica un elemento o archivo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="b7d10-105">The **AttachmentId** element identifies an item or file attachment.</span></span> <span data-ttu-id="b7d10-106">Este elemento se usa en las respuestas CreateAttachment.</span><span class="sxs-lookup"><span data-stu-id="b7d10-106">This element is used in CreateAttachment responses.</span></span> 
  
```xml
<AttachmentId Id="" RootItemId="" RootItemChangeKey="" />
```

 <span data-ttu-id="b7d10-107">**AttachmentIdType**</span><span class="sxs-lookup"><span data-stu-id="b7d10-107">**AttachmentIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b7d10-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b7d10-108">Attributes and elements</span></span>

<span data-ttu-id="b7d10-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b7d10-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7d10-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="b7d10-110">Attributes</span></span>

|<span data-ttu-id="b7d10-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b7d10-111">**Attribute**</span></span>|<span data-ttu-id="b7d10-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b7d10-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b7d10-113">**Id**</span><span class="sxs-lookup"><span data-stu-id="b7d10-113">**Id**</span></span> <br/> |<span data-ttu-id="b7d10-114">Identifica el identificador único de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="b7d10-114">Identifies the unique identifier of the attachment.</span></span>  <br/> |
|<span data-ttu-id="b7d10-115">**RootItemId**</span><span class="sxs-lookup"><span data-stu-id="b7d10-115">**RootItemId**</span></span> <br/> |<span data-ttu-id="b7d10-116">Identifica el identificador único del elemento de almacén raíz al que se adjunta los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="b7d10-116">Identifies the unique identifier of the root store item to which the attachment is attached.</span></span>  <br/> |
|<span data-ttu-id="b7d10-117">**RootItemChangeKey**</span><span class="sxs-lookup"><span data-stu-id="b7d10-117">**RootItemChangeKey**</span></span> <br/> |<span data-ttu-id="b7d10-118">Identifica la clave de cambio del elemento raíz del almacén al que se adjunta los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="b7d10-118">Identifies the change key of the root store item to which the attachment is attached.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b7d10-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b7d10-119">Child elements</span></span>

<span data-ttu-id="b7d10-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b7d10-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b7d10-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b7d10-121">Parent elements</span></span>

|<span data-ttu-id="b7d10-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="b7d10-122">**Element**</span></span>|<span data-ttu-id="b7d10-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b7d10-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7d10-124">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="b7d10-124">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="b7d10-125">Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b7d10-125">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="b7d10-126">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="b7d10-126">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="b7d10-127">Representa un archivo que se adjunta a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b7d10-127">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7d10-128">Notas</span><span class="sxs-lookup"><span data-stu-id="b7d10-128">Remarks</span></span>

<span data-ttu-id="b7d10-129">Es importante tener en cuenta que cuando se crea un archivo adjunto, se modifica la clave de cambio del elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="b7d10-129">It is important to note that when an attachment is created, the change key of the root item is altered.</span></span>
  
<span data-ttu-id="b7d10-130">El elemento [AttachmentId (GetAttachment y DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md) se usa en las solicitudes DeleteAttachment y GetAttachment.</span><span class="sxs-lookup"><span data-stu-id="b7d10-130">The [AttachmentId (GetAttachment and DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md) element is used in DeleteAttachment and GetAttachment requests.</span></span> 
  
<span data-ttu-id="b7d10-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b7d10-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7d10-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b7d10-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7d10-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b7d10-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b7d10-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b7d10-134">Schema name</span></span>  <br/> |<span data-ttu-id="b7d10-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b7d10-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="b7d10-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b7d10-136">Validation file</span></span>  <br/> |<span data-ttu-id="b7d10-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b7d10-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b7d10-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b7d10-138">Can be empty</span></span>  <br/> |<span data-ttu-id="b7d10-139">False</span><span class="sxs-lookup"><span data-stu-id="b7d10-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7d10-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="b7d10-140">See also</span></span>

- [<span data-ttu-id="b7d10-141">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b7d10-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

