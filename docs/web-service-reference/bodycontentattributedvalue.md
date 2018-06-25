---
title: BodyContentAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f99e9590-8388-4203-ac30-1ea394f351a6
description: El elemento BodyContentAttributedValue especifica el contenido del cuerpo de un elemento.
ms.openlocfilehash: f5b8f0a19b77ce550b1d7f1c415cc8ee4340863a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763656"
---
# <a name="bodycontentattributedvalue"></a><span data-ttu-id="89f99-103">BodyContentAttributedValue</span><span class="sxs-lookup"><span data-stu-id="89f99-103">BodyContentAttributedValue</span></span>

<span data-ttu-id="89f99-104">El elemento **BodyContentAttributedValue** especifica el contenido del cuerpo de un elemento.</span><span class="sxs-lookup"><span data-stu-id="89f99-104">The **BodyContentAttributedValue** element specifies the body content of an item.</span></span> 
  
```XML
<BodyContentAttributedValue>
   <Value></Value>
   <Attributions></Attributions>
</ BodyContentAttributedValue>
```

 <span data-ttu-id="89f99-105">**BodyContentAttributedValueType**</span><span class="sxs-lookup"><span data-stu-id="89f99-105">**BodyContentAttributedValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="89f99-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="89f99-106">Attributes and elements</span></span>

<span data-ttu-id="89f99-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="89f99-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89f99-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="89f99-108">Attributes</span></span>

<span data-ttu-id="89f99-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="89f99-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="89f99-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="89f99-110">Child elements</span></span>

|<span data-ttu-id="89f99-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="89f99-111">**Element**</span></span>|<span data-ttu-id="89f99-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="89f99-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89f99-113">Valor (BodyContentType)</span><span class="sxs-lookup"><span data-stu-id="89f99-113">Value (BodyContentType)</span></span>](value-bodycontenttype.md) <br/> |<span data-ttu-id="89f99-114">Especifica el valor de un elemento **BodyContentAttributedValue** .</span><span class="sxs-lookup"><span data-stu-id="89f99-114">Specifies the value of a **BodyContentAttributedValue** element.</span></span>  <br/> |
|[<span data-ttu-id="89f99-115">Atribuciones (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="89f99-115">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md) <br/> |<span data-ttu-id="89f99-116">Especifica una matriz de información de atribución para uno o varios de los contactos o los destinatarios de active directory agregados a la persona asociada.</span><span class="sxs-lookup"><span data-stu-id="89f99-116">Specifies an array of attribution information for one or more of the contacts or active directory recipients aggregated into the associated persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="89f99-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="89f99-117">Parent elements</span></span>

|<span data-ttu-id="89f99-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="89f99-118">**Element**</span></span>|<span data-ttu-id="89f99-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="89f99-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89f99-120">Cuerpos</span><span class="sxs-lookup"><span data-stu-id="89f99-120">Bodies</span></span>](bodies.md) <br/> |<span data-ttu-id="89f99-121">Especifica una matriz de elementos de **BodyContentAttributedValue** .</span><span class="sxs-lookup"><span data-stu-id="89f99-121">Specifies an array of **BodyContentAttributedValue** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89f99-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="89f99-122">Remarks</span></span>

<span data-ttu-id="89f99-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="89f99-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="89f99-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="89f99-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89f99-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="89f99-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89f99-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="89f99-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="89f99-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="89f99-127">Schema Name</span></span>  <br/> |<span data-ttu-id="89f99-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="89f99-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="89f99-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="89f99-129">Validation File</span></span>  <br/> |<span data-ttu-id="89f99-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="89f99-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="89f99-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="89f99-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="89f99-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="89f99-132">See also</span></span>



- [<span data-ttu-id="89f99-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="89f99-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

