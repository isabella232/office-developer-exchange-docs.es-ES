---
title: HomePhones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8ea43d5a-4bcf-497e-a559-6efe94fa604b
description: El elemento HomePhones especifica una matriz de números de teléfono de casa y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: b55d6ca752a5b00a27eb158c6a22412a9f4ecdda
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460837"
---
# <a name="homephones"></a><span data-ttu-id="56975-103">HomePhones</span><span class="sxs-lookup"><span data-stu-id="56975-103">HomePhones</span></span>

<span data-ttu-id="56975-104">El elemento **HomePhones** especifica una matriz de números de teléfono de casa y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="56975-104">The **HomePhones** element specifies an array of home phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<HomePhones>
    <PhoneNumberAttributedValue/>
</HomePhones>
```

 <span data-ttu-id="56975-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="56975-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="56975-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="56975-106">Attributes and elements</span></span>

<span data-ttu-id="56975-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="56975-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="56975-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="56975-108">Attributes</span></span>

<span data-ttu-id="56975-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="56975-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="56975-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="56975-110">Child elements</span></span>

|<span data-ttu-id="56975-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="56975-111">**Element**</span></span>|<span data-ttu-id="56975-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="56975-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="56975-113">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="56975-113">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md) <br/> |<span data-ttu-id="56975-114">Contiene un número de teléfono con atributos único para un rol.</span><span class="sxs-lookup"><span data-stu-id="56975-114">Contains a single attributed phone number for a persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="56975-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="56975-115">Parent elements</span></span>

|<span data-ttu-id="56975-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="56975-116">**Element**</span></span>|<span data-ttu-id="56975-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="56975-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="56975-118">Rol</span><span class="sxs-lookup"><span data-stu-id="56975-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="56975-119">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="56975-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56975-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="56975-120">Remarks</span></span>

<span data-ttu-id="56975-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="56975-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="56975-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="56975-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="56975-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="56975-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56975-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="56975-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="56975-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="56975-125">Schema Name</span></span>  <br/> |<span data-ttu-id="56975-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="56975-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="56975-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="56975-127">Validation File</span></span>  <br/> |<span data-ttu-id="56975-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="56975-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="56975-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="56975-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="56975-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="56975-130">See also</span></span>



- [<span data-ttu-id="56975-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="56975-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

