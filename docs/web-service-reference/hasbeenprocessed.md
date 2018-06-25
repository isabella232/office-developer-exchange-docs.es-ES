---
title: HasBeenProcessed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HasBeenProcessed
api_type:
- schema
ms.assetid: 46d4af8e-0f11-4a74-9365-1d983731fed8
description: El elemento HasBeenProcessed indica si un mensaje de reunión item se han procesado.
ms.openlocfilehash: cccd3b2258490fcbe902bcd391f25b0be2fe7c26
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835796"
---
# <a name="hasbeenprocessed"></a><span data-ttu-id="e8d71-103">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="e8d71-103">HasBeenProcessed</span></span>

<span data-ttu-id="e8d71-104">El elemento **HasBeenProcessed** indica si un mensaje de reunión item se han procesado.</span><span class="sxs-lookup"><span data-stu-id="e8d71-104">The **HasBeenProcessed** element indicates whether a meeting message item has been processed.</span></span> 
  
```xml
<HasBeenProcessed/>
```

 <span data-ttu-id="e8d71-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e8d71-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e8d71-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e8d71-106">Attributes and elements</span></span>

<span data-ttu-id="e8d71-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e8d71-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8d71-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e8d71-108">Attributes</span></span>

<span data-ttu-id="e8d71-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e8d71-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e8d71-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e8d71-110">Child elements</span></span>

<span data-ttu-id="e8d71-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e8d71-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e8d71-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e8d71-112">Parent elements</span></span>

|<span data-ttu-id="e8d71-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e8d71-113">**Element**</span></span>|<span data-ttu-id="e8d71-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8d71-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8d71-115">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="e8d71-115">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="e8d71-116">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e8d71-116">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e8d71-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="e8d71-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="e8d71-118">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e8d71-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e8d71-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e8d71-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="e8d71-120">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e8d71-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e8d71-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="e8d71-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="e8d71-122">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e8d71-122">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e8d71-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e8d71-123">Text value</span></span>

<span data-ttu-id="e8d71-124">Un valor de texto de **true** indica que se ha procesado el mensaje de la reunión.</span><span class="sxs-lookup"><span data-stu-id="e8d71-124">A text value of **true** indicates that the meeting message has been processed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e8d71-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8d71-125">Remarks</span></span>

<span data-ttu-id="e8d71-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="e8d71-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8d71-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e8d71-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8d71-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e8d71-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e8d71-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e8d71-129">Schema Name</span></span>  <br/> |<span data-ttu-id="e8d71-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e8d71-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="e8d71-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e8d71-131">Validation File</span></span>  <br/> |<span data-ttu-id="e8d71-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e8d71-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e8d71-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e8d71-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="e8d71-134">False</span><span class="sxs-lookup"><span data-stu-id="e8d71-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8d71-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8d71-135">See also</span></span>



- [<span data-ttu-id="e8d71-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e8d71-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

