---
title: ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7034730-210d-4916-b992-dda342f890f8
description: El elemento ExtendedProperties especifica una matriz de propiedades adicionales.
ms.openlocfilehash: 36011e0252ed391daefab190d4da679fb3a3f856
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463100"
---
# <a name="extendedproperties-nonemptyarrayofextendedpropertytype"></a><span data-ttu-id="9c67e-103">ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)</span><span class="sxs-lookup"><span data-stu-id="9c67e-103">ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)</span></span>

<span data-ttu-id="9c67e-104">El elemento **ExtendedProperties** especifica una matriz de propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="9c67e-104">The **ExtendedProperties** element specifies an array of additional properties.</span></span> 
  
```XML
<ExtendedProperties>
    <ExtendedProperty/>
</ExtendedProperties>
```

 <span data-ttu-id="9c67e-105">**NonEmptyArrayOfExtendedPropertyType**</span><span class="sxs-lookup"><span data-stu-id="9c67e-105">**NonEmptyArrayOfExtendedPropertyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9c67e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9c67e-106">Attributes and elements</span></span>

<span data-ttu-id="9c67e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9c67e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9c67e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9c67e-108">Attributes</span></span>

<span data-ttu-id="9c67e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9c67e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9c67e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9c67e-110">Child elements</span></span>

|<span data-ttu-id="9c67e-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9c67e-111">**Element**</span></span>|<span data-ttu-id="9c67e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9c67e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9c67e-113">Las extendedproperty</span><span class="sxs-lookup"><span data-stu-id="9c67e-113">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="9c67e-114">Identifica las propiedades de MAPI extendidas en carpetas y elementos.</span><span class="sxs-lookup"><span data-stu-id="9c67e-114">Identifies extended MAPI properties on folders and items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9c67e-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9c67e-115">Parent elements</span></span>

|<span data-ttu-id="9c67e-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9c67e-116">**Element**</span></span>|<span data-ttu-id="9c67e-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9c67e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9c67e-118">Desagrupo</span><span class="sxs-lookup"><span data-stu-id="9c67e-118">ImGroup</span></span>](imgroup.md) <br/> |<span data-ttu-id="9c67e-119">Representa un grupo de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="9c67e-119">Represents an instant messaging group.</span></span>  <br/> |
|[<span data-ttu-id="9c67e-120">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="9c67e-120">SearchPreviewItem</span></span>](searchpreviewitem.md) <br/> |<span data-ttu-id="9c67e-121">Especifica los primeros 256 caracteres de un elemento de buzón de correo para la vista previa sin abrir el elemento.</span><span class="sxs-lookup"><span data-stu-id="9c67e-121">Specifies the first 256 characters of a mailbox item for preview without opening the item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c67e-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9c67e-122">Remarks</span></span>

<span data-ttu-id="9c67e-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9c67e-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9c67e-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9c67e-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9c67e-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9c67e-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c67e-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="9c67e-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9c67e-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9c67e-127">Schema Name</span></span>  <br/> |<span data-ttu-id="9c67e-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="9c67e-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="9c67e-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9c67e-129">Validation File</span></span>  <br/> |<span data-ttu-id="9c67e-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="9c67e-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="9c67e-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9c67e-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="9c67e-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c67e-132">See also</span></span>



- [<span data-ttu-id="9c67e-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="9c67e-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

