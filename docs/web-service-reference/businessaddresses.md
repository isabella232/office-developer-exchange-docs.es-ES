---
title: BusinessAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 828f8f62-7abf-44d4-8d58-f706d595a812
description: El elemento BusinessAddresses especifica una matriz de direcciones de negocio y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: bc7ad948572c24f913ae02abb9e8fc5a7b1e0b0d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763655"
---
# <a name="businessaddresses"></a><span data-ttu-id="05297-103">BusinessAddresses</span><span class="sxs-lookup"><span data-stu-id="05297-103">BusinessAddresses</span></span>

<span data-ttu-id="05297-104">El elemento **BusinessAddresses** especifica una matriz de direcciones de negocio y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="05297-104">The **BusinessAddresses** element specifies an array of business addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<BusinessAddresses>
    <PostalAddressAttributedValue></PostalAddressAttributedValue>
</BusinessAddresses
```

 <span data-ttu-id="05297-105">**ArrayOfPostalAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="05297-105">**ArrayOfPostalAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="05297-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="05297-106">Attributes and elements</span></span>

<span data-ttu-id="05297-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="05297-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05297-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="05297-108">Attributes</span></span>

<span data-ttu-id="05297-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="05297-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="05297-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="05297-110">Child elements</span></span>

|<span data-ttu-id="05297-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="05297-111">**Element**</span></span>|<span data-ttu-id="05297-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="05297-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05297-113">PostalAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="05297-113">PostalAddressAttributedValue</span></span>](postaladdressattributedvalue.md) <br/> |<span data-ttu-id="05297-114">Especifica una instancia de una matriz de direcciones postales y sus atribuciones asociados.</span><span class="sxs-lookup"><span data-stu-id="05297-114">Specifies an instance of an array of postal addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="05297-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="05297-115">Parent elements</span></span>

|<span data-ttu-id="05297-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="05297-116">**Element**</span></span>|<span data-ttu-id="05297-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="05297-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05297-118">Rol</span><span class="sxs-lookup"><span data-stu-id="05297-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="05297-119">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="05297-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05297-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="05297-120">Remarks</span></span>

<span data-ttu-id="05297-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="05297-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="05297-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="05297-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05297-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="05297-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05297-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="05297-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="05297-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="05297-125">Schema Name</span></span>  <br/> |<span data-ttu-id="05297-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="05297-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="05297-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="05297-127">Validation File</span></span>  <br/> |<span data-ttu-id="05297-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="05297-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="05297-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="05297-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="05297-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="05297-130">See also</span></span>



- [<span data-ttu-id="05297-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="05297-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

