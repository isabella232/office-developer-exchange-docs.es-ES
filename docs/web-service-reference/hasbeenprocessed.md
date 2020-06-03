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
description: El elemento HasBeenProcessed indica si se ha procesado un elemento de mensaje de reunión.
ms.openlocfilehash: 7251ca86e07a0b72c186c65094b6469331dfd12e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462896"
---
# <a name="hasbeenprocessed"></a><span data-ttu-id="15ee0-103">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="15ee0-103">HasBeenProcessed</span></span>

<span data-ttu-id="15ee0-104">El elemento **HasBeenProcessed** indica si se ha procesado un elemento de mensaje de reunión.</span><span class="sxs-lookup"><span data-stu-id="15ee0-104">The **HasBeenProcessed** element indicates whether a meeting message item has been processed.</span></span> 
  
```xml
<HasBeenProcessed/>
```

 <span data-ttu-id="15ee0-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="15ee0-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15ee0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="15ee0-106">Attributes and elements</span></span>

<span data-ttu-id="15ee0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="15ee0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15ee0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="15ee0-108">Attributes</span></span>

<span data-ttu-id="15ee0-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="15ee0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="15ee0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="15ee0-110">Child elements</span></span>

<span data-ttu-id="15ee0-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="15ee0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="15ee0-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="15ee0-112">Parent elements</span></span>

|<span data-ttu-id="15ee0-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="15ee0-113">**Element**</span></span>|<span data-ttu-id="15ee0-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="15ee0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15ee0-115">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="15ee0-115">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="15ee0-116">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="15ee0-116">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15ee0-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="15ee0-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="15ee0-118">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="15ee0-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15ee0-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="15ee0-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="15ee0-120">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="15ee0-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15ee0-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="15ee0-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="15ee0-122">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="15ee0-122">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="15ee0-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="15ee0-123">Text value</span></span>

<span data-ttu-id="15ee0-124">Un valor de texto de **true** indica que el mensaje de reunión se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="15ee0-124">A text value of **true** indicates that the meeting message has been processed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="15ee0-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="15ee0-125">Remarks</span></span>

<span data-ttu-id="15ee0-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="15ee0-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15ee0-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="15ee0-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15ee0-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="15ee0-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="15ee0-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="15ee0-129">Schema Name</span></span>  <br/> |<span data-ttu-id="15ee0-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="15ee0-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="15ee0-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="15ee0-131">Validation File</span></span>  <br/> |<span data-ttu-id="15ee0-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="15ee0-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="15ee0-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="15ee0-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="15ee0-134">Falso</span><span class="sxs-lookup"><span data-stu-id="15ee0-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15ee0-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="15ee0-135">See also</span></span>



- [<span data-ttu-id="15ee0-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="15ee0-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

