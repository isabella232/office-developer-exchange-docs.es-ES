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
description: El elemento SendNotification contiene las notificaciones de inserción que envía el equipo que ejecuta Microsoft Exchange Server 2007 a la aplicación cliente.
ms.openlocfilehash: 49f2f6cb7f5c8e1171b54ff965ee1d22accc9bf2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462118"
---
# <a name="sendnotification"></a><span data-ttu-id="2333c-103">SendNotification</span><span class="sxs-lookup"><span data-stu-id="2333c-103">SendNotification</span></span>

<span data-ttu-id="2333c-104">El elemento **SendNotification** contiene las notificaciones de inserción que envía el equipo que ejecuta Microsoft Exchange Server 2007 a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="2333c-104">The **SendNotification** element contains the push notifications that are sent by the computer that is running Microsoft Exchange Server 2007 to the client application.</span></span> 
  
```xml
<SendNotification>
   <ResponseMessages/>
</SendNotification>
```

 <span data-ttu-id="2333c-105">**SendNotificationResponseType**</span><span class="sxs-lookup"><span data-stu-id="2333c-105">**SendNotificationResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2333c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2333c-106">Attributes and elements</span></span>

<span data-ttu-id="2333c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2333c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2333c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2333c-108">Attributes</span></span>

<span data-ttu-id="2333c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2333c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2333c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2333c-110">Child elements</span></span>

|<span data-ttu-id="2333c-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2333c-111">**Element**</span></span>|<span data-ttu-id="2333c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2333c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2333c-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2333c-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="2333c-114">Contiene las notificaciones de inserción enviadas por el servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="2333c-114">Contains the push notifications that are sent by the Client Access server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2333c-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2333c-115">Parent elements</span></span>

<span data-ttu-id="2333c-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2333c-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2333c-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2333c-117">Remarks</span></span>

<span data-ttu-id="2333c-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="2333c-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2333c-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2333c-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2333c-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="2333c-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2333c-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2333c-121">Schema Name</span></span>  <br/> |<span data-ttu-id="2333c-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2333c-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2333c-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2333c-123">Validation File</span></span>  <br/> |<span data-ttu-id="2333c-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2333c-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2333c-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2333c-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="2333c-126">Falso</span><span class="sxs-lookup"><span data-stu-id="2333c-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2333c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2333c-127">See also</span></span>



- [<span data-ttu-id="2333c-128">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2333c-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="2333c-129">Notificaciones de eventos en EWS</span><span class="sxs-lookup"><span data-stu-id="2333c-129">Event notifications in EWS</span></span>](https://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)
  
[<span data-ttu-id="2333c-130">Aplicación de ejemplo de notificación de inserción</span><span class="sxs-lookup"><span data-stu-id="2333c-130">Push Notification Sample Application</span></span>](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

