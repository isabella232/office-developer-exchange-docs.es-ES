---
title: PhoneCallId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhoneCallId
api_type:
- schema
ms.assetid: 79e31a4c-fc84-4802-8761-470df8d63694
description: El elemento PhoneCallId especifica el identificador de una llamada telefónica. Se requiere este elemento.
ms.openlocfilehash: 1886d9510fe254c016779166efccc9882fd77d2c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836757"
---
# <a name="phonecallid"></a><span data-ttu-id="3df13-104">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="3df13-104">PhoneCallId</span></span>

<span data-ttu-id="3df13-105">El elemento **PhoneCallId** especifica el identificador de una llamada telefónica.</span><span class="sxs-lookup"><span data-stu-id="3df13-105">The **PhoneCallId** element specifies the identifier of a phone call.</span></span> <span data-ttu-id="3df13-106">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="3df13-106">This element is required.</span></span> 
  
```xml
<PhoneCallId Id="" />
```

 <span data-ttu-id="3df13-107">**PhoneCallIdType**</span><span class="sxs-lookup"><span data-stu-id="3df13-107">**PhoneCallIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3df13-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3df13-108">Attributes and elements</span></span>

<span data-ttu-id="3df13-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3df13-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3df13-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="3df13-110">Attributes</span></span>

|<span data-ttu-id="3df13-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="3df13-111">**Attribute**</span></span>|<span data-ttu-id="3df13-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3df13-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3df13-113">Id</span><span class="sxs-lookup"><span data-stu-id="3df13-113">Id</span></span>  <br/> |<span data-ttu-id="3df13-114">Identifica la llamada de teléfono a desconectar.</span><span class="sxs-lookup"><span data-stu-id="3df13-114">Identifies the phone call to disconnect.</span></span> <span data-ttu-id="3df13-115">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="3df13-115">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3df13-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3df13-116">Child elements</span></span>

<span data-ttu-id="3df13-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3df13-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3df13-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3df13-118">Parent elements</span></span>

|<span data-ttu-id="3df13-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="3df13-119">**Element**</span></span>|<span data-ttu-id="3df13-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3df13-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3df13-121">DisconnectPhoneCall</span><span class="sxs-lookup"><span data-stu-id="3df13-121">DisconnectPhoneCall</span></span>](disconnectphonecall.md) <br/> |<span data-ttu-id="3df13-122">Representa una solicitud para desconectar la llamada.</span><span class="sxs-lookup"><span data-stu-id="3df13-122">Represents a request to disconnect a call.</span></span>  <br/> |
|[<span data-ttu-id="3df13-123">GetPhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="3df13-123">GetPhoneCallInformation</span></span>](getphonecallinformation.md) <br/> |<span data-ttu-id="3df13-124">Representa una solicitud para obtener información de la llamada de teléfono.</span><span class="sxs-lookup"><span data-stu-id="3df13-124">Represents a request to get telephone call information.</span></span>  <br/> |
|[<span data-ttu-id="3df13-125">PlayOnPhoneResponse (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="3df13-125">PlayOnPhoneResponse (Exchange Web Services)</span></span>](playonphoneresponse-exchange-web-services.md) <br/> |<span data-ttu-id="3df13-126">Define una respuesta a una solicitud de PlayOnPhone.</span><span class="sxs-lookup"><span data-stu-id="3df13-126">Defines a response to a PlayOnPhone request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3df13-127">Notas</span><span class="sxs-lookup"><span data-stu-id="3df13-127">Remarks</span></span>

<span data-ttu-id="3df13-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3df13-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3df13-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3df13-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3df13-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3df13-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3df13-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3df13-131">Schema Name</span></span>  <br/> |<span data-ttu-id="3df13-132">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3df13-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3df13-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3df13-133">Validation File</span></span>  <br/> |<span data-ttu-id="3df13-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3df13-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3df13-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3df13-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="3df13-136">False</span><span class="sxs-lookup"><span data-stu-id="3df13-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3df13-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="3df13-137">See also</span></span>



- [<span data-ttu-id="3df13-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3df13-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

