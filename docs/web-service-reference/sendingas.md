---
title: Envíoas
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendingAs
api_type:
- schema
ms.assetid: b43ce19f-9ab0-4946-acb2-c5aafead9d35
description: El elemento sendas representa una dirección de correo electrónico que un usuario intenta enviar como.
ms.openlocfilehash: cd11bd60cbbe3434fcc1b0b9a1cfe0de9f0b1e21
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462139"
---
# <a name="sendingas"></a><span data-ttu-id="36df3-103">Envíoas</span><span class="sxs-lookup"><span data-stu-id="36df3-103">SendingAs</span></span>

<span data-ttu-id="36df3-104">El **elemento** sendas representa una dirección de correo electrónico que un usuario intenta enviar como.</span><span class="sxs-lookup"><span data-stu-id="36df3-104">The **SendingAs** element represents an e-mail address that a user is trying to send as.</span></span> 
  
```XML
<SendingAs>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</SendingAs>
```

 <span data-ttu-id="36df3-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="36df3-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="36df3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="36df3-106">Attributes and elements</span></span>

<span data-ttu-id="36df3-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="36df3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36df3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="36df3-108">Attributes</span></span>

<span data-ttu-id="36df3-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="36df3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="36df3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="36df3-110">Child elements</span></span>

|<span data-ttu-id="36df3-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="36df3-111">**Element**</span></span>|<span data-ttu-id="36df3-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="36df3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36df3-113">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="36df3-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="36df3-114">Representa el nombre del usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="36df3-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="36df3-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="36df3-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="36df3-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="36df3-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="36df3-117">Define la dirección principal del Protocolo simple de transferencia de correo (SMTP) de un usuario de buzón.</span><span class="sxs-lookup"><span data-stu-id="36df3-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="36df3-118">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="36df3-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="36df3-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="36df3-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="36df3-120">Define el tipo de dirección para el buzón.</span><span class="sxs-lookup"><span data-stu-id="36df3-120">Defines the address type for the mailbox.</span></span> <span data-ttu-id="36df3-121">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="36df3-121">The default is SMTP.</span></span> <span data-ttu-id="36df3-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="36df3-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="36df3-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="36df3-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="36df3-124">Representa el tipo de buzón que está representado por un usuario de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="36df3-124">Represents the type of mailbox that is represented by an e-mail user.</span></span> <span data-ttu-id="36df3-125">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="36df3-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="36df3-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="36df3-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="36df3-127">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="36df3-127">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder.</span></span> <span data-ttu-id="36df3-128">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="36df3-128">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="36df3-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="36df3-129">Parent elements</span></span>

|<span data-ttu-id="36df3-130">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="36df3-130">**Element**</span></span>|<span data-ttu-id="36df3-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="36df3-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36df3-132">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="36df3-132">GetMailTips</span></span>](getmailtips.md) <br/> |<span data-ttu-id="36df3-133">Contiene los destinatarios y los tipos de sugerencias de correo que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="36df3-133">Contains the recipients and types of mail tips to retrieve.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="36df3-134">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="36df3-134">Text value</span></span>

<span data-ttu-id="36df3-135">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="36df3-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="36df3-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="36df3-136">Remarks</span></span>

<span data-ttu-id="36df3-137">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="36df3-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="36df3-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="36df3-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36df3-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="36df3-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="36df3-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="36df3-140">Schema Name</span></span>  <br/> |<span data-ttu-id="36df3-141">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="36df3-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="36df3-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="36df3-142">Validation File</span></span>  <br/> |<span data-ttu-id="36df3-143">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="36df3-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="36df3-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="36df3-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="36df3-145">Falso</span><span class="sxs-lookup"><span data-stu-id="36df3-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36df3-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="36df3-146">See also</span></span>



- [<span data-ttu-id="36df3-147">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="36df3-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

