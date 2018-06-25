---
title: Elementos secundarios (ArrayOfStringArrayAttributedValuesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d37b3fd5-63f1-4003-a6ec-54adfce23d52
description: El elemento de elementos secundarios especifica una matriz de nombres secundarios y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 7c98e7cb96cecad0d1b5122236b6cd0947c6b3d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763737"
---
# <a name="children-arrayofstringarrayattributedvaluestype"></a><span data-ttu-id="da8c7-103">Elementos secundarios (ArrayOfStringArrayAttributedValuesType)</span><span class="sxs-lookup"><span data-stu-id="da8c7-103">Children (ArrayOfStringArrayAttributedValuesType)</span></span>

<span data-ttu-id="da8c7-104">El elemento de **elementos secundarios** especifica una matriz de nombres secundarios y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="da8c7-104">The **Children** element specifies an array of child names and identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Children>
    <StringAttributedValue></StringAttributedValue>
</Children>
```

 <span data-ttu-id="da8c7-105">**ArrayOfStringArrayAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="da8c7-105">**ArrayOfStringArrayAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="da8c7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="da8c7-106">Attributes and elements</span></span>

<span data-ttu-id="da8c7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="da8c7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da8c7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="da8c7-108">Attributes</span></span>

<span data-ttu-id="da8c7-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="da8c7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da8c7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="da8c7-110">Child elements</span></span>

|<span data-ttu-id="da8c7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="da8c7-111">**Element**</span></span>|<span data-ttu-id="da8c7-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="da8c7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da8c7-113">StringArrayAttributedValue</span><span class="sxs-lookup"><span data-stu-id="da8c7-113">StringArrayAttributedValue</span></span>](stringarrayattributedvalue.md) <br/> |<span data-ttu-id="da8c7-114">Especifica una instancia de una matriz de datos de cadena de un elemento de la persona.</span><span class="sxs-lookup"><span data-stu-id="da8c7-114">Specifies an instance of an array of string data for a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="da8c7-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="da8c7-115">Parent elements</span></span>

|<span data-ttu-id="da8c7-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="da8c7-116">**Element**</span></span>|<span data-ttu-id="da8c7-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="da8c7-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da8c7-118">Rol</span><span class="sxs-lookup"><span data-stu-id="da8c7-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="da8c7-119">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="da8c7-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da8c7-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="da8c7-120">Remarks</span></span>

<span data-ttu-id="da8c7-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="da8c7-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="da8c7-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="da8c7-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="da8c7-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="da8c7-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da8c7-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="da8c7-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="da8c7-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="da8c7-125">Schema Name</span></span>  <br/> |<span data-ttu-id="da8c7-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="da8c7-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="da8c7-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="da8c7-127">Validation File</span></span>  <br/> |<span data-ttu-id="da8c7-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="da8c7-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="da8c7-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="da8c7-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="da8c7-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="da8c7-130">See also</span></span>



- [<span data-ttu-id="da8c7-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="da8c7-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

