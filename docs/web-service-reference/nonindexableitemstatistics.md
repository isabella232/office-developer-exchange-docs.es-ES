---
title: NonIndexableItemStatistics
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 12f2934a-008c-4236-b8b3-7c7b6b5707e2
description: El elemento NonIndexableItemStatistics contiene una matriz de estadísticas de los elementos que no se pueden indizar.
ms.openlocfilehash: 1414053b6d39f4cd08ccfd1a11faaf1b13c2052b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836544"
---
# <a name="nonindexableitemstatistics"></a><span data-ttu-id="dd9a8-103">NonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="dd9a8-103">NonIndexableItemStatistics</span></span>

<span data-ttu-id="dd9a8-104">El elemento **NonIndexableItemStatistics** contiene una matriz de estadísticas de los elementos que no se pueden indizar.</span><span class="sxs-lookup"><span data-stu-id="dd9a8-104">The **NonIndexableItemStatistics** element contains an array of statistics for items that could not be indexed.</span></span> 
  
```XML
<NonIndexableItemStatistics>
   <NonIndexableItemStatistic/>
</NonIndexableItemStatistics>
```

 <span data-ttu-id="dd9a8-105">**ArrayOfNonIndexableItemStatisticsType**</span><span class="sxs-lookup"><span data-stu-id="dd9a8-105">**ArrayOfNonIndexableItemStatisticsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dd9a8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dd9a8-106">Attributes and elements</span></span>

<span data-ttu-id="dd9a8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dd9a8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dd9a8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dd9a8-108">Attributes</span></span>

<span data-ttu-id="dd9a8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dd9a8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dd9a8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dd9a8-110">Child elements</span></span>

[<span data-ttu-id="dd9a8-111">NonIndexableItemStatistic</span><span class="sxs-lookup"><span data-stu-id="dd9a8-111">NonIndexableItemStatistic</span></span>](nonindexableitemstatistic.md)
  
### <a name="parent-elements"></a><span data-ttu-id="dd9a8-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dd9a8-112">Parent elements</span></span>

<span data-ttu-id="dd9a8-113">[GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md) , [GetNonIndexableItemStatisticsResponseMessage](getnonindexableitemstatisticsresponsemessage.md)</span><span class="sxs-lookup"><span data-stu-id="dd9a8-113">[GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md) , [GetNonIndexableItemStatisticsResponseMessage](getnonindexableitemstatisticsresponsemessage.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dd9a8-114">Notas</span><span class="sxs-lookup"><span data-stu-id="dd9a8-114">Remarks</span></span>

<span data-ttu-id="dd9a8-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dd9a8-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dd9a8-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="dd9a8-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dd9a8-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dd9a8-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd9a8-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dd9a8-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dd9a8-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dd9a8-119">Schema name</span></span>  <br/> |<span data-ttu-id="dd9a8-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="dd9a8-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dd9a8-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dd9a8-121">Validation file</span></span>  <br/> |<span data-ttu-id="dd9a8-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dd9a8-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dd9a8-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dd9a8-123">Can be empty</span></span>  <br/> |<span data-ttu-id="dd9a8-124">False</span><span class="sxs-lookup"><span data-stu-id="dd9a8-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dd9a8-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="dd9a8-125">See also</span></span>



[<span data-ttu-id="dd9a8-126">Operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="dd9a8-126">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)


- [<span data-ttu-id="dd9a8-127">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="dd9a8-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

