---
title: ContainsHeaderStrings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContainsHeaderStrings
api_type:
- schema
ms.assetid: 5f68427b-990a-4a27-bfb3-fce3115b02d7
description: El elemento ContainsHeaderStrings indica las cadenas que deben aparecer en los encabezados de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: 360870d63853a0e79f801cc2f17473b1a1b28c25
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763821"
---
# <a name="containsheaderstrings"></a><span data-ttu-id="96af7-103">ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="96af7-103">ContainsHeaderStrings</span></span>

<span data-ttu-id="96af7-104">El elemento **ContainsHeaderStrings** indica las cadenas que deben aparecer en los encabezados de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="96af7-104">The **ContainsHeaderStrings** element indicates the strings that must appear in the headers of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ContainsHeaderStrings>
    <String/>
</ContainsHeaderStrings>
```

 <span data-ttu-id="96af7-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="96af7-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="96af7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="96af7-106">Attributes and elements</span></span>

<span data-ttu-id="96af7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="96af7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="96af7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="96af7-108">Attributes</span></span>

<span data-ttu-id="96af7-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="96af7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="96af7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="96af7-110">Child elements</span></span>

|<span data-ttu-id="96af7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="96af7-111">**Element**</span></span>|<span data-ttu-id="96af7-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="96af7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96af7-113">String</span><span class="sxs-lookup"><span data-stu-id="96af7-113">String</span></span>](string.md) <br/> |<span data-ttu-id="96af7-114">Representa una cadena que debe aparecer en los encabezados de mensaje en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="96af7-114">Represents a string that must appear in message headers in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="96af7-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="96af7-115">Parent elements</span></span>

|<span data-ttu-id="96af7-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="96af7-116">**Element**</span></span>|<span data-ttu-id="96af7-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="96af7-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96af7-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="96af7-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="96af7-119">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="96af7-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="96af7-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="96af7-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="96af7-121">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="96af7-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="96af7-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="96af7-122">Text value</span></span>

<span data-ttu-id="96af7-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="96af7-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="96af7-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96af7-124">Remarks</span></span>

<span data-ttu-id="96af7-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="96af7-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="96af7-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="96af7-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96af7-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="96af7-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="96af7-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="96af7-128">Schema Name</span></span>  <br/> |<span data-ttu-id="96af7-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="96af7-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="96af7-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="96af7-130">Validation File</span></span>  <br/> |<span data-ttu-id="96af7-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="96af7-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="96af7-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="96af7-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="96af7-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="96af7-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="96af7-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="96af7-134">See also</span></span>



- [<span data-ttu-id="96af7-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="96af7-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

