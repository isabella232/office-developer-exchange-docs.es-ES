---
title: FromConnectedAccounts
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FromConnectedAccounts
api_type:
- schema
ms.assetid: d4d7ddd7-078d-4f1a-a26b-22dce0c49f3a
description: El elemento FromConnectedAccounts representa los nombres de cuenta de correo electrónico desde la que los mensajes entrantes tienen que agregadas en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: 426e81bbbe96fb5fb4b36506438dc4af4f560eef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764720"
---
# <a name="fromconnectedaccounts"></a><span data-ttu-id="0f5eb-103">FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="0f5eb-103">FromConnectedAccounts</span></span>

<span data-ttu-id="0f5eb-104">El elemento **FromConnectedAccounts** representa los nombres de cuenta de correo electrónico desde la que los mensajes entrantes tienen que agregadas en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="0f5eb-104">The **FromConnectedAccounts** element represents the e-mail account names from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span> 
  
```XML
<FromConnectedAccounts>
    <String/>
</FromConnectedAccounts>
```

 <span data-ttu-id="0f5eb-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="0f5eb-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0f5eb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0f5eb-106">Attributes and elements</span></span>

<span data-ttu-id="0f5eb-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0f5eb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0f5eb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0f5eb-108">Attributes</span></span>

<span data-ttu-id="0f5eb-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0f5eb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0f5eb-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0f5eb-110">Child elements</span></span>

|<span data-ttu-id="0f5eb-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0f5eb-111">**Element**</span></span>|<span data-ttu-id="0f5eb-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0f5eb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0f5eb-113">String</span><span class="sxs-lookup"><span data-stu-id="0f5eb-113">String</span></span>](string.md) <br/> |<span data-ttu-id="0f5eb-114">Representa un nombre de cuenta de correo electrónico desde la que los mensajes entrantes tienen que agregadas en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="0f5eb-114">Represents an e-mail account name from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0f5eb-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0f5eb-115">Parent elements</span></span>

|<span data-ttu-id="0f5eb-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="0f5eb-116">**Element**</span></span>|<span data-ttu-id="0f5eb-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0f5eb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0f5eb-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="0f5eb-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="0f5eb-119">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="0f5eb-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="0f5eb-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="0f5eb-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="0f5eb-121">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="0f5eb-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0f5eb-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0f5eb-122">Text value</span></span>

<span data-ttu-id="0f5eb-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0f5eb-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0f5eb-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f5eb-124">Remarks</span></span>

<span data-ttu-id="0f5eb-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0f5eb-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0f5eb-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0f5eb-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f5eb-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0f5eb-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0f5eb-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0f5eb-128">Schema Name</span></span>  <br/> |<span data-ttu-id="0f5eb-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0f5eb-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0f5eb-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0f5eb-130">Validation File</span></span>  <br/> |<span data-ttu-id="0f5eb-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0f5eb-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0f5eb-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0f5eb-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="0f5eb-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="0f5eb-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0f5eb-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="0f5eb-134">See also</span></span>



- [<span data-ttu-id="0f5eb-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0f5eb-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

