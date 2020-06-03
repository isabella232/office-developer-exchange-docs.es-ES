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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459759"
---
# <a name="offset"></a><span data-ttu-id="d0c70-104">Offset</span><span class="sxs-lookup"><span data-stu-id="d0c70-104">Offset</span></span>

<span data-ttu-id="d0c70-105">El elemento **offset** describe el desplazamiento desde [BaseOffset](baseoffset.md).</span><span class="sxs-lookup"><span data-stu-id="d0c70-105">The **Offset** element describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="d0c70-106">Junto con el elemento **BaseOffset** , el elemento **offset** identifica si la hora es estándar o de horario de verano.</span><span class="sxs-lookup"><span data-stu-id="d0c70-106">Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard or daylight saving time.</span></span> 
  
```xml
<Offset/>
```

 <span data-ttu-id="d0c70-107">**duration**</span><span class="sxs-lookup"><span data-stu-id="d0c70-107">**duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0c70-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d0c70-108">Attributes and elements</span></span>

<span data-ttu-id="d0c70-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d0c70-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0c70-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="d0c70-110">Attributes</span></span>

<span data-ttu-id="d0c70-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d0c70-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0c70-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d0c70-112">Child elements</span></span>

<span data-ttu-id="d0c70-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d0c70-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d0c70-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d0c70-114">Parent elements</span></span>

|<span data-ttu-id="d0c70-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d0c70-115">**Element**</span></span>|<span data-ttu-id="d0c70-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0c70-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0c70-117">Horario</span><span class="sxs-lookup"><span data-stu-id="d0c70-117">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="d0c70-118">Representa la fecha y la hora en que cambia el horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="d0c70-118">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="d0c70-119">Estándar</span><span class="sxs-lookup"><span data-stu-id="d0c70-119">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="d0c70-120">Representa la fecha y la hora en que cambia el horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="d0c70-120">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d0c70-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d0c70-121">Text value</span></span>

<span data-ttu-id="d0c70-122">El valor de texto representa el desplazamiento de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="d0c70-122">The text value represents the offset from Coordinated Universal Time (UTC).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d0c70-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d0c70-123">Remarks</span></span>

<span data-ttu-id="d0c70-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="d0c70-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0c70-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d0c70-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0c70-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0c70-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d0c70-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d0c70-127">Schema Name</span></span>  <br/> |<span data-ttu-id="d0c70-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d0c70-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="d0c70-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d0c70-129">Validation File</span></span>  <br/> |<span data-ttu-id="d0c70-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d0c70-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d0c70-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d0c70-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="d0c70-132">Falso</span><span class="sxs-lookup"><span data-stu-id="d0c70-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0c70-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0c70-133">See also</span></span>



- [<span data-ttu-id="d0c70-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d0c70-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

