---
title: ConnectionStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectionStatus
api_type:
- schema
ms.assetid: 4300f9d6-8bf9-48c2-9f07-d80197864e17
description: El elemento ConnectionStatus proporciona una descripción de texto del estado de una suscripción de transmisión por secuencias.
ms.openlocfilehash: 567308d79eaccba24230deddf5d78a724b8746af
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763776"
---
# <a name="connectionstatus"></a><span data-ttu-id="89729-103">ConnectionStatus</span><span class="sxs-lookup"><span data-stu-id="89729-103">ConnectionStatus</span></span>

<span data-ttu-id="89729-104">El elemento **ConnectionStatus** proporciona una descripción de texto del estado de una suscripción de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="89729-104">The **ConnectionStatus** element provides a text description of the status of a streaming subscription.</span></span> 
  
```xml
<ConnectionStatus>OK or Closed</ConnectionStatus>
```

 <span data-ttu-id="89729-105">**ConnectionStatusType**</span><span class="sxs-lookup"><span data-stu-id="89729-105">**ConnectionStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="89729-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="89729-106">Attributes and elements</span></span>

<span data-ttu-id="89729-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="89729-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89729-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="89729-108">Attributes</span></span>

<span data-ttu-id="89729-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="89729-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="89729-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="89729-110">Child elements</span></span>

<span data-ttu-id="89729-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="89729-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="89729-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="89729-112">Parent elements</span></span>

|<span data-ttu-id="89729-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="89729-113">**Element**</span></span>|<span data-ttu-id="89729-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="89729-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89729-115">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="89729-115">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="89729-116">Contiene el estado y el resultado de una única solicitud de [operación GetStreamingEvents](getstreamingevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="89729-116">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="89729-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="89729-117">Text value</span></span>

<span data-ttu-id="89729-118">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="89729-118">A text value is required.</span></span> <span data-ttu-id="89729-119">Los siguientes son los posibles valores de texto para este elemento:</span><span class="sxs-lookup"><span data-stu-id="89729-119">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="89729-120">Aceptar</span><span class="sxs-lookup"><span data-stu-id="89729-120">OK</span></span>
    
- <span data-ttu-id="89729-121">Cerrado</span><span class="sxs-lookup"><span data-stu-id="89729-121">Closed</span></span>
    
## <a name="remarks"></a><span data-ttu-id="89729-122">Notas</span><span class="sxs-lookup"><span data-stu-id="89729-122">Remarks</span></span>

<span data-ttu-id="89729-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="89729-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89729-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="89729-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89729-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="89729-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="89729-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="89729-126">Schema Name</span></span>  <br/> |<span data-ttu-id="89729-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="89729-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="89729-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="89729-128">Validation File</span></span>  <br/> |<span data-ttu-id="89729-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="89729-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="89729-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="89729-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="89729-131">False</span><span class="sxs-lookup"><span data-stu-id="89729-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89729-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="89729-132">See also</span></span>



[<span data-ttu-id="89729-133">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="89729-133">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="89729-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="89729-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

