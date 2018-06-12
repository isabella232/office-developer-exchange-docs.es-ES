---
title: ItemClasses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemClasses
api_type:
- schema
ms.assetid: f95430cc-2860-47c1-af2d-8c4156c9b281
description: El elemento ItemClasses representa las clases de elemento deben estar marcados en los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: 70a4823f9017ba8c6f894394d5907f1adeb80167
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836148"
---
# <a name="itemclasses"></a><span data-ttu-id="f00c4-103">ItemClasses</span><span class="sxs-lookup"><span data-stu-id="f00c4-103">ItemClasses</span></span>

<span data-ttu-id="f00c4-104">El elemento **ItemClasses** representa las clases de elemento deben estar marcados en los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="f00c4-104">The **ItemClasses** element represents the item classes that must be stamped on incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ItemClasses>
    <String/>
</ItemClasses>
```

 <span data-ttu-id="f00c4-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="f00c4-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f00c4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f00c4-106">Attributes and elements</span></span>

<span data-ttu-id="f00c4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f00c4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f00c4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f00c4-108">Attributes</span></span>

<span data-ttu-id="f00c4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f00c4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f00c4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f00c4-110">Child elements</span></span>

|<span data-ttu-id="f00c4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f00c4-111">**Element**</span></span>|<span data-ttu-id="f00c4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f00c4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f00c4-113">String</span><span class="sxs-lookup"><span data-stu-id="f00c4-113">String</span></span>](string.md) <br/> |<span data-ttu-id="f00c4-114">Representa una clase de elemento único.</span><span class="sxs-lookup"><span data-stu-id="f00c4-114">Represents a single item class.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f00c4-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f00c4-115">Parent elements</span></span>

|<span data-ttu-id="f00c4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f00c4-116">**Element**</span></span>|<span data-ttu-id="f00c4-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f00c4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f00c4-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="f00c4-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="f00c4-119">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="f00c4-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="f00c4-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="f00c4-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="f00c4-121">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="f00c4-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f00c4-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f00c4-122">Text value</span></span>

<span data-ttu-id="f00c4-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f00c4-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f00c4-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f00c4-124">Remarks</span></span>

<span data-ttu-id="f00c4-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f00c4-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f00c4-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f00c4-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f00c4-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f00c4-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f00c4-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f00c4-128">Schema name</span></span>  <br/> |<span data-ttu-id="f00c4-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f00c4-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="f00c4-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f00c4-130">Validation file</span></span>  <br/> |<span data-ttu-id="f00c4-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f00c4-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f00c4-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f00c4-132">Can be empty</span></span>  <br/> |<span data-ttu-id="f00c4-133">False</span><span class="sxs-lookup"><span data-stu-id="f00c4-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f00c4-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="f00c4-134">See also</span></span>



- [<span data-ttu-id="f00c4-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f00c4-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

