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
description: El elemento PhoneCallState especifica el estado actual de una llamada telefónica.
ms.openlocfilehash: 184a7400810711442e565d1ef37094bd63b00914
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836761"
---
# <a name="phonecallstate"></a><span data-ttu-id="3a56f-103">PhoneCallState</span><span class="sxs-lookup"><span data-stu-id="3a56f-103">PhoneCallState</span></span>

<span data-ttu-id="3a56f-104">El elemento **PhoneCallState** especifica el estado actual de una llamada telefónica.</span><span class="sxs-lookup"><span data-stu-id="3a56f-104">The **PhoneCallState** element specifies the current state for a phone call.</span></span> 
  
```xml
<PhoneCallState>Idle or Connecting or Alerted or Connected or Disconnected or Incoming or Transferring or Forwarding</PhoneCallState>
```

 <span data-ttu-id="3a56f-105">**PhoneCallStateType**</span><span class="sxs-lookup"><span data-stu-id="3a56f-105">**PhoneCallStateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3a56f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3a56f-106">Attributes and elements</span></span>

<span data-ttu-id="3a56f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3a56f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a56f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3a56f-108">Attributes</span></span>

<span data-ttu-id="3a56f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3a56f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a56f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3a56f-110">Child elements</span></span>

<span data-ttu-id="3a56f-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3a56f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3a56f-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3a56f-112">Parent elements</span></span>

|<span data-ttu-id="3a56f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a56f-113">**Element**</span></span>|<span data-ttu-id="3a56f-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a56f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a56f-115">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="3a56f-115">PhoneCallInformation</span></span>](phonecallinformation.md) <br/> |<span data-ttu-id="3a56f-116">Especifica la información de estado para una llamada de teléfono.</span><span class="sxs-lookup"><span data-stu-id="3a56f-116">Specifies the state information for a phone call.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3a56f-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3a56f-117">Text value</span></span>

<span data-ttu-id="3a56f-118">En la siguiente tabla se enumera los valores posibles para el elemento **PhoneCallState** .</span><span class="sxs-lookup"><span data-stu-id="3a56f-118">The following table lists the possible values for the **PhoneCallState** element.</span></span> 
  
<span data-ttu-id="3a56f-119">**Valores de elemento PhoneCallState**</span><span class="sxs-lookup"><span data-stu-id="3a56f-119">**PhoneCallState element values**</span></span>

|<span data-ttu-id="3a56f-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3a56f-120">**Value**</span></span>|<span data-ttu-id="3a56f-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a56f-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3a56f-122">Inactividad</span><span class="sxs-lookup"><span data-stu-id="3a56f-122">Idle</span></span>  <br/> |<span data-ttu-id="3a56f-123">Estado de llamada inicial.</span><span class="sxs-lookup"><span data-stu-id="3a56f-123">Initial call state.</span></span>  <br/> |
|<span data-ttu-id="3a56f-124">Conectando</span><span class="sxs-lookup"><span data-stu-id="3a56f-124">Connecting</span></span>  <br/> |<span data-ttu-id="3a56f-125">El sistema está marcando esta llamada.</span><span class="sxs-lookup"><span data-stu-id="3a56f-125">The system is dialing this call.</span></span>  <br/> |
|<span data-ttu-id="3a56f-126">Una alerta</span><span class="sxs-lookup"><span data-stu-id="3a56f-126">Alerted</span></span>  <br/> |<span data-ttu-id="3a56f-127">La llamada está en estado de alerta (teléfono está sonando).</span><span class="sxs-lookup"><span data-stu-id="3a56f-127">The call is in alerting state (phone is ringing).</span></span>  <br/> |
|<span data-ttu-id="3a56f-128">Conectado</span><span class="sxs-lookup"><span data-stu-id="3a56f-128">Connected</span></span>  <br/> |<span data-ttu-id="3a56f-129">La llamada se encuentra en el estado de la conexión.</span><span class="sxs-lookup"><span data-stu-id="3a56f-129">The call is in the connected state.</span></span>  <br/> |
|<span data-ttu-id="3a56f-130">Desconectado</span><span class="sxs-lookup"><span data-stu-id="3a56f-130">Disconnected</span></span>  <br/> |<span data-ttu-id="3a56f-131">Se desconectó la llamada.</span><span class="sxs-lookup"><span data-stu-id="3a56f-131">The call is disconnected.</span></span>  <br/> |
|<span data-ttu-id="3a56f-132">Entrante</span><span class="sxs-lookup"><span data-stu-id="3a56f-132">Incoming</span></span>  <br/> |<span data-ttu-id="3a56f-133">La llamada es entrante.</span><span class="sxs-lookup"><span data-stu-id="3a56f-133">The call is inbound.</span></span>  <br/> |
|<span data-ttu-id="3a56f-134">Transferir</span><span class="sxs-lookup"><span data-stu-id="3a56f-134">Transferring</span></span>  <br/> |<span data-ttu-id="3a56f-135">La llamada se transfiere a otro destino.</span><span class="sxs-lookup"><span data-stu-id="3a56f-135">The call is being transferred to another destination.</span></span>  <br/> |
|<span data-ttu-id="3a56f-136">Desvío de llamadas</span><span class="sxs-lookup"><span data-stu-id="3a56f-136">Forwarding</span></span>  <br/> |<span data-ttu-id="3a56f-137">La llamada es se reenvíen a otro destino.</span><span class="sxs-lookup"><span data-stu-id="3a56f-137">The call is being forwarded to another destination.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a56f-138">Notas</span><span class="sxs-lookup"><span data-stu-id="3a56f-138">Remarks</span></span>

<span data-ttu-id="3a56f-139">El esquema que describe este elemento se encuentra en el directorio /ews/ del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3a56f-139">The schema that describes this element is located in the /ews/ directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a56f-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3a56f-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a56f-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3a56f-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3a56f-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3a56f-142">Schema Name</span></span>  <br/> |<span data-ttu-id="3a56f-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3a56f-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="3a56f-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3a56f-144">Validation File</span></span>  <br/> |<span data-ttu-id="3a56f-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3a56f-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3a56f-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3a56f-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="3a56f-147">False</span><span class="sxs-lookup"><span data-stu-id="3a56f-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a56f-148">Ver también</span><span class="sxs-lookup"><span data-stu-id="3a56f-148">See also</span></span>



- [<span data-ttu-id="3a56f-149">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3a56f-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

