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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840772"
---
# <a name="uniquebodytype"></a><span data-ttu-id="07447-103">UniqueBodyType</span><span class="sxs-lookup"><span data-stu-id="07447-103">UniqueBodyType</span></span>

<span data-ttu-id="07447-104">El elemento **UniqueBodyType** especifica si el cuerpo único se devuelve en formato de texto o HTML.</span><span class="sxs-lookup"><span data-stu-id="07447-104">The **UniqueBodyType** element specifies whether the unique body is returned in text or HTML format.</span></span> 
  
```XML
<UniqueBodyType> Best | HTML | Text </UniqueBodyType>
```

 <span data-ttu-id="07447-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="07447-105">**BodyTypeResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07447-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="07447-106">Attributes and elements</span></span>

<span data-ttu-id="07447-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="07447-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07447-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="07447-108">Attributes</span></span>

<span data-ttu-id="07447-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="07447-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="07447-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="07447-110">Child elements</span></span>

<span data-ttu-id="07447-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="07447-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="07447-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="07447-112">Parent elements</span></span>

[<span data-ttu-id="07447-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="07447-113">ItemShape</span></span>](itemshape.md)
  
## <a name="text-value"></a><span data-ttu-id="07447-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="07447-114">Text value</span></span>

<span data-ttu-id="07447-115">El valor de texto del elemento **UniqueBodyType** indica que se devuelve el formato del cuerpo único en.</span><span class="sxs-lookup"><span data-stu-id="07447-115">The text value of the **UniqueBodyType** element indicates format the unique body is returned in.</span></span> <span data-ttu-id="07447-116">En la siguiente tabla se enumera los valores posibles para este elemento.</span><span class="sxs-lookup"><span data-stu-id="07447-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="07447-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="07447-117">**Value**</span></span>|<span data-ttu-id="07447-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07447-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07447-119">Mejor</span><span class="sxs-lookup"><span data-stu-id="07447-119">Best</span></span>  <br/> |<span data-ttu-id="07447-120">La respuesta devolverá el contenido disponible más completa del texto del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="07447-120">The response will return the richest available content of body text.</span></span> <span data-ttu-id="07447-121">Esto es útil si se desconoce si el contenido es texto o HTML.</span><span class="sxs-lookup"><span data-stu-id="07447-121">This is useful if it is unknown whether the content is text or HTML.</span></span>  <br/> <span data-ttu-id="07447-122">El cuerpo devuelto será texto si el cuerpo almacenado es texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="07447-122">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="07447-123">De lo contrario, la respuesta devolverá HTML si se encuentra el cuerpo almacenado en formato HTML o RTF.</span><span class="sxs-lookup"><span data-stu-id="07447-123">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span>  <br/> <span data-ttu-id="07447-124">Éste es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="07447-124">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="07447-125">HTML</span><span class="sxs-lookup"><span data-stu-id="07447-125">HTML</span></span>  <br/> |<span data-ttu-id="07447-126">La respuesta devolverá un único cuerpo como HTML.</span><span class="sxs-lookup"><span data-stu-id="07447-126">The response will return a unique body as HTML.</span></span>  <br/> |
|<span data-ttu-id="07447-127">Texto</span><span class="sxs-lookup"><span data-stu-id="07447-127">Text</span></span>  <br/> |<span data-ttu-id="07447-128">La respuesta devolverá un único cuerpo como texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="07447-128">The response will return a unique body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07447-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07447-129">Remarks</span></span>

<span data-ttu-id="07447-130">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="07447-130">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="07447-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="07447-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07447-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="07447-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07447-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="07447-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="07447-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="07447-134">Schema Name</span></span>  <br/> |<span data-ttu-id="07447-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="07447-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="07447-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="07447-136">Validation File</span></span>  <br/> |<span data-ttu-id="07447-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="07447-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="07447-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="07447-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="07447-139">Verdadero</span><span class="sxs-lookup"><span data-stu-id="07447-139">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07447-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="07447-140">See also</span></span>



[<span data-ttu-id="07447-141">ItemShape</span><span class="sxs-lookup"><span data-stu-id="07447-141">ItemShape</span></span>](itemshape.md)


- [<span data-ttu-id="07447-142">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="07447-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

