---
title: BusinessPhoneNumbers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ecbe4f1c-1c9e-44e0-a8f7-08c160a0fddb
description: El elemento BusinessPhoneNumbers especifica una matriz de números de teléfono de negocio y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 692c38a00241da9f753c431612f4a8fcf26cc7ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763685"
---
# <a name="businessphonenumbers"></a><span data-ttu-id="aaf7d-103">BusinessPhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="aaf7d-103">BusinessPhoneNumbers</span></span>

<span data-ttu-id="aaf7d-104">El elemento **BusinessPhoneNumbers** especifica una matriz de números de teléfono de negocio y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="aaf7d-104">The **BusinessPhoneNumbers** element specifies an array of business phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<BusinessPhoneNumbers>
    <Value></Value>
    <Attributions></Attributions>
</BusinessPhoneNumbers>
```

 <span data-ttu-id="aaf7d-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="aaf7d-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aaf7d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="aaf7d-106">Attributes and elements</span></span>

<span data-ttu-id="aaf7d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="aaf7d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aaf7d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="aaf7d-108">Attributes</span></span>

<span data-ttu-id="aaf7d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aaf7d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aaf7d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aaf7d-110">Child elements</span></span>

|<span data-ttu-id="aaf7d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="aaf7d-111">**Element**</span></span>|<span data-ttu-id="aaf7d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aaf7d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aaf7d-113">Valor (PersonaPhoneNumberType)</span><span class="sxs-lookup"><span data-stu-id="aaf7d-113">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md) <br/> |<span data-ttu-id="aaf7d-114">Especifica un teléfono número y tipo de la información y está asociado con un conjunto de atribuciones.</span><span class="sxs-lookup"><span data-stu-id="aaf7d-114">Specifies a phone number and type information and is associated with a set of attributions.</span></span>  <br/> |
|[<span data-ttu-id="aaf7d-115">Atribuciones (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="aaf7d-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="aaf7d-116">Especifica una matriz de atribuciones para su elemento de **valor** asociado.</span><span class="sxs-lookup"><span data-stu-id="aaf7d-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aaf7d-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="aaf7d-117">Parent elements</span></span>

|<span data-ttu-id="aaf7d-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="aaf7d-118">**Element**</span></span>|<span data-ttu-id="aaf7d-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aaf7d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aaf7d-120">Rol</span><span class="sxs-lookup"><span data-stu-id="aaf7d-120">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="aaf7d-121">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="aaf7d-121">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aaf7d-122">Notas</span><span class="sxs-lookup"><span data-stu-id="aaf7d-122">Remarks</span></span>

<span data-ttu-id="aaf7d-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="aaf7d-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="aaf7d-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="aaf7d-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aaf7d-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="aaf7d-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aaf7d-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aaf7d-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aaf7d-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="aaf7d-127">Schema Name</span></span>  <br/> |<span data-ttu-id="aaf7d-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="aaf7d-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="aaf7d-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="aaf7d-129">Validation File</span></span>  <br/> |<span data-ttu-id="aaf7d-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="aaf7d-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="aaf7d-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="aaf7d-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="aaf7d-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="aaf7d-132">See also</span></span>



- [<span data-ttu-id="aaf7d-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="aaf7d-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

