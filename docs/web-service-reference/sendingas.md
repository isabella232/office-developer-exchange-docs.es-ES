---
title: SendingAs
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
description: El elemento SendingAs representa una dirección de correo electrónico que un usuario está intentando enviar como.
ms.openlocfilehash: a5468ddb8facf99038d319252f7e1c780a888ca1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837338"
---
# <a name="sendingas"></a><span data-ttu-id="c1ba7-103">SendingAs</span><span class="sxs-lookup"><span data-stu-id="c1ba7-103">SendingAs</span></span>

<span data-ttu-id="c1ba7-104">El elemento **SendingAs** representa una dirección de correo electrónico que un usuario está intentando enviar como.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-104">The **SendingAs** element represents an e-mail address that a user is trying to send as.</span></span> 
  
```XML
<SendingAs>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</SendingAs>
```

 <span data-ttu-id="c1ba7-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="c1ba7-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1ba7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c1ba7-106">Attributes and elements</span></span>

<span data-ttu-id="c1ba7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1ba7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c1ba7-108">Attributes</span></span>

<span data-ttu-id="c1ba7-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1ba7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c1ba7-110">Child elements</span></span>

|<span data-ttu-id="c1ba7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1ba7-111">**Element**</span></span>|<span data-ttu-id="c1ba7-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1ba7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1ba7-113">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="c1ba7-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="c1ba7-114">Representa el nombre del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="c1ba7-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c1ba7-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="c1ba7-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="c1ba7-117">Define la dirección de Protocolo Simple de transferencia de correo (SMTP) principal de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="c1ba7-118">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c1ba7-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="c1ba7-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="c1ba7-120">Define el tipo de dirección para el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-120">Defines the address type for the mailbox.</span></span> <span data-ttu-id="c1ba7-121">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-121">The default is SMTP.</span></span> <span data-ttu-id="c1ba7-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c1ba7-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="c1ba7-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="c1ba7-124">Representa el tipo de buzón de correo que está representada por un usuario de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-124">Represents the type of mailbox that is represented by an e-mail user.</span></span> <span data-ttu-id="c1ba7-125">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c1ba7-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="c1ba7-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="c1ba7-127">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-127">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder.</span></span> <span data-ttu-id="c1ba7-128">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-128">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c1ba7-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c1ba7-129">Parent elements</span></span>

|<span data-ttu-id="c1ba7-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1ba7-130">**Element**</span></span>|<span data-ttu-id="c1ba7-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1ba7-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1ba7-132">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="c1ba7-132">GetMailTips</span></span>](getmailtips.md) <br/> |<span data-ttu-id="c1ba7-133">Contiene los destinatarios y los tipos de sugerencias de correo para recuperar.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-133">Contains the recipients and types of mail tips to retrieve.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c1ba7-134">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c1ba7-134">Text value</span></span>

<span data-ttu-id="c1ba7-135">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c1ba7-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1ba7-136">Remarks</span></span>

<span data-ttu-id="c1ba7-137">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1ba7-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1ba7-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c1ba7-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1ba7-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c1ba7-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c1ba7-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c1ba7-140">Schema Name</span></span>  <br/> |<span data-ttu-id="c1ba7-141">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c1ba7-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c1ba7-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c1ba7-142">Validation File</span></span>  <br/> |<span data-ttu-id="c1ba7-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c1ba7-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c1ba7-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c1ba7-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1ba7-145">False</span><span class="sxs-lookup"><span data-stu-id="c1ba7-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1ba7-146">Ver también</span><span class="sxs-lookup"><span data-stu-id="c1ba7-146">See also</span></span>



- [<span data-ttu-id="c1ba7-147">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c1ba7-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

