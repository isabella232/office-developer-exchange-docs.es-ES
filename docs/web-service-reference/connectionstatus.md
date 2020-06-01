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
description: El elemento ConnectionStatus proporciona una descripción textual del estado de una suscripción de transmisión por secuencias.
ms.openlocfilehash: 928537201041950011ae06444e3c412228d252ea
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462720"
---
# <a name="connectionstatus"></a><span data-ttu-id="b727a-103">ConnectionStatus</span><span class="sxs-lookup"><span data-stu-id="b727a-103">ConnectionStatus</span></span>

<span data-ttu-id="b727a-104">El elemento **ConnectionStatus** proporciona una descripción textual del estado de una suscripción de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="b727a-104">The **ConnectionStatus** element provides a text description of the status of a streaming subscription.</span></span> 
  
```xml
<ConnectionStatus>OK or Closed</ConnectionStatus>
```

 <span data-ttu-id="b727a-105">**ConnectionStatusType**</span><span class="sxs-lookup"><span data-stu-id="b727a-105">**ConnectionStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b727a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b727a-106">Attributes and elements</span></span>

<span data-ttu-id="b727a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b727a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b727a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b727a-108">Attributes</span></span>

<span data-ttu-id="b727a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b727a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b727a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b727a-110">Child elements</span></span>

<span data-ttu-id="b727a-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b727a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b727a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b727a-112">Parent elements</span></span>

|<span data-ttu-id="b727a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b727a-113">**Element**</span></span>|<span data-ttu-id="b727a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b727a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b727a-115">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b727a-115">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="b727a-116">Contiene el estado y el resultado de una sola solicitud de [operación GetStreamingEvents](getstreamingevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="b727a-116">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b727a-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b727a-117">Text value</span></span>

<span data-ttu-id="b727a-118">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="b727a-118">A text value is required.</span></span> <span data-ttu-id="b727a-119">A continuación se muestran los valores de texto posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="b727a-119">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="b727a-120">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b727a-120">OK</span></span>
    
- <span data-ttu-id="b727a-121">Closed</span><span class="sxs-lookup"><span data-stu-id="b727a-121">Closed</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b727a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b727a-122">Remarks</span></span>

<span data-ttu-id="b727a-123">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b727a-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b727a-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b727a-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b727a-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="b727a-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b727a-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b727a-126">Schema Name</span></span>  <br/> |<span data-ttu-id="b727a-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b727a-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b727a-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b727a-128">Validation File</span></span>  <br/> |<span data-ttu-id="b727a-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b727a-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b727a-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b727a-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="b727a-131">Falso</span><span class="sxs-lookup"><span data-stu-id="b727a-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b727a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b727a-132">See also</span></span>



[<span data-ttu-id="b727a-133">Operación GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="b727a-133">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)


- [<span data-ttu-id="b727a-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b727a-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

