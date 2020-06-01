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
ms.openlocfilehash: 7e6c4631ef589555ce4d5da747c200ffe956f3a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459443"
---
# <a name="uniquebodytype"></a><span data-ttu-id="668bc-103">UniqueBodyType</span><span class="sxs-lookup"><span data-stu-id="668bc-103">UniqueBodyType</span></span>

<span data-ttu-id="668bc-104">El elemento **UniqueBodyType** especifica si el cuerpo único se devuelve en formato de texto o HTML.</span><span class="sxs-lookup"><span data-stu-id="668bc-104">The **UniqueBodyType** element specifies whether the unique body is returned in text or HTML format.</span></span> 
  
```XML
<UniqueBodyType> Best | HTML | Text </UniqueBodyType>
```

 <span data-ttu-id="668bc-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="668bc-105">**BodyTypeResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="668bc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="668bc-106">Attributes and elements</span></span>

<span data-ttu-id="668bc-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="668bc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="668bc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="668bc-108">Attributes</span></span>

<span data-ttu-id="668bc-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="668bc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="668bc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="668bc-110">Child elements</span></span>

<span data-ttu-id="668bc-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="668bc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="668bc-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="668bc-112">Parent elements</span></span>

[<span data-ttu-id="668bc-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="668bc-113">ItemShape</span></span>](itemshape.md)
  
## <a name="text-value"></a><span data-ttu-id="668bc-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="668bc-114">Text value</span></span>

<span data-ttu-id="668bc-115">El valor de texto del elemento **UniqueBodyType** indica el formato en el que se devuelve el cuerpo único.</span><span class="sxs-lookup"><span data-stu-id="668bc-115">The text value of the **UniqueBodyType** element indicates format the unique body is returned in.</span></span> <span data-ttu-id="668bc-116">En la siguiente tabla se enumeran los valores posibles para este elemento.</span><span class="sxs-lookup"><span data-stu-id="668bc-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="668bc-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="668bc-117">**Value**</span></span>|<span data-ttu-id="668bc-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="668bc-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="668bc-119">Procedimientos</span><span class="sxs-lookup"><span data-stu-id="668bc-119">Best</span></span>  <br/> |<span data-ttu-id="668bc-120">La respuesta devolverá el contenido más enriquecido disponible del texto del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="668bc-120">The response will return the richest available content of body text.</span></span> <span data-ttu-id="668bc-121">Esto es útil si es desconocido si el contenido es de texto o HTML.</span><span class="sxs-lookup"><span data-stu-id="668bc-121">This is useful if it is unknown whether the content is text or HTML.</span></span>  <br/> <span data-ttu-id="668bc-122">El cuerpo devuelto será Text si el cuerpo almacenado es texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="668bc-122">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="668bc-123">De lo contrario, la respuesta devolverá HTML si el cuerpo almacenado está en formato HTML o RTF.</span><span class="sxs-lookup"><span data-stu-id="668bc-123">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span>  <br/> <span data-ttu-id="668bc-124">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="668bc-124">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="668bc-125">HTML</span><span class="sxs-lookup"><span data-stu-id="668bc-125">HTML</span></span>  <br/> |<span data-ttu-id="668bc-126">La respuesta devolverá un cuerpo único como HTML.</span><span class="sxs-lookup"><span data-stu-id="668bc-126">The response will return a unique body as HTML.</span></span>  <br/> |
|<span data-ttu-id="668bc-127">Texto</span><span class="sxs-lookup"><span data-stu-id="668bc-127">Text</span></span>  <br/> |<span data-ttu-id="668bc-128">La respuesta devolverá un cuerpo único como texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="668bc-128">The response will return a unique body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="668bc-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="668bc-129">Remarks</span></span>

<span data-ttu-id="668bc-130">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="668bc-130">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="668bc-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="668bc-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="668bc-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="668bc-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="668bc-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="668bc-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="668bc-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="668bc-134">Schema Name</span></span>  <br/> |<span data-ttu-id="668bc-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="668bc-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="668bc-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="668bc-136">Validation File</span></span>  <br/> |<span data-ttu-id="668bc-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="668bc-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="668bc-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="668bc-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="668bc-139">Verdadero</span><span class="sxs-lookup"><span data-stu-id="668bc-139">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="668bc-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="668bc-140">See also</span></span>



[<span data-ttu-id="668bc-141">ItemShape</span><span class="sxs-lookup"><span data-stu-id="668bc-141">ItemShape</span></span>](itemshape.md)


- [<span data-ttu-id="668bc-142">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="668bc-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

