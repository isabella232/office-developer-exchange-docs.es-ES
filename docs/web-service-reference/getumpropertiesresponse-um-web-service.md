---
title: GetUMPropertiesResponse (servicio Web de mensajería unificada)
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
description: El elemento GetUMPropertiesResponse define una respuesta a una solicitud de GetUMProperties (servicio Web de mensajería unificada).
ms.openlocfilehash: 3247489a305c694c10764d7a0c6f02b1fad51ebf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459128"
---
# <a name="getumpropertiesresponse-um-web-service"></a><span data-ttu-id="a09e7-103">GetUMPropertiesResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a09e7-103">GetUMPropertiesResponse (UM web service)</span></span>

<span data-ttu-id="a09e7-104">El elemento **GetUMPropertiesResponse** define una respuesta a una solicitud de [GetUMProperties (servicio Web de mensajería unificada)](getumproperties-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="a09e7-104">The **GetUMPropertiesResponse** element defines a response to a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="a09e7-105">GetUMPropertiesResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a09e7-105">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
  <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 <span data-ttu-id="a09e7-106">**UMProperties**</span><span class="sxs-lookup"><span data-stu-id="a09e7-106">**UMProperties**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a09e7-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a09e7-107">Attributes and elements</span></span>

<span data-ttu-id="a09e7-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a09e7-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a09e7-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="a09e7-109">Attributes</span></span>

<span data-ttu-id="a09e7-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a09e7-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a09e7-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a09e7-111">Child elements</span></span>

|<span data-ttu-id="a09e7-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a09e7-112">**Element**</span></span>|<span data-ttu-id="a09e7-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a09e7-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a09e7-114">MissedCallNotificationEnabled (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a09e7-114">MissedCallNotificationEnabled (UM web service)</span></span>](missedcallnotificationenabled-um-web-service.md) <br/> |<span data-ttu-id="a09e7-115">Indica si las notificaciones de llamadas perdidas están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="a09e7-115">Indicates whether missed call notifications are enabled.</span></span>  <br/> |
|[<span data-ttu-id="a09e7-116">PlayOnPhoneDialString (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a09e7-116">PlayOnPhoneDialString (UM web service)</span></span>](playonphonedialstring-um-web-service.md) <br/> |<span data-ttu-id="a09e7-117">Contiene la cadena de marcado predeterminada que se debe usar para la [operación reproducir (servicio Web de mensajería unificada)](playonphone-operation-um-web-service.md) y la [operación PlayOnPhoneGreeting (servicio Web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="a09e7-117">Contains the default dial string to use for the [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md).</span></span>  <br/> |
|[<span data-ttu-id="a09e7-118">TelephoneAccessNumbers (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a09e7-118">TelephoneAccessNumbers (UM web service)</span></span>](telephoneaccessnumbers-um-web-service.md) <br/> |<span data-ttu-id="a09e7-119">Contiene la lista de números de teléfono que el usuario puede usar para tener acceso a la mensajería unificada a través de un teléfono.</span><span class="sxs-lookup"><span data-stu-id="a09e7-119">Contains the list of telephone numbers the user can use to access Unified Messaging via a telephone.</span></span>  <br/> |
|[<span data-ttu-id="a09e7-120">TelephoneAccessFolderEmail (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a09e7-120">TelephoneAccessFolderEmail (UM web service)</span></span>](telephoneaccessfolderemail-um-web-service.md) <br/> |<span data-ttu-id="a09e7-121">Contiene el identificador de la carpeta de correo electrónico desde la que la mensajería unificada leerá los mensajes a través del teléfono.</span><span class="sxs-lookup"><span data-stu-id="a09e7-121">Contains the identifier for the e-mail folder from which Unified Messaging will read messages over the telephone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a09e7-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a09e7-122">Parent elements</span></span>

<span data-ttu-id="a09e7-123">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a09e7-123">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a09e7-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a09e7-124">Text value</span></span>

<span data-ttu-id="a09e7-125">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a09e7-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a09e7-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a09e7-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a09e7-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="a09e7-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a09e7-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a09e7-128">Schema Name</span></span>  <br/> |<span data-ttu-id="a09e7-129">Mensajes</span><span class="sxs-lookup"><span data-stu-id="a09e7-129">Messages</span></span>  <br/> |
|<span data-ttu-id="a09e7-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a09e7-130">Validation File</span></span>  <br/> |<span data-ttu-id="a09e7-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a09e7-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a09e7-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a09e7-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="a09e7-133">Falso</span><span class="sxs-lookup"><span data-stu-id="a09e7-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a09e7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="a09e7-134">See also</span></span>



[<span data-ttu-id="a09e7-135">Operación GetUMProperties (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a09e7-135">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)

