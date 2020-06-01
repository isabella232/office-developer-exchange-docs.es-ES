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
description: El elemento AttachmentId identifica un elemento o datos adjuntos de archivo. Este elemento se usa en las respuestas de CreateAttachment.
ms.openlocfilehash: b5dc9299b615f0fc01b8afcbaabf0ec7996e53d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459114"
---
# <a name="attachmentid"></a><span data-ttu-id="7ff4e-104">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="7ff4e-104">AttachmentId</span></span>

<span data-ttu-id="7ff4e-105">El elemento **AttachmentId** identifica un elemento o datos adjuntos de archivo.</span><span class="sxs-lookup"><span data-stu-id="7ff4e-105">The **AttachmentId** element identifies an item or file attachment.</span></span> <span data-ttu-id="7ff4e-106">Este elemento se usa en las respuestas de CreateAttachment.</span><span class="sxs-lookup"><span data-stu-id="7ff4e-106">This element is used in CreateAttachment responses.</span></span> 
  
```xml
<AttachmentId Id="" RootItemId="" RootItemChangeKey="" />
```

 <span data-ttu-id="7ff4e-107">**AttachmentIdType**</span><span class="sxs-lookup"><span data-stu-id="7ff4e-107">**AttachmentIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7ff4e-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7ff4e-108">Attributes and elements</span></span>

<span data-ttu-id="7ff4e-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7ff4e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7ff4e-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="7ff4e-110">Attributes</span></span>

|<span data-ttu-id="7ff4e-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7ff4e-111">**Attribute**</span></span>|<span data-ttu-id="7ff4e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7ff4e-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7ff4e-113">**Id**</span><span class="sxs-lookup"><span data-stu-id="7ff4e-113">**Id**</span></span> <br/> |<span data-ttu-id="7ff4e-114">Identifica el identificador único de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7ff4e-114">Identifies the unique identifier of the attachment.</span></span>  <br/> |
|<span data-ttu-id="7ff4e-115">**RootItemId**</span><span class="sxs-lookup"><span data-stu-id="7ff4e-115">**RootItemId**</span></span> <br/> |<span data-ttu-id="7ff4e-116">Identifica el identificador único del elemento de almacén raíz al que se adjuntan los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7ff4e-116">Identifies the unique identifier of the root store item to which the attachment is attached.</span></span>  <br/> |
|<span data-ttu-id="7ff4e-117">**RootItemChangeKey**</span><span class="sxs-lookup"><span data-stu-id="7ff4e-117">**RootItemChangeKey**</span></span> <br/> |<span data-ttu-id="7ff4e-118">Identifica la clave de cambio del elemento de almacén raíz al que se adjuntan los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7ff4e-118">Identifies the change key of the root store item to which the attachment is attached.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7ff4e-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7ff4e-119">Child elements</span></span>

<span data-ttu-id="7ff4e-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7ff4e-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7ff4e-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7ff4e-121">Parent elements</span></span>

|<span data-ttu-id="7ff4e-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7ff4e-122">**Element**</span></span>|<span data-ttu-id="7ff4e-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7ff4e-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ff4e-124">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="7ff4e-124">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="7ff4e-125">Representa un elemento de Exchange que está adjunto a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7ff4e-125">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="7ff4e-126">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="7ff4e-126">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="7ff4e-127">Representa un archivo que está adjunto a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7ff4e-127">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ff4e-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ff4e-128">Remarks</span></span>

<span data-ttu-id="7ff4e-129">Es importante tener en cuenta que cuando se crea un archivo adjunto, se modifica la clave de cambio del elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="7ff4e-129">It is important to note that when an attachment is created, the change key of the root item is altered.</span></span>
  
<span data-ttu-id="7ff4e-130">El elemento [AttachmentId (GetAttachment y DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md) se usa en solicitudes DeleteAttachment y GetAttachment.</span><span class="sxs-lookup"><span data-stu-id="7ff4e-130">The [AttachmentId (GetAttachment and DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md) element is used in DeleteAttachment and GetAttachment requests.</span></span> 
  
<span data-ttu-id="7ff4e-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="7ff4e-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7ff4e-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7ff4e-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ff4e-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="7ff4e-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7ff4e-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7ff4e-134">Schema name</span></span>  <br/> |<span data-ttu-id="7ff4e-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7ff4e-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="7ff4e-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7ff4e-136">Validation file</span></span>  <br/> |<span data-ttu-id="7ff4e-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="7ff4e-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7ff4e-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7ff4e-138">Can be empty</span></span>  <br/> |<span data-ttu-id="7ff4e-139">Falso</span><span class="sxs-lookup"><span data-stu-id="7ff4e-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ff4e-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ff4e-140">See also</span></span>

- [<span data-ttu-id="7ff4e-141">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7ff4e-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

