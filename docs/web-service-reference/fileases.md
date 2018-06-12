---
title: FileAses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f81efc37-bb70-4d52-a614-cec87d1b0f04
description: El elemento FileAses especifica una matriz de elementos de StringAttributedValue y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: e660c74135dca9a2eb58b3486e0d2e19f85e012f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764590"
---
# <a name="fileases"></a><span data-ttu-id="39589-103">FileAses</span><span class="sxs-lookup"><span data-stu-id="39589-103">FileAses</span></span>

<span data-ttu-id="39589-104">El elemento **FileAses** especifica una matriz de elementos de **StringAttributedValue** y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="39589-104">The **FileAses** element specifies an array of **StringAttributedValue** elements and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<FileAses>
    <StringAttributedValue/>
</FileAses>
```

 <span data-ttu-id="39589-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="39589-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="39589-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="39589-106">Attributes and elements</span></span>

<span data-ttu-id="39589-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="39589-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39589-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="39589-108">Attributes</span></span>

<span data-ttu-id="39589-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="39589-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="39589-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="39589-110">Child elements</span></span>

|<span data-ttu-id="39589-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="39589-111">**Element**</span></span>|<span data-ttu-id="39589-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="39589-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39589-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="39589-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="39589-114">Especifica una instancia de una matriz de atributos asociados con un elemento de la persona.</span><span class="sxs-lookup"><span data-stu-id="39589-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="39589-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="39589-115">Parent elements</span></span>

|<span data-ttu-id="39589-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="39589-116">**Element**</span></span>|<span data-ttu-id="39589-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="39589-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39589-118">Rol</span><span class="sxs-lookup"><span data-stu-id="39589-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="39589-119">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="39589-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39589-120">Notas</span><span class="sxs-lookup"><span data-stu-id="39589-120">Remarks</span></span>

<span data-ttu-id="39589-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="39589-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="39589-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="39589-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39589-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="39589-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39589-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="39589-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="39589-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="39589-125">Schema Name</span></span>  <br/> |<span data-ttu-id="39589-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="39589-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="39589-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="39589-127">Validation File</span></span>  <br/> |<span data-ttu-id="39589-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="39589-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="39589-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="39589-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="39589-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="39589-130">See also</span></span>



- [<span data-ttu-id="39589-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="39589-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

