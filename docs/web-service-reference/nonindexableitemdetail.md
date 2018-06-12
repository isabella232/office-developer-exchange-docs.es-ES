---
title: NonIndexableItemDetail
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a26d4c02-f1bd-40c4-9257-5db45e839f17
description: El elemento NonIndexableItemDetail especifica la información de todos los detalles acerca de un elemento que no se pueden indizar.
ms.openlocfilehash: ef1bd072a44b42b501a3016c394b89fe6ab25bf0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836543"
---
# <a name="nonindexableitemdetail"></a><span data-ttu-id="54170-103">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="54170-103">NonIndexableItemDetail</span></span>

<span data-ttu-id="54170-104">El elemento **NonIndexableItemDetail** especifica la información de todos los detalles acerca de un elemento que no se pueden indizar.</span><span class="sxs-lookup"><span data-stu-id="54170-104">The **NonIndexableItemDetail** element specifies detail information about an item that cannot be indexed.</span></span> 
  
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

 <span data-ttu-id="54170-105">**NonIndexableItemDetailType**</span><span class="sxs-lookup"><span data-stu-id="54170-105">**NonIndexableItemDetailType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="54170-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="54170-106">Attributes and elements</span></span>

<span data-ttu-id="54170-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="54170-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54170-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="54170-108">Attributes</span></span>

<span data-ttu-id="54170-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="54170-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="54170-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="54170-110">Child elements</span></span>

<span data-ttu-id="54170-111">[ItemId](itemid.md) | [ErrorCode (ItemIndexErrorType)](errorcode-itemindexerrortype.md) | [ErrorDescription](errordescription.md) | [IsPartiallyIndexed](ispartiallyindexed.md) | [IsPermanentFailure](ispermanentfailure.md) | [SortValue](sortvalue.md) | [AttemptCount ](attemptcount.md)  |  [LastAttemptTime](lastattempttime.md) | [AdditionalInfo](additionalinfo.md)</span><span class="sxs-lookup"><span data-stu-id="54170-111">[ItemId](itemid.md) | [ErrorCode (ItemIndexErrorType)](errorcode-itemindexerrortype.md) | [ErrorDescription](errordescription.md) | [IsPartiallyIndexed](ispartiallyindexed.md) | [IsPermanentFailure](ispermanentfailure.md) | [SortValue](sortvalue.md) | [AttemptCount](attemptcount.md) | [LastAttemptTime](lastattempttime.md) | [AdditionalInfo](additionalinfo.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="54170-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="54170-112">Parent elements</span></span>

[<span data-ttu-id="54170-113">Elementos (ArrayOfNonIndexableItemDetailsType)</span><span class="sxs-lookup"><span data-stu-id="54170-113">Items (ArrayOfNonIndexableItemDetailsType)</span></span>](items-arrayofnonindexableitemdetailstype.md)
  
## <a name="remarks"></a><span data-ttu-id="54170-114">Notas</span><span class="sxs-lookup"><span data-stu-id="54170-114">Remarks</span></span>

<span data-ttu-id="54170-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="54170-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="54170-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="54170-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54170-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="54170-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54170-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="54170-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="54170-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="54170-119">Schema name</span></span>  <br/> |<span data-ttu-id="54170-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="54170-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="54170-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="54170-121">Validation file</span></span>  <br/> |<span data-ttu-id="54170-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="54170-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="54170-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="54170-123">Can be empty</span></span>  <br/> ||
   

