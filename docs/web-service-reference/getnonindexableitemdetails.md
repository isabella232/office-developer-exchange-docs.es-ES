---
title: GetNonIndexableItemDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3994c1-3bb4-4571-b026-34a6c5705410
description: El elemento GetNonIndexableItemDetails especifica una solicitud para recuperar detalles de elemento de nonindexable.
ms.openlocfilehash: 0aeda85973aa78eff240a017db58ffb57fc0de06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764908"
---
# <a name="getnonindexableitemdetails"></a><span data-ttu-id="512e7-103">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="512e7-103">GetNonIndexableItemDetails</span></span>

<span data-ttu-id="512e7-104">El elemento **GetNonIndexableItemDetails** especifica una solicitud para recuperar detalles de elemento de nonindexable.</span><span class="sxs-lookup"><span data-stu-id="512e7-104">The **GetNonIndexableItemDetails** element specifies a request to retrieve nonindexable item details.</span></span> 
  
```XML
<GetNonIndexableItemDetails>
    <Mailboxes/>
    <PageSize/>
    <PageItemReference/>
    <PageDirection/>
</GetNonIndexableItemDetails>
```

 <span data-ttu-id="512e7-105">**GetNonIndexableItemDetailsType**</span><span class="sxs-lookup"><span data-stu-id="512e7-105">**GetNonIndexableItemDetailsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="512e7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="512e7-106">Attributes and elements</span></span>

<span data-ttu-id="512e7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="512e7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="512e7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="512e7-108">Attributes</span></span>

<span data-ttu-id="512e7-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="512e7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="512e7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="512e7-110">Child elements</span></span>

|<span data-ttu-id="512e7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="512e7-111">**Element**</span></span>|<span data-ttu-id="512e7-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="512e7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="512e7-113">Buzones de correo (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="512e7-113">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md) <br/> |<span data-ttu-id="512e7-114">Especifica una matriz de elementos de **buzón de correo** .</span><span class="sxs-lookup"><span data-stu-id="512e7-114">Specifies an array of **Mailbox** elements.</span></span>  <br/> |
|[<span data-ttu-id="512e7-115">PageSize</span><span class="sxs-lookup"><span data-stu-id="512e7-115">PageSize</span></span>](pagesize.md) <br/> |<span data-ttu-id="512e7-116">Contiene el número de elementos que se devuelven en una sola página para un resultado de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="512e7-116">Contains the number of items to be returned in a single page for a search result.</span></span>  <br/> |
|[<span data-ttu-id="512e7-117">PageItemReference</span><span class="sxs-lookup"><span data-stu-id="512e7-117">PageItemReference</span></span>](pageitemreference.md) <br/> |<span data-ttu-id="512e7-118">Especifica la referencia de un elemento de página.</span><span class="sxs-lookup"><span data-stu-id="512e7-118">Specifies the reference for a page item.</span></span>  <br/> |
|[<span data-ttu-id="512e7-119">PageDirection</span><span class="sxs-lookup"><span data-stu-id="512e7-119">PageDirection</span></span>](pagedirection.md) <br/> |<span data-ttu-id="512e7-120">Contiene la dirección para la paginación en el resultado de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="512e7-120">Contains the direction for pagination in the search result.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="512e7-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="512e7-121">Parent elements</span></span>

<span data-ttu-id="512e7-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="512e7-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="512e7-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="512e7-123">Remarks</span></span>

<span data-ttu-id="512e7-124">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="512e7-124">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="512e7-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="512e7-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="512e7-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="512e7-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="512e7-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="512e7-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="512e7-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="512e7-128">Schema Name</span></span>  <br/> |<span data-ttu-id="512e7-129">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="512e7-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="512e7-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="512e7-130">Validation File</span></span>  <br/> |<span data-ttu-id="512e7-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="512e7-131">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="512e7-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="512e7-132">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="512e7-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="512e7-133">See also</span></span>



- [<span data-ttu-id="512e7-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="512e7-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

