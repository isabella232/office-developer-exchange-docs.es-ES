---
title: Identificadores de
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Ids
api_type:
- schema
ms.assetid: c54cdeaf-6761-4d1a-a329-fb279f0e2a64
description: El elemento de identificadores contiene una matriz de identificadores de definición de zona horaria.
ms.openlocfilehash: e4f8afb1292b3cb9f3990d4613b7461050976a59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835856"
---
# <a name="ids"></a><span data-ttu-id="f62fe-103">Identificadores de</span><span class="sxs-lookup"><span data-stu-id="f62fe-103">Ids</span></span>

<span data-ttu-id="f62fe-104">El elemento de **identificadores** contiene una matriz de identificadores de definición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="f62fe-104">The **Ids** element contains an array of time zone definition identifiers.</span></span> 
  
```XML
<Ids>
   <Id/>
</Ids>
```

 <span data-ttu-id="f62fe-105">**NonEmptyArrayOfTimeZoneIdType**</span><span class="sxs-lookup"><span data-stu-id="f62fe-105">**NonEmptyArrayOfTimeZoneIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f62fe-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f62fe-106">Attributes and elements</span></span>

<span data-ttu-id="f62fe-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f62fe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f62fe-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f62fe-108">Attributes</span></span>

<span data-ttu-id="f62fe-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f62fe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f62fe-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f62fe-110">Child elements</span></span>

|<span data-ttu-id="f62fe-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f62fe-111">**Element**</span></span>|<span data-ttu-id="f62fe-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f62fe-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f62fe-113">Identificador (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="f62fe-113">Id (TimeZone)</span></span>](id-timezone.md) <br/> |<span data-ttu-id="f62fe-114">El elemento que identifica la definición de una sola zona horaria.</span><span class="sxs-lookup"><span data-stu-id="f62fe-114">The element that identifies a single time zone definition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f62fe-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f62fe-115">Parent elements</span></span>

|<span data-ttu-id="f62fe-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f62fe-116">**Element**</span></span>|<span data-ttu-id="f62fe-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f62fe-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f62fe-118">GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="f62fe-118">GetServerTimeZones</span></span>](getservertimezones.md) <br/> |<span data-ttu-id="f62fe-119">Define una solicitud para recuperar las definiciones de zona horaria desde el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f62fe-119">Defines a request to retrieve time zone definitions from the Exchange server.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="f62fe-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f62fe-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f62fe-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f62fe-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f62fe-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f62fe-122">Schema Name</span></span>  <br/> |<span data-ttu-id="f62fe-123">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f62fe-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f62fe-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f62fe-124">Validation File</span></span>  <br/> |<span data-ttu-id="f62fe-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f62fe-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f62fe-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f62fe-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="f62fe-127">False</span><span class="sxs-lookup"><span data-stu-id="f62fe-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f62fe-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f62fe-128">See also</span></span>



- [<span data-ttu-id="f62fe-129">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f62fe-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

