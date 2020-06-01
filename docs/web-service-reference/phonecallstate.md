---
title: PhoneCallState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhoneCallState
api_type:
- schema
ms.assetid: ac009eb3-6334-49ce-82be-48fe83577f9c
description: El elemento PhoneCallState especifica el estado actual de una llamada de teléfono.
ms.openlocfilehash: d2088b9b2811befe80684188d49c8034c577cc55
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468533"
---
# <a name="phonecallstate"></a><span data-ttu-id="84cf6-103">PhoneCallState</span><span class="sxs-lookup"><span data-stu-id="84cf6-103">PhoneCallState</span></span>

<span data-ttu-id="84cf6-104">El elemento **PhoneCallState** especifica el estado actual de una llamada de teléfono.</span><span class="sxs-lookup"><span data-stu-id="84cf6-104">The **PhoneCallState** element specifies the current state for a phone call.</span></span> 
  
```xml
<PhoneCallState>Idle or Connecting or Alerted or Connected or Disconnected or Incoming or Transferring or Forwarding</PhoneCallState>
```

 <span data-ttu-id="84cf6-105">**PhoneCallStateType**</span><span class="sxs-lookup"><span data-stu-id="84cf6-105">**PhoneCallStateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="84cf6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="84cf6-106">Attributes and elements</span></span>

<span data-ttu-id="84cf6-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="84cf6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84cf6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="84cf6-108">Attributes</span></span>

<span data-ttu-id="84cf6-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="84cf6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="84cf6-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="84cf6-110">Child elements</span></span>

<span data-ttu-id="84cf6-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="84cf6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="84cf6-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="84cf6-112">Parent elements</span></span>

|<span data-ttu-id="84cf6-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="84cf6-113">**Element**</span></span>|<span data-ttu-id="84cf6-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="84cf6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84cf6-115">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="84cf6-115">PhoneCallInformation</span></span>](phonecallinformation.md) <br/> |<span data-ttu-id="84cf6-116">Especifica la información de estado de una llamada telefónica.</span><span class="sxs-lookup"><span data-stu-id="84cf6-116">Specifies the state information for a phone call.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="84cf6-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="84cf6-117">Text value</span></span>

<span data-ttu-id="84cf6-118">En la siguiente tabla se enumeran los valores posibles para el elemento **PhoneCallState** .</span><span class="sxs-lookup"><span data-stu-id="84cf6-118">The following table lists the possible values for the **PhoneCallState** element.</span></span> 
  
<span data-ttu-id="84cf6-119">**Valores del elemento PhoneCallState**</span><span class="sxs-lookup"><span data-stu-id="84cf6-119">**PhoneCallState element values**</span></span>

|<span data-ttu-id="84cf6-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="84cf6-120">**Value**</span></span>|<span data-ttu-id="84cf6-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="84cf6-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="84cf6-122">Usado</span><span class="sxs-lookup"><span data-stu-id="84cf6-122">Idle</span></span>  <br/> |<span data-ttu-id="84cf6-123">Estado de la llamada inicial.</span><span class="sxs-lookup"><span data-stu-id="84cf6-123">Initial call state.</span></span>  <br/> |
|<span data-ttu-id="84cf6-124">Conectando</span><span class="sxs-lookup"><span data-stu-id="84cf6-124">Connecting</span></span>  <br/> |<span data-ttu-id="84cf6-125">El sistema está llamando a esta llamada.</span><span class="sxs-lookup"><span data-stu-id="84cf6-125">The system is dialing this call.</span></span>  <br/> |
|<span data-ttu-id="84cf6-126">Alertas</span><span class="sxs-lookup"><span data-stu-id="84cf6-126">Alerted</span></span>  <br/> |<span data-ttu-id="84cf6-127">La llamada está en estado de alerta (el teléfono está sonando).</span><span class="sxs-lookup"><span data-stu-id="84cf6-127">The call is in alerting state (phone is ringing).</span></span>  <br/> |
|<span data-ttu-id="84cf6-128">Conectado</span><span class="sxs-lookup"><span data-stu-id="84cf6-128">Connected</span></span>  <br/> |<span data-ttu-id="84cf6-129">La llamada está en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="84cf6-129">The call is in the connected state.</span></span>  <br/> |
|<span data-ttu-id="84cf6-130">Desconectado</span><span class="sxs-lookup"><span data-stu-id="84cf6-130">Disconnected</span></span>  <br/> |<span data-ttu-id="84cf6-131">La llamada está desconectada.</span><span class="sxs-lookup"><span data-stu-id="84cf6-131">The call is disconnected.</span></span>  <br/> |
|<span data-ttu-id="84cf6-132">Entra</span><span class="sxs-lookup"><span data-stu-id="84cf6-132">Incoming</span></span>  <br/> |<span data-ttu-id="84cf6-133">La llamada es entrante.</span><span class="sxs-lookup"><span data-stu-id="84cf6-133">The call is inbound.</span></span>  <br/> |
|<span data-ttu-id="84cf6-134">Transferencia</span><span class="sxs-lookup"><span data-stu-id="84cf6-134">Transferring</span></span>  <br/> |<span data-ttu-id="84cf6-135">La llamada se está transfiriendo a otro destino.</span><span class="sxs-lookup"><span data-stu-id="84cf6-135">The call is being transferred to another destination.</span></span>  <br/> |
|<span data-ttu-id="84cf6-136">Reenvío</span><span class="sxs-lookup"><span data-stu-id="84cf6-136">Forwarding</span></span>  <br/> |<span data-ttu-id="84cf6-137">La llamada se está reenviando a otro destino.</span><span class="sxs-lookup"><span data-stu-id="84cf6-137">The call is being forwarded to another destination.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84cf6-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="84cf6-138">Remarks</span></span>

<span data-ttu-id="84cf6-139">El esquema que describe este elemento se encuentra en el directorio/EWS/del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="84cf6-139">The schema that describes this element is located in the /ews/ directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="84cf6-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="84cf6-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84cf6-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="84cf6-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="84cf6-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="84cf6-142">Schema Name</span></span>  <br/> |<span data-ttu-id="84cf6-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="84cf6-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="84cf6-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="84cf6-144">Validation File</span></span>  <br/> |<span data-ttu-id="84cf6-145">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="84cf6-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="84cf6-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="84cf6-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="84cf6-147">Falso</span><span class="sxs-lookup"><span data-stu-id="84cf6-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84cf6-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="84cf6-148">See also</span></span>



- [<span data-ttu-id="84cf6-149">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="84cf6-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

