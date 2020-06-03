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
description: El elemento SharingEffectiveRights indica los permisos que tiene el usuario para los datos de calendario que se están compartiendo.
ms.openlocfilehash: 5581e9cc001608a124ae94e69eba836f6fd98520
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458582"
---
# <a name="sharingeffectiverights-calendarpermissionreadaccesstype"></a><span data-ttu-id="6b40b-103">SharingEffectiveRights (CalendarPermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="6b40b-103">SharingEffectiveRights (CalendarPermissionReadAccessType)</span></span>

<span data-ttu-id="6b40b-104">El elemento **SharingEffectiveRights** indica los permisos que tiene el usuario para los datos de calendario que se están compartiendo.</span><span class="sxs-lookup"><span data-stu-id="6b40b-104">The **SharingEffectiveRights** element indicates the permissions that the user has for the calendar data that is being shared.</span></span> 
  
```XML
<SharingEffectiveRights>None | TimeOnly | TimeAndSubjectAndLocation | FullDetails</SharingEffectiveRights>
```

 <span data-ttu-id="6b40b-105">**CalendarPermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="6b40b-105">**CalendarPermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6b40b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6b40b-106">Attributes and elements</span></span>

<span data-ttu-id="6b40b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6b40b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b40b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6b40b-108">Attributes</span></span>

<span data-ttu-id="6b40b-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6b40b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6b40b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6b40b-110">Child elements</span></span>

<span data-ttu-id="6b40b-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6b40b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6b40b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6b40b-112">Parent elements</span></span>

|<span data-ttu-id="6b40b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6b40b-113">**Element**</span></span>|<span data-ttu-id="6b40b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b40b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b40b-115">Hubiera</span><span class="sxs-lookup"><span data-stu-id="6b40b-115">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="6b40b-116">Representa una carpeta que contiene principalmente elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="6b40b-116">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6b40b-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6b40b-117">Text value</span></span>

<span data-ttu-id="6b40b-118">En la siguiente tabla se enumeran los valores posibles para el elemento **SharingEffectiveRights** .</span><span class="sxs-lookup"><span data-stu-id="6b40b-118">The following table lists the possible values for the **SharingEffectiveRights** element.</span></span> 
  
|<span data-ttu-id="6b40b-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6b40b-119">**Value**</span></span>|<span data-ttu-id="6b40b-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b40b-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6b40b-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6b40b-121">None</span></span>  <br/> |<span data-ttu-id="6b40b-122">Indica que el usuario no tiene permiso para ver los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="6b40b-122">Indicates that the user does not have permission to view items in the calendar.</span></span>  <br/> |
|<span data-ttu-id="6b40b-123">TimeOnly</span><span class="sxs-lookup"><span data-stu-id="6b40b-123">TimeOnly</span></span>  <br/> |<span data-ttu-id="6b40b-124">Indica que el usuario tiene permiso para ver solo la hora de disponibilidad en el calendario.</span><span class="sxs-lookup"><span data-stu-id="6b40b-124">Indicates that the user has permission to view only free/busy time in the calendar.</span></span>  <br/> |
|<span data-ttu-id="6b40b-125">TimeAndSubjectAndLocation</span><span class="sxs-lookup"><span data-stu-id="6b40b-125">TimeAndSubjectAndLocation</span></span>  <br/> |<span data-ttu-id="6b40b-126">Indica que el usuario tiene permiso para ver la fecha de disponibilidad en el calendario y el asunto y la ubicación de las citas.</span><span class="sxs-lookup"><span data-stu-id="6b40b-126">Indicates that the user has permission to view free/busy time in the calendar and the subject and location of appointments.</span></span>  <br/> |
|<span data-ttu-id="6b40b-127">FullDetails</span><span class="sxs-lookup"><span data-stu-id="6b40b-127">FullDetails</span></span>  <br/> |<span data-ttu-id="6b40b-128">Indica que el usuario tiene permiso para ver todos los elementos del calendario, incluidos el asunto, la ubicación y la fecha de disponibilidad de las citas.</span><span class="sxs-lookup"><span data-stu-id="6b40b-128">Indicates that the user has permission to view all items in the calendar, including free/busy time and subject, location, and details of appointments.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b40b-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b40b-129">Remarks</span></span>

<span data-ttu-id="6b40b-130">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b40b-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b40b-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6b40b-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b40b-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="6b40b-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6b40b-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6b40b-133">Schema Name</span></span>  <br/> |<span data-ttu-id="6b40b-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6b40b-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="6b40b-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6b40b-135">Validation File</span></span>  <br/> |<span data-ttu-id="6b40b-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6b40b-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6b40b-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6b40b-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="6b40b-138">Falso</span><span class="sxs-lookup"><span data-stu-id="6b40b-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b40b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b40b-139">See also</span></span>



- [<span data-ttu-id="6b40b-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6b40b-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

