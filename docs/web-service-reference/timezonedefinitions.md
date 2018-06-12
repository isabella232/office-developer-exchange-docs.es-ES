---
title: TimeZoneDefinitions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZoneDefinitions
api_type:
- schema
ms.assetid: 9ca1584e-65b8-49ba-a408-e3e8597e6607
description: El elemento TimeZoneDefinitions representa una matriz de definiciones de zona horaria.
ms.openlocfilehash: 0bc1b69ef564bb4e239d9845a4b1a0133292ff12
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840678"
---
# <a name="timezonedefinitions"></a><span data-ttu-id="91a68-103">TimeZoneDefinitions</span><span class="sxs-lookup"><span data-stu-id="91a68-103">TimeZoneDefinitions</span></span>

<span data-ttu-id="91a68-104">El elemento **TimeZoneDefinitions** representa una matriz de definiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="91a68-104">The **TimeZoneDefinitions** element represents an array of time zone definitions.</span></span> 
  
```XML
<TimeZoneDefinitions>
   <TimeZoneDefinition/>
</TimeZoneDefinitions>
```

 <span data-ttu-id="91a68-105">**ArrayOfTimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="91a68-105">**ArrayOfTimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="91a68-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="91a68-106">Attributes and elements</span></span>

<span data-ttu-id="91a68-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="91a68-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91a68-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="91a68-108">Attributes</span></span>

<span data-ttu-id="91a68-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="91a68-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="91a68-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="91a68-110">Child elements</span></span>

|<span data-ttu-id="91a68-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="91a68-111">**Element**</span></span>|<span data-ttu-id="91a68-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="91a68-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91a68-113">Definición de zona horaria</span><span class="sxs-lookup"><span data-stu-id="91a68-113">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="91a68-114">Especifica los períodos y las transiciones que definen una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="91a68-114">Specifies the periods and transitions that define a time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="91a68-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="91a68-115">Parent elements</span></span>

|<span data-ttu-id="91a68-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="91a68-116">**Element**</span></span>|<span data-ttu-id="91a68-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="91a68-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91a68-118">GetServerTimeZonesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="91a68-118">GetServerTimeZonesResponseMessage</span></span>](getservertimezonesresponsemessage.md) <br/> |<span data-ttu-id="91a68-119">Contiene el estado y el resultado de una solicitud de [operación GetServerTimeZones](getservertimezones-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="91a68-119">Contains the status and result of a [GetServerTimeZones operation](getservertimezones-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91a68-120">Notas</span><span class="sxs-lookup"><span data-stu-id="91a68-120">Remarks</span></span>

<span data-ttu-id="91a68-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="91a68-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="91a68-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="91a68-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91a68-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="91a68-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="91a68-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="91a68-124">Schema Name</span></span>  <br/> |<span data-ttu-id="91a68-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="91a68-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="91a68-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="91a68-126">Validation File</span></span>  <br/> |<span data-ttu-id="91a68-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="91a68-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="91a68-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="91a68-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="91a68-129">False</span><span class="sxs-lookup"><span data-stu-id="91a68-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91a68-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="91a68-130">See also</span></span>



- [<span data-ttu-id="91a68-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="91a68-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

