---
title: SortBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3dc4ab23-26b0-42b3-8930-f1c7eefecdeb
description: El elemento SortBy contiene una propiedad de elemento que se utiliza para ordenar los resultados de búsqueda.
ms.openlocfilehash: 357958e393ba9331d23ee48661f21e2afe00cf01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837518"
---
# <a name="sortby"></a><span data-ttu-id="c9baa-103">SortBy</span><span class="sxs-lookup"><span data-stu-id="c9baa-103">SortBy</span></span>

<span data-ttu-id="c9baa-104">El elemento **SortBy** contiene una propiedad de elemento que se utiliza para ordenar los resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c9baa-104">The **SortBy** element contains an item property used for sorting the search result.</span></span> 
  
```XML
<SortBy Order="">
   <FieldURI/>
   <IndexedFieldURI/>
</SortBy>
```

 <span data-ttu-id="c9baa-105">**FieldOrderType**</span><span class="sxs-lookup"><span data-stu-id="c9baa-105">**FieldOrderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c9baa-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c9baa-106">Attributes and elements</span></span>

<span data-ttu-id="c9baa-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c9baa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c9baa-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c9baa-108">Attributes</span></span>

|<span data-ttu-id="c9baa-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c9baa-109">**Attribute**</span></span>|<span data-ttu-id="c9baa-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9baa-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c9baa-111">Order</span><span class="sxs-lookup"><span data-stu-id="c9baa-111">Order</span></span>  <br/> |<span data-ttu-id="c9baa-112">El valor de texto del atributo **orden** es el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="c9baa-112">The text value of the **Order** attribute is the sort order.</span></span> <span data-ttu-id="c9baa-113">Un valor de texto de **ascendente** indica que los resultados están en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="c9baa-113">A text value of **Ascending** indicates that the results are in ascending order.</span></span> <span data-ttu-id="c9baa-114">Un valor de texto de **descendente** indica que los resultados están en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="c9baa-114">A text value of **Descending** indicates that the results are in descending order.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c9baa-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c9baa-115">Child elements</span></span>

<span data-ttu-id="c9baa-116">[FieldURI](fielduri.md) | [IndexedFieldURI](indexedfielduri.md)</span><span class="sxs-lookup"><span data-stu-id="c9baa-116">[FieldURI](fielduri.md) | [IndexedFieldURI](indexedfielduri.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c9baa-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c9baa-117">Parent elements</span></span>

[<span data-ttu-id="c9baa-118">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="c9baa-118">SearchMailboxes</span></span>](searchmailboxes.md)
  
## <a name="remarks"></a><span data-ttu-id="c9baa-119">Notas</span><span class="sxs-lookup"><span data-stu-id="c9baa-119">Remarks</span></span>

<span data-ttu-id="c9baa-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c9baa-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c9baa-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c9baa-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c9baa-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c9baa-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9baa-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c9baa-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c9baa-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c9baa-124">Schema name</span></span>  <br/> |<span data-ttu-id="c9baa-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c9baa-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c9baa-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c9baa-126">Validation file</span></span>  <br/> |<span data-ttu-id="c9baa-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c9baa-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c9baa-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c9baa-128">Can be empty</span></span>  <br/> ||
   

