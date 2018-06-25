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
description: El elemento de destinatario representa al destinatario para el que se produjo el evento.
ms.openlocfilehash: e8e8f9d6031d27c7441017c85eb26a143258b183
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836971"
---
# <a name="recipient"></a><span data-ttu-id="90950-103">Destinatario</span><span class="sxs-lookup"><span data-stu-id="90950-103">Recipient</span></span>

<span data-ttu-id="90950-104">El elemento de **destinatario** representa al destinatario para el que se produjo el evento.</span><span class="sxs-lookup"><span data-stu-id="90950-104">The **Recipient** element represents the recipient for whom the event occurred.</span></span> 
  
```XML
<Recipient>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Recipient>
```

 <span data-ttu-id="90950-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="90950-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="90950-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="90950-106">Attributes and elements</span></span>

<span data-ttu-id="90950-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="90950-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="90950-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="90950-108">Attributes</span></span>

<span data-ttu-id="90950-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="90950-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="90950-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="90950-110">Child elements</span></span>

|<span data-ttu-id="90950-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="90950-111">**Element**</span></span>|<span data-ttu-id="90950-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90950-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90950-113">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="90950-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="90950-114">Representa el nombre del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="90950-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="90950-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="90950-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="90950-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="90950-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="90950-117">Define la dirección de Protocolo Simple de transferencia de correo (SMTP) principal de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="90950-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="90950-118">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="90950-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="90950-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="90950-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="90950-120">Define la ruta que se usa para el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="90950-120">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="90950-121">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="90950-121">The default value is SMTP.</span></span> <span data-ttu-id="90950-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="90950-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="90950-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="90950-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="90950-124">Representa el tipo de buzón de correo que está representada por la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="90950-124">Represents the type of mailbox that is represented by the e-mail address.</span></span> <span data-ttu-id="90950-125">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="90950-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="90950-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="90950-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="90950-127">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="90950-127">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder.</span></span> <span data-ttu-id="90950-128">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="90950-128">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="90950-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="90950-129">Parent elements</span></span>

|<span data-ttu-id="90950-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="90950-130">**Element**</span></span>|<span data-ttu-id="90950-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90950-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90950-132">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="90950-132">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="90950-133">Contiene información de un solo evento de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="90950-133">Contains information for a single event for a recipient.</span></span>  <br/> |
|[<span data-ttu-id="90950-134">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="90950-134">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="90950-135">Especifica los criterios para los tipos de mensajes para buscar.</span><span class="sxs-lookup"><span data-stu-id="90950-135">Specifies criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="90950-136">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="90950-136">Text value</span></span>

<span data-ttu-id="90950-137">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="90950-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="90950-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="90950-138">Remarks</span></span>

<span data-ttu-id="90950-139">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="90950-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="90950-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="90950-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90950-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="90950-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="90950-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="90950-142">Schema Name</span></span>  <br/> |<span data-ttu-id="90950-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="90950-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="90950-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="90950-144">Validation File</span></span>  <br/> |<span data-ttu-id="90950-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="90950-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="90950-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="90950-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="90950-147">False</span><span class="sxs-lookup"><span data-stu-id="90950-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="90950-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="90950-148">See also</span></span>



- [<span data-ttu-id="90950-149">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="90950-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

