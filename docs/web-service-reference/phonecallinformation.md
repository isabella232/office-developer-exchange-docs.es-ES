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
description: El elemento PhoneCallInformation especifica la información de estado de una llamada de teléfono.
ms.openlocfilehash: 75370bccb841818a8302bdd055ad96fd16b2e8df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468848"
---
# <a name="phonecallinformation"></a><span data-ttu-id="9bd4d-103">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="9bd4d-103">PhoneCallInformation</span></span>

<span data-ttu-id="9bd4d-104">El elemento **PhoneCallInformation** especifica la información de estado de una llamada de teléfono.</span><span class="sxs-lookup"><span data-stu-id="9bd4d-104">The **PhoneCallInformation** element specifies the state information for a phone call.</span></span> 
  
```XML
<PhoneCallInformation>
   <PhoneCallState/>
   <ConnectionFailureCause/>
   <SIPResponseText/>
   <SIPResponseCode/>
</PhoneCallInformation>
```

 <span data-ttu-id="9bd4d-105">**PhoneCallInformationType**</span><span class="sxs-lookup"><span data-stu-id="9bd4d-105">**PhoneCallInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9bd4d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9bd4d-106">Attributes and elements</span></span>

<span data-ttu-id="9bd4d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9bd4d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9bd4d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9bd4d-108">Attributes</span></span>

<span data-ttu-id="9bd4d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9bd4d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9bd4d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9bd4d-110">Child elements</span></span>

|<span data-ttu-id="9bd4d-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9bd4d-111">**Element**</span></span>|<span data-ttu-id="9bd4d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9bd4d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9bd4d-113">PhoneCallState</span><span class="sxs-lookup"><span data-stu-id="9bd4d-113">PhoneCallState</span></span>](phonecallstate.md) <br/> |<span data-ttu-id="9bd4d-114">Especifica el estado de una llamada de teléfono.</span><span class="sxs-lookup"><span data-stu-id="9bd4d-114">Specifies the state for a phone call.</span></span> <span data-ttu-id="9bd4d-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="9bd4d-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="9bd4d-116">ConnectionFailureCause</span><span class="sxs-lookup"><span data-stu-id="9bd4d-116">ConnectionFailureCause</span></span>](connectionfailurecause.md) <br/> |<span data-ttu-id="9bd4d-117">Especifica la causa de un error de conexión.</span><span class="sxs-lookup"><span data-stu-id="9bd4d-117">Specifies the cause of a connection failure.</span></span> <span data-ttu-id="9bd4d-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="9bd4d-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="9bd4d-119">SIPResponseText</span><span class="sxs-lookup"><span data-stu-id="9bd4d-119">SIPResponseText</span></span>](sipresponsetext.md) <br/> |<span data-ttu-id="9bd4d-120">Especifica el texto de respuesta SIP.</span><span class="sxs-lookup"><span data-stu-id="9bd4d-120">Specifies the SIP response text.</span></span> <span data-ttu-id="9bd4d-121">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="9bd4d-121">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="9bd4d-122">SIPResponseCode</span><span class="sxs-lookup"><span data-stu-id="9bd4d-122">SIPResponseCode</span></span>](sipresponsecode.md) <br/> |<span data-ttu-id="9bd4d-123">Especifica el código de respuesta SIP.</span><span class="sxs-lookup"><span data-stu-id="9bd4d-123">Specifies the SIP response code.</span></span> <span data-ttu-id="9bd4d-124">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="9bd4d-124">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9bd4d-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9bd4d-125">Parent elements</span></span>

|<span data-ttu-id="9bd4d-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9bd4d-126">**Element**</span></span>|<span data-ttu-id="9bd4d-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9bd4d-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9bd4d-128">GetPhoneCallInformationResponse</span><span class="sxs-lookup"><span data-stu-id="9bd4d-128">GetPhoneCallInformationResponse</span></span>](getphonecallinformationresponse.md) <br/> |<span data-ttu-id="9bd4d-129">Define una respuesta a una solicitud de [operación de GetPhoneCallInformation](getphonecallinformation-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="9bd4d-129">Defines a response to a [GetPhoneCallInformation operation](getphonecallinformation-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9bd4d-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9bd4d-130">Remarks</span></span>

<span data-ttu-id="9bd4d-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9bd4d-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9bd4d-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9bd4d-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9bd4d-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="9bd4d-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9bd4d-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9bd4d-134">Schema Name</span></span>  <br/> |<span data-ttu-id="9bd4d-135">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="9bd4d-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9bd4d-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9bd4d-136">Validation File</span></span>  <br/> |<span data-ttu-id="9bd4d-137">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9bd4d-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9bd4d-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9bd4d-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="9bd4d-139">Falso</span><span class="sxs-lookup"><span data-stu-id="9bd4d-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9bd4d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bd4d-140">See also</span></span>



- [<span data-ttu-id="9bd4d-141">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="9bd4d-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

