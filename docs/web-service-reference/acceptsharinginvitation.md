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
description: El elemento AcceptSharingInvitation se usa para aceptar una invitación que permite el acceso al calendario de otro usuario o datos de los contactos.
ms.openlocfilehash: 06439739e6cc544d5039ac9d18e0452b1d42a0ed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764539"
---
# <a name="acceptsharinginvitation"></a><span data-ttu-id="46568-103">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="46568-103">AcceptSharingInvitation</span></span>

<span data-ttu-id="46568-104">El elemento **AcceptSharingInvitation** se usa para aceptar una invitación que permite el acceso al calendario de otro usuario o datos de los contactos.</span><span class="sxs-lookup"><span data-stu-id="46568-104">The **AcceptSharingInvitation** element is used to accept an invitation that allows access to another user's calendar or contacts data.</span></span> 
  
```xml
<AcceptSharingInvitation>
   <ReferenceItemId/>
</AcceptSharingInvitation>
```

 <span data-ttu-id="46568-105">**AcceptSharingInvitationType**</span><span class="sxs-lookup"><span data-stu-id="46568-105">**AcceptSharingInvitationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="46568-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="46568-106">Attributes and elements</span></span>

<span data-ttu-id="46568-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="46568-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="46568-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="46568-108">Attributes</span></span>

<span data-ttu-id="46568-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="46568-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="46568-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="46568-110">Child elements</span></span>

|<span data-ttu-id="46568-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="46568-111">**Element**</span></span>|<span data-ttu-id="46568-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="46568-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46568-113">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="46568-113">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="46568-114">Identifica el elemento al que hace referencia el objeto de respuesta.</span><span class="sxs-lookup"><span data-stu-id="46568-114">Identifies the item to which the response object refers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="46568-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="46568-115">Parent elements</span></span>

|<span data-ttu-id="46568-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="46568-116">**Element**</span></span>|<span data-ttu-id="46568-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="46568-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46568-118">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="46568-118">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="46568-119">Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="46568-119">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="46568-120">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="46568-120">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="46568-121">Contiene una matriz de elementos que desea crear en la carpeta que se identifica con el elemento [ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) .</span><span class="sxs-lookup"><span data-stu-id="46568-121">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46568-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46568-122">Remarks</span></span>

<span data-ttu-id="46568-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="46568-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="46568-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="46568-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46568-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="46568-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="46568-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="46568-126">Schema Name</span></span>  <br/> |<span data-ttu-id="46568-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="46568-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="46568-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="46568-128">Validation File</span></span>  <br/> |<span data-ttu-id="46568-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="46568-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="46568-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="46568-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="46568-131">False</span><span class="sxs-lookup"><span data-stu-id="46568-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46568-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="46568-132">See also</span></span>

- [<span data-ttu-id="46568-133">CreateItem (AcceptSharingInvitation)</span><span class="sxs-lookup"><span data-stu-id="46568-133">CreateItem (AcceptSharingInvitation)</span></span>](createitem-acceptsharinginvitation.md)
- [<span data-ttu-id="46568-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="46568-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

