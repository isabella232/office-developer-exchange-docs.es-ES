---
title: PhoneCallInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhoneCallInformation
api_type:
- schema
ms.assetid: a0363c42-6d35-4074-bc17-946eb12736ff
description: El elemento PhoneCallInformation especifica la información de estado para una llamada de teléfono.
ms.openlocfilehash: e64e7b38b3801c60df8a966e95d980746533d3a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836758"
---
# <a name="phonecallinformation"></a><span data-ttu-id="34603-103">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="34603-103">PhoneCallInformation</span></span>

<span data-ttu-id="34603-104">El elemento **PhoneCallInformation** especifica la información de estado para una llamada de teléfono.</span><span class="sxs-lookup"><span data-stu-id="34603-104">The **PhoneCallInformation** element specifies the state information for a phone call.</span></span> 
  
```XML
<PhoneCallInformation>
   <PhoneCallState/>
   <ConnectionFailureCause/>
   <SIPResponseText/>
   <SIPResponseCode/>
</PhoneCallInformation>
```

 <span data-ttu-id="34603-105">**PhoneCallInformationType**</span><span class="sxs-lookup"><span data-stu-id="34603-105">**PhoneCallInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="34603-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="34603-106">Attributes and elements</span></span>

<span data-ttu-id="34603-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="34603-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="34603-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="34603-108">Attributes</span></span>

<span data-ttu-id="34603-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="34603-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="34603-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="34603-110">Child elements</span></span>

|<span data-ttu-id="34603-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="34603-111">**Element**</span></span>|<span data-ttu-id="34603-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="34603-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="34603-113">PhoneCallState</span><span class="sxs-lookup"><span data-stu-id="34603-113">PhoneCallState</span></span>](phonecallstate.md) <br/> |<span data-ttu-id="34603-114">Especifica el estado de una llamada telefónica.</span><span class="sxs-lookup"><span data-stu-id="34603-114">Specifies the state for a phone call.</span></span> <span data-ttu-id="34603-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="34603-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="34603-116">ConnectionFailureCause</span><span class="sxs-lookup"><span data-stu-id="34603-116">ConnectionFailureCause</span></span>](connectionfailurecause.md) <br/> |<span data-ttu-id="34603-117">Especifica la causa de un error de conexión.</span><span class="sxs-lookup"><span data-stu-id="34603-117">Specifies the cause of a connection failure.</span></span> <span data-ttu-id="34603-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="34603-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="34603-119">SIPResponseText</span><span class="sxs-lookup"><span data-stu-id="34603-119">SIPResponseText</span></span>](sipresponsetext.md) <br/> |<span data-ttu-id="34603-120">Especifica el texto de respuesta SIP.</span><span class="sxs-lookup"><span data-stu-id="34603-120">Specifies the SIP response text.</span></span> <span data-ttu-id="34603-121">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="34603-121">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="34603-122">SIPResponseCode</span><span class="sxs-lookup"><span data-stu-id="34603-122">SIPResponseCode</span></span>](sipresponsecode.md) <br/> |<span data-ttu-id="34603-123">Especifica el código de respuesta SIP.</span><span class="sxs-lookup"><span data-stu-id="34603-123">Specifies the SIP response code.</span></span> <span data-ttu-id="34603-124">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="34603-124">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="34603-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="34603-125">Parent elements</span></span>

|<span data-ttu-id="34603-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="34603-126">**Element**</span></span>|<span data-ttu-id="34603-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="34603-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="34603-128">GetPhoneCallInformationResponse</span><span class="sxs-lookup"><span data-stu-id="34603-128">GetPhoneCallInformationResponse</span></span>](getphonecallinformationresponse.md) <br/> |<span data-ttu-id="34603-129">Define una respuesta a una solicitud de [operación GetPhoneCallInformation](getphonecallinformation-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="34603-129">Defines a response to a [GetPhoneCallInformation operation](getphonecallinformation-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34603-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="34603-130">Remarks</span></span>

<span data-ttu-id="34603-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="34603-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="34603-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="34603-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34603-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="34603-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="34603-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="34603-134">Schema Name</span></span>  <br/> |<span data-ttu-id="34603-135">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="34603-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="34603-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="34603-136">Validation File</span></span>  <br/> |<span data-ttu-id="34603-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="34603-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="34603-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="34603-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="34603-139">False</span><span class="sxs-lookup"><span data-stu-id="34603-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="34603-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="34603-140">See also</span></span>



- [<span data-ttu-id="34603-141">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="34603-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

