---
title: PlayOnPhoneGreeting (servicio Web de mensajería unificada)
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
description: El elemento PlayOnPhoneGreeting define una solicitud para reproducir un saludo de mensajería unificada en un teléfono.
ms.openlocfilehash: 197e4ba671e1711b73b1e7c239339db589357581
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529927"
---
# <a name="playonphonegreeting-um-web-service"></a><span data-ttu-id="a90e9-103">PlayOnPhoneGreeting (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a90e9-103">PlayOnPhoneGreeting (UM web service)</span></span>

<span data-ttu-id="a90e9-104">El elemento **PlayOnPhoneGreeting** define una solicitud para reproducir un saludo de mensajería unificada en un teléfono.</span><span class="sxs-lookup"><span data-stu-id="a90e9-104">The **PlayOnPhoneGreeting** element defines a request to play a Unified Messaging greeting on a telephone.</span></span> 
  
[<span data-ttu-id="a90e9-105">PlayOnPhoneGreeting (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a90e9-105">PlayOnPhoneGreeting (UM web service)</span></span>](playonphonegreeting-um-web-service.md)
  
```xml
<PlayOnPhoneGreeting>
  <GreetingType/>
  <DialString/>
</PlayOnPhoneGreeting>
```

 <span data-ttu-id="a90e9-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="a90e9-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a90e9-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a90e9-107">Attributes and elements</span></span>

<span data-ttu-id="a90e9-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a90e9-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a90e9-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="a90e9-109">Attributes</span></span>

<span data-ttu-id="a90e9-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a90e9-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a90e9-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a90e9-111">Child elements</span></span>

|<span data-ttu-id="a90e9-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a90e9-112">**Element**</span></span>|<span data-ttu-id="a90e9-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a90e9-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a90e9-114">GreetingType (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a90e9-114">GreetingType (UM web service)</span></span>](greetingtype-um-web-service.md) <br/> |<span data-ttu-id="a90e9-115">Define el tipo de saludo que se debe usar en una solicitud de [operación de PlayOnPhoneGreeting (servicio Web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="a90e9-115">Defines the type of greeting to use in a [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md) request.</span></span>  <br/> |
|[<span data-ttu-id="a90e9-116">dialString (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a90e9-116">dialString (UM web service)</span></span>](dialstring-um-web-service.md) <br/> |<span data-ttu-id="a90e9-117">Contiene el valor del número de teléfono que se marca.</span><span class="sxs-lookup"><span data-stu-id="a90e9-117">Contains the value for the telephone number to dial.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a90e9-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a90e9-118">Parent elements</span></span>

<span data-ttu-id="a90e9-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a90e9-119">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a90e9-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a90e9-120">Text value</span></span>

<span data-ttu-id="a90e9-121">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a90e9-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a90e9-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a90e9-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a90e9-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="a90e9-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a90e9-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a90e9-124">Schema Name</span></span>  <br/> |<span data-ttu-id="a90e9-125">Mensajes</span><span class="sxs-lookup"><span data-stu-id="a90e9-125">Messages</span></span>  <br/> |
|<span data-ttu-id="a90e9-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a90e9-126">Validation File</span></span>  <br/> |<span data-ttu-id="a90e9-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a90e9-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a90e9-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a90e9-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="a90e9-129">Falso</span><span class="sxs-lookup"><span data-stu-id="a90e9-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a90e9-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a90e9-130">See also</span></span>



[<span data-ttu-id="a90e9-131">Operación PlayOnPhoneGreeting (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="a90e9-131">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)

