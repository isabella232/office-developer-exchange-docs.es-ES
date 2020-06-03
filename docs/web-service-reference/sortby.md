---
title: SortBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3dc4ab23-26b0-42b3-8930-f1c7eefecdeb
description: El elemento SortBy contiene una propiedad de elemento usada para ordenar los resultados de búsqueda.
ms.openlocfilehash: cf2b1e633bc66e526028078833afade363e4c5e0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468400"
---
# <a name="sortby"></a><span data-ttu-id="ba23d-103">SortBy</span><span class="sxs-lookup"><span data-stu-id="ba23d-103">SortBy</span></span>

<span data-ttu-id="ba23d-104">El elemento **sortBy** contiene una propiedad de elemento usada para ordenar los resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ba23d-104">The **SortBy** element contains an item property used for sorting the search result.</span></span> 
  
```XML
<SortBy Order="">
   <FieldURI/>
   <IndexedFieldURI/>
</SortBy>
```

 <span data-ttu-id="ba23d-105">**FieldOrderType**</span><span class="sxs-lookup"><span data-stu-id="ba23d-105">**FieldOrderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba23d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ba23d-106">Attributes and elements</span></span>

<span data-ttu-id="ba23d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ba23d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba23d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ba23d-108">Attributes</span></span>

|<span data-ttu-id="ba23d-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ba23d-109">**Attribute**</span></span>|<span data-ttu-id="ba23d-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba23d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ba23d-111">Order</span><span class="sxs-lookup"><span data-stu-id="ba23d-111">Order</span></span>  <br/> |<span data-ttu-id="ba23d-112">El valor de texto del atributo **Order** es el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="ba23d-112">The text value of the **Order** attribute is the sort order.</span></span> <span data-ttu-id="ba23d-113">Un valor de texto **ascendente** indica que los resultados están en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="ba23d-113">A text value of **Ascending** indicates that the results are in ascending order.</span></span> <span data-ttu-id="ba23d-114">Un valor de texto **descendente** indica que los resultados están en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="ba23d-114">A text value of **Descending** indicates that the results are in descending order.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ba23d-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ba23d-115">Child elements</span></span>

<span data-ttu-id="ba23d-116">[FieldURI](fielduri.md)  |  [IndexedFieldURI](indexedfielduri.md)</span><span class="sxs-lookup"><span data-stu-id="ba23d-116">[FieldURI](fielduri.md) | [IndexedFieldURI](indexedfielduri.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ba23d-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ba23d-117">Parent elements</span></span>

[<span data-ttu-id="ba23d-118">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="ba23d-118">SearchMailboxes</span></span>](searchmailboxes.md)
  
## <a name="remarks"></a><span data-ttu-id="ba23d-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ba23d-119">Remarks</span></span>

<span data-ttu-id="ba23d-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ba23d-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ba23d-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ba23d-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba23d-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ba23d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba23d-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba23d-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ba23d-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ba23d-124">Schema name</span></span>  <br/> |<span data-ttu-id="ba23d-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ba23d-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ba23d-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ba23d-126">Validation file</span></span>  <br/> |<span data-ttu-id="ba23d-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ba23d-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ba23d-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ba23d-128">Can be empty</span></span>  <br/> ||
   

