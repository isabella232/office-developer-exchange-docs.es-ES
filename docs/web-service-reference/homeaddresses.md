---
title: HomeAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 57fb1b9d-2ba8-4359-ae79-35c0d56a2d0f
description: El elemento HomeAddresses especifica una matriz de direcciones principales y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: a9d4ceafcac9cf0809668871b4df932b31525ac8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835817"
---
# <a name="homeaddresses"></a><span data-ttu-id="c2721-103">HomeAddresses</span><span class="sxs-lookup"><span data-stu-id="c2721-103">HomeAddresses</span></span>

<span data-ttu-id="c2721-104">El elemento **HomeAddresses** especifica una matriz de direcciones principales y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="c2721-104">The **HomeAddresses** element specifies an array of home addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<HomeAddresses>
    <PostalAddressAttributedValue/>
</HomeAddresses>
```

 <span data-ttu-id="c2721-105">**ArrayOfPostalAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="c2721-105">**ArrayOfPostalAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c2721-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c2721-106">Attributes and elements</span></span>

<span data-ttu-id="c2721-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c2721-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c2721-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c2721-108">Attributes</span></span>

<span data-ttu-id="c2721-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c2721-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c2721-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c2721-110">Child elements</span></span>

|<span data-ttu-id="c2721-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c2721-111">**Element**</span></span>|<span data-ttu-id="c2721-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2721-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2721-113">PostalAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="c2721-113">PostalAddressAttributedValue</span></span>](postaladdressattributedvalue.md) <br/> |<span data-ttu-id="c2721-114">Especifica una instancia de una matriz de direcciones postales y sus atribuciones asociados.</span><span class="sxs-lookup"><span data-stu-id="c2721-114">Specifies an instance of an array of postal addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c2721-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c2721-115">Parent elements</span></span>

|<span data-ttu-id="c2721-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c2721-116">**Element**</span></span>|<span data-ttu-id="c2721-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2721-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2721-118">Rol</span><span class="sxs-lookup"><span data-stu-id="c2721-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="c2721-119">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="c2721-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2721-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2721-120">Remarks</span></span>

<span data-ttu-id="c2721-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c2721-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c2721-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c2721-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c2721-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c2721-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2721-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c2721-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c2721-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c2721-125">Schema Name</span></span>  <br/> |<span data-ttu-id="c2721-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="c2721-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="c2721-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c2721-127">Validation File</span></span>  <br/> |<span data-ttu-id="c2721-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c2721-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c2721-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c2721-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c2721-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2721-130">See also</span></span>



- [<span data-ttu-id="c2721-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c2721-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

