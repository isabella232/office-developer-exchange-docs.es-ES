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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468848"
---
# <a name="phonecallinformation"></a><span data-ttu-id="28b50-103">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="28b50-103">PhoneCallInformation</span></span>

<span data-ttu-id="28b50-104">El elemento **PhoneCallInformation** especifica la información de estado de una llamada de teléfono.</span><span class="sxs-lookup"><span data-stu-id="28b50-104">The **PhoneCallInformation** element specifies the state information for a phone call.</span></span> 
  
```XML
<PhoneCallInformation>
   <PhoneCallState/>
   <ConnectionFailureCause/>
   <SIPResponseText/>
   <SIPResponseCode/>
</PhoneCallInformation>
```

 <span data-ttu-id="28b50-105">**PhoneCallInformationType**</span><span class="sxs-lookup"><span data-stu-id="28b50-105">**PhoneCallInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28b50-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="28b50-106">Attributes and elements</span></span>

<span data-ttu-id="28b50-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="28b50-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28b50-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="28b50-108">Attributes</span></span>

<span data-ttu-id="28b50-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="28b50-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="28b50-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="28b50-110">Child elements</span></span>

|<span data-ttu-id="28b50-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="28b50-111">**Element**</span></span>|<span data-ttu-id="28b50-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28b50-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28b50-113">PhoneCallState</span><span class="sxs-lookup"><span data-stu-id="28b50-113">PhoneCallState</span></span>](phonecallstate.md) <br/> |<span data-ttu-id="28b50-114">Especifica el estado de una llamada de teléfono.</span><span class="sxs-lookup"><span data-stu-id="28b50-114">Specifies the state for a phone call.</span></span> <span data-ttu-id="28b50-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="28b50-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="28b50-116">ConnectionFailureCause</span><span class="sxs-lookup"><span data-stu-id="28b50-116">ConnectionFailureCause</span></span>](connectionfailurecause.md) <br/> |<span data-ttu-id="28b50-117">Especifica la causa de un error de conexión.</span><span class="sxs-lookup"><span data-stu-id="28b50-117">Specifies the cause of a connection failure.</span></span> <span data-ttu-id="28b50-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="28b50-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="28b50-119">SIPResponseText</span><span class="sxs-lookup"><span data-stu-id="28b50-119">SIPResponseText</span></span>](sipresponsetext.md) <br/> |<span data-ttu-id="28b50-120">Especifica el texto de respuesta SIP.</span><span class="sxs-lookup"><span data-stu-id="28b50-120">Specifies the SIP response text.</span></span> <span data-ttu-id="28b50-121">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="28b50-121">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="28b50-122">SIPResponseCode</span><span class="sxs-lookup"><span data-stu-id="28b50-122">SIPResponseCode</span></span>](sipresponsecode.md) <br/> |<span data-ttu-id="28b50-123">Especifica el código de respuesta SIP.</span><span class="sxs-lookup"><span data-stu-id="28b50-123">Specifies the SIP response code.</span></span> <span data-ttu-id="28b50-124">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="28b50-124">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="28b50-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="28b50-125">Parent elements</span></span>

|<span data-ttu-id="28b50-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="28b50-126">**Element**</span></span>|<span data-ttu-id="28b50-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28b50-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28b50-128">GetPhoneCallInformationResponse</span><span class="sxs-lookup"><span data-stu-id="28b50-128">GetPhoneCallInformationResponse</span></span>](getphonecallinformationresponse.md) <br/> |<span data-ttu-id="28b50-129">Define una respuesta a una solicitud de [operación de GetPhoneCallInformation](getphonecallinformation-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="28b50-129">Defines a response to a [GetPhoneCallInformation operation](getphonecallinformation-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28b50-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="28b50-130">Remarks</span></span>

<span data-ttu-id="28b50-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="28b50-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28b50-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="28b50-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28b50-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="28b50-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="28b50-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="28b50-134">Schema Name</span></span>  <br/> |<span data-ttu-id="28b50-135">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="28b50-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="28b50-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="28b50-136">Validation File</span></span>  <br/> |<span data-ttu-id="28b50-137">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="28b50-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="28b50-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="28b50-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="28b50-139">Falso</span><span class="sxs-lookup"><span data-stu-id="28b50-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28b50-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="28b50-140">See also</span></span>



- [<span data-ttu-id="28b50-141">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="28b50-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

