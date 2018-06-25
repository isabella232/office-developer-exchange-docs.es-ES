---
title: ContainsSenderStrings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContainsSenderStrings
api_type:
- schema
ms.assetid: 3e16163f-cffe-4c4e-9a2a-00245d25ba96
description: El elemento ContainsSenderStrings indica las cadenas que deben aparecer en la propiedad From de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: d174c0d7e2cbfd5b671a825a867d3ee7e24c2f2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763829"
---
# <a name="containssenderstrings"></a><span data-ttu-id="fa6c2-103">ContainsSenderStrings</span><span class="sxs-lookup"><span data-stu-id="fa6c2-103">ContainsSenderStrings</span></span>

<span data-ttu-id="fa6c2-104">El elemento **ContainsSenderStrings** indica las cadenas que deben aparecer en la propiedad **From** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="fa6c2-104">The **ContainsSenderStrings** element indicates the strings that must appear in the **From** property of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ContainsSenderStrings>
    <String/>
</ContainsSenderStrings>
```

 <span data-ttu-id="fa6c2-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="fa6c2-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa6c2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fa6c2-106">Attributes and elements</span></span>

<span data-ttu-id="fa6c2-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fa6c2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa6c2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fa6c2-108">Attributes</span></span>

<span data-ttu-id="fa6c2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fa6c2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa6c2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fa6c2-110">Child elements</span></span>

|<span data-ttu-id="fa6c2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa6c2-111">**Element**</span></span>|<span data-ttu-id="fa6c2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa6c2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa6c2-113">String</span><span class="sxs-lookup"><span data-stu-id="fa6c2-113">String</span></span>](string.md) <br/> |<span data-ttu-id="fa6c2-114">Representa una cadena que debe aparecer en la propiedad **From** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="fa6c2-114">Represents a string that must appear in the **From** property of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fa6c2-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fa6c2-115">Parent elements</span></span>

|<span data-ttu-id="fa6c2-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa6c2-116">**Element**</span></span>|<span data-ttu-id="fa6c2-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa6c2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa6c2-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="fa6c2-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="fa6c2-119">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="fa6c2-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="fa6c2-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="fa6c2-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="fa6c2-121">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="fa6c2-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fa6c2-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fa6c2-122">Text value</span></span>

<span data-ttu-id="fa6c2-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fa6c2-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fa6c2-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa6c2-124">Remarks</span></span>

<span data-ttu-id="fa6c2-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa6c2-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa6c2-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fa6c2-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa6c2-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fa6c2-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fa6c2-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fa6c2-128">Schema Name</span></span>  <br/> |<span data-ttu-id="fa6c2-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="fa6c2-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fa6c2-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fa6c2-130">Validation File</span></span>  <br/> |<span data-ttu-id="fa6c2-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fa6c2-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fa6c2-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fa6c2-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="fa6c2-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="fa6c2-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa6c2-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa6c2-134">See also</span></span>



- [<span data-ttu-id="fa6c2-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="fa6c2-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

