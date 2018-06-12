---
title: SendNotification
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendNotification
api_type:
- schema
ms.assetid: e45c4451-a286-4aec-a691-119ec41c58e0
description: El elemento SendNotification contiene las notificaciones de inserción que se envían por el equipo que ejecuta Microsoft Exchange Server 2007 a la aplicación cliente.
ms.openlocfilehash: 2288dbb5cf97b57a64b3c645eb72836342f4c178
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837345"
---
# <a name="sendnotification"></a><span data-ttu-id="6dbea-103">SendNotification</span><span class="sxs-lookup"><span data-stu-id="6dbea-103">SendNotification</span></span>

<span data-ttu-id="6dbea-104">El elemento **SendNotification** contiene las notificaciones de inserción que se envían por el equipo que ejecuta Microsoft Exchange Server 2007 a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="6dbea-104">The **SendNotification** element contains the push notifications that are sent by the computer that is running Microsoft Exchange Server 2007 to the client application.</span></span> 
  
```xml
<SendNotification>
   <ResponseMessages/>
</SendNotification>
```

 <span data-ttu-id="6dbea-105">**SendNotificationResponseType**</span><span class="sxs-lookup"><span data-stu-id="6dbea-105">**SendNotificationResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6dbea-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6dbea-106">Attributes and elements</span></span>

<span data-ttu-id="6dbea-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6dbea-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6dbea-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6dbea-108">Attributes</span></span>

<span data-ttu-id="6dbea-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6dbea-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6dbea-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6dbea-110">Child elements</span></span>

|<span data-ttu-id="6dbea-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6dbea-111">**Element**</span></span>|<span data-ttu-id="6dbea-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6dbea-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6dbea-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6dbea-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="6dbea-114">Contiene las notificaciones de inserción que se envían por el servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="6dbea-114">Contains the push notifications that are sent by the Client Access server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6dbea-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6dbea-115">Parent elements</span></span>

<span data-ttu-id="6dbea-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6dbea-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6dbea-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6dbea-117">Remarks</span></span>

<span data-ttu-id="6dbea-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="6dbea-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6dbea-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6dbea-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6dbea-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6dbea-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6dbea-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6dbea-121">Schema Name</span></span>  <br/> |<span data-ttu-id="6dbea-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6dbea-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6dbea-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6dbea-123">Validation File</span></span>  <br/> |<span data-ttu-id="6dbea-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6dbea-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6dbea-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6dbea-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="6dbea-126">False</span><span class="sxs-lookup"><span data-stu-id="6dbea-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6dbea-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="6dbea-127">See also</span></span>



- [<span data-ttu-id="6dbea-128">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="6dbea-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="6dbea-129">Notificaciones de eventos en EWS</span><span class="sxs-lookup"><span data-stu-id="6dbea-129">Event notifications in EWS</span></span>](http://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)
  
[<span data-ttu-id="6dbea-130">Aplicación de ejemplo de notificación de inserción</span><span class="sxs-lookup"><span data-stu-id="6dbea-130">Push Notification Sample Application</span></span>](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

