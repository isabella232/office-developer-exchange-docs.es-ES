---
title: SendSMSAlertToRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendSMSAlertToRecipients
api_type:
- schema
ms.assetid: c4dd000b-11b6-4b7b-91e0-dbfeae11d770
description: El elemento SendSMSAlertToRecipients indica los números de teléfono móvil a los que es una alerta de servicio de mensajes cortos (SMS) que se envíen.
ms.openlocfilehash: b28202c71257fccca67879713d5d7df03f69b06d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837347"
---
# <a name="sendsmsalerttorecipients"></a><span data-ttu-id="be521-103">SendSMSAlertToRecipients</span><span class="sxs-lookup"><span data-stu-id="be521-103">SendSMSAlertToRecipients</span></span>

<span data-ttu-id="be521-104">El elemento **SendSMSAlertToRecipients** indica los números de teléfono móvil a los que es una alerta de servicio de mensajes cortos (SMS) que se envíen.</span><span class="sxs-lookup"><span data-stu-id="be521-104">The **SendSMSAlertToRecipients** element indicates the mobile phone numbers to which a Short Message Service (SMS) alert is to be sent.</span></span> 
  
```XML
<SendSMSAlertToRecipients>
   <Address/>
</SendSMSAlertToRecipients>
```

 <span data-ttu-id="be521-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="be521-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="be521-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="be521-106">Attributes and elements</span></span>

<span data-ttu-id="be521-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="be521-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="be521-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="be521-108">Attributes</span></span>

<span data-ttu-id="be521-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="be521-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="be521-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="be521-110">Child elements</span></span>

|<span data-ttu-id="be521-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="be521-111">**Element**</span></span>|<span data-ttu-id="be521-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="be521-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be521-113">Dirección (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="be521-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="be521-114">Representa una dirección de correo electrónico completa resuelta.</span><span class="sxs-lookup"><span data-stu-id="be521-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="be521-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="be521-115">Parent elements</span></span>

|<span data-ttu-id="be521-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="be521-116">**Element**</span></span>|<span data-ttu-id="be521-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="be521-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be521-118">Acciones</span><span class="sxs-lookup"><span data-stu-id="be521-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="be521-119">Representa el conjunto de acciones que están disponibles para ser tomadas en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="be521-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="be521-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="be521-120">Text value</span></span>

<span data-ttu-id="be521-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="be521-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="be521-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be521-122">Remarks</span></span>

<span data-ttu-id="be521-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="be521-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="be521-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="be521-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be521-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="be521-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="be521-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="be521-126">Schema Name</span></span>  <br/> |<span data-ttu-id="be521-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="be521-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="be521-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="be521-128">Validation File</span></span>  <br/> |<span data-ttu-id="be521-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="be521-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="be521-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="be521-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="be521-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="be521-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="be521-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="be521-132">See also</span></span>



- [<span data-ttu-id="be521-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="be521-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

