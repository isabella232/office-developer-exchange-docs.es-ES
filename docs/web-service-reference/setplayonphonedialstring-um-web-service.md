---
title: SetPlayOnPhoneDialString (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetPlayOnPhoneDialString
api_type:
- schema
ms.assetid: 513a5072-c3ac-405f-98c2-0ab982d0a360
description: El elemento SetPlayOnPhoneDialString define una solicitud para establecer la cadena de marcado predeterminada para las solicitudes de reproducir operación (servicio Web de mensajería unificada) y operación PlayOnPhoneGreeting (servicio Web de mensajería unificada).
ms.openlocfilehash: 40021e9dedafb5fafda91bf3612d8a6485dae8e7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458631"
---
# <a name="setplayonphonedialstring-um-web-service"></a><span data-ttu-id="b06ba-103">SetPlayOnPhoneDialString (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="b06ba-103">SetPlayOnPhoneDialString (UM web service)</span></span>

<span data-ttu-id="b06ba-104">El elemento **SetPlayOnPhoneDialString** define una solicitud para establecer la cadena de marcado predeterminada para las solicitudes de [reproducir operación (servicio Web de mensajería unificada)](playonphone-operation-um-web-service.md) y [operación PlayOnPhoneGreeting (servicio Web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="b06ba-104">The **SetPlayOnPhoneDialString** element defines a request to set the default dial string for [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md) requests.</span></span> 
  
[<span data-ttu-id="b06ba-105">SetPlayOnPhoneDialString (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="b06ba-105">SetPlayOnPhoneDialString (UM web service)</span></span>](setplayonphonedialstring-um-web-service.md)
  
```xml
<SetPlayOnPhoneDialString>
  <dialString>   </dialString>
</SetPlayOnPhoneDialString>
```

 <span data-ttu-id="b06ba-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="b06ba-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b06ba-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b06ba-107">Attributes and elements</span></span>

<span data-ttu-id="b06ba-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b06ba-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b06ba-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="b06ba-109">Attributes</span></span>

<span data-ttu-id="b06ba-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b06ba-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b06ba-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b06ba-111">Child elements</span></span>

|<span data-ttu-id="b06ba-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b06ba-112">**Element**</span></span>|<span data-ttu-id="b06ba-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b06ba-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b06ba-114">dialString (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="b06ba-114">dialString (UM web service)</span></span>](dialstring-um-web-service.md) <br/> |<span data-ttu-id="b06ba-115">El número de teléfono que se establece como la cadena de marcado predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b06ba-115">The telephone number to set as the default dial string.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b06ba-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b06ba-116">Parent elements</span></span>

<span data-ttu-id="b06ba-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b06ba-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="b06ba-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b06ba-118">Text value</span></span>

<span data-ttu-id="b06ba-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b06ba-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b06ba-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b06ba-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b06ba-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="b06ba-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b06ba-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b06ba-122">Schema Name</span></span>  <br/> |<span data-ttu-id="b06ba-123">Mensajes</span><span class="sxs-lookup"><span data-stu-id="b06ba-123">Messages</span></span>  <br/> |
|<span data-ttu-id="b06ba-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b06ba-124">Validation File</span></span>  <br/> |<span data-ttu-id="b06ba-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b06ba-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b06ba-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b06ba-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="b06ba-127">Falso</span><span class="sxs-lookup"><span data-stu-id="b06ba-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b06ba-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b06ba-128">See also</span></span>



[<span data-ttu-id="b06ba-129">Operación SetPlayOnPhoneDialString (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="b06ba-129">SetPlayOnPhoneDialString operation (UM web service)</span></span>](setplayonphonedialstring-operation-um-web-service.md)

