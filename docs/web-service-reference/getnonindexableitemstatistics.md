---
title: GetNonIndexableItemStatistics
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dd16d1fb-d82d-42e5-b64a-bc6c19c48fa8
description: El elemento GetNonIndexableItemStatistics especifica una solicitud para recuperar las estadísticas de elemento nonindexable.
ms.openlocfilehash: 4e6f9a0ba94e9946a3910661810bc2c9e748ba9f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764914"
---
# <a name="getnonindexableitemstatistics"></a><span data-ttu-id="8ca34-103">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="8ca34-103">GetNonIndexableItemStatistics</span></span>

<span data-ttu-id="8ca34-104">El elemento **GetNonIndexableItemStatistics** especifica una solicitud para recuperar las estadísticas de elemento nonindexable.</span><span class="sxs-lookup"><span data-stu-id="8ca34-104">The **GetNonIndexableItemStatistics** element specifies a request to retrieve nonindexable item statistics.</span></span> 
  
```XML
<GetNonIndexableItemStatistics>
    <Mailboxes/>
</GetNonIndexableItemStatistics>
```

 <span data-ttu-id="8ca34-105">**GetNonIndexableItemStatisticsType**</span><span class="sxs-lookup"><span data-stu-id="8ca34-105">**GetNonIndexableItemStatisticsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8ca34-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8ca34-106">Attributes and elements</span></span>

<span data-ttu-id="8ca34-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8ca34-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8ca34-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8ca34-108">Attributes</span></span>

<span data-ttu-id="8ca34-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8ca34-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8ca34-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8ca34-110">Child elements</span></span>

|<span data-ttu-id="8ca34-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8ca34-111">**Element**</span></span>|<span data-ttu-id="8ca34-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8ca34-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ca34-113">Buzones de correo (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="8ca34-113">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md) <br/> |<span data-ttu-id="8ca34-114">Especifica una matriz de elementos de **buzón de correo** .</span><span class="sxs-lookup"><span data-stu-id="8ca34-114">Specifies an array of **Mailbox** elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8ca34-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8ca34-115">Parent elements</span></span>

<span data-ttu-id="8ca34-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8ca34-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8ca34-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ca34-117">Remarks</span></span>

<span data-ttu-id="8ca34-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8ca34-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8ca34-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="8ca34-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8ca34-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8ca34-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ca34-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8ca34-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8ca34-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8ca34-122">Schema Name</span></span>  <br/> |<span data-ttu-id="8ca34-123">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="8ca34-123">Message schema</span></span>  <br/> |
|<span data-ttu-id="8ca34-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8ca34-124">Validation File</span></span>  <br/> |<span data-ttu-id="8ca34-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8ca34-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8ca34-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8ca34-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="8ca34-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="8ca34-127">See also</span></span>



- [<span data-ttu-id="8ca34-128">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="8ca34-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

