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
ms.openlocfilehash: e5d968673403eba24a68c67175e3ebcbb35eca39
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462664"
---
# <a name="normalizedbodytype"></a><span data-ttu-id="1ffd2-103">NormalizedBodyType</span><span class="sxs-lookup"><span data-stu-id="1ffd2-103">NormalizedBodyType</span></span>

<span data-ttu-id="1ffd2-104">El elemento **NormalizedBodyType** especifica si el cuerpo normalizado se devuelve en formato de texto o HTML.</span><span class="sxs-lookup"><span data-stu-id="1ffd2-104">The **NormalizedBodyType** element specifies whether the normalized body is returned in text or HTML format.</span></span> 
  
```XML
<NormalizedBodyType> Best | HTML | Text </NormalizedBodyType>
```

 <span data-ttu-id="1ffd2-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="1ffd2-105">**BodyTypeResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1ffd2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1ffd2-106">Attributes and elements</span></span>

<span data-ttu-id="1ffd2-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1ffd2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ffd2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1ffd2-108">Attributes</span></span>

<span data-ttu-id="1ffd2-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1ffd2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1ffd2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1ffd2-110">Child elements</span></span>

<span data-ttu-id="1ffd2-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1ffd2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1ffd2-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1ffd2-112">Parent elements</span></span>

[<span data-ttu-id="1ffd2-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="1ffd2-113">ItemShape</span></span>](itemshape.md)
  
## <a name="text-value"></a><span data-ttu-id="1ffd2-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1ffd2-114">Text value</span></span>

<span data-ttu-id="1ffd2-115">El valor de texto del elemento **NormalizedBodyType** indica el formato en el que se devuelve el cuerpo normalizado.</span><span class="sxs-lookup"><span data-stu-id="1ffd2-115">The text value of the **NormalizedBodyType** element indicates format the normalized body is returned in.</span></span> <span data-ttu-id="1ffd2-116">En la siguiente tabla se enumeran los valores posibles para este elemento.</span><span class="sxs-lookup"><span data-stu-id="1ffd2-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="1ffd2-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1ffd2-117">**Value**</span></span>|<span data-ttu-id="1ffd2-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ffd2-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ffd2-119">Procedimientos</span><span class="sxs-lookup"><span data-stu-id="1ffd2-119">Best</span></span>  <br/> |<span data-ttu-id="1ffd2-120">La respuesta devolverá el contenido más enriquecido disponible del texto del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="1ffd2-120">The response will return the richest available content of body text.</span></span> <span data-ttu-id="1ffd2-121">Esto es útil si es desconocido si el contenido es de texto o HTML.</span><span class="sxs-lookup"><span data-stu-id="1ffd2-121">This is useful if it is unknown whether the content is text or HTML.</span></span>  <br/> <span data-ttu-id="1ffd2-122">El cuerpo devuelto será Text si el cuerpo almacenado es texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="1ffd2-122">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="1ffd2-123">De lo contrario, la respuesta devolverá HTML si el cuerpo almacenado está en formato HTML o RTF.</span><span class="sxs-lookup"><span data-stu-id="1ffd2-123">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span>  <br/> <span data-ttu-id="1ffd2-124">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1ffd2-124">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="1ffd2-125">HTML</span><span class="sxs-lookup"><span data-stu-id="1ffd2-125">HTML</span></span>  <br/> |<span data-ttu-id="1ffd2-126">La respuesta devolverá un cuerpo normalizado como HTML.</span><span class="sxs-lookup"><span data-stu-id="1ffd2-126">The response will return a normalized body as HTML.</span></span>  <br/> |
|<span data-ttu-id="1ffd2-127">Texto</span><span class="sxs-lookup"><span data-stu-id="1ffd2-127">Text</span></span>  <br/> |<span data-ttu-id="1ffd2-128">La respuesta devolverá un cuerpo normalizado como texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="1ffd2-128">The response will return a normalized body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ffd2-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ffd2-129">Remarks</span></span>

<span data-ttu-id="1ffd2-130">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="1ffd2-130">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="1ffd2-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1ffd2-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ffd2-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1ffd2-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ffd2-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ffd2-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1ffd2-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1ffd2-134">Schema Name</span></span>  <br/> |<span data-ttu-id="1ffd2-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1ffd2-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="1ffd2-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1ffd2-136">Validation File</span></span>  <br/> |<span data-ttu-id="1ffd2-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1ffd2-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1ffd2-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1ffd2-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="1ffd2-139">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1ffd2-139">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ffd2-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ffd2-140">See also</span></span>



[<span data-ttu-id="1ffd2-141">ItemShape</span><span class="sxs-lookup"><span data-stu-id="1ffd2-141">ItemShape</span></span>](itemshape.md)


- [<span data-ttu-id="1ffd2-142">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1ffd2-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

