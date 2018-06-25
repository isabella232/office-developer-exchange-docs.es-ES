---
title: NonIndexableItemDetailsResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7cbdbc21-5405-4cbc-8ca0-d7b0257927aa
description: El elemento NonIndexableItemDetailsResult especifica los resultados de la operación WSDL GetNonIndexableItemDetails.
ms.openlocfilehash: 6e271f2cf0e37f26b945332c94167b6a42354115
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836535"
---
# <a name="nonindexableitemdetailsresult"></a><span data-ttu-id="cb6dd-103">NonIndexableItemDetailsResult</span><span class="sxs-lookup"><span data-stu-id="cb6dd-103">NonIndexableItemDetailsResult</span></span>

<span data-ttu-id="cb6dd-104">El elemento **NonIndexableItemDetailsResult** especifica los resultados de la operación de WSDL **GetNonIndexableItemDetails** .</span><span class="sxs-lookup"><span data-stu-id="cb6dd-104">The **NonIndexableItemDetailsResult** element specifies the results of the **GetNonIndexableItemDetails** WSDL operation.</span></span> 
  
```XML
<NonIndexableItemDetailsResult>
   <Items/>
   <FailedMailboxes/>
</NonIndexableItemDetailsResult>
```

 <span data-ttu-id="cb6dd-105">**NonIndexableItemDetailResultType**</span><span class="sxs-lookup"><span data-stu-id="cb6dd-105">**NonIndexableItemDetailResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cb6dd-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cb6dd-106">Attributes and elements</span></span>

<span data-ttu-id="cb6dd-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cb6dd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb6dd-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cb6dd-108">Attributes</span></span>

<span data-ttu-id="cb6dd-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cb6dd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cb6dd-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cb6dd-110">Child elements</span></span>

<span data-ttu-id="cb6dd-111">[Elementos (ArrayOfNonIndexableItemDetailsType)](items-arrayofnonindexableitemdetailstype.md) , [FailedMailboxes](failedmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="cb6dd-111">[Items (ArrayOfNonIndexableItemDetailsType)](items-arrayofnonindexableitemdetailstype.md) , [FailedMailboxes](failedmailboxes.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cb6dd-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cb6dd-112">Parent elements</span></span>

<span data-ttu-id="cb6dd-113">[GetNonIndexableItemDetailsResponse](getnonindexableitemdetailsresponse.md) , [GetNonIndexableItemDetailsResponseMessage](getnonindexableitemdetailsresponsemessage.md)</span><span class="sxs-lookup"><span data-stu-id="cb6dd-113">[GetNonIndexableItemDetailsResponse](getnonindexableitemdetailsresponse.md) , [GetNonIndexableItemDetailsResponseMessage](getnonindexableitemdetailsresponsemessage.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb6dd-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb6dd-114">Remarks</span></span>

<span data-ttu-id="cb6dd-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cb6dd-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="cb6dd-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="cb6dd-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb6dd-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cb6dd-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb6dd-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cb6dd-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cb6dd-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cb6dd-119">Schema name</span></span>  <br/> |<span data-ttu-id="cb6dd-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="cb6dd-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cb6dd-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cb6dd-121">Validation file</span></span>  <br/> |<span data-ttu-id="cb6dd-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cb6dd-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cb6dd-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cb6dd-123">Can be empty</span></span>  <br/> |<span data-ttu-id="cb6dd-124">False</span><span class="sxs-lookup"><span data-stu-id="cb6dd-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb6dd-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb6dd-125">See also</span></span>



[<span data-ttu-id="cb6dd-126">Operación GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="cb6dd-126">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)


- [<span data-ttu-id="cb6dd-127">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="cb6dd-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

