---
title: Distintas
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 637560b5-2b08-4787-a5d8-e0467f83acca
description: El elemento generaciones especifica una matriz de valores de generación y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: a3ef0e2c73e2ebd7c121f817b8ea97c5e4d4d333
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463016"
---
# <a name="generations"></a><span data-ttu-id="7ac22-103">Distintas</span><span class="sxs-lookup"><span data-stu-id="7ac22-103">Generations</span></span>

<span data-ttu-id="7ac22-104">El elemento **generaciones** especifica una matriz de valores de generación y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="7ac22-104">The **Generations** element specifies an array of generation values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Generations>
    <StringAttributedValue/>
</Generations>
```

 <span data-ttu-id="7ac22-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="7ac22-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7ac22-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7ac22-106">Attributes and elements</span></span>

<span data-ttu-id="7ac22-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7ac22-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7ac22-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7ac22-108">Attributes</span></span>

<span data-ttu-id="7ac22-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7ac22-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7ac22-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7ac22-110">Child elements</span></span>

|<span data-ttu-id="7ac22-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7ac22-111">**Element**</span></span>|<span data-ttu-id="7ac22-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7ac22-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ac22-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="7ac22-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="7ac22-114">Especifica una instancia de una matriz de atributos asociada a un elemento de rol.</span><span class="sxs-lookup"><span data-stu-id="7ac22-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7ac22-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7ac22-115">Parent elements</span></span>

|<span data-ttu-id="7ac22-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7ac22-116">**Element**</span></span>|<span data-ttu-id="7ac22-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7ac22-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ac22-118">Rol</span><span class="sxs-lookup"><span data-stu-id="7ac22-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="7ac22-119">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="7ac22-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ac22-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ac22-120">Remarks</span></span>

<span data-ttu-id="7ac22-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7ac22-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7ac22-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7ac22-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7ac22-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7ac22-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ac22-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="7ac22-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7ac22-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7ac22-125">Schema Name</span></span>  <br/> |<span data-ttu-id="7ac22-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="7ac22-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="7ac22-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7ac22-127">Validation File</span></span>  <br/> |<span data-ttu-id="7ac22-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="7ac22-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="7ac22-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7ac22-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="7ac22-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ac22-130">See also</span></span>



- [<span data-ttu-id="7ac22-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7ac22-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

