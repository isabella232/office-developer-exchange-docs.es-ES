---
title: NormalizedBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c6973aee-ec7b-44c1-b328-f2204d9de5d1
description: El elemento NormalizedBodyType especifica si el cuerpo normalizado se devuelve en formato de texto o HTML.
ms.openlocfilehash: 33575594b22f972a9eb762dfac884fa91459f04a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836554"
---
# <a name="normalizedbodytype"></a><span data-ttu-id="348d7-103">NormalizedBodyType</span><span class="sxs-lookup"><span data-stu-id="348d7-103">NormalizedBodyType</span></span>

<span data-ttu-id="348d7-104">El elemento **NormalizedBodyType** especifica si el cuerpo normalizado se devuelve en formato de texto o HTML.</span><span class="sxs-lookup"><span data-stu-id="348d7-104">The **NormalizedBodyType** element specifies whether the normalized body is returned in text or HTML format.</span></span> 
  
```XML
<NormalizedBodyType> Best | HTML | Text </NormalizedBodyType>
```

 <span data-ttu-id="348d7-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="348d7-105">**BodyTypeResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="348d7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="348d7-106">Attributes and elements</span></span>

<span data-ttu-id="348d7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="348d7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="348d7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="348d7-108">Attributes</span></span>

<span data-ttu-id="348d7-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="348d7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="348d7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="348d7-110">Child elements</span></span>

<span data-ttu-id="348d7-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="348d7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="348d7-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="348d7-112">Parent elements</span></span>

[<span data-ttu-id="348d7-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="348d7-113">ItemShape</span></span>](itemshape.md)
  
## <a name="text-value"></a><span data-ttu-id="348d7-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="348d7-114">Text value</span></span>

<span data-ttu-id="348d7-115">El valor de texto del elemento **NormalizedBodyType** indica el formato del cuerpo normalizado se devuelve en.</span><span class="sxs-lookup"><span data-stu-id="348d7-115">The text value of the **NormalizedBodyType** element indicates format the normalized body is returned in.</span></span> <span data-ttu-id="348d7-116">En la siguiente tabla se enumera los valores posibles para este elemento.</span><span class="sxs-lookup"><span data-stu-id="348d7-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="348d7-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="348d7-117">**Value**</span></span>|<span data-ttu-id="348d7-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="348d7-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="348d7-119">Mejor</span><span class="sxs-lookup"><span data-stu-id="348d7-119">Best</span></span>  <br/> |<span data-ttu-id="348d7-120">La respuesta devolverá el contenido disponible más completa del texto del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="348d7-120">The response will return the richest available content of body text.</span></span> <span data-ttu-id="348d7-121">Esto es útil si se desconoce si el contenido es texto o HTML.</span><span class="sxs-lookup"><span data-stu-id="348d7-121">This is useful if it is unknown whether the content is text or HTML.</span></span>  <br/> <span data-ttu-id="348d7-122">El cuerpo devuelto será texto si el cuerpo almacenado es texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="348d7-122">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="348d7-123">De lo contrario, la respuesta devolverá HTML si se encuentra el cuerpo almacenado en formato HTML o RTF.</span><span class="sxs-lookup"><span data-stu-id="348d7-123">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span>  <br/> <span data-ttu-id="348d7-124">Éste es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="348d7-124">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="348d7-125">HTML</span><span class="sxs-lookup"><span data-stu-id="348d7-125">HTML</span></span>  <br/> |<span data-ttu-id="348d7-126">La respuesta devolverá un cuerpo normalizado como HTML.</span><span class="sxs-lookup"><span data-stu-id="348d7-126">The response will return a normalized body as HTML.</span></span>  <br/> |
|<span data-ttu-id="348d7-127">Texto</span><span class="sxs-lookup"><span data-stu-id="348d7-127">Text</span></span>  <br/> |<span data-ttu-id="348d7-128">La respuesta devolverá un cuerpo normalizado como texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="348d7-128">The response will return a normalized body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="348d7-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="348d7-129">Remarks</span></span>

<span data-ttu-id="348d7-130">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="348d7-130">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="348d7-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="348d7-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="348d7-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="348d7-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="348d7-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="348d7-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="348d7-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="348d7-134">Schema Name</span></span>  <br/> |<span data-ttu-id="348d7-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="348d7-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="348d7-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="348d7-136">Validation File</span></span>  <br/> |<span data-ttu-id="348d7-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="348d7-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="348d7-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="348d7-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="348d7-139">Verdadero</span><span class="sxs-lookup"><span data-stu-id="348d7-139">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="348d7-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="348d7-140">See also</span></span>



[<span data-ttu-id="348d7-141">ItemShape</span><span class="sxs-lookup"><span data-stu-id="348d7-141">ItemShape</span></span>](itemshape.md)


- [<span data-ttu-id="348d7-142">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="348d7-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

