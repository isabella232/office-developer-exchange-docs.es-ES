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
description: El elemento SendSMSAlertToRecipients indica los números de teléfono móvil a los que se enviará una alerta de servicio de mensajes cortos (SMS).
ms.openlocfilehash: ed17bf9ad20a51cbead4b86f385a53d19562fa64
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464850"
---
# <a name="sendsmsalerttorecipients"></a><span data-ttu-id="11a1d-103">SendSMSAlertToRecipients</span><span class="sxs-lookup"><span data-stu-id="11a1d-103">SendSMSAlertToRecipients</span></span>

<span data-ttu-id="11a1d-104">El elemento **SendSMSAlertToRecipients** indica los números de teléfono móvil a los que se enviará una alerta de servicio de mensajes cortos (SMS).</span><span class="sxs-lookup"><span data-stu-id="11a1d-104">The **SendSMSAlertToRecipients** element indicates the mobile phone numbers to which a Short Message Service (SMS) alert is to be sent.</span></span> 
  
```XML
<SendSMSAlertToRecipients>
   <Address/>
</SendSMSAlertToRecipients>
```

 <span data-ttu-id="11a1d-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="11a1d-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="11a1d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="11a1d-106">Attributes and elements</span></span>

<span data-ttu-id="11a1d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="11a1d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11a1d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="11a1d-108">Attributes</span></span>

<span data-ttu-id="11a1d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="11a1d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="11a1d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="11a1d-110">Child elements</span></span>

|<span data-ttu-id="11a1d-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="11a1d-111">**Element**</span></span>|<span data-ttu-id="11a1d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="11a1d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11a1d-113">Dirección (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="11a1d-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="11a1d-114">Representa una dirección de correo electrónico completamente resuelta.</span><span class="sxs-lookup"><span data-stu-id="11a1d-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="11a1d-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="11a1d-115">Parent elements</span></span>

|<span data-ttu-id="11a1d-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="11a1d-116">**Element**</span></span>|<span data-ttu-id="11a1d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="11a1d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11a1d-118">Actions</span><span class="sxs-lookup"><span data-stu-id="11a1d-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="11a1d-119">Representa el conjunto de acciones que se pueden realizar en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="11a1d-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="11a1d-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="11a1d-120">Text value</span></span>

<span data-ttu-id="11a1d-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="11a1d-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="11a1d-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="11a1d-122">Remarks</span></span>

<span data-ttu-id="11a1d-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="11a1d-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="11a1d-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="11a1d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11a1d-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="11a1d-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="11a1d-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="11a1d-126">Schema Name</span></span>  <br/> |<span data-ttu-id="11a1d-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="11a1d-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="11a1d-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="11a1d-128">Validation File</span></span>  <br/> |<span data-ttu-id="11a1d-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="11a1d-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="11a1d-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="11a1d-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="11a1d-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="11a1d-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11a1d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="11a1d-132">See also</span></span>



- [<span data-ttu-id="11a1d-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="11a1d-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

