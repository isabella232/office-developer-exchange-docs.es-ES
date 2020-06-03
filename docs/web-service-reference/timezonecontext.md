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
description: El elemento TimeZoneContext se usa en el encabezado del Protocolo simple de acceso a objetos (SOAP) para especificar la definición de zona horaria que se va a usar como predeterminada al asignar la zona horaria para las propiedades DateTime de los objetos que se crean, actualizan y recuperan mediante los servicios web Exchange (EWS).
ms.openlocfilehash: 26727317ccf34338e8d62ec92bd7a44d43a6cfdb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460256"
---
# <a name="timezonecontext"></a><span data-ttu-id="e90da-103">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="e90da-103">TimeZoneContext</span></span>

<span data-ttu-id="e90da-104">El elemento **TimeZoneContext** se usa en el encabezado del Protocolo simple de acceso a objetos (SOAP) para especificar la definición de zona horaria que se va a usar como predeterminada al asignar la zona horaria para las propiedades DateTime de los objetos que se crean, actualizan y recuperan mediante los servicios web Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="e90da-104">The **TimeZoneContext** element is used in the Simple Object Access Protocol (SOAP) header to specify the time zone definition that is to be used as the default when assigning the time zone for the DateTime properties of objects that are created, updated, and retrieved by using Exchange Web Services (EWS).</span></span> 
  
```xml
<TimeZoneContext>
   <TimeZoneDefinition/>
</TimeZoneContext>
```

 <span data-ttu-id="e90da-105">**TimeZoneContextType**</span><span class="sxs-lookup"><span data-stu-id="e90da-105">**TimeZoneContextType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e90da-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e90da-106">Attributes and elements</span></span>

<span data-ttu-id="e90da-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e90da-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e90da-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e90da-108">Attributes</span></span>

<span data-ttu-id="e90da-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e90da-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e90da-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e90da-110">Child elements</span></span>

|<span data-ttu-id="e90da-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e90da-111">**Element**</span></span>|<span data-ttu-id="e90da-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e90da-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e90da-113">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="e90da-113">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="e90da-114">Especifica los períodos y las transiciones que definen una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="e90da-114">Specifies the periods and transitions that define a time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e90da-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e90da-115">Parent elements</span></span>

<span data-ttu-id="e90da-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e90da-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e90da-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e90da-117">Remarks</span></span>

<span data-ttu-id="e90da-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="e90da-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e90da-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e90da-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e90da-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="e90da-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e90da-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e90da-121">Schema Name</span></span>  <br/> |<span data-ttu-id="e90da-122">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e90da-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="e90da-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e90da-123">Validation File</span></span>  <br/> |<span data-ttu-id="e90da-124">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e90da-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e90da-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e90da-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="e90da-126">Falso</span><span class="sxs-lookup"><span data-stu-id="e90da-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e90da-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e90da-127">See also</span></span>



- [<span data-ttu-id="e90da-128">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e90da-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

