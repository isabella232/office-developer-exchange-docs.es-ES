---
title: Falta
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
description: El elemento IDS contiene una matriz de identificadores de definición de zona horaria.
ms.openlocfilehash: 1c5a6974c8d3abc318ff122f3db09d8c3472dc65
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457623"
---
# <a name="ids"></a><span data-ttu-id="d36f9-103">Falta</span><span class="sxs-lookup"><span data-stu-id="d36f9-103">Ids</span></span>

<span data-ttu-id="d36f9-104">El elemento **IDS** contiene una matriz de identificadores de definición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="d36f9-104">The **Ids** element contains an array of time zone definition identifiers.</span></span> 
  
```XML
<Ids>
   <Id/>
</Ids>
```

 <span data-ttu-id="d36f9-105">**NonEmptyArrayOfTimeZoneIdType**</span><span class="sxs-lookup"><span data-stu-id="d36f9-105">**NonEmptyArrayOfTimeZoneIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d36f9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d36f9-106">Attributes and elements</span></span>

<span data-ttu-id="d36f9-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d36f9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d36f9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d36f9-108">Attributes</span></span>

<span data-ttu-id="d36f9-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d36f9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d36f9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d36f9-110">Child elements</span></span>

|<span data-ttu-id="d36f9-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d36f9-111">**Element**</span></span>|<span data-ttu-id="d36f9-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d36f9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d36f9-113">Identificador (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="d36f9-113">Id (TimeZone)</span></span>](id-timezone.md) <br/> |<span data-ttu-id="d36f9-114">Elemento que identifica una definición de zona horaria única.</span><span class="sxs-lookup"><span data-stu-id="d36f9-114">The element that identifies a single time zone definition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d36f9-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d36f9-115">Parent elements</span></span>

|<span data-ttu-id="d36f9-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d36f9-116">**Element**</span></span>|<span data-ttu-id="d36f9-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d36f9-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d36f9-118">GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="d36f9-118">GetServerTimeZones</span></span>](getservertimezones.md) <br/> |<span data-ttu-id="d36f9-119">Define una solicitud para recuperar definiciones de zona horaria del servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="d36f9-119">Defines a request to retrieve time zone definitions from the Exchange server.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="d36f9-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d36f9-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d36f9-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="d36f9-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d36f9-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d36f9-122">Schema Name</span></span>  <br/> |<span data-ttu-id="d36f9-123">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="d36f9-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d36f9-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d36f9-124">Validation File</span></span>  <br/> |<span data-ttu-id="d36f9-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d36f9-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d36f9-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d36f9-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="d36f9-127">Falso</span><span class="sxs-lookup"><span data-stu-id="d36f9-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d36f9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d36f9-128">See also</span></span>



- [<span data-ttu-id="d36f9-129">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d36f9-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

