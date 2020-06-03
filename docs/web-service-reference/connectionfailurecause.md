---
title: ConnectionFailureCause
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectionFailureCause
api_type:
- schema
ms.assetid: d2160c8a-015c-4964-b7f7-93478764a173
description: El elemento ConnectionFailureCause especifica el motivo por el que se ha desconectado una llamada telefónica.
ms.openlocfilehash: 6385641eaee140a114906703232974d51d5ce344
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529451"
---
# <a name="connectionfailurecause"></a><span data-ttu-id="7c420-103">ConnectionFailureCause</span><span class="sxs-lookup"><span data-stu-id="7c420-103">ConnectionFailureCause</span></span>

<span data-ttu-id="7c420-104">El elemento **ConnectionFailureCause** especifica el motivo por el que se ha desconectado una llamada telefónica.</span><span class="sxs-lookup"><span data-stu-id="7c420-104">The **ConnectionFailureCause** element specifies the reason for a disconnection from a telephone call.</span></span> 
  
```xml
<ConnectionFailureCause>None or UserBusy or NoAnswer or Unavailable or Other</ConnectionFailureCause>
```

 <span data-ttu-id="7c420-105">**ConnectionFailureCauseType**</span><span class="sxs-lookup"><span data-stu-id="7c420-105">**ConnectionFailureCauseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7c420-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7c420-106">Attributes and elements</span></span>

<span data-ttu-id="7c420-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7c420-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7c420-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7c420-108">Attributes</span></span>

<span data-ttu-id="7c420-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7c420-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7c420-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7c420-110">Child elements</span></span>

<span data-ttu-id="7c420-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7c420-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7c420-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7c420-112">Parent elements</span></span>

|<span data-ttu-id="7c420-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7c420-113">**Element**</span></span>|<span data-ttu-id="7c420-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7c420-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7c420-115">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="7c420-115">PhoneCallInformation</span></span>](phonecallinformation.md) <br/> |<span data-ttu-id="7c420-116">Especifica la información de estado de una llamada telefónica.</span><span class="sxs-lookup"><span data-stu-id="7c420-116">Specifies the state information for a telephone call.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7c420-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7c420-117">Text value</span></span>

<span data-ttu-id="7c420-118">En la siguiente tabla se enumeran los valores posibles para el elemento **ConnectionFailureCause** .</span><span class="sxs-lookup"><span data-stu-id="7c420-118">The following table lists the possible values for the **ConnectionFailureCause** element.</span></span> 
  
<span data-ttu-id="7c420-119">**Valores del elemento ConnectionFailureCause**</span><span class="sxs-lookup"><span data-stu-id="7c420-119">**ConnectionFailureCause element values**</span></span>

|<span data-ttu-id="7c420-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7c420-120">**Value**</span></span>|<span data-ttu-id="7c420-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7c420-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7c420-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7c420-122">None</span></span>  <br/> |<span data-ttu-id="7c420-123">El estado de la llamada no se desconecta o no se conoce el motivo de la desconexión.</span><span class="sxs-lookup"><span data-stu-id="7c420-123">Call state is not disconnected or the disconnect reason is not known.</span></span>  <br/> |
|<span data-ttu-id="7c420-124">UserBusy</span><span class="sxs-lookup"><span data-stu-id="7c420-124">UserBusy</span></span>  <br/> |<span data-ttu-id="7c420-125">La línea de parte llamada estaba ocupada.</span><span class="sxs-lookup"><span data-stu-id="7c420-125">The called party line was busy.</span></span>  <br/> |
|<span data-ttu-id="7c420-126">Noanswer</span><span class="sxs-lookup"><span data-stu-id="7c420-126">NoAnswer</span></span>  <br/> |<span data-ttu-id="7c420-127">La parte llamada no responde.</span><span class="sxs-lookup"><span data-stu-id="7c420-127">The called party did not answer.</span></span>  <br/> |
|<span data-ttu-id="7c420-128">Momentos</span><span class="sxs-lookup"><span data-stu-id="7c420-128">Unavailable</span></span>  <br/> |<span data-ttu-id="7c420-129">El número de la parte llamada no estaba disponible.</span><span class="sxs-lookup"><span data-stu-id="7c420-129">The called party number was not available.</span></span>  <br/> |
|<span data-ttu-id="7c420-130">Otros</span><span class="sxs-lookup"><span data-stu-id="7c420-130">Other</span></span>  <br/> |<span data-ttu-id="7c420-131">Comodín para otros motivos de desconexión.</span><span class="sxs-lookup"><span data-stu-id="7c420-131">Catch-all for other disconnect reasons.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c420-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7c420-132">Remarks</span></span>

<span data-ttu-id="7c420-133">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7c420-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7c420-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7c420-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c420-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="7c420-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7c420-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7c420-136">Schema Name</span></span>  <br/> |<span data-ttu-id="7c420-137">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7c420-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="7c420-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7c420-138">Validation File</span></span>  <br/> |<span data-ttu-id="7c420-139">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="7c420-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7c420-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7c420-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="7c420-141">Falso</span><span class="sxs-lookup"><span data-stu-id="7c420-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7c420-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c420-142">See also</span></span>



- [<span data-ttu-id="7c420-143">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7c420-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

