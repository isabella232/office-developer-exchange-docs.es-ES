---
title: GetServerTimeZones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServerTimeZones
api_type:
- schema
ms.assetid: 2a89098b-d89b-4d01-827b-50be00f7cbe9
description: El elemento GetServerTimeZones es el elemento raíz en una solicitud para recuperar las definiciones de zona horaria desde el servidor de Exchange.
ms.openlocfilehash: 1ad503ff312497189f57bce9a3670571aedad5ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764978"
---
# <a name="getservertimezones"></a><span data-ttu-id="208af-103">GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="208af-103">GetServerTimeZones</span></span>

<span data-ttu-id="208af-104">El elemento **GetServerTimeZones** es el elemento raíz en una solicitud para recuperar las definiciones de zona horaria desde el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="208af-104">The **GetServerTimeZones** element is the root element in a request to retrieve time zone definitions from the Exchange server.</span></span> 
  
```xml
<GetServerTimeZones ReturnFullTimeZoneData="">   <Ids/></GetServerTimeZones>
```

 <span data-ttu-id="208af-105">**GetServerTimeZonesType**</span><span class="sxs-lookup"><span data-stu-id="208af-105">**GetServerTimeZonesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="208af-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="208af-106">Attributes and elements</span></span>

<span data-ttu-id="208af-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="208af-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="208af-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="208af-108">Attributes</span></span>

|<span data-ttu-id="208af-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="208af-109">**Attribute**</span></span>|<span data-ttu-id="208af-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="208af-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="208af-111">**ReturnFullTimeZoneData**</span><span class="sxs-lookup"><span data-stu-id="208af-111">**ReturnFullTimeZoneData**</span></span> <br/> |<span data-ttu-id="208af-112">Especifica si la [operación de GetServerTimeZones](getservertimezones-operation.md) devuelve la definición completa o sólo el nombre y el identificador de cada zona horaria.</span><span class="sxs-lookup"><span data-stu-id="208af-112">Specifies whether the [GetServerTimeZones operation](getservertimezones-operation.md) returns the complete definition or only the name and identifier for each time zone.</span></span> <span data-ttu-id="208af-113">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="208af-113">This attribute is optional.</span></span> <span data-ttu-id="208af-114">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="208af-114">The default value is **true**.</span></span>  <br/> |
   
#### <a name="returnfulltimezonedata-attribute"></a><span data-ttu-id="208af-115">Atributo ReturnFullTimeZoneData</span><span class="sxs-lookup"><span data-stu-id="208af-115">ReturnFullTimeZoneData Attribute</span></span>

|<span data-ttu-id="208af-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="208af-116">**Value**</span></span>|<span data-ttu-id="208af-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="208af-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="208af-118">**True**</span><span class="sxs-lookup"><span data-stu-id="208af-118">**true**</span></span> <br/> |<span data-ttu-id="208af-119">Devolver las definiciones de completadas para cada zona horaria.</span><span class="sxs-lookup"><span data-stu-id="208af-119">Return the complete definitions for each time zone.</span></span>  <br/> |
|<span data-ttu-id="208af-120">**False**</span><span class="sxs-lookup"><span data-stu-id="208af-120">**false**</span></span> <br/> |<span data-ttu-id="208af-121">Devolver solo el nombre y el identificador de cada zona horaria.</span><span class="sxs-lookup"><span data-stu-id="208af-121">Return only the name and identifier for each time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="208af-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="208af-122">Child elements</span></span>

|<span data-ttu-id="208af-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="208af-123">**Element**</span></span>|<span data-ttu-id="208af-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="208af-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="208af-125">Identificadores de</span><span class="sxs-lookup"><span data-stu-id="208af-125">Ids</span></span>](ids.md) <br/> |<span data-ttu-id="208af-126">Contiene una matriz de identificadores de definición de zona horaria que especifica las definiciones de zona horaria solicitado.</span><span class="sxs-lookup"><span data-stu-id="208af-126">Contains an array of time zone definition identifiers that specifies the requested time zone definitions.</span></span> <span data-ttu-id="208af-127">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="208af-127">This element is optional.</span></span> <span data-ttu-id="208af-128">Si este elemento no está incluido en la solicitud de la [operación de GetServerTimeZones](getservertimezones-operation.md) , se devuelven todas las definiciones de zona horaria que están disponibles en el servidor en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="208af-128">If this element is not included in the [GetServerTimeZones operation](getservertimezones-operation.md) request, all time zone definitions that are available on the server are returned in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="208af-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="208af-129">Parent elements</span></span>

<span data-ttu-id="208af-130">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="208af-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="208af-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="208af-131">Remarks</span></span>

<span data-ttu-id="208af-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="208af-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="208af-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="208af-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="208af-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="208af-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="208af-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="208af-135">Schema Name</span></span>  <br/> |<span data-ttu-id="208af-136">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="208af-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="208af-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="208af-137">Validation File</span></span>  <br/> |<span data-ttu-id="208af-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="208af-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="208af-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="208af-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="208af-140">False</span><span class="sxs-lookup"><span data-stu-id="208af-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="208af-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="208af-141">See also</span></span>



[<span data-ttu-id="208af-142">Operación GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="208af-142">GetServerTimeZones operation</span></span>](getservertimezones-operation.md)
  
[<span data-ttu-id="208af-143">GetServerTimeZonesResponse</span><span class="sxs-lookup"><span data-stu-id="208af-143">GetServerTimeZonesResponse</span></span>](getservertimezonesresponse.md)


- [<span data-ttu-id="208af-144">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="208af-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

