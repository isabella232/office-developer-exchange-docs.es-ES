---
title: GetUMPropertiesResponse (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetUMPropertiesResponse
api_type:
- schema
ms.assetid: fcd93ce5-7403-46a9-b46e-56d2ebdd2f79
description: El elemento GetUMPropertiesResponse define una respuesta a una solicitud de GetUMProperties operación (servicio web de mensajería unificada).
ms.openlocfilehash: c0df872ad6b8e6541fa750ab87f4c1e5f0118b00
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835685"
---
# <a name="getumpropertiesresponse-um-web-service"></a><span data-ttu-id="7d68a-103">GetUMPropertiesResponse (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="7d68a-103">GetUMPropertiesResponse (UM web service)</span></span>

<span data-ttu-id="7d68a-104">El elemento **GetUMPropertiesResponse** define una respuesta a una solicitud de [operación GetUMProperties (servicio web de mensajería unificada)](getumproperties-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="7d68a-104">The **GetUMPropertiesResponse** element defines a response to a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="7d68a-105">GetUMPropertiesResponse (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="7d68a-105">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
  <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 <span data-ttu-id="7d68a-106">**UMProperties**</span><span class="sxs-lookup"><span data-stu-id="7d68a-106">**UMProperties**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7d68a-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7d68a-107">Attributes and elements</span></span>

<span data-ttu-id="7d68a-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7d68a-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7d68a-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="7d68a-109">Attributes</span></span>

<span data-ttu-id="7d68a-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7d68a-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7d68a-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7d68a-111">Child elements</span></span>

|<span data-ttu-id="7d68a-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="7d68a-112">**Element**</span></span>|<span data-ttu-id="7d68a-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7d68a-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7d68a-114">MissedCallNotificationEnabled (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="7d68a-114">MissedCallNotificationEnabled (UM web service)</span></span>](missedcallnotificationenabled-um-web-service.md) <br/> |<span data-ttu-id="7d68a-115">Indica si están habilitadas las notificaciones de llamadas perdidas.</span><span class="sxs-lookup"><span data-stu-id="7d68a-115">Indicates whether missed call notifications are enabled.</span></span>  <br/> |
|[<span data-ttu-id="7d68a-116">PlayOnPhoneDialString (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="7d68a-116">PlayOnPhoneDialString (UM web service)</span></span>](playonphonedialstring-um-web-service.md) <br/> |<span data-ttu-id="7d68a-117">Contiene la cadena de marcado predeterminado que se usará para la [operación de PlayOnPhone (servicio web de mensajería unificada)](playonphone-operation-um-web-service.md) y el [funcionamiento de PlayOnPhoneGreeting (servicio web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="7d68a-117">Contains the default dial string to use for the [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md).</span></span>  <br/> |
|[<span data-ttu-id="7d68a-118">TelephoneAccessNumbers (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="7d68a-118">TelephoneAccessNumbers (UM web service)</span></span>](telephoneaccessnumbers-um-web-service.md) <br/> |<span data-ttu-id="7d68a-119">Contiene la lista de números de teléfono que el usuario puede utilizar para tener acceso a mensajería unificada a través de un teléfono.</span><span class="sxs-lookup"><span data-stu-id="7d68a-119">Contains the list of telephone numbers the user can use to access Unified Messaging via a telephone.</span></span>  <br/> |
|[<span data-ttu-id="7d68a-120">TelephoneAccessFolderEmail (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="7d68a-120">TelephoneAccessFolderEmail (UM web service)</span></span>](telephoneaccessfolderemail-um-web-service.md) <br/> |<span data-ttu-id="7d68a-121">Contiene el identificador de la carpeta de correo electrónico desde la que mensajería unificada va a leer los mensajes a través del teléfono.</span><span class="sxs-lookup"><span data-stu-id="7d68a-121">Contains the identifier for the e-mail folder from which Unified Messaging will read messages over the telephone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7d68a-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7d68a-122">Parent elements</span></span>

<span data-ttu-id="7d68a-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7d68a-123">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="7d68a-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7d68a-124">Text value</span></span>

<span data-ttu-id="7d68a-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7d68a-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7d68a-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7d68a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d68a-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7d68a-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7d68a-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7d68a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="7d68a-129">Mensajes</span><span class="sxs-lookup"><span data-stu-id="7d68a-129">Messages</span></span>  <br/> |
|<span data-ttu-id="7d68a-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7d68a-130">Validation File</span></span>  <br/> |<span data-ttu-id="7d68a-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7d68a-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7d68a-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7d68a-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="7d68a-133">False</span><span class="sxs-lookup"><span data-stu-id="7d68a-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d68a-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="7d68a-134">See also</span></span>



[<span data-ttu-id="7d68a-135">Operación GetUMProperties (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="7d68a-135">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)

