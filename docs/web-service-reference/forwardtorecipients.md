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
description: El elemento ForwardToRecipients indica las direcciones de correo electrónico a las que se deben reenviar los mensajes.
ms.openlocfilehash: d565fa9f59794a4e10e91b05a507354a2f6ef0c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458323"
---
# <a name="forwardtorecipients"></a><span data-ttu-id="72dab-103">ForwardToRecipients</span><span class="sxs-lookup"><span data-stu-id="72dab-103">ForwardToRecipients</span></span>

<span data-ttu-id="72dab-104">El elemento **ForwardToRecipients** indica las direcciones de correo electrónico a las que se deben reenviar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="72dab-104">The **ForwardToRecipients** element indicates the e-mail addresses to which messages are to be forwarded.</span></span> 
  
```XML
<ForwardToRecipients>
   <Address/>
</ForwardToRecipients>
```

 <span data-ttu-id="72dab-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="72dab-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="72dab-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="72dab-106">Attributes and elements</span></span>

<span data-ttu-id="72dab-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="72dab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="72dab-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="72dab-108">Attributes</span></span>

<span data-ttu-id="72dab-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="72dab-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="72dab-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="72dab-110">Child elements</span></span>

|<span data-ttu-id="72dab-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="72dab-111">**Element**</span></span>|<span data-ttu-id="72dab-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="72dab-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="72dab-113">Dirección (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="72dab-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="72dab-114">Representa una dirección de correo electrónico completamente resuelta.</span><span class="sxs-lookup"><span data-stu-id="72dab-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="72dab-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="72dab-115">Parent elements</span></span>

|<span data-ttu-id="72dab-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="72dab-116">**Element**</span></span>|<span data-ttu-id="72dab-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="72dab-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="72dab-118">Actions</span><span class="sxs-lookup"><span data-stu-id="72dab-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="72dab-119">Representa el conjunto de acciones que se pueden realizar en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="72dab-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="72dab-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="72dab-120">Text value</span></span>

<span data-ttu-id="72dab-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="72dab-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="72dab-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="72dab-122">Remarks</span></span>

<span data-ttu-id="72dab-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="72dab-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="72dab-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="72dab-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72dab-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="72dab-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="72dab-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="72dab-126">Schema Name</span></span>  <br/> |<span data-ttu-id="72dab-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="72dab-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="72dab-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="72dab-128">Validation File</span></span>  <br/> |<span data-ttu-id="72dab-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="72dab-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="72dab-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="72dab-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="72dab-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="72dab-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="72dab-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="72dab-132">See also</span></span>



- [<span data-ttu-id="72dab-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="72dab-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

