---
title: NewMailEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NewMailEvent
api_type:
- schema
ms.assetid: 45057945-a3ec-4dac-92db-f0dc5fcfc34d
description: El elemento NewMailEvent representa un evento que se desencadena por un nuevo elemento de correo en un buzón de correo.
ms.openlocfilehash: 8df3e4a218a8eaa9d129854e4816a3a43beddafa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836527"
---
# <a name="newmailevent"></a><span data-ttu-id="8688a-103">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="8688a-103">NewMailEvent</span></span>

<span data-ttu-id="8688a-104">El elemento **NewMailEvent** representa un evento que se desencadena por un nuevo elemento de correo en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="8688a-104">The **NewMailEvent** element represents an event that is triggered by a new mail item in a mailbox.</span></span> 
  
```xml
<NewMailEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</NewMailEvent>
```

 <span data-ttu-id="8688a-105">**BaseObjectChangedEventType**</span><span class="sxs-lookup"><span data-stu-id="8688a-105">**BaseObjectChangedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8688a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8688a-106">Attributes and elements</span></span>

<span data-ttu-id="8688a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8688a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8688a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8688a-108">Attributes</span></span>

<span data-ttu-id="8688a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8688a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8688a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8688a-110">Child elements</span></span>

|<span data-ttu-id="8688a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8688a-111">**Element**</span></span>|<span data-ttu-id="8688a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8688a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8688a-113">Marca de agua</span><span class="sxs-lookup"><span data-stu-id="8688a-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="8688a-114">Representa un marcador de evento en la tabla de eventos de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="8688a-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="8688a-115">Marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="8688a-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="8688a-116">Representa la marca de tiempo de la llegada de un nuevo elemento de correo en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="8688a-116">Represents the timestamp of the arrival of a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="8688a-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="8688a-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="8688a-118">Representa el identificador de un nuevo elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="8688a-118">Represents the identifier of a new mail item.</span></span>  <br/> |
|[<span data-ttu-id="8688a-119">Id</span><span class="sxs-lookup"><span data-stu-id="8688a-119">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="8688a-120">Representa el identificador de la carpeta principal del nuevo elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="8688a-120">Represents the identifier of the parent folder of the new mail item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8688a-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8688a-121">Parent elements</span></span>

|<span data-ttu-id="8688a-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="8688a-122">**Element**</span></span>|<span data-ttu-id="8688a-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8688a-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8688a-124">Notificación</span><span class="sxs-lookup"><span data-stu-id="8688a-124">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8688a-125">Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="8688a-125">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8688a-126">Notas</span><span class="sxs-lookup"><span data-stu-id="8688a-126">Remarks</span></span>

<span data-ttu-id="8688a-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="8688a-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8688a-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8688a-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8688a-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8688a-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8688a-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8688a-130">Schema name</span></span>  <br/> |<span data-ttu-id="8688a-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8688a-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="8688a-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8688a-132">Validation file</span></span>  <br/> |<span data-ttu-id="8688a-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8688a-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8688a-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8688a-134">Can be empty</span></span>  <br/> |<span data-ttu-id="8688a-135">False</span><span class="sxs-lookup"><span data-stu-id="8688a-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8688a-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="8688a-136">See also</span></span>



[<span data-ttu-id="8688a-137">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="8688a-137">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="8688a-138">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="8688a-138">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="8688a-139">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="8688a-139">Unsubscribe operation</span></span>](unsubscribe-operation.md)

