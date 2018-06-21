---
title: IsDelegated
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsDelegated
api_type:
- schema
ms.assetid: c12907db-be80-4924-9469-8e58612cf42c
description: El elemento IsDelegated indica si una reunión se ha controlado por una cuenta que tenga acceso delegado.
ms.openlocfilehash: a6f42a57b2d0fdb760e4c36d3211ba57289a3c7c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19836005"
---
# <a name="isdelegated"></a><span data-ttu-id="a9a10-103">IsDelegated</span><span class="sxs-lookup"><span data-stu-id="a9a10-103">IsDelegated</span></span>

<span data-ttu-id="a9a10-104">El elemento **IsDelegated** indica si una reunión se ha controlado por una cuenta que tenga acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="a9a10-104">The **IsDelegated** element indicates whether a meeting was handled by an account that has delegate access.</span></span> 
  
```xml
<IsDelegated/>
```

 <span data-ttu-id="a9a10-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a9a10-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a9a10-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a9a10-106">Attributes and elements</span></span>

<span data-ttu-id="a9a10-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a9a10-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a9a10-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a9a10-108">Attributes</span></span>

<span data-ttu-id="a9a10-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a9a10-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a9a10-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a9a10-110">Child elements</span></span>

<span data-ttu-id="a9a10-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a9a10-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a9a10-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a9a10-112">Parent elements</span></span>

|<span data-ttu-id="a9a10-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9a10-113">**Element**</span></span>|<span data-ttu-id="a9a10-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9a10-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9a10-115">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="a9a10-115">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="a9a10-116">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a9a10-116">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a9a10-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="a9a10-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="a9a10-118">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a9a10-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a9a10-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="a9a10-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="a9a10-120">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a9a10-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a9a10-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="a9a10-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="a9a10-122">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a9a10-122">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a9a10-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a9a10-123">Text value</span></span>

<span data-ttu-id="a9a10-124">Un valor de texto de **true** indica que la reunión se ha controlado por una cuenta que tenga acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="a9a10-124">A text value of **true** indicates that the meeting was handled by an account that has delegate access.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a9a10-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a9a10-125">Remarks</span></span>

<span data-ttu-id="a9a10-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a9a10-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a9a10-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a9a10-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9a10-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a9a10-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a9a10-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a9a10-129">Schema Name</span></span>  <br/> |<span data-ttu-id="a9a10-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a9a10-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="a9a10-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a9a10-131">Validation File</span></span>  <br/> |<span data-ttu-id="a9a10-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a9a10-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a9a10-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a9a10-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="a9a10-134">False</span><span class="sxs-lookup"><span data-stu-id="a9a10-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9a10-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9a10-135">See also</span></span>



- [<span data-ttu-id="a9a10-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a9a10-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

