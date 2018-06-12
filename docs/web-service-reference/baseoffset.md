---
title: BaseOffset
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BaseOffset
api_type:
- schema
ms.assetid: 0ffad7a6-8e1b-452b-9d87-8e0f6c77f0a6
description: El elemento BaseOffset representa la hourly desplazamiento de hora Universal coordinada (UTC) para la zona horaria actual.
ms.openlocfilehash: 56fc136537b7d5370074a0e6d492f214da3fd960
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763609"
---
# <a name="baseoffset"></a><span data-ttu-id="4785c-103">BaseOffset</span><span class="sxs-lookup"><span data-stu-id="4785c-103">BaseOffset</span></span>

<span data-ttu-id="4785c-104">El elemento **BaseOffset** representa la hourly desplazamiento de hora Universal coordinada (UTC) para la zona horaria actual.</span><span class="sxs-lookup"><span data-stu-id="4785c-104">The **BaseOffset** element represents the hourly offset from Coordinated Universal Time (UTC) for the current time zone.</span></span> 
  
```xml
<BaseOffset/>
```

 <span data-ttu-id="4785c-105">**duration**</span><span class="sxs-lookup"><span data-stu-id="4785c-105">**duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4785c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4785c-106">Attributes and elements</span></span>

<span data-ttu-id="4785c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4785c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4785c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4785c-108">Attributes</span></span>

<span data-ttu-id="4785c-109">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4785c-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4785c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4785c-110">Child elements</span></span>

<span data-ttu-id="4785c-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4785c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4785c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4785c-112">Parent elements</span></span>

|<span data-ttu-id="4785c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4785c-113">**Element**</span></span>|<span data-ttu-id="4785c-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4785c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4785c-115">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="4785c-115">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="4785c-116">Representa la zona horaria de la ubicación donde se hospeda la reunión.</span><span class="sxs-lookup"><span data-stu-id="4785c-116">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4785c-117">Notas</span><span class="sxs-lookup"><span data-stu-id="4785c-117">Remarks</span></span>

<span data-ttu-id="4785c-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4785c-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4785c-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4785c-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4785c-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4785c-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4785c-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4785c-121">Schema Name</span></span>  <br/> |<span data-ttu-id="4785c-122">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4785c-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="4785c-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4785c-123">Validation File</span></span>  <br/> |<span data-ttu-id="4785c-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4785c-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4785c-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4785c-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="4785c-126">False</span><span class="sxs-lookup"><span data-stu-id="4785c-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4785c-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="4785c-127">See also</span></span>



- [<span data-ttu-id="4785c-128">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4785c-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

