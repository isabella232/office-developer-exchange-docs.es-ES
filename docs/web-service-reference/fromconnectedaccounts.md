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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764720"
---
# <a name="fromconnectedaccounts"></a><span data-ttu-id="e9024-103">FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="e9024-103">FromConnectedAccounts</span></span>

<span data-ttu-id="e9024-104">El elemento **FromConnectedAccounts** representa los nombres de cuenta de correo electrónico desde la que los mensajes entrantes tienen que agregadas en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="e9024-104">The **FromConnectedAccounts** element represents the e-mail account names from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span> 
  
```XML
<FromConnectedAccounts>
    <String/>
</FromConnectedAccounts>
```

 <span data-ttu-id="e9024-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="e9024-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e9024-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e9024-106">Attributes and elements</span></span>

<span data-ttu-id="e9024-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e9024-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e9024-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e9024-108">Attributes</span></span>

<span data-ttu-id="e9024-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e9024-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e9024-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e9024-110">Child elements</span></span>

|<span data-ttu-id="e9024-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e9024-111">**Element**</span></span>|<span data-ttu-id="e9024-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e9024-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9024-113">String</span><span class="sxs-lookup"><span data-stu-id="e9024-113">String</span></span>](string.md) <br/> |<span data-ttu-id="e9024-114">Representa un nombre de cuenta de correo electrónico desde la que los mensajes entrantes tienen que agregadas en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="e9024-114">Represents an e-mail account name from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e9024-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e9024-115">Parent elements</span></span>

|<span data-ttu-id="e9024-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="e9024-116">**Element**</span></span>|<span data-ttu-id="e9024-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e9024-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9024-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="e9024-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="e9024-119">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="e9024-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="e9024-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="e9024-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="e9024-121">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="e9024-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e9024-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e9024-122">Text value</span></span>

<span data-ttu-id="e9024-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e9024-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e9024-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e9024-124">Remarks</span></span>

<span data-ttu-id="e9024-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e9024-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e9024-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e9024-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e9024-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e9024-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e9024-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e9024-128">Schema Name</span></span>  <br/> |<span data-ttu-id="e9024-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e9024-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e9024-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e9024-130">Validation File</span></span>  <br/> |<span data-ttu-id="e9024-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e9024-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e9024-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e9024-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="e9024-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="e9024-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9024-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9024-134">See also</span></span>



- [<span data-ttu-id="e9024-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e9024-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

