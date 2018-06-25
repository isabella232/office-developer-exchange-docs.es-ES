---
title: ForwardToRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ForwardToRecipients
api_type:
- schema
ms.assetid: dd58fd72-591d-4891-b226-465bcf12c19b
description: El elemento ForwardToRecipients indica las direcciones de correo electrónico a la que los mensajes se se transfieran.
ms.openlocfilehash: f2538f62bb9d837ef64bdc742b01d26d3d7d77f5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764701"
---
# <a name="forwardtorecipients"></a><span data-ttu-id="3a96f-103">ForwardToRecipients</span><span class="sxs-lookup"><span data-stu-id="3a96f-103">ForwardToRecipients</span></span>

<span data-ttu-id="3a96f-104">El elemento **ForwardToRecipients** indica las direcciones de correo electrónico a la que los mensajes se se transfieran.</span><span class="sxs-lookup"><span data-stu-id="3a96f-104">The **ForwardToRecipients** element indicates the e-mail addresses to which messages are to be forwarded.</span></span> 
  
```XML
<ForwardToRecipients>
   <Address/>
</ForwardToRecipients>
```

 <span data-ttu-id="3a96f-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="3a96f-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3a96f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3a96f-106">Attributes and elements</span></span>

<span data-ttu-id="3a96f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3a96f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a96f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3a96f-108">Attributes</span></span>

<span data-ttu-id="3a96f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3a96f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a96f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3a96f-110">Child elements</span></span>

|<span data-ttu-id="3a96f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a96f-111">**Element**</span></span>|<span data-ttu-id="3a96f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a96f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a96f-113">Dirección (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="3a96f-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="3a96f-114">Representa una dirección de correo electrónico completa resuelta.</span><span class="sxs-lookup"><span data-stu-id="3a96f-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3a96f-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3a96f-115">Parent elements</span></span>

|<span data-ttu-id="3a96f-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a96f-116">**Element**</span></span>|<span data-ttu-id="3a96f-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a96f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a96f-118">Acciones</span><span class="sxs-lookup"><span data-stu-id="3a96f-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="3a96f-119">Representa el conjunto de acciones que están disponibles para ser tomadas en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="3a96f-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3a96f-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3a96f-120">Text value</span></span>

<span data-ttu-id="3a96f-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3a96f-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3a96f-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3a96f-122">Remarks</span></span>

<span data-ttu-id="3a96f-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a96f-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a96f-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3a96f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a96f-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3a96f-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3a96f-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3a96f-126">Schema Name</span></span>  <br/> |<span data-ttu-id="3a96f-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3a96f-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3a96f-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3a96f-128">Validation File</span></span>  <br/> |<span data-ttu-id="3a96f-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3a96f-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3a96f-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3a96f-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="3a96f-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="3a96f-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a96f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a96f-132">See also</span></span>



- [<span data-ttu-id="3a96f-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3a96f-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

