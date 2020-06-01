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
description: El elemento GetServerTimeZones es el elemento raíz de una solicitud para recuperar definiciones de zona horaria del servidor de Exchange.
ms.openlocfilehash: 797e4543c94b0628242bcf544fe9a735ebaa5a63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460942"
---
# <a name="getservertimezones"></a><span data-ttu-id="65aa3-103">GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="65aa3-103">GetServerTimeZones</span></span>

<span data-ttu-id="65aa3-104">El elemento **GetServerTimeZones** es el elemento raíz de una solicitud para recuperar definiciones de zona horaria del servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="65aa3-104">The **GetServerTimeZones** element is the root element in a request to retrieve time zone definitions from the Exchange server.</span></span> 
  
```xml
<GetServerTimeZones ReturnFullTimeZoneData="">   <Ids/></GetServerTimeZones>
```

 <span data-ttu-id="65aa3-105">**GetServerTimeZonesType**</span><span class="sxs-lookup"><span data-stu-id="65aa3-105">**GetServerTimeZonesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="65aa3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="65aa3-106">Attributes and elements</span></span>

<span data-ttu-id="65aa3-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="65aa3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65aa3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="65aa3-108">Attributes</span></span>

|<span data-ttu-id="65aa3-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="65aa3-109">**Attribute**</span></span>|<span data-ttu-id="65aa3-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65aa3-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="65aa3-111">**ReturnFullTimeZoneData**</span><span class="sxs-lookup"><span data-stu-id="65aa3-111">**ReturnFullTimeZoneData**</span></span> <br/> |<span data-ttu-id="65aa3-112">Especifica si la [operación GetServerTimeZones](getservertimezones-operation.md) devuelve la definición completa o solo el nombre y el identificador de cada zona horaria.</span><span class="sxs-lookup"><span data-stu-id="65aa3-112">Specifies whether the [GetServerTimeZones operation](getservertimezones-operation.md) returns the complete definition or only the name and identifier for each time zone.</span></span> <span data-ttu-id="65aa3-113">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="65aa3-113">This attribute is optional.</span></span> <span data-ttu-id="65aa3-114">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="65aa3-114">The default value is **true**.</span></span>  <br/> |
   
#### <a name="returnfulltimezonedata-attribute"></a><span data-ttu-id="65aa3-115">Atributo ReturnFullTimeZoneData</span><span class="sxs-lookup"><span data-stu-id="65aa3-115">ReturnFullTimeZoneData Attribute</span></span>

|<span data-ttu-id="65aa3-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="65aa3-116">**Value**</span></span>|<span data-ttu-id="65aa3-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65aa3-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="65aa3-118">**true**</span><span class="sxs-lookup"><span data-stu-id="65aa3-118">**true**</span></span> <br/> |<span data-ttu-id="65aa3-119">Devuelve las definiciones completas para cada zona horaria.</span><span class="sxs-lookup"><span data-stu-id="65aa3-119">Return the complete definitions for each time zone.</span></span>  <br/> |
|<span data-ttu-id="65aa3-120">**false**</span><span class="sxs-lookup"><span data-stu-id="65aa3-120">**false**</span></span> <br/> |<span data-ttu-id="65aa3-121">Devolver solo el nombre y el identificador de cada zona horaria.</span><span class="sxs-lookup"><span data-stu-id="65aa3-121">Return only the name and identifier for each time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="65aa3-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="65aa3-122">Child elements</span></span>

|<span data-ttu-id="65aa3-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="65aa3-123">**Element**</span></span>|<span data-ttu-id="65aa3-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65aa3-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65aa3-125">Falta</span><span class="sxs-lookup"><span data-stu-id="65aa3-125">Ids</span></span>](ids.md) <br/> |<span data-ttu-id="65aa3-126">Contiene una matriz de identificadores de definición de zona horaria que especifica las definiciones de zona horaria solicitada.</span><span class="sxs-lookup"><span data-stu-id="65aa3-126">Contains an array of time zone definition identifiers that specifies the requested time zone definitions.</span></span> <span data-ttu-id="65aa3-127">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="65aa3-127">This element is optional.</span></span> <span data-ttu-id="65aa3-128">Si este elemento no se incluye en la solicitud de [operación GetServerTimeZones](getservertimezones-operation.md) , todas las definiciones de zona horaria que estén disponibles en el servidor se devolverán en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65aa3-128">If this element is not included in the [GetServerTimeZones operation](getservertimezones-operation.md) request, all time zone definitions that are available on the server are returned in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="65aa3-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="65aa3-129">Parent elements</span></span>

<span data-ttu-id="65aa3-130">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="65aa3-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="65aa3-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="65aa3-131">Remarks</span></span>

<span data-ttu-id="65aa3-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="65aa3-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65aa3-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="65aa3-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65aa3-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="65aa3-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="65aa3-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="65aa3-135">Schema Name</span></span>  <br/> |<span data-ttu-id="65aa3-136">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="65aa3-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="65aa3-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="65aa3-137">Validation File</span></span>  <br/> |<span data-ttu-id="65aa3-138">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="65aa3-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="65aa3-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="65aa3-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="65aa3-140">Falso</span><span class="sxs-lookup"><span data-stu-id="65aa3-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65aa3-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="65aa3-141">See also</span></span>



[<span data-ttu-id="65aa3-142">Operación GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="65aa3-142">GetServerTimeZones operation</span></span>](getservertimezones-operation.md)
  
[<span data-ttu-id="65aa3-143">GetServerTimeZonesResponse</span><span class="sxs-lookup"><span data-stu-id="65aa3-143">GetServerTimeZonesResponse</span></span>](getservertimezonesresponse.md)


- [<span data-ttu-id="65aa3-144">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="65aa3-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

