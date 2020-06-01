---
title: SearchMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d8c367a-67e9-43b3-8be0-6362d2152431
description: El elemento SearchMailboxes indica el principio de la solicitud SearchMailboxes.
ms.openlocfilehash: 7ccc94157ef6bde7b6ba86e70c16ef6e90d712fa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456804"
---
# <a name="searchmailboxes"></a><span data-ttu-id="6e7b0-103">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="6e7b0-103">SearchMailboxes</span></span>

<span data-ttu-id="6e7b0-104">El elemento **SearchMailboxes** indica el principio de la solicitud **SearchMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="6e7b0-104">The **SearchMailboxes** element indicates the beginning of the **SearchMailboxes** request.</span></span> 
  
```XML
<SearchMailboxes>
   <SearchQueries/>
   <ResultType/>
   <PreviewItemResponseShape/>
   <SortBy/>
   <Language/>
   <Deduplication/>
   <PageSize/>
   <PageItemReference/>
   <PageDirection/>
</SearchMailboxes>
```

 <span data-ttu-id="6e7b0-105">**SearchMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="6e7b0-105">**SearchMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6e7b0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6e7b0-106">Attributes and elements</span></span>

<span data-ttu-id="6e7b0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6e7b0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e7b0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6e7b0-108">Attributes</span></span>

<span data-ttu-id="6e7b0-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6e7b0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6e7b0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6e7b0-110">Child elements</span></span>

<span data-ttu-id="6e7b0-111">[SearchQueries](searchqueries.md)  |  [ResultType](resulttype.md)  |  [PreviewItemResponseShape](previewitemresponseshape.md)  |  [SortBy](sortby.md)  |  [Idioma](language.md)  |  [Desduplicación](deduplication.md)  |  [PageSize](pagesize.md)  |  [PageItemReference](pageitemreference.md)  |  [PageDirection](pagedirection.md)</span><span class="sxs-lookup"><span data-stu-id="6e7b0-111">[SearchQueries](searchqueries.md) | [ResultType](resulttype.md) | [PreviewItemResponseShape](previewitemresponseshape.md) | [SortBy](sortby.md) | [Language](language.md) | [Deduplication](deduplication.md) | [PageSize](pagesize.md) | [PageItemReference](pageitemreference.md) | [PageDirection](pagedirection.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6e7b0-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6e7b0-112">Parent elements</span></span>

<span data-ttu-id="6e7b0-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6e7b0-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6e7b0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6e7b0-114">Remarks</span></span>

<span data-ttu-id="6e7b0-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6e7b0-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6e7b0-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6e7b0-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6e7b0-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6e7b0-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e7b0-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e7b0-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6e7b0-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6e7b0-119">Schema name</span></span>  <br/> |<span data-ttu-id="6e7b0-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6e7b0-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6e7b0-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6e7b0-121">Validation file</span></span>  <br/> |<span data-ttu-id="6e7b0-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6e7b0-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6e7b0-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6e7b0-123">Can be empty</span></span>  <br/> |<span data-ttu-id="6e7b0-124">false</span><span class="sxs-lookup"><span data-stu-id="6e7b0-124">false</span></span>  <br/> |
   

