---
title: RedirectToRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RedirectToRecipients
api_type:
- schema
ms.assetid: 00ef4a84-76d2-4669-b597-f52abbbc34f5
description: El elemento RedirectToRecipients indica las direcciones de correo electrónico a la que los mensajes se que se redirija.
ms.openlocfilehash: ca0422f2ca678cabe1a88f99e617bee691f2e2f8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837024"
---
# <a name="redirecttorecipients"></a><span data-ttu-id="add4e-103">RedirectToRecipients</span><span class="sxs-lookup"><span data-stu-id="add4e-103">RedirectToRecipients</span></span>

<span data-ttu-id="add4e-104">El elemento **RedirectToRecipients** indica las direcciones de correo electrónico a la que los mensajes se que se redirija.</span><span class="sxs-lookup"><span data-stu-id="add4e-104">The **RedirectToRecipients** element indicates the e-mail addresses to which messages are to be redirected.</span></span> 
  
```XML
<RedirectToRecipients>
   <Address/>
</RedirectToRecipients>
```

 <span data-ttu-id="add4e-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="add4e-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="add4e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="add4e-106">Attributes and elements</span></span>

<span data-ttu-id="add4e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="add4e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="add4e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="add4e-108">Attributes</span></span>

<span data-ttu-id="add4e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="add4e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="add4e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="add4e-110">Child elements</span></span>

|<span data-ttu-id="add4e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="add4e-111">**Element**</span></span>|<span data-ttu-id="add4e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="add4e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="add4e-113">Dirección (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="add4e-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="add4e-114">Representa una dirección de correo electrónico completa resuelta.</span><span class="sxs-lookup"><span data-stu-id="add4e-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="add4e-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="add4e-115">Parent elements</span></span>

|<span data-ttu-id="add4e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="add4e-116">**Element**</span></span>|<span data-ttu-id="add4e-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="add4e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="add4e-118">Acciones</span><span class="sxs-lookup"><span data-stu-id="add4e-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="add4e-119">Representa el conjunto de acciones que están disponibles para ser tomadas en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="add4e-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="add4e-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="add4e-120">Text value</span></span>

<span data-ttu-id="add4e-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="add4e-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="add4e-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="add4e-122">Remarks</span></span>

<span data-ttu-id="add4e-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="add4e-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="add4e-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="add4e-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="add4e-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="add4e-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="add4e-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="add4e-126">Schema Name</span></span>  <br/> |<span data-ttu-id="add4e-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="add4e-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="add4e-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="add4e-128">Validation File</span></span>  <br/> |<span data-ttu-id="add4e-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="add4e-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="add4e-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="add4e-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="add4e-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="add4e-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="add4e-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="add4e-132">See also</span></span>



- [<span data-ttu-id="add4e-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="add4e-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

