---
title: HomeAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 57fb1b9d-2ba8-4359-ae79-35c0d56a2d0f
description: El elemento HomeAddresses especifica una matriz de direcciones de inicio y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: d6a1808bf000ac8bca1e2ce7865aa099037c5a5d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460893"
---
# <a name="homeaddresses"></a><span data-ttu-id="31c48-103">HomeAddresses</span><span class="sxs-lookup"><span data-stu-id="31c48-103">HomeAddresses</span></span>

<span data-ttu-id="31c48-104">El elemento **HomeAddresses** especifica una matriz de direcciones de inicio y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="31c48-104">The **HomeAddresses** element specifies an array of home addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<HomeAddresses>
    <PostalAddressAttributedValue/>
</HomeAddresses>
```

 <span data-ttu-id="31c48-105">**ArrayOfPostalAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="31c48-105">**ArrayOfPostalAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31c48-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="31c48-106">Attributes and elements</span></span>

<span data-ttu-id="31c48-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="31c48-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31c48-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="31c48-108">Attributes</span></span>

<span data-ttu-id="31c48-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="31c48-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="31c48-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="31c48-110">Child elements</span></span>

|<span data-ttu-id="31c48-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="31c48-111">**Element**</span></span>|<span data-ttu-id="31c48-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="31c48-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31c48-113">PostalAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="31c48-113">PostalAddressAttributedValue</span></span>](postaladdressattributedvalue.md) <br/> |<span data-ttu-id="31c48-114">Especifica una instancia de una matriz de direcciones postales y sus atribuciones asociadas.</span><span class="sxs-lookup"><span data-stu-id="31c48-114">Specifies an instance of an array of postal addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="31c48-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="31c48-115">Parent elements</span></span>

|<span data-ttu-id="31c48-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="31c48-116">**Element**</span></span>|<span data-ttu-id="31c48-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="31c48-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31c48-118">Rol</span><span class="sxs-lookup"><span data-stu-id="31c48-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="31c48-119">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="31c48-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31c48-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31c48-120">Remarks</span></span>

<span data-ttu-id="31c48-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="31c48-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="31c48-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="31c48-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31c48-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="31c48-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31c48-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="31c48-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="31c48-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="31c48-125">Schema Name</span></span>  <br/> |<span data-ttu-id="31c48-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="31c48-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="31c48-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="31c48-127">Validation File</span></span>  <br/> |<span data-ttu-id="31c48-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="31c48-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="31c48-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="31c48-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="31c48-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="31c48-130">See also</span></span>



- [<span data-ttu-id="31c48-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="31c48-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

