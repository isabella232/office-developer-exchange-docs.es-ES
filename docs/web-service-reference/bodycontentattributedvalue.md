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
ms.openlocfilehash: 3550d9307e9bd652afc217f72610379a0a5b2f68
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527400"
---
# <a name="bodycontentattributedvalue"></a><span data-ttu-id="116da-103">BodyContentAttributedValue</span><span class="sxs-lookup"><span data-stu-id="116da-103">BodyContentAttributedValue</span></span>

<span data-ttu-id="116da-104">El elemento **BodyContentAttributedValue** especifica el contenido del cuerpo de un elemento.</span><span class="sxs-lookup"><span data-stu-id="116da-104">The **BodyContentAttributedValue** element specifies the body content of an item.</span></span> 
  
```XML
<BodyContentAttributedValue>
   <Value></Value>
   <Attributions></Attributions>
</ BodyContentAttributedValue>
```

 <span data-ttu-id="116da-105">**BodyContentAttributedValueType**</span><span class="sxs-lookup"><span data-stu-id="116da-105">**BodyContentAttributedValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="116da-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="116da-106">Attributes and elements</span></span>

<span data-ttu-id="116da-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="116da-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="116da-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="116da-108">Attributes</span></span>

<span data-ttu-id="116da-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="116da-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="116da-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="116da-110">Child elements</span></span>

|<span data-ttu-id="116da-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="116da-111">**Element**</span></span>|<span data-ttu-id="116da-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="116da-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="116da-113">Valor (BodyContentType)</span><span class="sxs-lookup"><span data-stu-id="116da-113">Value (BodyContentType)</span></span>](value-bodycontenttype.md) <br/> |<span data-ttu-id="116da-114">Especifica el valor de un elemento **BodyContentAttributedValue** .</span><span class="sxs-lookup"><span data-stu-id="116da-114">Specifies the value of a **BodyContentAttributedValue** element.</span></span>  <br/> |
|[<span data-ttu-id="116da-115">Atribuciones (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="116da-115">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md) <br/> |<span data-ttu-id="116da-116">Especifica una matriz de información de atribución de uno o varios de los contactos o de los destinatarios de Active Directory agregados al rol asociado.</span><span class="sxs-lookup"><span data-stu-id="116da-116">Specifies an array of attribution information for one or more of the contacts or active directory recipients aggregated into the associated persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="116da-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="116da-117">Parent elements</span></span>

|<span data-ttu-id="116da-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="116da-118">**Element**</span></span>|<span data-ttu-id="116da-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="116da-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="116da-120">Los</span><span class="sxs-lookup"><span data-stu-id="116da-120">Bodies</span></span>](bodies.md) <br/> |<span data-ttu-id="116da-121">Especifica una matriz de elementos **BodyContentAttributedValue** .</span><span class="sxs-lookup"><span data-stu-id="116da-121">Specifies an array of **BodyContentAttributedValue** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="116da-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="116da-122">Remarks</span></span>

<span data-ttu-id="116da-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="116da-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="116da-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="116da-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="116da-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="116da-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="116da-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="116da-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="116da-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="116da-127">Schema Name</span></span>  <br/> |<span data-ttu-id="116da-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="116da-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="116da-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="116da-129">Validation File</span></span>  <br/> |<span data-ttu-id="116da-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="116da-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="116da-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="116da-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="116da-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="116da-132">See also</span></span>



- [<span data-ttu-id="116da-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="116da-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

