---
title: GetNonIndexableItemDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3994c1-3bb4-4571-b026-34a6c5705410
description: El elemento GetNonIndexableItemDetails especifica una solicitud para recuperar los detalles de elementos no indizables.
ms.openlocfilehash: 1c04b4cd7a86183210be869973c9779188fa0adf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458603"
---
# <a name="getnonindexableitemdetails"></a><span data-ttu-id="f242a-103">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="f242a-103">GetNonIndexableItemDetails</span></span>

<span data-ttu-id="f242a-104">El elemento **GetNonIndexableItemDetails** especifica una solicitud para recuperar los detalles de elementos no indizables.</span><span class="sxs-lookup"><span data-stu-id="f242a-104">The **GetNonIndexableItemDetails** element specifies a request to retrieve nonindexable item details.</span></span> 
  
```XML
<GetNonIndexableItemDetails>
    <Mailboxes/>
    <PageSize/>
    <PageItemReference/>
    <PageDirection/>
</GetNonIndexableItemDetails>
```

 <span data-ttu-id="f242a-105">**GetNonIndexableItemDetailsType**</span><span class="sxs-lookup"><span data-stu-id="f242a-105">**GetNonIndexableItemDetailsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f242a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f242a-106">Attributes and elements</span></span>

<span data-ttu-id="f242a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f242a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f242a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f242a-108">Attributes</span></span>

<span data-ttu-id="f242a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f242a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f242a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f242a-110">Child elements</span></span>

|<span data-ttu-id="f242a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f242a-111">**Element**</span></span>|<span data-ttu-id="f242a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f242a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f242a-113">Buzones de correo (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="f242a-113">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md) <br/> |<span data-ttu-id="f242a-114">Especifica una matriz de elementos **Mailbox** .</span><span class="sxs-lookup"><span data-stu-id="f242a-114">Specifies an array of **Mailbox** elements.</span></span>  <br/> |
|[<span data-ttu-id="f242a-115">PageSize</span><span class="sxs-lookup"><span data-stu-id="f242a-115">PageSize</span></span>](pagesize.md) <br/> |<span data-ttu-id="f242a-116">Contiene el número de elementos que se van a devolver en una sola página para un resultado de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f242a-116">Contains the number of items to be returned in a single page for a search result.</span></span>  <br/> |
|[<span data-ttu-id="f242a-117">PageItemReference</span><span class="sxs-lookup"><span data-stu-id="f242a-117">PageItemReference</span></span>](pageitemreference.md) <br/> |<span data-ttu-id="f242a-118">Especifica la referencia para un elemento de página.</span><span class="sxs-lookup"><span data-stu-id="f242a-118">Specifies the reference for a page item.</span></span>  <br/> |
|[<span data-ttu-id="f242a-119">PageDirection</span><span class="sxs-lookup"><span data-stu-id="f242a-119">PageDirection</span></span>](pagedirection.md) <br/> |<span data-ttu-id="f242a-120">Contiene la dirección de paginación en el resultado de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f242a-120">Contains the direction for pagination in the search result.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f242a-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f242a-121">Parent elements</span></span>

<span data-ttu-id="f242a-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f242a-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f242a-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f242a-123">Remarks</span></span>

<span data-ttu-id="f242a-124">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f242a-124">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f242a-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f242a-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f242a-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f242a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f242a-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="f242a-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f242a-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f242a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="f242a-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f242a-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="f242a-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f242a-130">Validation File</span></span>  <br/> |<span data-ttu-id="f242a-131">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f242a-131">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f242a-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f242a-132">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f242a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f242a-133">See also</span></span>



- [<span data-ttu-id="f242a-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f242a-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

