---
title: CarPhones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ad096246-113c-42ea-9e63-861b546003e8
description: El elemento de teléfono de automóvil especifica una matriz de números de teléfono del automóvil y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 694b3578e127a84dfd2fb844c6e81b28553b687c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763726"
---
# <a name="carphones"></a><span data-ttu-id="3a2d7-103">CarPhones</span><span class="sxs-lookup"><span data-stu-id="3a2d7-103">CarPhones</span></span>

<span data-ttu-id="3a2d7-104">El elemento de **teléfono de automóvil** especifica una matriz de números de teléfono del automóvil y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="3a2d7-104">The **CarPhone** element specifies an array of car phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<CarPhones>
    <Value></Value>
    <Attributions></Attributions>
</CarPhones>
```

 <span data-ttu-id="3a2d7-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="3a2d7-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3a2d7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3a2d7-106">Attributes and elements</span></span>

<span data-ttu-id="3a2d7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3a2d7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a2d7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3a2d7-108">Attributes</span></span>

<span data-ttu-id="3a2d7-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3a2d7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a2d7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3a2d7-110">Child elements</span></span>

|<span data-ttu-id="3a2d7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a2d7-111">**Element**</span></span>|<span data-ttu-id="3a2d7-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a2d7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a2d7-113">Valor (PersonaPhoneNumberType)</span><span class="sxs-lookup"><span data-stu-id="3a2d7-113">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md) <br/> |<span data-ttu-id="3a2d7-114">Especifica un teléfono número y tipo de la información y está asociado con un conjunto de atribuciones.</span><span class="sxs-lookup"><span data-stu-id="3a2d7-114">Specifies a phone number and type information and is associated with a set of attributions.</span></span>  <br/> |
|[<span data-ttu-id="3a2d7-115">Atribuciones (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="3a2d7-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="3a2d7-116">Especifica una matriz de atribuciones para su elemento de **valor** asociado.</span><span class="sxs-lookup"><span data-stu-id="3a2d7-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3a2d7-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3a2d7-117">Parent elements</span></span>

|<span data-ttu-id="3a2d7-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a2d7-118">**Element**</span></span>|<span data-ttu-id="3a2d7-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a2d7-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a2d7-120">Rol</span><span class="sxs-lookup"><span data-stu-id="3a2d7-120">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="3a2d7-121">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="3a2d7-121">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a2d7-122">Notas</span><span class="sxs-lookup"><span data-stu-id="3a2d7-122">Remarks</span></span>

<span data-ttu-id="3a2d7-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3a2d7-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3a2d7-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a2d7-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a2d7-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3a2d7-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a2d7-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3a2d7-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3a2d7-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3a2d7-127">Schema Name</span></span>  <br/> |<span data-ttu-id="3a2d7-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="3a2d7-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="3a2d7-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3a2d7-129">Validation File</span></span>  <br/> |<span data-ttu-id="3a2d7-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3a2d7-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3a2d7-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3a2d7-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3a2d7-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="3a2d7-132">See also</span></span>



- [<span data-ttu-id="3a2d7-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3a2d7-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

