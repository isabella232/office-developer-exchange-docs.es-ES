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
ms.openlocfilehash: b92108ecde63d4a3ac3cc80861c204c4d1950cc0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764528"
---
# <a name="extendedproperties-nonemptyarrayofextendedpropertytype"></a><span data-ttu-id="17dc1-103">ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)</span><span class="sxs-lookup"><span data-stu-id="17dc1-103">ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)</span></span>

<span data-ttu-id="17dc1-104">El elemento **ExtendedProperties** especifica una matriz de propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="17dc1-104">The **ExtendedProperties** element specifies an array of additional properties.</span></span> 
  
```XML
<ExtendedProperties>
    <ExtendedProperty/>
</ExtendedProperties>
```

 <span data-ttu-id="17dc1-105">**NonEmptyArrayOfExtendedPropertyType**</span><span class="sxs-lookup"><span data-stu-id="17dc1-105">**NonEmptyArrayOfExtendedPropertyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="17dc1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="17dc1-106">Attributes and elements</span></span>

<span data-ttu-id="17dc1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="17dc1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17dc1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="17dc1-108">Attributes</span></span>

<span data-ttu-id="17dc1-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="17dc1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="17dc1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="17dc1-110">Child elements</span></span>

|<span data-ttu-id="17dc1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="17dc1-111">**Element**</span></span>|<span data-ttu-id="17dc1-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="17dc1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17dc1-113">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="17dc1-113">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="17dc1-114">Identifica las propiedades MAPI extendidas en carpetas y elementos.</span><span class="sxs-lookup"><span data-stu-id="17dc1-114">Identifies extended MAPI properties on folders and items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="17dc1-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="17dc1-115">Parent elements</span></span>

|<span data-ttu-id="17dc1-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="17dc1-116">**Element**</span></span>|<span data-ttu-id="17dc1-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="17dc1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17dc1-118">ImGroup</span><span class="sxs-lookup"><span data-stu-id="17dc1-118">ImGroup</span></span>](imgroup.md) <br/> |<span data-ttu-id="17dc1-119">Representa un grupo de mensajería instantáneo.</span><span class="sxs-lookup"><span data-stu-id="17dc1-119">Represents an instant messaging group.</span></span>  <br/> |
|[<span data-ttu-id="17dc1-120">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="17dc1-120">SearchPreviewItem</span></span>](searchpreviewitem.md) <br/> |<span data-ttu-id="17dc1-121">Especifica los primeros 256 caracteres de un elemento de buzón de correo para vista previa sin abrir el elemento.</span><span class="sxs-lookup"><span data-stu-id="17dc1-121">Specifies the first 256 characters of a mailbox item for preview without opening the item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17dc1-122">Notas</span><span class="sxs-lookup"><span data-stu-id="17dc1-122">Remarks</span></span>

<span data-ttu-id="17dc1-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="17dc1-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="17dc1-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="17dc1-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17dc1-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="17dc1-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17dc1-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="17dc1-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="17dc1-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="17dc1-127">Schema Name</span></span>  <br/> |<span data-ttu-id="17dc1-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="17dc1-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="17dc1-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="17dc1-129">Validation File</span></span>  <br/> |<span data-ttu-id="17dc1-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="17dc1-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="17dc1-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="17dc1-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="17dc1-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="17dc1-132">See also</span></span>



- [<span data-ttu-id="17dc1-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="17dc1-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

