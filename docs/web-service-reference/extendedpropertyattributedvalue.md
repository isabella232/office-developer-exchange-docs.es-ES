---
title: ExtendedPropertyAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 90f3c5c5-f612-4e1b-b1f5-f92dd8524179
description: El elemento ExtendedPropertyAttributedValue especifica propiedades extendidas para un rol.
ms.openlocfilehash: 5c2ad5918d7ac666d5e26af6597b2c4c3dde6202
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460130"
---
# <a name="extendedpropertyattributedvalue"></a><span data-ttu-id="ebcb7-103">ExtendedPropertyAttributedValue</span><span class="sxs-lookup"><span data-stu-id="ebcb7-103">ExtendedPropertyAttributedValue</span></span>

<span data-ttu-id="ebcb7-104">El elemento **ExtendedPropertyAttributedValue** especifica propiedades extendidas para un rol.</span><span class="sxs-lookup"><span data-stu-id="ebcb7-104">The **ExtendedPropertyAttributedValue** element specifies extended properties for a persona.</span></span> 
  
```XML
<ExtendedPropertyAttributedValue>
    <Value/>
    <Attributions/>
</ExtendedPropertyAttributedValue>
```

 <span data-ttu-id="ebcb7-105">**ExtendedPropertyAttributedValueType**</span><span class="sxs-lookup"><span data-stu-id="ebcb7-105">**ExtendedPropertyAttributedValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ebcb7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ebcb7-106">Attributes and elements</span></span>

<span data-ttu-id="ebcb7-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ebcb7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ebcb7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ebcb7-108">Attributes</span></span>

<span data-ttu-id="ebcb7-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ebcb7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ebcb7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ebcb7-110">Child elements</span></span>

|<span data-ttu-id="ebcb7-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ebcb7-111">**Element**</span></span>|<span data-ttu-id="ebcb7-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ebcb7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ebcb7-113">Valor (ExtendedPropertyType)</span><span class="sxs-lookup"><span data-stu-id="ebcb7-113">Value (ExtendedPropertyType)</span></span>](value-extendedpropertytype.md) <br/> |<span data-ttu-id="ebcb7-114">Especifica una matriz de propiedades extendidas para un rol.</span><span class="sxs-lookup"><span data-stu-id="ebcb7-114">Specifies an array of extended properties for a persona.</span></span>  <br/> |
|[<span data-ttu-id="ebcb7-115">Atribuciones (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="ebcb7-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="ebcb7-116">Especifica una matriz de atribuciones para su elemento de **valor** asociado.</span><span class="sxs-lookup"><span data-stu-id="ebcb7-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ebcb7-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ebcb7-117">Parent elements</span></span>

|<span data-ttu-id="ebcb7-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ebcb7-118">**Element**</span></span>|<span data-ttu-id="ebcb7-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ebcb7-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ebcb7-120">ExtendedProperties (ArrayOfExtendedPropertyAttributedValueType)</span><span class="sxs-lookup"><span data-stu-id="ebcb7-120">ExtendedProperties (ArrayOfExtendedPropertyAttributedValueType)</span></span>](extendedproperties-arrayofextendedpropertyattributedvaluetype.md) <br/> |<span data-ttu-id="ebcb7-121">Contiene las propiedades extendidas usadas para las operaciones de almacenamiento de contactos unificadas.</span><span class="sxs-lookup"><span data-stu-id="ebcb7-121">Contains the extended properties used for Unified Contact Store operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ebcb7-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ebcb7-122">Remarks</span></span>

<span data-ttu-id="ebcb7-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ebcb7-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ebcb7-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ebcb7-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ebcb7-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ebcb7-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ebcb7-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="ebcb7-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ebcb7-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ebcb7-127">Schema Name</span></span>  <br/> |<span data-ttu-id="ebcb7-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="ebcb7-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="ebcb7-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ebcb7-129">Validation File</span></span>  <br/> |<span data-ttu-id="ebcb7-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ebcb7-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="ebcb7-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ebcb7-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ebcb7-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebcb7-132">See also</span></span>



- [<span data-ttu-id="ebcb7-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ebcb7-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

