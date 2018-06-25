---
title: ContainsBodyStrings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContainsBodyStrings
api_type:
- schema
ms.assetid: 70639472-64bb-456a-8b40-dce727542443
description: El elemento ContainsBodyStrings indica las cadenas que deben aparecer en el cuerpo de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: 5993bd4061298e82a2393768eccb051326564e98
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763815"
---
# <a name="containsbodystrings"></a><span data-ttu-id="f9c54-103">ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="f9c54-103">ContainsBodyStrings</span></span>

<span data-ttu-id="f9c54-104">El elemento **ContainsBodyStrings** indica las cadenas que deben aparecer en el cuerpo de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="f9c54-104">The **ContainsBodyStrings** element indicates the strings that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ContainsBodyStrings>
    <String/>
</ContainsBodyStrings>
```

 <span data-ttu-id="f9c54-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="f9c54-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f9c54-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f9c54-106">Attributes and elements</span></span>

<span data-ttu-id="f9c54-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f9c54-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9c54-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f9c54-108">Attributes</span></span>

<span data-ttu-id="f9c54-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f9c54-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f9c54-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f9c54-110">Child elements</span></span>

|<span data-ttu-id="f9c54-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f9c54-111">**Element**</span></span>|<span data-ttu-id="f9c54-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f9c54-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9c54-113">String</span><span class="sxs-lookup"><span data-stu-id="f9c54-113">String</span></span>](string.md) <br/> |<span data-ttu-id="f9c54-114">Representa una cadena que debe aparecer en el cuerpo de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="f9c54-114">Represents a string that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f9c54-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f9c54-115">Parent elements</span></span>

|<span data-ttu-id="f9c54-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f9c54-116">**Element**</span></span>|<span data-ttu-id="f9c54-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f9c54-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9c54-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="f9c54-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="f9c54-119">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="f9c54-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="f9c54-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="f9c54-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="f9c54-121">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="f9c54-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f9c54-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f9c54-122">Text value</span></span>

<span data-ttu-id="f9c54-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f9c54-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f9c54-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9c54-124">Remarks</span></span>

<span data-ttu-id="f9c54-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f9c54-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9c54-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f9c54-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9c54-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f9c54-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f9c54-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f9c54-128">Schema Name</span></span>  <br/> |<span data-ttu-id="f9c54-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f9c54-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f9c54-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f9c54-130">Validation File</span></span>  <br/> |<span data-ttu-id="f9c54-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f9c54-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f9c54-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f9c54-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="f9c54-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="f9c54-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f9c54-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9c54-134">See also</span></span>



- [<span data-ttu-id="f9c54-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f9c54-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

