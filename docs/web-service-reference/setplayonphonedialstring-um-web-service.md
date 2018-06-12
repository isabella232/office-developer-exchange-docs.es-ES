---
title: SetPlayOnPhoneDialString (servicio web de mensajería unificada)
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
description: El elemento SetPlayOnPhoneDialString define una solicitud para establecer la cadena de marcado predeterminado para la operación de PlayOnPhone (servicio web de mensajería unificada) y las solicitudes de PlayOnPhoneGreeting operación (servicio web de mensajería unificada).
ms.openlocfilehash: fd82dc6ef0dd90a2318da93191f657005b7a5c87
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837450"
---
# <a name="setplayonphonedialstring-um-web-service"></a><span data-ttu-id="ac3ef-103">SetPlayOnPhoneDialString (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="ac3ef-103">SetPlayOnPhoneDialString (UM web service)</span></span>

<span data-ttu-id="ac3ef-104">El elemento **SetPlayOnPhoneDialString** define una solicitud para establecer la cadena de marcado de forma predeterminada para las solicitudes de [la operación de PlayOnPhone (servicio web de mensajería unificada)](playonphone-operation-um-web-service.md) y [PlayOnPhoneGreeting (servicio web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="ac3ef-104">The **SetPlayOnPhoneDialString** element defines a request to set the default dial string for [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md) requests.</span></span> 
  
[<span data-ttu-id="ac3ef-105">SetPlayOnPhoneDialString (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="ac3ef-105">SetPlayOnPhoneDialString (UM web service)</span></span>](setplayonphonedialstring-um-web-service.md)
  
```xml
<SetPlayOnPhoneDialString>
  <dialString>   </dialString>
</SetPlayOnPhoneDialString>
```

 <span data-ttu-id="ac3ef-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="ac3ef-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ac3ef-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ac3ef-107">Attributes and elements</span></span>

<span data-ttu-id="ac3ef-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ac3ef-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac3ef-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="ac3ef-109">Attributes</span></span>

<span data-ttu-id="ac3ef-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ac3ef-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ac3ef-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ac3ef-111">Child elements</span></span>

|<span data-ttu-id="ac3ef-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="ac3ef-112">**Element**</span></span>|<span data-ttu-id="ac3ef-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ac3ef-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac3ef-114">dialString (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="ac3ef-114">dialString (UM web service)</span></span>](dialstring-um-web-service.md) <br/> |<span data-ttu-id="ac3ef-115">El número de teléfono para establecer como la cadena de marcado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ac3ef-115">The telephone number to set as the default dial string.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ac3ef-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ac3ef-116">Parent elements</span></span>

<span data-ttu-id="ac3ef-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ac3ef-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ac3ef-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ac3ef-118">Text value</span></span>

<span data-ttu-id="ac3ef-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ac3ef-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac3ef-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ac3ef-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac3ef-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ac3ef-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ac3ef-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ac3ef-122">Schema Name</span></span>  <br/> |<span data-ttu-id="ac3ef-123">Mensajes</span><span class="sxs-lookup"><span data-stu-id="ac3ef-123">Messages</span></span>  <br/> |
|<span data-ttu-id="ac3ef-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ac3ef-124">Validation File</span></span>  <br/> |<span data-ttu-id="ac3ef-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ac3ef-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ac3ef-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ac3ef-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="ac3ef-127">False</span><span class="sxs-lookup"><span data-stu-id="ac3ef-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac3ef-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="ac3ef-128">See also</span></span>



[<span data-ttu-id="ac3ef-129">Operación SetPlayOnPhoneDialString (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="ac3ef-129">SetPlayOnPhoneDialString operation (UM web service)</span></span>](setplayonphonedialstring-operation-um-web-service.md)

