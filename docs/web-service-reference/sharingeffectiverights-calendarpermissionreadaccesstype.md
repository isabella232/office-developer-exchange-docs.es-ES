---
title: SharingEffectiveRights (CalendarPermissionReadAccessType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharingEffectiveRights
api_type:
- schema
ms.assetid: b519f642-a9ef-4300-92e6-ed8202855fde
description: El elemento SharingEffectiveRights indica los permisos que tiene el usuario para los datos del calendario que se está compartiendo.
ms.openlocfilehash: e7d2aa061650c33d27de042ae8a6348f9a7d3430
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837480"
---
# <a name="sharingeffectiverights-calendarpermissionreadaccesstype"></a><span data-ttu-id="0d030-103">SharingEffectiveRights (CalendarPermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="0d030-103">SharingEffectiveRights (CalendarPermissionReadAccessType)</span></span>

<span data-ttu-id="0d030-104">El elemento **SharingEffectiveRights** indica los permisos que tiene el usuario para los datos del calendario que se está compartiendo.</span><span class="sxs-lookup"><span data-stu-id="0d030-104">The **SharingEffectiveRights** element indicates the permissions that the user has for the calendar data that is being shared.</span></span> 
  
```XML
<SharingEffectiveRights>None | TimeOnly | TimeAndSubjectAndLocation | FullDetails</SharingEffectiveRights>
```

 <span data-ttu-id="0d030-105">**CalendarPermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="0d030-105">**CalendarPermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0d030-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0d030-106">Attributes and elements</span></span>

<span data-ttu-id="0d030-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0d030-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d030-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0d030-108">Attributes</span></span>

<span data-ttu-id="0d030-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0d030-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d030-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0d030-110">Child elements</span></span>

<span data-ttu-id="0d030-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0d030-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0d030-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0d030-112">Parent elements</span></span>

|<span data-ttu-id="0d030-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d030-113">**Element**</span></span>|<span data-ttu-id="0d030-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0d030-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d030-115">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="0d030-115">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="0d030-116">Representa una carpeta que principalmente contiene los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="0d030-116">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0d030-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0d030-117">Text value</span></span>

<span data-ttu-id="0d030-118">En la siguiente tabla se enumera los valores posibles para el elemento **SharingEffectiveRights** .</span><span class="sxs-lookup"><span data-stu-id="0d030-118">The following table lists the possible values for the **SharingEffectiveRights** element.</span></span> 
  
|<span data-ttu-id="0d030-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0d030-119">**Value**</span></span>|<span data-ttu-id="0d030-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0d030-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0d030-121">None</span><span class="sxs-lookup"><span data-stu-id="0d030-121">None</span></span>  <br/> |<span data-ttu-id="0d030-122">Indica que el usuario no tiene permiso para ver los elementos en el calendario.</span><span class="sxs-lookup"><span data-stu-id="0d030-122">Indicates that the user does not have permission to view items in the calendar.</span></span>  <br/> |
|<span data-ttu-id="0d030-123">TimeOnly</span><span class="sxs-lookup"><span data-stu-id="0d030-123">TimeOnly</span></span>  <br/> |<span data-ttu-id="0d030-124">Indica que el usuario tiene permiso para ver sólo horas de disponibilidad en el calendario.</span><span class="sxs-lookup"><span data-stu-id="0d030-124">Indicates that the user has permission to view only free/busy time in the calendar.</span></span>  <br/> |
|<span data-ttu-id="0d030-125">TimeAndSubjectAndLocation</span><span class="sxs-lookup"><span data-stu-id="0d030-125">TimeAndSubjectAndLocation</span></span>  <br/> |<span data-ttu-id="0d030-126">Indica que el usuario tiene permiso para ver el tiempo libre/ocupada en el calendario y el asunto y la ubicación de las citas.</span><span class="sxs-lookup"><span data-stu-id="0d030-126">Indicates that the user has permission to view free/busy time in the calendar and the subject and location of appointments.</span></span>  <br/> |
|<span data-ttu-id="0d030-127">FullDetails</span><span class="sxs-lookup"><span data-stu-id="0d030-127">FullDetails</span></span>  <br/> |<span data-ttu-id="0d030-128">Indica que el usuario tiene permiso para ver todos los elementos en el calendario, incluidos el tiempo libre/ocupado y asunto, ubicación y detalles de las citas.</span><span class="sxs-lookup"><span data-stu-id="0d030-128">Indicates that the user has permission to view all items in the calendar, including free/busy time and subject, location, and details of appointments.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d030-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0d030-129">Remarks</span></span>

<span data-ttu-id="0d030-130">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0d030-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d030-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0d030-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d030-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0d030-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0d030-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0d030-133">Schema Name</span></span>  <br/> |<span data-ttu-id="0d030-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0d030-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="0d030-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0d030-135">Validation File</span></span>  <br/> |<span data-ttu-id="0d030-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0d030-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0d030-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0d030-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="0d030-138">False</span><span class="sxs-lookup"><span data-stu-id="0d030-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d030-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d030-139">See also</span></span>



- [<span data-ttu-id="0d030-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0d030-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

