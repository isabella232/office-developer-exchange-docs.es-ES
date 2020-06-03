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
description: El elemento ReadItems indica si un usuario tiene permiso para leer elementos dentro de una carpeta calendario. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: e040b643016781f9f890050f189191356f8d4f0b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468302"
---
# <a name="readitems-calendarpermissiontype"></a><span data-ttu-id="3edbe-104">ReadItems (CalendarPermissionType)</span><span class="sxs-lookup"><span data-stu-id="3edbe-104">ReadItems (CalendarPermissionType)</span></span>

<span data-ttu-id="3edbe-105">El elemento **ReadItems** indica si un usuario tiene permiso para leer elementos dentro de una carpeta calendario.</span><span class="sxs-lookup"><span data-stu-id="3edbe-105">The **ReadItems** element indicates whether a user has permission to read items within a Calendar folder.</span></span> <span data-ttu-id="3edbe-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="3edbe-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ReadItems>None or TimeOnly or TimeAndSubjectAndLocation or FullDetails</ReadItems>
```

 <span data-ttu-id="3edbe-107">**CalendarPermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="3edbe-107">**CalendarPermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3edbe-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3edbe-108">Attributes and elements</span></span>

<span data-ttu-id="3edbe-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3edbe-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3edbe-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="3edbe-110">Attributes</span></span>

<span data-ttu-id="3edbe-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3edbe-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3edbe-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3edbe-112">Child elements</span></span>

<span data-ttu-id="3edbe-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3edbe-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3edbe-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3edbe-114">Parent elements</span></span>

|<span data-ttu-id="3edbe-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3edbe-115">**Element**</span></span>|<span data-ttu-id="3edbe-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3edbe-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3edbe-117">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="3edbe-117">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="3edbe-118">Define el acceso que tiene un usuario a una carpeta de calendario.</span><span class="sxs-lookup"><span data-stu-id="3edbe-118">Defines the access that a user has to a Calendar folder.</span></span> <span data-ttu-id="3edbe-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="3edbe-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3edbe-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3edbe-120">Text value</span></span>

<span data-ttu-id="3edbe-121">En la siguiente tabla se enumeran los valores posibles para el elemento **ReadItems** .</span><span class="sxs-lookup"><span data-stu-id="3edbe-121">The following table lists the possible values for the **ReadItems** element.</span></span> 
  
<span data-ttu-id="3edbe-122">**Valores de texto del elemento ReadItems**</span><span class="sxs-lookup"><span data-stu-id="3edbe-122">**ReadItems element text values**</span></span>

|<span data-ttu-id="3edbe-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3edbe-123">**Value**</span></span>|<span data-ttu-id="3edbe-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3edbe-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3edbe-125">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3edbe-125">None</span></span>  <br/> |<span data-ttu-id="3edbe-126">Indica que el usuario no tiene permiso para ver los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="3edbe-126">Indicates that the user does not have permission to view items in the calendar.</span></span>  <br/> |
|<span data-ttu-id="3edbe-127">TimeOnly</span><span class="sxs-lookup"><span data-stu-id="3edbe-127">TimeOnly</span></span>  <br/> |<span data-ttu-id="3edbe-128">Indica que el usuario tiene permiso para ver solo la hora de disponibilidad en el calendario.</span><span class="sxs-lookup"><span data-stu-id="3edbe-128">Indicates that the user has permission to view only free/busy time in the calendar.</span></span>  <br/> |
|<span data-ttu-id="3edbe-129">TimeAndSubjectAndLocation</span><span class="sxs-lookup"><span data-stu-id="3edbe-129">TimeAndSubjectAndLocation</span></span>  <br/> |<span data-ttu-id="3edbe-130">Indica que el usuario tiene permiso para ver la fecha de disponibilidad en el calendario y el asunto y la ubicación de las citas.</span><span class="sxs-lookup"><span data-stu-id="3edbe-130">Indicates that the user has permission to view free/busy time in the calendar and the subject and location of appointments.</span></span>  <br/> |
|<span data-ttu-id="3edbe-131">FullDetails</span><span class="sxs-lookup"><span data-stu-id="3edbe-131">FullDetails</span></span>  <br/> |<span data-ttu-id="3edbe-132">Indica que el usuario tiene permiso para ver todos los elementos del calendario, incluidos el asunto, la ubicación y la fecha de disponibilidad de las citas.</span><span class="sxs-lookup"><span data-stu-id="3edbe-132">Indicates that the user has permission to view all items in the calendar, including free/busy time and subject, location, and details of appointments.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3edbe-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3edbe-133">Remarks</span></span>

<span data-ttu-id="3edbe-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="3edbe-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3edbe-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3edbe-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3edbe-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="3edbe-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3edbe-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3edbe-137">Schema Name</span></span>  <br/> |<span data-ttu-id="3edbe-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3edbe-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="3edbe-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3edbe-139">Validation File</span></span>  <br/> |<span data-ttu-id="3edbe-140">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="3edbe-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3edbe-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3edbe-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="3edbe-142">Falso</span><span class="sxs-lookup"><span data-stu-id="3edbe-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3edbe-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="3edbe-143">See also</span></span>



- [<span data-ttu-id="3edbe-144">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3edbe-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="3edbe-145">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="3edbe-145">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

