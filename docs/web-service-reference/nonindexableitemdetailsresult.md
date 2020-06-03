---
title: NonIndexableItemDetailsResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7cbdbc21-5405-4cbc-8ca0-d7b0257927aa
description: El elemento NonIndexableItemDetailsResult especifica los resultados de la operación WSDL de GetNonIndexableItemDetails.
ms.openlocfilehash: 647f58b5e7285af70bbfb3a203ba71c9a3ccebcc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465446"
---
# <a name="nonindexableitemdetailsresult"></a><span data-ttu-id="d05e6-103">NonIndexableItemDetailsResult</span><span class="sxs-lookup"><span data-stu-id="d05e6-103">NonIndexableItemDetailsResult</span></span>

<span data-ttu-id="d05e6-104">El elemento **NonIndexableItemDetailsResult** especifica los resultados de la operación WSDL de **GetNonIndexableItemDetails** .</span><span class="sxs-lookup"><span data-stu-id="d05e6-104">The **NonIndexableItemDetailsResult** element specifies the results of the **GetNonIndexableItemDetails** WSDL operation.</span></span> 
  
```XML
<NonIndexableItemDetailsResult>
   <Items/>
   <FailedMailboxes/>
</NonIndexableItemDetailsResult>
```

 <span data-ttu-id="d05e6-105">**NonIndexableItemDetailResultType**</span><span class="sxs-lookup"><span data-stu-id="d05e6-105">**NonIndexableItemDetailResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d05e6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d05e6-106">Attributes and elements</span></span>

<span data-ttu-id="d05e6-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d05e6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d05e6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d05e6-108">Attributes</span></span>

<span data-ttu-id="d05e6-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d05e6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d05e6-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d05e6-110">Child elements</span></span>

<span data-ttu-id="d05e6-111">[Items (ArrayOfNonIndexableItemDetailsType)](items-arrayofnonindexableitemdetailstype.md) , [FailedMailboxes](failedmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="d05e6-111">[Items (ArrayOfNonIndexableItemDetailsType)](items-arrayofnonindexableitemdetailstype.md) , [FailedMailboxes](failedmailboxes.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d05e6-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d05e6-112">Parent elements</span></span>

<span data-ttu-id="d05e6-113">[GetNonIndexableItemDetailsResponse](getnonindexableitemdetailsresponse.md) , [GetNonIndexableItemDetailsResponseMessage](getnonindexableitemdetailsresponsemessage.md)</span><span class="sxs-lookup"><span data-stu-id="d05e6-113">[GetNonIndexableItemDetailsResponse](getnonindexableitemdetailsresponse.md) , [GetNonIndexableItemDetailsResponseMessage](getnonindexableitemdetailsresponsemessage.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d05e6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d05e6-114">Remarks</span></span>

<span data-ttu-id="d05e6-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d05e6-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d05e6-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d05e6-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d05e6-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d05e6-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d05e6-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="d05e6-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d05e6-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d05e6-119">Schema name</span></span>  <br/> |<span data-ttu-id="d05e6-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="d05e6-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d05e6-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d05e6-121">Validation file</span></span>  <br/> |<span data-ttu-id="d05e6-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d05e6-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d05e6-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d05e6-123">Can be empty</span></span>  <br/> |<span data-ttu-id="d05e6-124">Falso</span><span class="sxs-lookup"><span data-stu-id="d05e6-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d05e6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d05e6-125">See also</span></span>



[<span data-ttu-id="d05e6-126">Operación GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="d05e6-126">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)


- [<span data-ttu-id="d05e6-127">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d05e6-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

