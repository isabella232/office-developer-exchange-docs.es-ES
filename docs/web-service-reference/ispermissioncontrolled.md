---
title: IsPermissionControlled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsPermissionControlled
api_type:
- schema
ms.assetid: a2fd0340-f31f-4389-a1cd-7e93b40bb3c6
description: El elemento IsPermissionControlled indica si los mensajes entrantes deben ser permiso controlado (protegido con RMS) en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: fdd9910b8c35d9d57e724d6fec57d203f38f0359
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836088"
---
# <a name="ispermissioncontrolled"></a><span data-ttu-id="27713-103">IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="27713-103">IsPermissionControlled</span></span>

<span data-ttu-id="27713-104">El elemento **IsPermissionControlled** indica si los mensajes entrantes deben ser permiso controlado (protegido con RMS) en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="27713-104">The **IsPermissionControlled** element indicates whether incoming messages must be permission controlled (RMS protected) in order for the condition or exception to apply.</span></span> 
  
```XML
<IsPermissionControlled>true | false</IsPermissionControlled>
```

 <span data-ttu-id="27713-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="27713-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="27713-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="27713-106">Attributes and elements</span></span>

<span data-ttu-id="27713-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="27713-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27713-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="27713-108">Attributes</span></span>

<span data-ttu-id="27713-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="27713-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="27713-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="27713-110">Child elements</span></span>

<span data-ttu-id="27713-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="27713-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="27713-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="27713-112">Parent elements</span></span>

|<span data-ttu-id="27713-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="27713-113">**Element**</span></span>|<span data-ttu-id="27713-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="27713-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27713-115">Condiciones</span><span class="sxs-lookup"><span data-stu-id="27713-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="27713-116">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="27713-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="27713-117">Excepciones</span><span class="sxs-lookup"><span data-stu-id="27713-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="27713-118">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="27713-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="27713-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="27713-119">Text value</span></span>

<span data-ttu-id="27713-120">Un valor de texto de **true** indica que el mensaje debe ser RMS protegida en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="27713-120">A text value of **true** indicates that the message must be RMS protected in order for the condition or exception to apply.</span></span> <span data-ttu-id="27713-121">Un valor de **false** indica que el mensaje no debe ser RMS protegida en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="27713-121">A value of **false** indicates that the message must not be RMS protected in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="27713-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="27713-122">Remarks</span></span>

<span data-ttu-id="27713-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="27713-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27713-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="27713-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27713-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="27713-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="27713-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="27713-126">Schema Name</span></span>  <br/> |<span data-ttu-id="27713-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="27713-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="27713-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="27713-128">Validation File</span></span>  <br/> |<span data-ttu-id="27713-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="27713-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="27713-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="27713-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="27713-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="27713-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27713-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="27713-132">See also</span></span>



- [<span data-ttu-id="27713-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="27713-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

