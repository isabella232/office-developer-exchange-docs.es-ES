---
title: Cuándo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- When
api_type:
- schema
ms.assetid: c7df1333-a33d-4cc6-a08a-34b68843f47d
description: El elemento When proporciona información sobre cuándo se produce un elemento de calendario o de reunión.
ms.openlocfilehash: 7c5f85184f966d909960bf1d79f5b8d33c67b51a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461859"
---
# <a name="when"></a><span data-ttu-id="4e4bf-103">Cuándo</span><span class="sxs-lookup"><span data-stu-id="4e4bf-103">When</span></span>

<span data-ttu-id="4e4bf-104">El elemento **When** proporciona información sobre cuándo se produce un elemento de calendario o de reunión.</span><span class="sxs-lookup"><span data-stu-id="4e4bf-104">The **When** element provides information about when a calendar or meeting item occurs.</span></span> 
  
```xml
<When/>
```

 <span data-ttu-id="4e4bf-105">**String**</span><span class="sxs-lookup"><span data-stu-id="4e4bf-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4e4bf-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4e4bf-106">Attributes and elements</span></span>

<span data-ttu-id="4e4bf-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4e4bf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e4bf-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4e4bf-108">Attributes</span></span>

<span data-ttu-id="4e4bf-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4e4bf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4e4bf-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4e4bf-110">Child elements</span></span>

<span data-ttu-id="4e4bf-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4e4bf-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4e4bf-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4e4bf-112">Parent elements</span></span>

|<span data-ttu-id="4e4bf-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4e4bf-113">**Element**</span></span>|<span data-ttu-id="4e4bf-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4e4bf-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e4bf-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="4e4bf-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="4e4bf-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4e4bf-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="4e4bf-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="4e4bf-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="4e4bf-118">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4e4bf-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4e4bf-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4e4bf-119">Text value</span></span>

<span data-ttu-id="4e4bf-120">El valor de texto es una cadena que describe cuándo se produce un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="4e4bf-120">The text value is a string that describes when a calendar item occurs.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4e4bf-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e4bf-121">Remarks</span></span>

<span data-ttu-id="4e4bf-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="4e4bf-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4e4bf-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4e4bf-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e4bf-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="4e4bf-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4e4bf-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4e4bf-125">Schema name</span></span>  <br/> |<span data-ttu-id="4e4bf-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4e4bf-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="4e4bf-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4e4bf-127">Validation file</span></span>  <br/> |<span data-ttu-id="4e4bf-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="4e4bf-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4e4bf-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4e4bf-129">Can be empty</span></span>  <br/> |<span data-ttu-id="4e4bf-130">Falso</span><span class="sxs-lookup"><span data-stu-id="4e4bf-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e4bf-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e4bf-131">See also</span></span>



- [<span data-ttu-id="4e4bf-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4e4bf-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

