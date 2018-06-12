---
title: SearchMailboxesResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ddb276c4-6c8a-46ef-a2eb-46b6a0bfce09
description: El elemento SearchMailboxesResult contiene el resultado de la solicitud de SearchMailboxes.
ms.openlocfilehash: 93e5837216ef8942b77ac2a91f5ef5f0ad001756
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837300"
---
# <a name="searchmailboxesresult"></a><span data-ttu-id="440cf-103">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="440cf-103">SearchMailboxesResult</span></span>

<span data-ttu-id="440cf-104">El elemento **SearchMailboxesResult** contiene el resultado de la solicitud de **SearchMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="440cf-104">The **SearchMailboxesResult** element contains the result of the **SearchMailboxes** request.</span></span> 
  
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

 <span data-ttu-id="440cf-105">**SearchMailboxesResultType**</span><span class="sxs-lookup"><span data-stu-id="440cf-105">**SearchMailboxesResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="440cf-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="440cf-106">Attributes and elements</span></span>

<span data-ttu-id="440cf-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="440cf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="440cf-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="440cf-108">Attributes</span></span>

<span data-ttu-id="440cf-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="440cf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="440cf-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="440cf-110">Child elements</span></span>

<span data-ttu-id="440cf-111">[SearchQueries](searchqueries.md) | [ResultType](resulttype.md) | [ItemCount](itemcount.md) | [tamaño (long)](size-long.md) | [PageItemCount](pageitemcount.md) | [PageItemSize](pageitemsize.md) | [KeywordStats](keywordstats.md) | [los elementos () ArrayOfSearchPreviewItemsType)](items-arrayofsearchpreviewitemstype.md) | [FailedMailboxes](failedmailboxes.md) | [refinadores](refiners.md) | [MailboxStats](mailboxstats.md)</span><span class="sxs-lookup"><span data-stu-id="440cf-111">[SearchQueries](searchqueries.md) | [ResultType](resulttype.md) | [ItemCount](itemcount.md) | [Size (long)](size-long.md) | [PageItemCount](pageitemcount.md) | [PageItemSize](pageitemsize.md) | [KeywordStats](keywordstats.md) | [Items (ArrayOfSearchPreviewItemsType)](items-arrayofsearchpreviewitemstype.md) | [FailedMailboxes](failedmailboxes.md) | [Refiners](refiners.md) | [MailboxStats](mailboxstats.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="440cf-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="440cf-112">Parent elements</span></span>

[<span data-ttu-id="440cf-113">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="440cf-113">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
  
## <a name="remarks"></a><span data-ttu-id="440cf-114">Notas</span><span class="sxs-lookup"><span data-stu-id="440cf-114">Remarks</span></span>

<span data-ttu-id="440cf-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="440cf-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="440cf-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="440cf-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="440cf-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="440cf-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="440cf-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="440cf-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="440cf-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="440cf-119">Schema name</span></span>  <br/> |<span data-ttu-id="440cf-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="440cf-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="440cf-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="440cf-121">Validation file</span></span>  <br/> |<span data-ttu-id="440cf-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="440cf-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="440cf-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="440cf-123">Can be empty</span></span>  <br/> |<span data-ttu-id="440cf-124">falso</span><span class="sxs-lookup"><span data-stu-id="440cf-124">false</span></span>  <br/> |
   

