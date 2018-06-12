---
title: SentToAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SentToAddresses
api_type:
- schema
ms.assetid: 086130d2-93b1-4de1-9553-10ec10322a0c
description: El elemento SentToAddresses indica las direcciones de correo electrónico que se han enviado en orden para la condición o la excepción que se debe aplicar a los mensajes entrantes.
ms.openlocfilehash: c5a4770ff22e08713e5cf40b9a81191d50a2f437
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837358"
---
# <a name="senttoaddresses"></a><span data-ttu-id="516ab-103">SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="516ab-103">SentToAddresses</span></span>

<span data-ttu-id="516ab-104">El elemento **SentToAddresses** indica las direcciones de correo electrónico que se han enviado en orden para la condición o la excepción que se debe aplicar a los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="516ab-104">The **SentToAddresses** element indicates the e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.</span></span> 
  
```XML
<SentToAddresses>
   <Address/>
</SentToAddresses>
```

 <span data-ttu-id="516ab-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="516ab-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="516ab-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="516ab-106">Attributes and elements</span></span>

<span data-ttu-id="516ab-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="516ab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="516ab-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="516ab-108">Attributes</span></span>

<span data-ttu-id="516ab-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="516ab-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="516ab-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="516ab-110">Child elements</span></span>

|<span data-ttu-id="516ab-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="516ab-111">**Element**</span></span>|<span data-ttu-id="516ab-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="516ab-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="516ab-113">Dirección (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="516ab-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="516ab-114">Representa una dirección de correo electrónico completa resuelta.</span><span class="sxs-lookup"><span data-stu-id="516ab-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="516ab-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="516ab-115">Parent elements</span></span>

|<span data-ttu-id="516ab-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="516ab-116">**Element**</span></span>|<span data-ttu-id="516ab-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="516ab-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="516ab-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="516ab-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="516ab-119">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="516ab-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="516ab-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="516ab-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="516ab-121">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="516ab-121">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="516ab-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="516ab-122">Text value</span></span>

<span data-ttu-id="516ab-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="516ab-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="516ab-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="516ab-124">Remarks</span></span>

<span data-ttu-id="516ab-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="516ab-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="516ab-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="516ab-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="516ab-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="516ab-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="516ab-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="516ab-128">Schema Name</span></span>  <br/> |<span data-ttu-id="516ab-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="516ab-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="516ab-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="516ab-130">Validation File</span></span>  <br/> |<span data-ttu-id="516ab-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="516ab-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="516ab-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="516ab-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="516ab-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="516ab-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="516ab-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="516ab-134">See also</span></span>



- [<span data-ttu-id="516ab-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="516ab-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

