---
title: ReadItems (CalendarPermissionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReadItems
api_type:
- schema
ms.assetid: bec01982-26a1-4373-b1e6-2e0c838d83c4
description: El elemento ReadItems indica si un usuario tiene permiso para leer elementos dentro de una carpeta de calendario. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 532b90c47cca7117a89d59e7012436268be9ebb0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836964"
---
# <a name="readitems-calendarpermissiontype"></a><span data-ttu-id="40ac5-104">ReadItems (CalendarPermissionType)</span><span class="sxs-lookup"><span data-stu-id="40ac5-104">ReadItems (CalendarPermissionType)</span></span>

<span data-ttu-id="40ac5-105">El elemento **ReadItems** indica si un usuario tiene permiso para leer elementos dentro de una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="40ac5-105">The **ReadItems** element indicates whether a user has permission to read items within a Calendar folder.</span></span> <span data-ttu-id="40ac5-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="40ac5-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ReadItems>None or TimeOnly or TimeAndSubjectAndLocation or FullDetails</ReadItems>
```

 <span data-ttu-id="40ac5-107">**CalendarPermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="40ac5-107">**CalendarPermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="40ac5-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="40ac5-108">Attributes and elements</span></span>

<span data-ttu-id="40ac5-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="40ac5-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="40ac5-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="40ac5-110">Attributes</span></span>

<span data-ttu-id="40ac5-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="40ac5-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="40ac5-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="40ac5-112">Child elements</span></span>

<span data-ttu-id="40ac5-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="40ac5-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="40ac5-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="40ac5-114">Parent elements</span></span>

|<span data-ttu-id="40ac5-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="40ac5-115">**Element**</span></span>|<span data-ttu-id="40ac5-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40ac5-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40ac5-117">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="40ac5-117">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="40ac5-118">Define el acceso que tiene un usuario a una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="40ac5-118">Defines the access that a user has to a Calendar folder.</span></span> <span data-ttu-id="40ac5-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="40ac5-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="40ac5-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="40ac5-120">Text value</span></span>

<span data-ttu-id="40ac5-121">En la siguiente tabla se enumera los valores posibles para el elemento **ReadItems** .</span><span class="sxs-lookup"><span data-stu-id="40ac5-121">The following table lists the possible values for the **ReadItems** element.</span></span> 
  
<span data-ttu-id="40ac5-122">**Valores de texto de elemento ReadItems**</span><span class="sxs-lookup"><span data-stu-id="40ac5-122">**ReadItems element text values**</span></span>

|<span data-ttu-id="40ac5-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="40ac5-123">**Value**</span></span>|<span data-ttu-id="40ac5-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40ac5-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="40ac5-125">None</span><span class="sxs-lookup"><span data-stu-id="40ac5-125">None</span></span>  <br/> |<span data-ttu-id="40ac5-126">Indica que el usuario no tiene permiso para ver los elementos en el calendario.</span><span class="sxs-lookup"><span data-stu-id="40ac5-126">Indicates that the user does not have permission to view items in the calendar.</span></span>  <br/> |
|<span data-ttu-id="40ac5-127">TimeOnly</span><span class="sxs-lookup"><span data-stu-id="40ac5-127">TimeOnly</span></span>  <br/> |<span data-ttu-id="40ac5-128">Indica que el usuario tiene permiso para ver sólo horas de disponibilidad en el calendario.</span><span class="sxs-lookup"><span data-stu-id="40ac5-128">Indicates that the user has permission to view only free/busy time in the calendar.</span></span>  <br/> |
|<span data-ttu-id="40ac5-129">TimeAndSubjectAndLocation</span><span class="sxs-lookup"><span data-stu-id="40ac5-129">TimeAndSubjectAndLocation</span></span>  <br/> |<span data-ttu-id="40ac5-130">Indica que el usuario tiene permiso para ver el tiempo libre/ocupada en el calendario y el asunto y la ubicación de las citas.</span><span class="sxs-lookup"><span data-stu-id="40ac5-130">Indicates that the user has permission to view free/busy time in the calendar and the subject and location of appointments.</span></span>  <br/> |
|<span data-ttu-id="40ac5-131">FullDetails</span><span class="sxs-lookup"><span data-stu-id="40ac5-131">FullDetails</span></span>  <br/> |<span data-ttu-id="40ac5-132">Indica que el usuario tiene permiso para ver todos los elementos en el calendario, incluidos el tiempo libre/ocupado y asunto, ubicación y detalles de las citas.</span><span class="sxs-lookup"><span data-stu-id="40ac5-132">Indicates that the user has permission to view all items in the calendar, including free/busy time and subject, location, and details of appointments.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40ac5-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40ac5-133">Remarks</span></span>

<span data-ttu-id="40ac5-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="40ac5-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="40ac5-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="40ac5-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40ac5-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="40ac5-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="40ac5-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="40ac5-137">Schema Name</span></span>  <br/> |<span data-ttu-id="40ac5-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="40ac5-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="40ac5-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="40ac5-139">Validation File</span></span>  <br/> |<span data-ttu-id="40ac5-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="40ac5-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="40ac5-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="40ac5-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="40ac5-142">False</span><span class="sxs-lookup"><span data-stu-id="40ac5-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40ac5-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="40ac5-143">See also</span></span>



- [<span data-ttu-id="40ac5-144">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="40ac5-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="40ac5-145">Establecimiento de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="40ac5-145">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

