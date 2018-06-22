---
title: EmailAddressAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ebdf224d-3796-4179-aa0a-87942e7585ff
description: El elemento EmailAddressAttributedValue especifica una instancia de una matriz de direcciones de correo electrónico y sus atribuciones asociados.
ms.openlocfilehash: 3bcbb5c0a2bc9a2dc24516b5fc62e6e3363a360b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764349"
---
# <a name="emailaddressattributedvalue"></a><span data-ttu-id="3eeb1-103">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="3eeb1-103">EmailAddressAttributedValue</span></span>

<span data-ttu-id="3eeb1-104">El elemento **EmailAddressAttributedValue** especifica una instancia de una matriz de direcciones de correo electrónico y sus atribuciones asociados.</span><span class="sxs-lookup"><span data-stu-id="3eeb1-104">The **EmailAddressAttributedValue** element specifies an instance of an array of email addresses and their associated attributions.</span></span> 
  
```XML
<EmailAddressAttributedValue>
    <Value></Value>
    <Attributions></Attributions>
<EmailAddressAttributedValue>
```

 <span data-ttu-id="3eeb1-105">**EmailAddressAttributedValueType**</span><span class="sxs-lookup"><span data-stu-id="3eeb1-105">**EmailAddressAttributedValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3eeb1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3eeb1-106">Attributes and elements</span></span>

<span data-ttu-id="3eeb1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3eeb1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3eeb1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3eeb1-108">Attributes</span></span>

<span data-ttu-id="3eeb1-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3eeb1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3eeb1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3eeb1-110">Child elements</span></span>

|<span data-ttu-id="3eeb1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3eeb1-111">**Element**</span></span>|<span data-ttu-id="3eeb1-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3eeb1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3eeb1-113">Valor (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="3eeb1-113">Value (EmailAddressType)</span></span>](value-emailaddresstype.md) <br/> |<span data-ttu-id="3eeb1-114">Especifica que el valor de un **EmailAddress** asociado con una matriz de atribuciones.</span><span class="sxs-lookup"><span data-stu-id="3eeb1-114">Specifies the value of an **EmailAddress** associated with an attributions array.</span></span>  <br/> |
|[<span data-ttu-id="3eeb1-115">Atribuciones (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="3eeb1-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="3eeb1-116">Especifica una matriz de atribuciones para su elemento de **valor** asociado.</span><span class="sxs-lookup"><span data-stu-id="3eeb1-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3eeb1-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3eeb1-117">Parent elements</span></span>

|<span data-ttu-id="3eeb1-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="3eeb1-118">**Element**</span></span>|<span data-ttu-id="3eeb1-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3eeb1-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3eeb1-120">Emails1</span><span class="sxs-lookup"><span data-stu-id="3eeb1-120">Emails1</span></span>](emails1.md) <br/> |<span data-ttu-id="3eeb1-121">Especifica una matriz de valores de correo electrónico y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="3eeb1-121">Specifies an array of email values and the identifiers of their source attributions for the associated persona.</span></span>  <br/> |
|[<span data-ttu-id="3eeb1-122">Emails2</span><span class="sxs-lookup"><span data-stu-id="3eeb1-122">Emails2</span></span>](emails2.md) <br/> |<span data-ttu-id="3eeb1-123">Especifica una matriz de valores de correo electrónico y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="3eeb1-123">Specifies an array of email values and the identifiers of their source attributions for the associated persona.</span></span>  <br/> |
|[<span data-ttu-id="3eeb1-124">Emails3</span><span class="sxs-lookup"><span data-stu-id="3eeb1-124">Emails3</span></span>](emails3.md) <br/> |<span data-ttu-id="3eeb1-125">Especifica una matriz de valores de correo electrónico y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="3eeb1-125">Specifies an array of email values and the identifiers of their source attributions for the associated persona.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3eeb1-126">Notas</span><span class="sxs-lookup"><span data-stu-id="3eeb1-126">Remarks</span></span>

<span data-ttu-id="3eeb1-127">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3eeb1-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3eeb1-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3eeb1-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3eeb1-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3eeb1-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3eeb1-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3eeb1-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3eeb1-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3eeb1-131">Schema Name</span></span>  <br/> |<span data-ttu-id="3eeb1-132">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="3eeb1-132">Type schema</span></span>  <br/> |
|<span data-ttu-id="3eeb1-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3eeb1-133">Validation File</span></span>  <br/> |<span data-ttu-id="3eeb1-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3eeb1-134">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3eeb1-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3eeb1-135">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3eeb1-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="3eeb1-136">See also</span></span>



- [<span data-ttu-id="3eeb1-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3eeb1-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

