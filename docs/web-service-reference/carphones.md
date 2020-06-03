---
title: CarPhones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ad096246-113c-42ea-9e63-861b546003e8
description: El elemento CarPhone especifica una matriz de números de teléfono de los coches y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 41d0cc264da69ab17b8ebf109759139c4249719e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462230"
---
# <a name="carphones"></a><span data-ttu-id="c020b-103">CarPhones</span><span class="sxs-lookup"><span data-stu-id="c020b-103">CarPhones</span></span>

<span data-ttu-id="c020b-104">El elemento **CarPhone** especifica una matriz de números de teléfono de los coches y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="c020b-104">The **CarPhone** element specifies an array of car phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<CarPhones>
    <Value></Value>
    <Attributions></Attributions>
</CarPhones>
```

 <span data-ttu-id="c020b-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="c020b-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c020b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c020b-106">Attributes and elements</span></span>

<span data-ttu-id="c020b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c020b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c020b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c020b-108">Attributes</span></span>

<span data-ttu-id="c020b-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c020b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c020b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c020b-110">Child elements</span></span>

|<span data-ttu-id="c020b-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c020b-111">**Element**</span></span>|<span data-ttu-id="c020b-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c020b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c020b-113">Valor (PersonaPhoneNumberType)</span><span class="sxs-lookup"><span data-stu-id="c020b-113">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md) <br/> |<span data-ttu-id="c020b-114">Especifica un número de teléfono y la información del tipo y está asociado a un conjunto de atribuciones.</span><span class="sxs-lookup"><span data-stu-id="c020b-114">Specifies a phone number and type information and is associated with a set of attributions.</span></span>  <br/> |
|[<span data-ttu-id="c020b-115">Atribuciones (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="c020b-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="c020b-116">Especifica una matriz de atribuciones para su elemento de **valor** asociado.</span><span class="sxs-lookup"><span data-stu-id="c020b-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c020b-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c020b-117">Parent elements</span></span>

|<span data-ttu-id="c020b-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c020b-118">**Element**</span></span>|<span data-ttu-id="c020b-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c020b-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c020b-120">Rol</span><span class="sxs-lookup"><span data-stu-id="c020b-120">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="c020b-121">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="c020b-121">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c020b-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c020b-122">Remarks</span></span>

<span data-ttu-id="c020b-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c020b-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c020b-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c020b-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c020b-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c020b-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c020b-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="c020b-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c020b-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c020b-127">Schema Name</span></span>  <br/> |<span data-ttu-id="c020b-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="c020b-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="c020b-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c020b-129">Validation File</span></span>  <br/> |<span data-ttu-id="c020b-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c020b-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c020b-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c020b-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c020b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="c020b-132">See also</span></span>



- [<span data-ttu-id="c020b-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c020b-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

