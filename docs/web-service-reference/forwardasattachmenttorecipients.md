---
title: ForwardAsAttachmentToRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ForwardAsAttachmentToRecipients
api_type:
- schema
ms.assetid: 8649ea14-672f-43c9-b10a-a2b02efd5867
description: El elemento ForwardAsAttachmentToRecipients indica las direcciones de correo electrónico a las que se deben reenviar los mensajes como datos adjuntos.
ms.openlocfilehash: bf8c3563460eea811602074bf16f9253b4610832
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44453339"
---
# <a name="forwardasattachmenttorecipients"></a><span data-ttu-id="2b8bc-103">ForwardAsAttachmentToRecipients</span><span class="sxs-lookup"><span data-stu-id="2b8bc-103">ForwardAsAttachmentToRecipients</span></span>

<span data-ttu-id="2b8bc-104">El elemento **ForwardAsAttachmentToRecipients** indica las direcciones de correo electrónico a las que se deben reenviar los mensajes como datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="2b8bc-104">The **ForwardAsAttachmentToRecipients** element indicates the e-mail addresses to which messages are to be forwarded as attachments.</span></span> 
  
```XML
<ForwardAsAttachmentToRecipients>
   <Address/>
</ForwardAsAttachmentToRecipients>
```

 <span data-ttu-id="2b8bc-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="2b8bc-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2b8bc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2b8bc-106">Attributes and elements</span></span>

<span data-ttu-id="2b8bc-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2b8bc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b8bc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2b8bc-108">Attributes</span></span>

<span data-ttu-id="2b8bc-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2b8bc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2b8bc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2b8bc-110">Child elements</span></span>

|<span data-ttu-id="2b8bc-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2b8bc-111">**Element**</span></span>|<span data-ttu-id="2b8bc-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b8bc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b8bc-113">Dirección (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="2b8bc-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="2b8bc-114">Representa una dirección de correo electrónico completamente resuelta.</span><span class="sxs-lookup"><span data-stu-id="2b8bc-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2b8bc-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2b8bc-115">Parent elements</span></span>

|<span data-ttu-id="2b8bc-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2b8bc-116">**Element**</span></span>|<span data-ttu-id="2b8bc-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b8bc-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b8bc-118">Actions</span><span class="sxs-lookup"><span data-stu-id="2b8bc-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="2b8bc-119">Representa el conjunto de acciones que se pueden realizar en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="2b8bc-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2b8bc-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2b8bc-120">Text value</span></span>

<span data-ttu-id="2b8bc-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2b8bc-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2b8bc-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2b8bc-122">Remarks</span></span>

<span data-ttu-id="2b8bc-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2b8bc-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2b8bc-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2b8bc-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b8bc-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b8bc-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2b8bc-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2b8bc-126">Schema Name</span></span>  <br/> |<span data-ttu-id="2b8bc-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2b8bc-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2b8bc-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2b8bc-128">Validation File</span></span>  <br/> |<span data-ttu-id="2b8bc-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2b8bc-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2b8bc-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2b8bc-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="2b8bc-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="2b8bc-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b8bc-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b8bc-132">See also</span></span>



- [<span data-ttu-id="2b8bc-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2b8bc-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

