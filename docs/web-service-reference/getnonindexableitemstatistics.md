---
title: GetNonIndexableItemStatistics
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dd16d1fb-d82d-42e5-b64a-bc6c19c48fa8
description: El elemento GetNonIndexableItemStatistics especifica una solicitud para recuperar las estadísticas de elementos no indizables.
ms.openlocfilehash: 4b605379f20f5558566f1cfbad9ef1aa33b6fce6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452793"
---
# <a name="getnonindexableitemstatistics"></a><span data-ttu-id="483c4-103">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="483c4-103">GetNonIndexableItemStatistics</span></span>

<span data-ttu-id="483c4-104">El elemento **GetNonIndexableItemStatistics** especifica una solicitud para recuperar las estadísticas de elementos no indizables.</span><span class="sxs-lookup"><span data-stu-id="483c4-104">The **GetNonIndexableItemStatistics** element specifies a request to retrieve nonindexable item statistics.</span></span> 
  
```XML
<GetNonIndexableItemStatistics>
    <Mailboxes/>
</GetNonIndexableItemStatistics>
```

 <span data-ttu-id="483c4-105">**GetNonIndexableItemStatisticsType**</span><span class="sxs-lookup"><span data-stu-id="483c4-105">**GetNonIndexableItemStatisticsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="483c4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="483c4-106">Attributes and elements</span></span>

<span data-ttu-id="483c4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="483c4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="483c4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="483c4-108">Attributes</span></span>

<span data-ttu-id="483c4-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="483c4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="483c4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="483c4-110">Child elements</span></span>

|<span data-ttu-id="483c4-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="483c4-111">**Element**</span></span>|<span data-ttu-id="483c4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="483c4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="483c4-113">Buzones de correo (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="483c4-113">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md) <br/> |<span data-ttu-id="483c4-114">Especifica una matriz de elementos **Mailbox** .</span><span class="sxs-lookup"><span data-stu-id="483c4-114">Specifies an array of **Mailbox** elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="483c4-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="483c4-115">Parent elements</span></span>

<span data-ttu-id="483c4-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="483c4-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="483c4-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="483c4-117">Remarks</span></span>

<span data-ttu-id="483c4-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="483c4-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="483c4-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="483c4-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="483c4-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="483c4-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="483c4-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="483c4-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="483c4-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="483c4-122">Schema Name</span></span>  <br/> |<span data-ttu-id="483c4-123">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="483c4-123">Message schema</span></span>  <br/> |
|<span data-ttu-id="483c4-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="483c4-124">Validation File</span></span>  <br/> |<span data-ttu-id="483c4-125">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="483c4-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="483c4-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="483c4-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="483c4-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="483c4-127">See also</span></span>



- [<span data-ttu-id="483c4-128">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="483c4-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

