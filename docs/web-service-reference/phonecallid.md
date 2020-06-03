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
description: El elemento PhoneCallId especifica el identificador de una llamada de teléfono. Se requiere este elemento.
ms.openlocfilehash: 3e4b9dba5e8be6e45a0c16508531fbc6cf91c170
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459703"
---
# <a name="phonecallid"></a><span data-ttu-id="8fae7-104">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="8fae7-104">PhoneCallId</span></span>

<span data-ttu-id="8fae7-105">El elemento **PhoneCallId** especifica el identificador de una llamada de teléfono.</span><span class="sxs-lookup"><span data-stu-id="8fae7-105">The **PhoneCallId** element specifies the identifier of a phone call.</span></span> <span data-ttu-id="8fae7-106">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="8fae7-106">This element is required.</span></span> 
  
```xml
<PhoneCallId Id="" />
```

 <span data-ttu-id="8fae7-107">**PhoneCallIdType**</span><span class="sxs-lookup"><span data-stu-id="8fae7-107">**PhoneCallIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8fae7-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8fae7-108">Attributes and elements</span></span>

<span data-ttu-id="8fae7-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8fae7-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8fae7-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="8fae7-110">Attributes</span></span>

|<span data-ttu-id="8fae7-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="8fae7-111">**Attribute**</span></span>|<span data-ttu-id="8fae7-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8fae7-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8fae7-113">Id</span><span class="sxs-lookup"><span data-stu-id="8fae7-113">Id</span></span>  <br/> |<span data-ttu-id="8fae7-114">Identifica la llamada telefónica que se va a desconectar.</span><span class="sxs-lookup"><span data-stu-id="8fae7-114">Identifies the phone call to disconnect.</span></span> <span data-ttu-id="8fae7-115">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8fae7-115">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8fae7-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8fae7-116">Child elements</span></span>

<span data-ttu-id="8fae7-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8fae7-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8fae7-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8fae7-118">Parent elements</span></span>

|<span data-ttu-id="8fae7-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8fae7-119">**Element**</span></span>|<span data-ttu-id="8fae7-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8fae7-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8fae7-121">DisconnectPhoneCall</span><span class="sxs-lookup"><span data-stu-id="8fae7-121">DisconnectPhoneCall</span></span>](disconnectphonecall.md) <br/> |<span data-ttu-id="8fae7-122">Representa una solicitud para desconectar una llamada.</span><span class="sxs-lookup"><span data-stu-id="8fae7-122">Represents a request to disconnect a call.</span></span>  <br/> |
|[<span data-ttu-id="8fae7-123">GetPhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="8fae7-123">GetPhoneCallInformation</span></span>](getphonecallinformation.md) <br/> |<span data-ttu-id="8fae7-124">Representa una solicitud para obtener información sobre llamadas telefónicas.</span><span class="sxs-lookup"><span data-stu-id="8fae7-124">Represents a request to get telephone call information.</span></span>  <br/> |
|[<span data-ttu-id="8fae7-125">PlayOnPhoneResponse (servicios web Exchange)</span><span class="sxs-lookup"><span data-stu-id="8fae7-125">PlayOnPhoneResponse (Exchange Web Services)</span></span>](playonphoneresponse-exchange-web-services.md) <br/> |<span data-ttu-id="8fae7-126">Define una respuesta a una solicitud reproducir.</span><span class="sxs-lookup"><span data-stu-id="8fae7-126">Defines a response to a PlayOnPhone request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8fae7-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8fae7-127">Remarks</span></span>

<span data-ttu-id="8fae7-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="8fae7-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8fae7-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8fae7-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8fae7-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="8fae7-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8fae7-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8fae7-131">Schema Name</span></span>  <br/> |<span data-ttu-id="8fae7-132">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="8fae7-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8fae7-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8fae7-133">Validation File</span></span>  <br/> |<span data-ttu-id="8fae7-134">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="8fae7-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8fae7-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8fae7-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="8fae7-136">Falso</span><span class="sxs-lookup"><span data-stu-id="8fae7-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8fae7-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fae7-137">See also</span></span>



- [<span data-ttu-id="8fae7-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8fae7-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

