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
description: El elemento NewMailEvent representa un evento desencadenado por un nuevo elemento de correo en un buzón.
ms.openlocfilehash: aa562b60a7299543af8653bbc767edf329075644
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466818"
---
# <a name="newmailevent"></a><span data-ttu-id="ac845-103">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="ac845-103">NewMailEvent</span></span>

<span data-ttu-id="ac845-104">El elemento **NewMailEvent** representa un evento desencadenado por un nuevo elemento de correo en un buzón.</span><span class="sxs-lookup"><span data-stu-id="ac845-104">The **NewMailEvent** element represents an event that is triggered by a new mail item in a mailbox.</span></span> 
  
```xml
<NewMailEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</NewMailEvent>
```

 <span data-ttu-id="ac845-105">**BaseObjectChangedEventType**</span><span class="sxs-lookup"><span data-stu-id="ac845-105">**BaseObjectChangedEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ac845-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ac845-106">Attributes and elements</span></span>

<span data-ttu-id="ac845-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ac845-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac845-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ac845-108">Attributes</span></span>

<span data-ttu-id="ac845-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ac845-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ac845-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ac845-110">Child elements</span></span>

|<span data-ttu-id="ac845-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ac845-111">**Element**</span></span>|<span data-ttu-id="ac845-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ac845-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac845-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="ac845-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="ac845-114">Representa un marcador de evento en la tabla de eventos del buzón.</span><span class="sxs-lookup"><span data-stu-id="ac845-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="ac845-115">Marca</span><span class="sxs-lookup"><span data-stu-id="ac845-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="ac845-116">Representa la marca de hora de la llegada de un nuevo elemento de correo en un buzón.</span><span class="sxs-lookup"><span data-stu-id="ac845-116">Represents the timestamp of the arrival of a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="ac845-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="ac845-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="ac845-118">Representa el identificador de un nuevo elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="ac845-118">Represents the identifier of a new mail item.</span></span>  <br/> |
|[<span data-ttu-id="ac845-119">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="ac845-119">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="ac845-120">Representa el identificador de la carpeta principal del nuevo elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="ac845-120">Represents the identifier of the parent folder of the new mail item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ac845-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ac845-121">Parent elements</span></span>

|<span data-ttu-id="ac845-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ac845-122">**Element**</span></span>|<span data-ttu-id="ac845-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ac845-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac845-124">Notificación</span><span class="sxs-lookup"><span data-stu-id="ac845-124">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ac845-125">Contiene información sobre la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="ac845-125">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac845-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ac845-126">Remarks</span></span>

<span data-ttu-id="ac845-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ac845-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac845-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ac845-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac845-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac845-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ac845-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ac845-130">Schema name</span></span>  <br/> |<span data-ttu-id="ac845-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ac845-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="ac845-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ac845-132">Validation file</span></span>  <br/> |<span data-ttu-id="ac845-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ac845-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ac845-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ac845-134">Can be empty</span></span>  <br/> |<span data-ttu-id="ac845-135">Falso</span><span class="sxs-lookup"><span data-stu-id="ac845-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac845-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac845-136">See also</span></span>



[<span data-ttu-id="ac845-137">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="ac845-137">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="ac845-138">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="ac845-138">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="ac845-139">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="ac845-139">Unsubscribe operation</span></span>](unsubscribe-operation.md)

