---
title: Notificaciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Notifications
api_type:
- schema
ms.assetid: 153cc420-d2fe-42f1-afb2-9a31ee09a750
description: El elemento de notificaciones contiene una matriz de información acerca de la suscripción y los eventos que se han producido desde la última notificación.
ms.openlocfilehash: f576bf579c91b77dcde8646a6af7fdc47145aef7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836550"
---
# <a name="notifications"></a><span data-ttu-id="60a58-103">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="60a58-103">Notifications</span></span>

<span data-ttu-id="60a58-104">El elemento de **notificaciones** contiene una matriz de información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="60a58-104">The **Notifications** element contains an array of information about the subscription and the events that have occurred since the last notification.</span></span> 
  
```xml
<Notifications>
   <Notification/>
</Notifications>
```

 <span data-ttu-id="60a58-105">**NonEmptyArrayOfNotificationsType**</span><span class="sxs-lookup"><span data-stu-id="60a58-105">**NonEmptyArrayOfNotificationsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="60a58-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="60a58-106">Attributes and elements</span></span>

<span data-ttu-id="60a58-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="60a58-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60a58-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="60a58-108">Attributes</span></span>

<span data-ttu-id="60a58-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="60a58-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="60a58-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="60a58-110">Child elements</span></span>

|<span data-ttu-id="60a58-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="60a58-111">**Element**</span></span>|<span data-ttu-id="60a58-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="60a58-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60a58-113">Notificación</span><span class="sxs-lookup"><span data-stu-id="60a58-113">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="60a58-114">Contiene información acerca de la suscripción y los eventos que se han producido desde la última notificación.</span><span class="sxs-lookup"><span data-stu-id="60a58-114">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="60a58-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="60a58-115">Parent elements</span></span>

|<span data-ttu-id="60a58-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="60a58-116">**Element**</span></span>|<span data-ttu-id="60a58-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="60a58-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60a58-118">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="60a58-118">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md) <br/> |<span data-ttu-id="60a58-119">Contiene el estado y el resultado de una única solicitud de [operación GetStreamingEvents](getstreamingevents-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="60a58-119">Contains the status and result of a single [GetStreamingEvents operation](getstreamingevents-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="60a58-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="60a58-120">Text value</span></span>

<span data-ttu-id="60a58-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="60a58-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="60a58-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60a58-122">Remarks</span></span>

<span data-ttu-id="60a58-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="60a58-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="60a58-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="60a58-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60a58-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="60a58-125">Namespace</span></span>  <br/> |<span data-ttu-id="60a58-126">http://schemas.microsoft.com/exchange/services/2006/messages y http://schemas.microsoft.com/exchange/services/2006/types</span><span class="sxs-lookup"><span data-stu-id="60a58-126">http://schemas.microsoft.com/exchange/services/2006/messages and http://schemas.microsoft.com/exchange/services/2006/types</span></span>  <br/> |
|<span data-ttu-id="60a58-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="60a58-127">Schema Name</span></span>  <br/> |<span data-ttu-id="60a58-128">Esquema de los mensajes; Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="60a58-128">Messages schema; Types schema</span></span>  <br/> |
|<span data-ttu-id="60a58-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="60a58-129">Validation File</span></span>  <br/> |<span data-ttu-id="60a58-130">Messages.xsd; Types.xsd</span><span class="sxs-lookup"><span data-stu-id="60a58-130">Messages.xsd; Types.xsd</span></span>  <br/> |
|<span data-ttu-id="60a58-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="60a58-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="60a58-132">False</span><span class="sxs-lookup"><span data-stu-id="60a58-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="60a58-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="60a58-133">See also</span></span>



[<span data-ttu-id="60a58-134">Operación GetFolder</span><span class="sxs-lookup"><span data-stu-id="60a58-134">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="60a58-135">Operación DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="60a58-135">DeleteFolder operation</span></span>](deletefolder-operation.md)
  
[<span data-ttu-id="60a58-136">Operación MoveFolder</span><span class="sxs-lookup"><span data-stu-id="60a58-136">MoveFolder operation</span></span>](movefolder-operation.md)
  
[<span data-ttu-id="60a58-137">Operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="60a58-137">CopyFolder operation</span></span>](copyfolder-operation.md)
  
[<span data-ttu-id="60a58-138">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="60a58-138">Subscribe operation</span></span>](subscribe-operation.md)

