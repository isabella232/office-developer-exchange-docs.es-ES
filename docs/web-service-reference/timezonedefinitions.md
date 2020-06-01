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
ms.openlocfilehash: 16a25eb4fdcad2554ebd19626d0a0bc7f6391ac5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468764"
---
# <a name="timezonedefinitions"></a><span data-ttu-id="02110-103">TimeZoneDefinitions</span><span class="sxs-lookup"><span data-stu-id="02110-103">TimeZoneDefinitions</span></span>

<span data-ttu-id="02110-104">El elemento **TimeZoneDefinitions** representa una matriz de definiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="02110-104">The **TimeZoneDefinitions** element represents an array of time zone definitions.</span></span> 
  
```XML
<TimeZoneDefinitions>
   <TimeZoneDefinition/>
</TimeZoneDefinitions>
```

 <span data-ttu-id="02110-105">**ArrayOfTimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="02110-105">**ArrayOfTimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="02110-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="02110-106">Attributes and elements</span></span>

<span data-ttu-id="02110-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="02110-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02110-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="02110-108">Attributes</span></span>

<span data-ttu-id="02110-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="02110-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="02110-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="02110-110">Child elements</span></span>

|<span data-ttu-id="02110-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="02110-111">**Element**</span></span>|<span data-ttu-id="02110-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02110-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02110-113">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="02110-113">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="02110-114">Especifica los períodos y las transiciones que definen una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="02110-114">Specifies the periods and transitions that define a time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="02110-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="02110-115">Parent elements</span></span>

|<span data-ttu-id="02110-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="02110-116">**Element**</span></span>|<span data-ttu-id="02110-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02110-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02110-118">GetServerTimeZonesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="02110-118">GetServerTimeZonesResponseMessage</span></span>](getservertimezonesresponsemessage.md) <br/> |<span data-ttu-id="02110-119">Contiene el estado y el resultado de una solicitud de [operación GetServerTimeZones](getservertimezones-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="02110-119">Contains the status and result of a [GetServerTimeZones operation](getservertimezones-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02110-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="02110-120">Remarks</span></span>

<span data-ttu-id="02110-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="02110-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02110-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="02110-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02110-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="02110-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="02110-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="02110-124">Schema Name</span></span>  <br/> |<span data-ttu-id="02110-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="02110-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="02110-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="02110-126">Validation File</span></span>  <br/> |<span data-ttu-id="02110-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="02110-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="02110-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="02110-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="02110-129">Falso</span><span class="sxs-lookup"><span data-stu-id="02110-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02110-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="02110-130">See also</span></span>



- [<span data-ttu-id="02110-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="02110-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

