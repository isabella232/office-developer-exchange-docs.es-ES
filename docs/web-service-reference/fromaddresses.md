---
title: FromAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FromAddresses
api_type:
- schema
ms.assetid: b219f315-c20a-4633-af3e-94bd3e4526b6
description: El elemento FromAddresses indica las direcciones de correo electrónico desde la que se deben enviar los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: 40ecb1f3e16ad961b8e4c38d5aa9d15f4f74469a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764722"
---
# <a name="fromaddresses"></a><span data-ttu-id="4cd4c-103">FromAddresses</span><span class="sxs-lookup"><span data-stu-id="4cd4c-103">FromAddresses</span></span>

<span data-ttu-id="4cd4c-104">El elemento **FromAddresses** indica las direcciones de correo electrónico desde la que se deben enviar los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-104">The **FromAddresses** element indicates the e-mail addresses from which incoming messages must be sent in order for the condition or exception to apply.</span></span> 
  
```XML
<FromAddresses>
   <Address/>
</FromAddresses>
```

 <span data-ttu-id="4cd4c-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="4cd4c-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4cd4c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4cd4c-106">Attributes and elements</span></span>

<span data-ttu-id="4cd4c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4cd4c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4cd4c-108">Attributes</span></span>

<span data-ttu-id="4cd4c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4cd4c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4cd4c-110">Child elements</span></span>

|<span data-ttu-id="4cd4c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4cd4c-111">**Element**</span></span>|<span data-ttu-id="4cd4c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4cd4c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4cd4c-113">Dirección (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="4cd4c-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="4cd4c-114">Representa una dirección de correo electrónico completa resuelta.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4cd4c-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4cd4c-115">Parent elements</span></span>

|<span data-ttu-id="4cd4c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="4cd4c-116">**Element**</span></span>|<span data-ttu-id="4cd4c-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4cd4c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4cd4c-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="4cd4c-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="4cd4c-119">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="4cd4c-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="4cd4c-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="4cd4c-121">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-121">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4cd4c-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4cd4c-122">Text value</span></span>

<span data-ttu-id="4cd4c-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4cd4c-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4cd4c-124">Remarks</span></span>

<span data-ttu-id="4cd4c-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="4cd4c-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4cd4c-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4cd4c-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4cd4c-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4cd4c-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4cd4c-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4cd4c-128">Schema Name</span></span>  <br/> |<span data-ttu-id="4cd4c-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="4cd4c-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4cd4c-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4cd4c-130">Validation File</span></span>  <br/> |<span data-ttu-id="4cd4c-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4cd4c-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4cd4c-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4cd4c-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="4cd4c-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="4cd4c-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4cd4c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cd4c-134">See also</span></span>



- [<span data-ttu-id="4cd4c-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4cd4c-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

