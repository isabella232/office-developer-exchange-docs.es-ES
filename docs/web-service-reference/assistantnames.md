---
title: AssistantNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4e69022d-1cef-4744-877c-848a0b5c4f40
description: El elemento AssistantNames especifica una matriz de nombres de asistente y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 7414caa74dc8221d0b1b471c3d5ed09552f7e200
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763561"
---
# <a name="assistantnames"></a><span data-ttu-id="04496-103">AssistantNames</span><span class="sxs-lookup"><span data-stu-id="04496-103">AssistantNames</span></span>

<span data-ttu-id="04496-104">El elemento **AssistantNames** especifica una matriz de nombres de asistente y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="04496-104">The **AssistantNames** element specifies an array of assistant names and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<AssistantNames>
    <StringAttributedValue></StringAttributedValue>
</AssistantNames>
```

 <span data-ttu-id="04496-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="04496-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="04496-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="04496-106">Attributes and elements</span></span>

<span data-ttu-id="04496-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="04496-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04496-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="04496-108">Attributes</span></span>

<span data-ttu-id="04496-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="04496-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="04496-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="04496-110">Child elements</span></span>

|<span data-ttu-id="04496-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="04496-111">**Element**</span></span>|<span data-ttu-id="04496-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="04496-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="04496-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="04496-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="04496-114">Especifica una instancia de una matriz de atributos asociados con un elemento de la persona.</span><span class="sxs-lookup"><span data-stu-id="04496-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="04496-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="04496-115">Parent elements</span></span>

|<span data-ttu-id="04496-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="04496-116">**Element**</span></span>|<span data-ttu-id="04496-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="04496-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="04496-118">Rol</span><span class="sxs-lookup"><span data-stu-id="04496-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="04496-119">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="04496-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04496-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04496-120">Remarks</span></span>

<span data-ttu-id="04496-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04496-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="04496-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="04496-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="04496-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="04496-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04496-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="04496-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="04496-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="04496-125">Schema Name</span></span>  <br/> |<span data-ttu-id="04496-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="04496-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="04496-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="04496-127">Validation File</span></span>  <br/> |<span data-ttu-id="04496-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="04496-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="04496-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="04496-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="04496-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="04496-130">See also</span></span>

- [<span data-ttu-id="04496-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="04496-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

