---
title: IsEncrypted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsEncrypted
api_type:
- schema
ms.assetid: 68a30e92-c2b1-4af5-bb16-ba38afb80c43
description: El elemento IsEncrypted indica si los mensajes entrantes deben ser S/MIME cifrado en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: 582a1f197d4ee6b60af91b1a178d79163b50052c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836003"
---
# <a name="isencrypted"></a><span data-ttu-id="7a4df-103">IsEncrypted</span><span class="sxs-lookup"><span data-stu-id="7a4df-103">IsEncrypted</span></span>

<span data-ttu-id="7a4df-104">El elemento **IsEncrypted** indica si los mensajes entrantes deben ser S/MIME cifrado en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="7a4df-104">The **IsEncrypted** element indicates whether incoming messages must be S/MIME encrypted in order for the condition or exception to apply.</span></span> 
  
```XML
<IsEncrypted>true | false</IsEncrypted>
```

 <span data-ttu-id="7a4df-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7a4df-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7a4df-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7a4df-106">Attributes and elements</span></span>

<span data-ttu-id="7a4df-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7a4df-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a4df-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7a4df-108">Attributes</span></span>

<span data-ttu-id="7a4df-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7a4df-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a4df-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7a4df-110">Child elements</span></span>

<span data-ttu-id="7a4df-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7a4df-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7a4df-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7a4df-112">Parent elements</span></span>

|<span data-ttu-id="7a4df-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7a4df-113">**Element**</span></span>|<span data-ttu-id="7a4df-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7a4df-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a4df-115">Condiciones</span><span class="sxs-lookup"><span data-stu-id="7a4df-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="7a4df-116">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="7a4df-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="7a4df-117">Excepciones</span><span class="sxs-lookup"><span data-stu-id="7a4df-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="7a4df-118">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="7a4df-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7a4df-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7a4df-119">Text value</span></span>

<span data-ttu-id="7a4df-120">Un valor de texto de **true** indica que el mensaje debe ser S/MIME cifrado en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="7a4df-120">A text value of **true** indicates that the message must be S/MIME encrypted in order for the condition or exception to apply.</span></span> <span data-ttu-id="7a4df-121">Un valor de **false** indica que el mensaje no tienen que ser S/MIME en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="7a4df-121">A value of **false** indicates that the message does not have to be S/MIME in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7a4df-122">Notas</span><span class="sxs-lookup"><span data-stu-id="7a4df-122">Remarks</span></span>

<span data-ttu-id="7a4df-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7a4df-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a4df-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7a4df-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a4df-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7a4df-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7a4df-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7a4df-126">Schema Name</span></span>  <br/> |<span data-ttu-id="7a4df-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7a4df-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7a4df-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7a4df-128">Validation File</span></span>  <br/> |<span data-ttu-id="7a4df-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7a4df-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7a4df-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7a4df-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="7a4df-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="7a4df-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a4df-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="7a4df-132">See also</span></span>



- [<span data-ttu-id="7a4df-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7a4df-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

