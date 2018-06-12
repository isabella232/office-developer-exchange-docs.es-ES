---
title: ContainsRecipientStrings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContainsRecipientStrings
api_type:
- schema
ms.assetid: a7fd13ac-0f13-4610-ac9b-98e27ac3940b
description: El elemento ContainsRecipientStrings indica las cadenas que deben aparecer en la ToRecipients o CcRecipients propiedades de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: 861aba22c9474caf02f9c50d8a7b65b9cc8a2eda
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763817"
---
# <a name="containsrecipientstrings"></a><span data-ttu-id="02a7f-103">ContainsRecipientStrings</span><span class="sxs-lookup"><span data-stu-id="02a7f-103">ContainsRecipientStrings</span></span>

<span data-ttu-id="02a7f-104">El elemento **ContainsRecipientStrings** indica las cadenas que deben aparecer en la **ToRecipients** o **CcRecipients** propiedades de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="02a7f-104">The **ContainsRecipientStrings** element indicates the strings that must appear in either the **ToRecipients** or **CcRecipients** properties of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ContainsRecipientStrings>
    <String/>
</ContainsRecipientStrings>
```

 <span data-ttu-id="02a7f-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="02a7f-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="02a7f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="02a7f-106">Attributes and elements</span></span>

<span data-ttu-id="02a7f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="02a7f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02a7f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="02a7f-108">Attributes</span></span>

<span data-ttu-id="02a7f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="02a7f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="02a7f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="02a7f-110">Child elements</span></span>

|<span data-ttu-id="02a7f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="02a7f-111">**Element**</span></span>|<span data-ttu-id="02a7f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02a7f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02a7f-113">String</span><span class="sxs-lookup"><span data-stu-id="02a7f-113">String</span></span>](string.md) <br/> |<span data-ttu-id="02a7f-114">Representa una cadena que debe aparecer en la **ToRecipients** o **CcRecipients** propiedades de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="02a7f-114">Represents a string that must appear in either the **ToRecipients** or **CcRecipients** properties of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="02a7f-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="02a7f-115">Parent elements</span></span>

|<span data-ttu-id="02a7f-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="02a7f-116">**Element**</span></span>|<span data-ttu-id="02a7f-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02a7f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02a7f-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="02a7f-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="02a7f-119">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="02a7f-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="02a7f-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="02a7f-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="02a7f-121">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="02a7f-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="02a7f-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="02a7f-122">Text value</span></span>

<span data-ttu-id="02a7f-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="02a7f-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="02a7f-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02a7f-124">Remarks</span></span>

<span data-ttu-id="02a7f-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="02a7f-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02a7f-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="02a7f-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02a7f-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="02a7f-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="02a7f-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="02a7f-128">Schema Name</span></span>  <br/> |<span data-ttu-id="02a7f-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="02a7f-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="02a7f-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="02a7f-130">Validation File</span></span>  <br/> |<span data-ttu-id="02a7f-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="02a7f-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="02a7f-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="02a7f-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="02a7f-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="02a7f-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02a7f-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="02a7f-134">See also</span></span>



- [<span data-ttu-id="02a7f-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="02a7f-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

