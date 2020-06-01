---
title: BusinessHomePages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9961c0c2-7cac-4af1-84ac-0eafdce0a6ab
description: El elemento BusinessHomePages especifica una matriz de páginas principales de negocio y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: f0e85e0b3c857e44d94bd42c6d3ea757d015eb25
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465915"
---
# <a name="businesshomepages"></a><span data-ttu-id="ae6cc-103">BusinessHomePages</span><span class="sxs-lookup"><span data-stu-id="ae6cc-103">BusinessHomePages</span></span>

<span data-ttu-id="ae6cc-104">El elemento **BusinessHomePages** especifica una matriz de páginas principales de negocio y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="ae6cc-104">The **BusinessHomePages** element specifies an array of business home pages and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<BusinessHomePages>
    <StringAttributedValue></StringAttributedValue>
</BusinessHomePages>
```

 <span data-ttu-id="ae6cc-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="ae6cc-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae6cc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ae6cc-106">Attributes and elements</span></span>

<span data-ttu-id="ae6cc-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ae6cc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae6cc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ae6cc-108">Attributes</span></span>

<span data-ttu-id="ae6cc-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ae6cc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae6cc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ae6cc-110">Child elements</span></span>

|<span data-ttu-id="ae6cc-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ae6cc-111">**Element**</span></span>|<span data-ttu-id="ae6cc-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae6cc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae6cc-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="ae6cc-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="ae6cc-114">Especifica una instancia de una matriz de atributos asociada a un elemento de rol.</span><span class="sxs-lookup"><span data-stu-id="ae6cc-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ae6cc-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ae6cc-115">Parent elements</span></span>

|<span data-ttu-id="ae6cc-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ae6cc-116">**Element**</span></span>|<span data-ttu-id="ae6cc-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae6cc-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae6cc-118">Rol</span><span class="sxs-lookup"><span data-stu-id="ae6cc-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="ae6cc-119">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="ae6cc-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae6cc-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae6cc-120">Remarks</span></span>

<span data-ttu-id="ae6cc-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ae6cc-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ae6cc-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ae6cc-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae6cc-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ae6cc-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae6cc-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae6cc-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ae6cc-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ae6cc-125">Schema Name</span></span>  <br/> |<span data-ttu-id="ae6cc-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="ae6cc-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="ae6cc-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ae6cc-127">Validation File</span></span>  <br/> |<span data-ttu-id="ae6cc-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ae6cc-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="ae6cc-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ae6cc-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ae6cc-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae6cc-130">See also</span></span>



- [<span data-ttu-id="ae6cc-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ae6cc-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

