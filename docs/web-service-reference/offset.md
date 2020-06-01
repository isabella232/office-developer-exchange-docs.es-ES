---
title: Offset
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
description: El elemento offset describe el desplazamiento desde BaseOffset. Junto con el elemento BaseOffset, el elemento offset identifica si la hora es estándar o de horario de verano.
ms.openlocfilehash: 74ad87026c2cb89f3b0c35218c91f81380029963
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459759"
---
# <a name="offset"></a><span data-ttu-id="3d207-104">Offset</span><span class="sxs-lookup"><span data-stu-id="3d207-104">Offset</span></span>

<span data-ttu-id="3d207-105">El elemento **offset** describe el desplazamiento desde [BaseOffset](baseoffset.md).</span><span class="sxs-lookup"><span data-stu-id="3d207-105">The **Offset** element describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="3d207-106">Junto con el elemento **BaseOffset** , el elemento **offset** identifica si la hora es estándar o de horario de verano.</span><span class="sxs-lookup"><span data-stu-id="3d207-106">Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard or daylight saving time.</span></span> 
  
```xml
<Offset/>
```

 <span data-ttu-id="3d207-107">**duration**</span><span class="sxs-lookup"><span data-stu-id="3d207-107">**duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3d207-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3d207-108">Attributes and elements</span></span>

<span data-ttu-id="3d207-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3d207-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3d207-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="3d207-110">Attributes</span></span>

<span data-ttu-id="3d207-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3d207-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3d207-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3d207-112">Child elements</span></span>

<span data-ttu-id="3d207-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3d207-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3d207-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3d207-114">Parent elements</span></span>

|<span data-ttu-id="3d207-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3d207-115">**Element**</span></span>|<span data-ttu-id="3d207-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3d207-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3d207-117">Horario</span><span class="sxs-lookup"><span data-stu-id="3d207-117">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="3d207-118">Representa la fecha y la hora en que cambia el horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="3d207-118">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="3d207-119">Estándar</span><span class="sxs-lookup"><span data-stu-id="3d207-119">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="3d207-120">Representa la fecha y la hora en que cambia el horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="3d207-120">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3d207-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3d207-121">Text value</span></span>

<span data-ttu-id="3d207-122">El valor de texto representa el desplazamiento de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="3d207-122">The text value represents the offset from Coordinated Universal Time (UTC).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3d207-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3d207-123">Remarks</span></span>

<span data-ttu-id="3d207-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="3d207-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3d207-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3d207-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3d207-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="3d207-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3d207-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3d207-127">Schema Name</span></span>  <br/> |<span data-ttu-id="3d207-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3d207-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="3d207-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3d207-129">Validation File</span></span>  <br/> |<span data-ttu-id="3d207-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="3d207-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3d207-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3d207-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="3d207-132">Falso</span><span class="sxs-lookup"><span data-stu-id="3d207-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3d207-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d207-133">See also</span></span>



- [<span data-ttu-id="3d207-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3d207-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

