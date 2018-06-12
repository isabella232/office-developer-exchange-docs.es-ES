---
title: Aficiones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f771b066-e42e-4880-bf18-709ad033d2af
description: El elemento aficiones especifica una matriz de las aficiones y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 0308269cb4b023c08433d62099fe22759ed498ef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835813"
---
# <a name="hobbies"></a><span data-ttu-id="ce542-103">Aficiones</span><span class="sxs-lookup"><span data-stu-id="ce542-103">Hobbies</span></span>

<span data-ttu-id="ce542-104">El elemento **aficiones** especifica una matriz de las aficiones y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="ce542-104">The **Hobbies** element specifies an array of hobbies and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Hobbies>
    <StringAttributedValue/>
</Hobbies>
```

 <span data-ttu-id="ce542-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="ce542-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ce542-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ce542-106">Attributes and elements</span></span>

<span data-ttu-id="ce542-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ce542-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce542-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ce542-108">Attributes</span></span>

<span data-ttu-id="ce542-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ce542-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ce542-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ce542-110">Child elements</span></span>

|<span data-ttu-id="ce542-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ce542-111">**Element**</span></span>|<span data-ttu-id="ce542-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce542-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce542-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="ce542-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="ce542-114">Especifica una instancia de una matriz de atributos asociados con un elemento de la persona.</span><span class="sxs-lookup"><span data-stu-id="ce542-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ce542-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ce542-115">Parent elements</span></span>

|<span data-ttu-id="ce542-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="ce542-116">**Element**</span></span>|<span data-ttu-id="ce542-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce542-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce542-118">Rol</span><span class="sxs-lookup"><span data-stu-id="ce542-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="ce542-119">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="ce542-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce542-120">Notas</span><span class="sxs-lookup"><span data-stu-id="ce542-120">Remarks</span></span>

<span data-ttu-id="ce542-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ce542-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ce542-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ce542-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ce542-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ce542-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce542-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ce542-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ce542-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ce542-125">Schema Name</span></span>  <br/> |<span data-ttu-id="ce542-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="ce542-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="ce542-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ce542-127">Validation File</span></span>  <br/> |<span data-ttu-id="ce542-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ce542-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="ce542-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ce542-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ce542-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="ce542-130">See also</span></span>



- [<span data-ttu-id="ce542-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ce542-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

