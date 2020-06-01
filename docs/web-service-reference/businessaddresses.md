---
title: BusinessAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 828f8f62-7abf-44d4-8d58-f706d595a812
description: El elemento BusinessAddresses especifica una matriz de direcciones de empresa y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: d314d0de679f8eabc51dc9ee3b2e9a57cd0b8da1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465929"
---
# <a name="businessaddresses"></a><span data-ttu-id="c9488-103">BusinessAddresses</span><span class="sxs-lookup"><span data-stu-id="c9488-103">BusinessAddresses</span></span>

<span data-ttu-id="c9488-104">El elemento **BusinessAddresses** especifica una matriz de direcciones de empresa y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="c9488-104">The **BusinessAddresses** element specifies an array of business addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<BusinessAddresses>
    <PostalAddressAttributedValue></PostalAddressAttributedValue>
</BusinessAddresses
```

 <span data-ttu-id="c9488-105">**ArrayOfPostalAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="c9488-105">**ArrayOfPostalAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c9488-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c9488-106">Attributes and elements</span></span>

<span data-ttu-id="c9488-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c9488-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c9488-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c9488-108">Attributes</span></span>

<span data-ttu-id="c9488-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c9488-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c9488-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c9488-110">Child elements</span></span>

|<span data-ttu-id="c9488-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c9488-111">**Element**</span></span>|<span data-ttu-id="c9488-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9488-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9488-113">PostalAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="c9488-113">PostalAddressAttributedValue</span></span>](postaladdressattributedvalue.md) <br/> |<span data-ttu-id="c9488-114">Especifica una instancia de una matriz de direcciones postales y sus atribuciones asociadas.</span><span class="sxs-lookup"><span data-stu-id="c9488-114">Specifies an instance of an array of postal addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c9488-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c9488-115">Parent elements</span></span>

|<span data-ttu-id="c9488-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c9488-116">**Element**</span></span>|<span data-ttu-id="c9488-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9488-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9488-118">Rol</span><span class="sxs-lookup"><span data-stu-id="c9488-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="c9488-119">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="c9488-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9488-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9488-120">Remarks</span></span>

<span data-ttu-id="c9488-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c9488-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c9488-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c9488-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c9488-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c9488-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9488-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9488-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c9488-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c9488-125">Schema Name</span></span>  <br/> |<span data-ttu-id="c9488-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="c9488-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="c9488-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c9488-127">Validation File</span></span>  <br/> |<span data-ttu-id="c9488-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c9488-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c9488-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c9488-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c9488-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9488-130">See also</span></span>



- [<span data-ttu-id="c9488-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c9488-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

