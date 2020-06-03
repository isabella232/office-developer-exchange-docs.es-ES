---
title: Destinatario
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recipient
api_type:
- schema
ms.assetid: 52adbb30-3bfd-48aa-9ea8-9f7d3b4bee44
description: El elemento recipient representa el destinatario para el que se ha producido el evento.
ms.openlocfilehash: eb7e85acf3c2b898b3f0bff4b63168d344e1daa8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465859"
---
# <a name="recipient"></a><span data-ttu-id="c575e-103">Destinatario</span><span class="sxs-lookup"><span data-stu-id="c575e-103">Recipient</span></span>

<span data-ttu-id="c575e-104">El elemento **Recipient** representa el destinatario para el que se ha producido el evento.</span><span class="sxs-lookup"><span data-stu-id="c575e-104">The **Recipient** element represents the recipient for whom the event occurred.</span></span> 
  
```XML
<Recipient>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Recipient>
```

 <span data-ttu-id="c575e-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="c575e-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c575e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c575e-106">Attributes and elements</span></span>

<span data-ttu-id="c575e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c575e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c575e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c575e-108">Attributes</span></span>

<span data-ttu-id="c575e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c575e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c575e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c575e-110">Child elements</span></span>

|<span data-ttu-id="c575e-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c575e-111">**Element**</span></span>|<span data-ttu-id="c575e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c575e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c575e-113">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="c575e-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="c575e-114">Representa el nombre del usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="c575e-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="c575e-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="c575e-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c575e-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="c575e-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="c575e-117">Define la dirección principal del Protocolo simple de transferencia de correo (SMTP) de un usuario de buzón.</span><span class="sxs-lookup"><span data-stu-id="c575e-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="c575e-118">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="c575e-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c575e-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="c575e-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="c575e-120">Define la ruta que se usa para el buzón.</span><span class="sxs-lookup"><span data-stu-id="c575e-120">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="c575e-121">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="c575e-121">The default value is SMTP.</span></span> <span data-ttu-id="c575e-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="c575e-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c575e-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="c575e-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="c575e-124">Representa el tipo de buzón que se representa mediante la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c575e-124">Represents the type of mailbox that is represented by the e-mail address.</span></span> <span data-ttu-id="c575e-125">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="c575e-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c575e-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="c575e-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="c575e-127">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="c575e-127">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder.</span></span> <span data-ttu-id="c575e-128">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="c575e-128">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c575e-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c575e-129">Parent elements</span></span>

|<span data-ttu-id="c575e-130">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c575e-130">**Element**</span></span>|<span data-ttu-id="c575e-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c575e-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c575e-132">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="c575e-132">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="c575e-133">Contiene información de un evento único para un destinatario.</span><span class="sxs-lookup"><span data-stu-id="c575e-133">Contains information for a single event for a recipient.</span></span>  <br/> |
|[<span data-ttu-id="c575e-134">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="c575e-134">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="c575e-135">Especifica los criterios para los tipos de mensajes que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="c575e-135">Specifies criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c575e-136">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c575e-136">Text value</span></span>

<span data-ttu-id="c575e-137">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c575e-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c575e-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c575e-138">Remarks</span></span>

<span data-ttu-id="c575e-139">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c575e-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c575e-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c575e-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c575e-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="c575e-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c575e-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c575e-142">Schema Name</span></span>  <br/> |<span data-ttu-id="c575e-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c575e-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="c575e-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c575e-144">Validation File</span></span>  <br/> |<span data-ttu-id="c575e-145">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c575e-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c575e-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c575e-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="c575e-147">Falso</span><span class="sxs-lookup"><span data-stu-id="c575e-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c575e-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="c575e-148">See also</span></span>



- [<span data-ttu-id="c575e-149">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c575e-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

