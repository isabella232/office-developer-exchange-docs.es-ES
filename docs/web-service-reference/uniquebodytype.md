---
title: UniqueBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f7276aa-e354-40e4-b9cb-950fad46ac93
description: El elemento UniqueBodyType especifica si el cuerpo único se devuelve en formato de texto o HTML.
ms.openlocfilehash: c6eb4ec4e39a0c5355775a635db4c63efc666820
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840772"
---
# <a name="uniquebodytype"></a><span data-ttu-id="905fc-103">UniqueBodyType</span><span class="sxs-lookup"><span data-stu-id="905fc-103">UniqueBodyType</span></span>

<span data-ttu-id="905fc-104">El elemento **UniqueBodyType** especifica si el cuerpo único se devuelve en formato de texto o HTML.</span><span class="sxs-lookup"><span data-stu-id="905fc-104">The **UniqueBodyType** element specifies whether the unique body is returned in text or HTML format.</span></span> 
  
```XML
<UniqueBodyType> Best | HTML | Text </UniqueBodyType>
```

 <span data-ttu-id="905fc-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="905fc-105">**BodyTypeResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="905fc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="905fc-106">Attributes and elements</span></span>

<span data-ttu-id="905fc-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="905fc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="905fc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="905fc-108">Attributes</span></span>

<span data-ttu-id="905fc-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="905fc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="905fc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="905fc-110">Child elements</span></span>

<span data-ttu-id="905fc-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="905fc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="905fc-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="905fc-112">Parent elements</span></span>

[<span data-ttu-id="905fc-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="905fc-113">ItemShape</span></span>](itemshape.md)
  
## <a name="text-value"></a><span data-ttu-id="905fc-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="905fc-114">Text value</span></span>

<span data-ttu-id="905fc-115">El valor de texto del elemento **UniqueBodyType** indica que se devuelve el formato del cuerpo único en.</span><span class="sxs-lookup"><span data-stu-id="905fc-115">The text value of the **UniqueBodyType** element indicates format the unique body is returned in.</span></span> <span data-ttu-id="905fc-116">En la siguiente tabla se enumera los valores posibles para este elemento.</span><span class="sxs-lookup"><span data-stu-id="905fc-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="905fc-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="905fc-117">**Value**</span></span>|<span data-ttu-id="905fc-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="905fc-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="905fc-119">Mejor</span><span class="sxs-lookup"><span data-stu-id="905fc-119">Best</span></span>  <br/> |<span data-ttu-id="905fc-120">La respuesta devolverá el contenido disponible más completa del texto del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="905fc-120">The response will return the richest available content of body text.</span></span> <span data-ttu-id="905fc-121">Esto es útil si se desconoce si el contenido es texto o HTML.</span><span class="sxs-lookup"><span data-stu-id="905fc-121">This is useful if it is unknown whether the content is text or HTML.</span></span>  <br/> <span data-ttu-id="905fc-122">El cuerpo devuelto será texto si el cuerpo almacenado es texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="905fc-122">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="905fc-123">De lo contrario, la respuesta devolverá HTML si se encuentra el cuerpo almacenado en formato HTML o RTF.</span><span class="sxs-lookup"><span data-stu-id="905fc-123">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span>  <br/> <span data-ttu-id="905fc-124">Éste es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="905fc-124">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="905fc-125">HTML</span><span class="sxs-lookup"><span data-stu-id="905fc-125">HTML</span></span>  <br/> |<span data-ttu-id="905fc-126">La respuesta devolverá un único cuerpo como HTML.</span><span class="sxs-lookup"><span data-stu-id="905fc-126">The response will return a unique body as HTML.</span></span>  <br/> |
|<span data-ttu-id="905fc-127">Texto</span><span class="sxs-lookup"><span data-stu-id="905fc-127">Text</span></span>  <br/> |<span data-ttu-id="905fc-128">La respuesta devolverá un único cuerpo como texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="905fc-128">The response will return a unique body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="905fc-129">Notas</span><span class="sxs-lookup"><span data-stu-id="905fc-129">Remarks</span></span>

<span data-ttu-id="905fc-130">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="905fc-130">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="905fc-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="905fc-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="905fc-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="905fc-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="905fc-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="905fc-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="905fc-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="905fc-134">Schema Name</span></span>  <br/> |<span data-ttu-id="905fc-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="905fc-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="905fc-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="905fc-136">Validation File</span></span>  <br/> |<span data-ttu-id="905fc-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="905fc-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="905fc-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="905fc-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="905fc-139">Verdadero</span><span class="sxs-lookup"><span data-stu-id="905fc-139">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="905fc-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="905fc-140">See also</span></span>



[<span data-ttu-id="905fc-141">ItemShape</span><span class="sxs-lookup"><span data-stu-id="905fc-141">ItemShape</span></span>](itemshape.md)


- [<span data-ttu-id="905fc-142">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="905fc-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

