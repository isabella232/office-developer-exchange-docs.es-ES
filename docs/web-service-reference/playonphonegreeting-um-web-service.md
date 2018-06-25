---
title: PlayOnPhoneGreeting (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhoneGreeting
api_type:
- schema
ms.assetid: 43eda596-3609-4e1b-8502-1db2636535cf
description: El elemento PlayOnPhoneGreeting define una solicitud para reproducir un mensajería unificada en un teléfono de saludo.
ms.openlocfilehash: c30140fc60b9e902517b4cc18deb9b61efa61e0c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836836"
---
# <a name="playonphonegreeting-um-web-service"></a><span data-ttu-id="09fc7-103">PlayOnPhoneGreeting (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="09fc7-103">PlayOnPhoneGreeting (UM web service)</span></span>

<span data-ttu-id="09fc7-104">El elemento **PlayOnPhoneGreeting** define una solicitud para reproducir un mensajería unificada en un teléfono de saludo.</span><span class="sxs-lookup"><span data-stu-id="09fc7-104">The **PlayOnPhoneGreeting** element defines a request to play a Unified Messaging greeting on a telephone.</span></span> 
  
[<span data-ttu-id="09fc7-105">PlayOnPhoneGreeting (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="09fc7-105">PlayOnPhoneGreeting (UM web service)</span></span>](playonphonegreeting-um-web-service.md)
  
```xml
<PlayOnPhoneGreeting>
  <GreetingType/>
  <DialString/>
</PlayOnPhoneGreeting>
```

 <span data-ttu-id="09fc7-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="09fc7-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="09fc7-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="09fc7-107">Attributes and elements</span></span>

<span data-ttu-id="09fc7-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="09fc7-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="09fc7-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="09fc7-109">Attributes</span></span>

<span data-ttu-id="09fc7-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="09fc7-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="09fc7-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="09fc7-111">Child elements</span></span>

|<span data-ttu-id="09fc7-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="09fc7-112">**Element**</span></span>|<span data-ttu-id="09fc7-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="09fc7-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="09fc7-114">GreetingType (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="09fc7-114">GreetingType (UM web service)</span></span>](greetingtype-um-web-service.md) <br/> |<span data-ttu-id="09fc7-115">Define el tipo de saludo para usar en una solicitud de [operación PlayOnPhoneGreeting (servicio web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="09fc7-115">Defines the type of greeting to use in a [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md) request.</span></span>  <br/> |
|[<span data-ttu-id="09fc7-116">dialString (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="09fc7-116">dialString (UM web service)</span></span>](dialstring-um-web-service.md) <br/> |<span data-ttu-id="09fc7-117">Contiene el valor para el número de teléfono a marcar.</span><span class="sxs-lookup"><span data-stu-id="09fc7-117">Contains the value for the telephone number to dial.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="09fc7-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="09fc7-118">Parent elements</span></span>

<span data-ttu-id="09fc7-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="09fc7-119">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="09fc7-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="09fc7-120">Text value</span></span>

<span data-ttu-id="09fc7-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="09fc7-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="09fc7-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="09fc7-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09fc7-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="09fc7-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="09fc7-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="09fc7-124">Schema Name</span></span>  <br/> |<span data-ttu-id="09fc7-125">Mensajes</span><span class="sxs-lookup"><span data-stu-id="09fc7-125">Messages</span></span>  <br/> |
|<span data-ttu-id="09fc7-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="09fc7-126">Validation File</span></span>  <br/> |<span data-ttu-id="09fc7-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="09fc7-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="09fc7-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="09fc7-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="09fc7-129">False</span><span class="sxs-lookup"><span data-stu-id="09fc7-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09fc7-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="09fc7-130">See also</span></span>



[<span data-ttu-id="09fc7-131">Operación PlayOnPhoneGreeting (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="09fc7-131">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)

