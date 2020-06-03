---
title: AcceptSharingInvitation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AcceptSharingInvitation
api_type:
- schema
ms.assetid: 3c2a47d6-490d-425b-8893-089a4f8882cd
description: El elemento AcceptSharingInvitation se usa para aceptar una invitación que permite obtener acceso a los datos de contactos o calendario de otro usuario.
ms.openlocfilehash: c8cdae707bd122e74fa0e284163d1540d857c3de
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461712"
---
# <a name="acceptsharinginvitation"></a><span data-ttu-id="6748f-103">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="6748f-103">AcceptSharingInvitation</span></span>

<span data-ttu-id="6748f-104">El elemento **AcceptSharingInvitation** se usa para aceptar una invitación que permite obtener acceso a los datos de contactos o calendario de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="6748f-104">The **AcceptSharingInvitation** element is used to accept an invitation that allows access to another user's calendar or contacts data.</span></span> 
  
```xml
<AcceptSharingInvitation>
   <ReferenceItemId/>
</AcceptSharingInvitation>
```

 <span data-ttu-id="6748f-105">**AcceptSharingInvitationType**</span><span class="sxs-lookup"><span data-stu-id="6748f-105">**AcceptSharingInvitationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6748f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6748f-106">Attributes and elements</span></span>

<span data-ttu-id="6748f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6748f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6748f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6748f-108">Attributes</span></span>

<span data-ttu-id="6748f-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6748f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6748f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6748f-110">Child elements</span></span>

|<span data-ttu-id="6748f-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6748f-111">**Element**</span></span>|<span data-ttu-id="6748f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6748f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6748f-113">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="6748f-113">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="6748f-114">Identifica el elemento al que hace referencia el objeto de respuesta.</span><span class="sxs-lookup"><span data-stu-id="6748f-114">Identifies the item to which the response object refers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6748f-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6748f-115">Parent elements</span></span>

|<span data-ttu-id="6748f-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6748f-116">**Element**</span></span>|<span data-ttu-id="6748f-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6748f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6748f-118">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="6748f-118">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="6748f-119">Contiene una colección de todos los objetos de respuesta que están asociados a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6748f-119">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6748f-120">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="6748f-120">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="6748f-121">Contiene una matriz de elementos que se van a crear en la carpeta identificada por el elemento [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="6748f-121">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6748f-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6748f-122">Remarks</span></span>

<span data-ttu-id="6748f-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6748f-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6748f-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6748f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6748f-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="6748f-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6748f-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6748f-126">Schema Name</span></span>  <br/> |<span data-ttu-id="6748f-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6748f-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="6748f-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6748f-128">Validation File</span></span>  <br/> |<span data-ttu-id="6748f-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6748f-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6748f-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6748f-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="6748f-131">Falso</span><span class="sxs-lookup"><span data-stu-id="6748f-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6748f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6748f-132">See also</span></span>

- [<span data-ttu-id="6748f-133">CreateItem (AcceptSharingInvitation)</span><span class="sxs-lookup"><span data-stu-id="6748f-133">CreateItem (AcceptSharingInvitation)</span></span>](createitem-acceptsharinginvitation.md)
- [<span data-ttu-id="6748f-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6748f-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

