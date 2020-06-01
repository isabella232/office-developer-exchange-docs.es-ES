---
title: IsOutOfDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsOutOfDate
api_type:
- schema
ms.assetid: 2b6005a6-56a9-4848-b998-32908c13e2e2
description: El elemento IsOutOfDate indica si un mensaje de reunión, una solicitud, una respuesta o una cancelación están desactualizados.
ms.openlocfilehash: b50b021e48789ba63016582450404b5da3ff86e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466552"
---
# <a name="isoutofdate"></a><span data-ttu-id="65719-103">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="65719-103">IsOutOfDate</span></span>

<span data-ttu-id="65719-104">El elemento **IsOutOfDate** indica si un mensaje de reunión, una solicitud, una respuesta o una cancelación están desactualizados.</span><span class="sxs-lookup"><span data-stu-id="65719-104">The **IsOutOfDate** element indicates whether a meeting message, request, response, or cancellation is out-of-date.</span></span> 
  
```xml
<IsOutOfDate/>
```

 <span data-ttu-id="65719-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="65719-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="65719-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="65719-106">Attributes and elements</span></span>

<span data-ttu-id="65719-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="65719-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65719-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="65719-108">Attributes</span></span>

<span data-ttu-id="65719-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="65719-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="65719-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="65719-110">Child elements</span></span>

<span data-ttu-id="65719-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="65719-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="65719-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="65719-112">Parent elements</span></span>

|<span data-ttu-id="65719-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="65719-113">**Element**</span></span>|<span data-ttu-id="65719-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65719-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65719-115">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="65719-115">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="65719-116">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="65719-116">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="65719-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="65719-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="65719-118">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="65719-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="65719-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="65719-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="65719-120">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="65719-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="65719-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="65719-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="65719-122">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="65719-122">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="65719-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="65719-123">Text value</span></span>

<span data-ttu-id="65719-124">Un valor de texto de **true** indica que el elemento de reunión no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="65719-124">A text value of **true** indicates that the meeting item is out-of-date.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="65719-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="65719-125">Remarks</span></span>

<span data-ttu-id="65719-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="65719-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65719-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="65719-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65719-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="65719-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="65719-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="65719-129">Schema Name</span></span>  <br/> |<span data-ttu-id="65719-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="65719-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="65719-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="65719-131">Validation File</span></span>  <br/> |<span data-ttu-id="65719-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="65719-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="65719-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="65719-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="65719-134">Falso</span><span class="sxs-lookup"><span data-stu-id="65719-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65719-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="65719-135">See also</span></span>



- [<span data-ttu-id="65719-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="65719-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

