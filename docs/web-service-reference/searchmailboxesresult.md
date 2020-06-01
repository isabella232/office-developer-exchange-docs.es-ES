---
title: SearchMailboxesResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ddb276c4-6c8a-46ef-a2eb-46b6a0bfce09
description: El elemento SearchMailboxesResult contiene el resultado de la solicitud SearchMailboxes.
ms.openlocfilehash: 79d593d99762aedc6290578b5458f9ac3cad3d26
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466706"
---
# <a name="searchmailboxesresult"></a><span data-ttu-id="b0c52-103">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="b0c52-103">SearchMailboxesResult</span></span>

<span data-ttu-id="b0c52-104">El elemento **SearchMailboxesResult** contiene el resultado de la solicitud **SearchMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="b0c52-104">The **SearchMailboxesResult** element contains the result of the **SearchMailboxes** request.</span></span> 
  
```XML
<SearchMailboxesResult>
   <SearchQueries/>
   <ResultType/>
   <ItemCount/>
   <Size/>
   <PageItemCount/>
   <PageItemSize/>
   <KeywordStats/>
   <Items/>
   <FailedMailboxes/>
   <Refiners/>
   <MailboxStats/>
</SearchMailboxesResult>
```

 <span data-ttu-id="b0c52-105">**SearchMailboxesResultType**</span><span class="sxs-lookup"><span data-stu-id="b0c52-105">**SearchMailboxesResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b0c52-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b0c52-106">Attributes and elements</span></span>

<span data-ttu-id="b0c52-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b0c52-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0c52-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b0c52-108">Attributes</span></span>

<span data-ttu-id="b0c52-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b0c52-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b0c52-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b0c52-110">Child elements</span></span>

<span data-ttu-id="b0c52-111">[SearchQueries](searchqueries.md)  |  [ResultType](resulttype.md)  |  [ItemCount](itemcount.md)  |  [Tamaño (largo)](size-long.md)  |  [PageItemCount](pageitemcount.md)  |  [PageItemSize](pageitemsize.md)  |  [KeywordStats](keywordstats.md)  |  [Elementos (ArrayOfSearchPreviewItemsType)](items-arrayofsearchpreviewitemstype.md)  |  [FailedMailboxes](failedmailboxes.md)  |  [Refinadores](refiners.md)  |  [MailboxStats](mailboxstats.md)</span><span class="sxs-lookup"><span data-stu-id="b0c52-111">[SearchQueries](searchqueries.md) | [ResultType](resulttype.md) | [ItemCount](itemcount.md) | [Size (long)](size-long.md) | [PageItemCount](pageitemcount.md) | [PageItemSize](pageitemsize.md) | [KeywordStats](keywordstats.md) | [Items (ArrayOfSearchPreviewItemsType)](items-arrayofsearchpreviewitemstype.md) | [FailedMailboxes](failedmailboxes.md) | [Refiners](refiners.md) | [MailboxStats](mailboxstats.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b0c52-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b0c52-112">Parent elements</span></span>

[<span data-ttu-id="b0c52-113">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b0c52-113">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
  
## <a name="remarks"></a><span data-ttu-id="b0c52-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0c52-114">Remarks</span></span>

<span data-ttu-id="b0c52-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b0c52-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b0c52-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b0c52-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b0c52-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b0c52-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0c52-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0c52-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b0c52-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b0c52-119">Schema name</span></span>  <br/> |<span data-ttu-id="b0c52-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b0c52-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b0c52-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b0c52-121">Validation file</span></span>  <br/> |<span data-ttu-id="b0c52-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b0c52-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b0c52-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b0c52-123">Can be empty</span></span>  <br/> |<span data-ttu-id="b0c52-124">false</span><span class="sxs-lookup"><span data-stu-id="b0c52-124">false</span></span>  <br/> |
   

