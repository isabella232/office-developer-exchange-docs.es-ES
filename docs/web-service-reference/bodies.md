---
title: Cuerpos
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a71a75f0-0b77-4cb9-8f9d-319de72fc1fd
description: El elemento de cuerpos especifica una matriz de elementos de BodyContentAttributedValue.
ms.openlocfilehash: 3316d25a567a791301c0e703a912ef28da42fa74
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763638"
---
# <a name="bodies"></a><span data-ttu-id="84f6c-103">Cuerpos</span><span class="sxs-lookup"><span data-stu-id="84f6c-103">Bodies</span></span>

<span data-ttu-id="84f6c-104">El elemento de **cuerpos** especifica una matriz de elementos de **BodyContentAttributedValue** .</span><span class="sxs-lookup"><span data-stu-id="84f6c-104">The **Bodies** element specifies an array of **BodyContentAttributedValue** elements.</span></span> 
  
```XML
<Bodies>
    <BodyContentAttributedValue></BodyContentAttributedValue>
<Bodies>
```

 <span data-ttu-id="84f6c-105">**ArrayOfBodyContentAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="84f6c-105">**ArrayOfBodyContentAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="84f6c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="84f6c-106">Attributes and elements</span></span>

<span data-ttu-id="84f6c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="84f6c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84f6c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="84f6c-108">Attributes</span></span>

<span data-ttu-id="84f6c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="84f6c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="84f6c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="84f6c-110">Child elements</span></span>

|<span data-ttu-id="84f6c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="84f6c-111">**Element**</span></span>|<span data-ttu-id="84f6c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="84f6c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84f6c-113">BodyContentAttributedValue</span><span class="sxs-lookup"><span data-stu-id="84f6c-113">BodyContentAttributedValue</span></span>](bodycontentattributedvalue.md) <br/> |<span data-ttu-id="84f6c-114">Especifica el contenido del cuerpo de un elemento.</span><span class="sxs-lookup"><span data-stu-id="84f6c-114">Specifies the body content of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="84f6c-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="84f6c-115">Parent elements</span></span>

|<span data-ttu-id="84f6c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="84f6c-116">**Element**</span></span>|<span data-ttu-id="84f6c-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="84f6c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84f6c-118">Rol</span><span class="sxs-lookup"><span data-stu-id="84f6c-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="84f6c-119">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="84f6c-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84f6c-120">Notas</span><span class="sxs-lookup"><span data-stu-id="84f6c-120">Remarks</span></span>

<span data-ttu-id="84f6c-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="84f6c-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="84f6c-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="84f6c-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="84f6c-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="84f6c-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84f6c-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="84f6c-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="84f6c-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="84f6c-125">Schema Name</span></span>  <br/> |<span data-ttu-id="84f6c-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="84f6c-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="84f6c-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="84f6c-127">Validation File</span></span>  <br/> |<span data-ttu-id="84f6c-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="84f6c-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="84f6c-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="84f6c-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="84f6c-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="84f6c-130">See also</span></span>



- [<span data-ttu-id="84f6c-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="84f6c-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

