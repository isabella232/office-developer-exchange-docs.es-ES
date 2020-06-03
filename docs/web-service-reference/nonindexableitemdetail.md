---
title: NonIndexableItemDetail
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a26d4c02-f1bd-40c4-9257-5db45e839f17
description: El elemento NonIndexableItemDetail especifica información detallada sobre un elemento que no se puede indizar.
ms.openlocfilehash: 4fc4324501570402d22aa303d6af2a60b50b3cc6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466741"
---
# <a name="nonindexableitemdetail"></a><span data-ttu-id="b5fa5-103">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="b5fa5-103">NonIndexableItemDetail</span></span>

<span data-ttu-id="b5fa5-104">El elemento **NonIndexableItemDetail** especifica información detallada sobre un elemento que no se puede indizar.</span><span class="sxs-lookup"><span data-stu-id="b5fa5-104">The **NonIndexableItemDetail** element specifies detail information about an item that cannot be indexed.</span></span> 
  
```XML
<NonIndexableItemDetail>
   <ItemId/>
   <ErrorCode/>
   <ErrorDescription/>
   <IsPartiallyIndexed/>
   <IsPermanentFailure/>
   <SortValue/>
   <AttemptCount/>
   <LastAttemptTime/>
   <AdditionalInfo/>
</NonIndexableItemDetail>
```

 <span data-ttu-id="b5fa5-105">**NonIndexableItemDetailType**</span><span class="sxs-lookup"><span data-stu-id="b5fa5-105">**NonIndexableItemDetailType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b5fa5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b5fa5-106">Attributes and elements</span></span>

<span data-ttu-id="b5fa5-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b5fa5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5fa5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b5fa5-108">Attributes</span></span>

<span data-ttu-id="b5fa5-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b5fa5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b5fa5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b5fa5-110">Child elements</span></span>

<span data-ttu-id="b5fa5-111">[Itemid](itemid.md)  |  [ErrorCode (ItemIndexErrorType)](errorcode-itemindexerrortype.md)  |  [ErrorDescription](errordescription.md)  |  [IsPartiallyIndexed](ispartiallyindexed.md)  |  [IsPermanentFailure](ispermanentfailure.md)  |  [SortValue](sortvalue.md)  |  [AttemptCount](attemptcount.md)  |  [LastAttemptTime](lastattempttime.md)  |  [AdditionalInfo](additionalinfo.md)</span><span class="sxs-lookup"><span data-stu-id="b5fa5-111">[ItemId](itemid.md) | [ErrorCode (ItemIndexErrorType)](errorcode-itemindexerrortype.md) | [ErrorDescription](errordescription.md) | [IsPartiallyIndexed](ispartiallyindexed.md) | [IsPermanentFailure](ispermanentfailure.md) | [SortValue](sortvalue.md) | [AttemptCount](attemptcount.md) | [LastAttemptTime](lastattempttime.md) | [AdditionalInfo](additionalinfo.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b5fa5-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b5fa5-112">Parent elements</span></span>

[<span data-ttu-id="b5fa5-113">Elementos (ArrayOfNonIndexableItemDetailsType)</span><span class="sxs-lookup"><span data-stu-id="b5fa5-113">Items (ArrayOfNonIndexableItemDetailsType)</span></span>](items-arrayofnonindexableitemdetailstype.md)
  
## <a name="remarks"></a><span data-ttu-id="b5fa5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b5fa5-114">Remarks</span></span>

<span data-ttu-id="b5fa5-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b5fa5-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b5fa5-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b5fa5-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5fa5-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b5fa5-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5fa5-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5fa5-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b5fa5-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b5fa5-119">Schema name</span></span>  <br/> |<span data-ttu-id="b5fa5-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b5fa5-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="b5fa5-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b5fa5-121">Validation file</span></span>  <br/> |<span data-ttu-id="b5fa5-122">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b5fa5-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b5fa5-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b5fa5-123">Can be empty</span></span>  <br/> ||
   

