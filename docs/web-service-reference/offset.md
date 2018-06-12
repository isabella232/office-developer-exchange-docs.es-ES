---
title: Desplazamiento
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Offset
api_type:
- schema
ms.assetid: dcbb9d85-d90c-4363-b4c9-d081ad03f407
description: El elemento de desplazamiento describe el desplazamiento desde el BaseOffset. Junto con el elemento BaseOffset, el elemento de desplazamiento identifica si el tiempo es estándar o el horario de verano.
ms.openlocfilehash: d85fef0d67633733f6aa1943d70413ea70a528d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836642"
---
# <a name="offset"></a><span data-ttu-id="25fd8-104">Desplazamiento</span><span class="sxs-lookup"><span data-stu-id="25fd8-104">Offset</span></span>

<span data-ttu-id="25fd8-105">El elemento de **desplazamiento** describe el desplazamiento desde el [BaseOffset](baseoffset.md).</span><span class="sxs-lookup"><span data-stu-id="25fd8-105">The **Offset** element describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="25fd8-106">Junto con el elemento **BaseOffset** , el elemento de **desplazamiento** identifica si el tiempo es estándar o el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="25fd8-106">Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard or daylight saving time.</span></span> 
  
```xml
<Offset/>
```

 <span data-ttu-id="25fd8-107">**duration**</span><span class="sxs-lookup"><span data-stu-id="25fd8-107">**duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="25fd8-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="25fd8-108">Attributes and elements</span></span>

<span data-ttu-id="25fd8-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="25fd8-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25fd8-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="25fd8-110">Attributes</span></span>

<span data-ttu-id="25fd8-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="25fd8-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25fd8-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="25fd8-112">Child elements</span></span>

<span data-ttu-id="25fd8-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="25fd8-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="25fd8-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="25fd8-114">Parent elements</span></span>

|<span data-ttu-id="25fd8-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="25fd8-115">**Element**</span></span>|<span data-ttu-id="25fd8-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="25fd8-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25fd8-117">Horario de verano</span><span class="sxs-lookup"><span data-stu-id="25fd8-117">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="25fd8-118">Representa la fecha y hora cuando se cambia la hora del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="25fd8-118">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="25fd8-119">Standard</span><span class="sxs-lookup"><span data-stu-id="25fd8-119">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="25fd8-120">Representa la fecha y hora cuando se cambia la hora del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="25fd8-120">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="25fd8-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="25fd8-121">Text value</span></span>

<span data-ttu-id="25fd8-122">El valor de texto representa el desplazamiento de hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="25fd8-122">The text value represents the offset from Coordinated Universal Time (UTC).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="25fd8-123">Notas</span><span class="sxs-lookup"><span data-stu-id="25fd8-123">Remarks</span></span>

<span data-ttu-id="25fd8-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="25fd8-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="25fd8-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="25fd8-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25fd8-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="25fd8-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="25fd8-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="25fd8-127">Schema Name</span></span>  <br/> |<span data-ttu-id="25fd8-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="25fd8-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="25fd8-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="25fd8-129">Validation File</span></span>  <br/> |<span data-ttu-id="25fd8-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="25fd8-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="25fd8-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="25fd8-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="25fd8-132">False</span><span class="sxs-lookup"><span data-stu-id="25fd8-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="25fd8-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="25fd8-133">See also</span></span>



- [<span data-ttu-id="25fd8-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="25fd8-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

