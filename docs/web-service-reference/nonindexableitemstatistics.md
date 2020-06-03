---
title: NonIndexableItemStatistics
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 12f2934a-008c-4236-b8b3-7c7b6b5707e2
description: El elemento NonIndexableItemStatistics contiene una matriz de estadísticas para los elementos que no se pudieron indizar.
ms.openlocfilehash: 5a11bd4d7ef0c574f26580613063a885530176f9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466734"
---
# <a name="nonindexableitemstatistics"></a><span data-ttu-id="95c4a-103">NonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="95c4a-103">NonIndexableItemStatistics</span></span>

<span data-ttu-id="95c4a-104">El elemento **NonIndexableItemStatistics** contiene una matriz de estadísticas para los elementos que no se pudieron indizar.</span><span class="sxs-lookup"><span data-stu-id="95c4a-104">The **NonIndexableItemStatistics** element contains an array of statistics for items that could not be indexed.</span></span> 
  
```XML
<NonIndexableItemStatistics>
   <NonIndexableItemStatistic/>
</NonIndexableItemStatistics>
```

 <span data-ttu-id="95c4a-105">**ArrayOfNonIndexableItemStatisticsType**</span><span class="sxs-lookup"><span data-stu-id="95c4a-105">**ArrayOfNonIndexableItemStatisticsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="95c4a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="95c4a-106">Attributes and elements</span></span>

<span data-ttu-id="95c4a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="95c4a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95c4a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="95c4a-108">Attributes</span></span>

<span data-ttu-id="95c4a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="95c4a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95c4a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="95c4a-110">Child elements</span></span>

[<span data-ttu-id="95c4a-111">NonIndexableItemStatistic</span><span class="sxs-lookup"><span data-stu-id="95c4a-111">NonIndexableItemStatistic</span></span>](nonindexableitemstatistic.md)
  
### <a name="parent-elements"></a><span data-ttu-id="95c4a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="95c4a-112">Parent elements</span></span>

<span data-ttu-id="95c4a-113">[GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md) , [GetNonIndexableItemStatisticsResponseMessage](getnonindexableitemstatisticsresponsemessage.md)</span><span class="sxs-lookup"><span data-stu-id="95c4a-113">[GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md) , [GetNonIndexableItemStatisticsResponseMessage](getnonindexableitemstatisticsresponsemessage.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="95c4a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95c4a-114">Remarks</span></span>

<span data-ttu-id="95c4a-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="95c4a-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="95c4a-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="95c4a-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95c4a-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="95c4a-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95c4a-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="95c4a-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="95c4a-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="95c4a-119">Schema name</span></span>  <br/> |<span data-ttu-id="95c4a-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="95c4a-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="95c4a-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="95c4a-121">Validation file</span></span>  <br/> |<span data-ttu-id="95c4a-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="95c4a-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="95c4a-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="95c4a-123">Can be empty</span></span>  <br/> |<span data-ttu-id="95c4a-124">Falso</span><span class="sxs-lookup"><span data-stu-id="95c4a-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95c4a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="95c4a-125">See also</span></span>



[<span data-ttu-id="95c4a-126">Operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="95c4a-126">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)


- [<span data-ttu-id="95c4a-127">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="95c4a-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

