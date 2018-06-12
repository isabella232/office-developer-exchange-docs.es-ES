---
title: TimeZoneContext
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZoneContext
api_type:
- schema
ms.assetid: 573c462b-aa1d-4ba0-8852-e3f48b26873b
description: El elemento de TimeZoneContext se usa en el encabezado de protocolo de acceso de objeto Simple (SOAP) para especificar la definición de zona horaria que se utiliza como el valor predeterminado al asignar la zona horaria para las propiedades de fecha y hora de objetos que se crean, actualizan y recuperados por uso de servicios Web de Exchange (EWS).
ms.openlocfilehash: 38b7ab4c587adac45fc3bcf351f417ea72313a97
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840679"
---
# <a name="timezonecontext"></a><span data-ttu-id="6835c-103">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="6835c-103">TimeZoneContext</span></span>

<span data-ttu-id="6835c-104">El elemento de **TimeZoneContext** se usa en el encabezado de protocolo de acceso de objeto Simple (SOAP) para especificar la definición de zona horaria que se utiliza como el valor predeterminado al asignar la zona horaria para las propiedades de fecha y hora de objetos que se crean, actualizan, y recuperado mediante servicios Web de Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="6835c-104">The **TimeZoneContext** element is used in the Simple Object Access Protocol (SOAP) header to specify the time zone definition that is to be used as the default when assigning the time zone for the DateTime properties of objects that are created, updated, and retrieved by using Exchange Web Services (EWS).</span></span> 
  
```xml
<TimeZoneContext>
   <TimeZoneDefinition/>
</TimeZoneContext>
```

 <span data-ttu-id="6835c-105">**TimeZoneContextType**</span><span class="sxs-lookup"><span data-stu-id="6835c-105">**TimeZoneContextType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6835c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6835c-106">Attributes and elements</span></span>

<span data-ttu-id="6835c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6835c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6835c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6835c-108">Attributes</span></span>

<span data-ttu-id="6835c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6835c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6835c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6835c-110">Child elements</span></span>

|<span data-ttu-id="6835c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6835c-111">**Element**</span></span>|<span data-ttu-id="6835c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6835c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6835c-113">Definición de zona horaria</span><span class="sxs-lookup"><span data-stu-id="6835c-113">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="6835c-114">Especifica los períodos y las transiciones que definen una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="6835c-114">Specifies the periods and transitions that define a time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6835c-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6835c-115">Parent elements</span></span>

<span data-ttu-id="6835c-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6835c-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6835c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6835c-117">Remarks</span></span>

<span data-ttu-id="6835c-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="6835c-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6835c-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6835c-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6835c-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6835c-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6835c-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6835c-121">Schema Name</span></span>  <br/> |<span data-ttu-id="6835c-122">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6835c-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="6835c-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6835c-123">Validation File</span></span>  <br/> |<span data-ttu-id="6835c-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6835c-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6835c-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6835c-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="6835c-126">False</span><span class="sxs-lookup"><span data-stu-id="6835c-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6835c-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="6835c-127">See also</span></span>



- [<span data-ttu-id="6835c-128">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="6835c-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

