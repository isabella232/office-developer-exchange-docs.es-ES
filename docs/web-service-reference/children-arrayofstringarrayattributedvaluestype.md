---
title: Elementos secundarios (ArrayOfStringArrayAttributedValuesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d37b3fd5-63f1-4003-a6ec-54adfce23d52
description: El elemento Children especifica una matriz de nombres y identificadores secundarios de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: f4217f8a444bfdb6d86ff7b912294cfad9cbdcdc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460235"
---
# <a name="children-arrayofstringarrayattributedvaluestype"></a><span data-ttu-id="e0a65-103">Elementos secundarios (ArrayOfStringArrayAttributedValuesType)</span><span class="sxs-lookup"><span data-stu-id="e0a65-103">Children (ArrayOfStringArrayAttributedValuesType)</span></span>

<span data-ttu-id="e0a65-104">El elemento **Children** especifica una matriz de nombres y identificadores secundarios de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="e0a65-104">The **Children** element specifies an array of child names and identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Children>
    <StringAttributedValue></StringAttributedValue>
</Children>
```

 <span data-ttu-id="e0a65-105">**ArrayOfStringArrayAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="e0a65-105">**ArrayOfStringArrayAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0a65-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e0a65-106">Attributes and elements</span></span>

<span data-ttu-id="e0a65-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e0a65-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0a65-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e0a65-108">Attributes</span></span>

<span data-ttu-id="e0a65-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e0a65-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0a65-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e0a65-110">Child elements</span></span>

|<span data-ttu-id="e0a65-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e0a65-111">**Element**</span></span>|<span data-ttu-id="e0a65-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0a65-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0a65-113">StringArrayAttributedValue</span><span class="sxs-lookup"><span data-stu-id="e0a65-113">StringArrayAttributedValue</span></span>](stringarrayattributedvalue.md) <br/> |<span data-ttu-id="e0a65-114">Especifica una instancia de una matriz de datos de cadena para un elemento de rol.</span><span class="sxs-lookup"><span data-stu-id="e0a65-114">Specifies an instance of an array of string data for a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e0a65-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e0a65-115">Parent elements</span></span>

|<span data-ttu-id="e0a65-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e0a65-116">**Element**</span></span>|<span data-ttu-id="e0a65-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0a65-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0a65-118">Rol</span><span class="sxs-lookup"><span data-stu-id="e0a65-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="e0a65-119">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="e0a65-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0a65-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0a65-120">Remarks</span></span>

<span data-ttu-id="e0a65-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e0a65-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e0a65-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0a65-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0a65-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e0a65-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0a65-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0a65-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e0a65-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e0a65-125">Schema Name</span></span>  <br/> |<span data-ttu-id="e0a65-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="e0a65-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="e0a65-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e0a65-127">Validation File</span></span>  <br/> |<span data-ttu-id="e0a65-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e0a65-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="e0a65-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e0a65-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e0a65-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0a65-130">See also</span></span>



- [<span data-ttu-id="e0a65-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e0a65-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

