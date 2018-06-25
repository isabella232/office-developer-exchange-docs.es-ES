---
title: BusinessPhoneNumbers2
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f335ea74-9b5b-4224-9475-40ef33fe76bd
description: El elemento BusinessPhoneNumbers2 especifica una matriz de elementos de BusinessPhoneNumber2 y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 8a03e102223e5542d6a672c4f47305cef84b850b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763698"
---
# <a name="businessphonenumbers2"></a><span data-ttu-id="8e0e9-103">BusinessPhoneNumbers2</span><span class="sxs-lookup"><span data-stu-id="8e0e9-103">BusinessPhoneNumbers2</span></span>

<span data-ttu-id="8e0e9-104">El elemento **BusinessPhoneNumbers2** especifica una matriz de elementos de **BusinessPhoneNumber2** y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="8e0e9-104">The **BusinessPhoneNumbers2** element specifies an array of **BusinessPhoneNumber2** elements and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<BusinessPhoneNumbers2>
    <Value></Value>
    <Attributions></Attributions>
</BusinessPhoneNumbers2>
```

 <span data-ttu-id="8e0e9-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="8e0e9-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8e0e9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8e0e9-106">Attributes and elements</span></span>

<span data-ttu-id="8e0e9-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8e0e9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8e0e9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8e0e9-108">Attributes</span></span>

<span data-ttu-id="8e0e9-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8e0e9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8e0e9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8e0e9-110">Child elements</span></span>

|<span data-ttu-id="8e0e9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8e0e9-111">**Element**</span></span>|<span data-ttu-id="8e0e9-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e0e9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e0e9-113">Valor (PersonaPhoneNumberType)</span><span class="sxs-lookup"><span data-stu-id="8e0e9-113">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md) <br/> |<span data-ttu-id="8e0e9-114">Especifica un teléfono número y tipo de la información y está asociado con un conjunto de atribuciones.</span><span class="sxs-lookup"><span data-stu-id="8e0e9-114">Specifies a phone number and type information and is associated with a set of attributions.</span></span>  <br/> |
|[<span data-ttu-id="8e0e9-115">Atribuciones (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="8e0e9-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="8e0e9-116">Especifica una matriz de atribuciones para su elemento de **valor** asociado.</span><span class="sxs-lookup"><span data-stu-id="8e0e9-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8e0e9-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8e0e9-117">Parent elements</span></span>

|<span data-ttu-id="8e0e9-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="8e0e9-118">**Element**</span></span>|<span data-ttu-id="8e0e9-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e0e9-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e0e9-120">Rol</span><span class="sxs-lookup"><span data-stu-id="8e0e9-120">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="8e0e9-121">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="8e0e9-121">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e0e9-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8e0e9-122">Remarks</span></span>

<span data-ttu-id="8e0e9-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8e0e9-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8e0e9-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="8e0e9-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8e0e9-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8e0e9-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e0e9-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8e0e9-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8e0e9-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8e0e9-127">Schema Name</span></span>  <br/> |<span data-ttu-id="8e0e9-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="8e0e9-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="8e0e9-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8e0e9-129">Validation File</span></span>  <br/> |<span data-ttu-id="8e0e9-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8e0e9-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="8e0e9-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8e0e9-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="8e0e9-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e0e9-132">See also</span></span>



- [<span data-ttu-id="8e0e9-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="8e0e9-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

