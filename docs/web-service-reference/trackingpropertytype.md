---
title: TrackingPropertyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TrackingPropertyType
api_type:
- schema
ms.assetid: 1d0f219b-1063-4eaa-9d3b-da384a544f89
description: El elemento TrackingPropertyType representa un par de nombre y valor de cadenas que se usa para crear propiedades para los informes de seguimiento de mensajes.
ms.openlocfilehash: 7812b52dd57fed0a9b6f1a8fc4e77660932a60dc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468085"
---
# <a name="trackingpropertytype"></a><span data-ttu-id="26ace-103">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="26ace-103">TrackingPropertyType</span></span>

<span data-ttu-id="26ace-104">El elemento **TrackingPropertyType** representa un par de nombre y valor de cadenas que se usa para crear propiedades para los informes de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="26ace-104">The **TrackingPropertyType** element represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span> 
  
[<span data-ttu-id="26ace-105">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="26ace-105">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md)
  
[<span data-ttu-id="26ace-106">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="26ace-106">TrackingPropertyType</span></span>](trackingpropertytype.md)
  
```xml
<TrackingPropertyType>
   <Name/>
   <Value/>
</TrackingPropertyType>
```

 <span data-ttu-id="26ace-107">**TrackingPropertyType**</span><span class="sxs-lookup"><span data-stu-id="26ace-107">**TrackingPropertyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="26ace-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="26ace-108">Attributes and elements</span></span>

<span data-ttu-id="26ace-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="26ace-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26ace-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="26ace-110">Attributes</span></span>

<span data-ttu-id="26ace-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="26ace-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26ace-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="26ace-112">Child elements</span></span>

|<span data-ttu-id="26ace-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="26ace-113">**Element**</span></span>|<span data-ttu-id="26ace-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26ace-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26ace-115">Nombre (seguimiento de mensajes)</span><span class="sxs-lookup"><span data-stu-id="26ace-115">Name (Message Tracking)</span></span>](name-message-tracking.md) <br/> |<span data-ttu-id="26ace-116">Define un nombre para la propiedad del informe de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="26ace-116">Defines a name for the message tracking report property.</span></span>  <br/> |
|[<span data-ttu-id="26ace-117">Valor (seguimiento de mensajes)</span><span class="sxs-lookup"><span data-stu-id="26ace-117">Value (Message Tracking)</span></span>](value-message-tracking.md) <br/> |<span data-ttu-id="26ace-118">Define un valor para la propiedad del informe de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="26ace-118">Defines a value for the message tracking report property.</span></span> <span data-ttu-id="26ace-119">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="26ace-119">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="26ace-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="26ace-120">Parent elements</span></span>

|<span data-ttu-id="26ace-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="26ace-121">**Element**</span></span>|<span data-ttu-id="26ace-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26ace-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26ace-123">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="26ace-123">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="26ace-124">Contiene una lista de una o varias propiedades de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="26ace-124">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="26ace-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="26ace-125">Text value</span></span>

<span data-ttu-id="26ace-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="26ace-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="26ace-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26ace-127">Remarks</span></span>

<span data-ttu-id="26ace-128">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="26ace-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26ace-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="26ace-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26ace-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="26ace-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="26ace-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="26ace-131">Schema Name</span></span>  <br/> |<span data-ttu-id="26ace-132">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="26ace-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="26ace-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="26ace-133">Validation File</span></span>  <br/> |<span data-ttu-id="26ace-134">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="26ace-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="26ace-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="26ace-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="26ace-136">Falso</span><span class="sxs-lookup"><span data-stu-id="26ace-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26ace-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="26ace-137">See also</span></span>



- [<span data-ttu-id="26ace-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="26ace-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

