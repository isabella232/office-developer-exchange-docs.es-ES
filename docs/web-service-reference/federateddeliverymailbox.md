---
title: FederatedDeliveryMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FederatedDeliveryMailbox
api_type:
- schema
ms.assetid: cd56bcc0-d24a-4e8b-87bd-999bf69234b7
description: El elemento FederatedDeliveryMailbox representa el buzón al que se envió un mensaje entre locales.
ms.openlocfilehash: 4a9250455f8de3ede25f2b5ba9433690137ca1d3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764583"
---
# <a name="federateddeliverymailbox"></a><span data-ttu-id="f52a0-103">FederatedDeliveryMailbox</span><span class="sxs-lookup"><span data-stu-id="f52a0-103">FederatedDeliveryMailbox</span></span>

<span data-ttu-id="f52a0-104">El elemento **FederatedDeliveryMailbox** representa el buzón al que se envió un mensaje entre locales.</span><span class="sxs-lookup"><span data-stu-id="f52a0-104">The **FederatedDeliveryMailbox** element represents the mailbox to which a cross-premise message was sent.</span></span> 
  
```XML
<FederatedDeliveryMailbox>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</FederatedDeliveryMailbox>
```

 <span data-ttu-id="f52a0-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="f52a0-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f52a0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f52a0-106">Attributes and elements</span></span>

<span data-ttu-id="f52a0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f52a0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f52a0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f52a0-108">Attributes</span></span>

<span data-ttu-id="f52a0-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f52a0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f52a0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f52a0-110">Child elements</span></span>

|<span data-ttu-id="f52a0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f52a0-111">**Element**</span></span>|<span data-ttu-id="f52a0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f52a0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f52a0-113">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="f52a0-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="f52a0-114">Define el nombre del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f52a0-114">Defines the name of the mailbox user.</span></span> <span data-ttu-id="f52a0-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="f52a0-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="f52a0-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="f52a0-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="f52a0-117">Define la dirección de Protocolo Simple de transferencia de correo (SMTP) de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f52a0-117">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="f52a0-118">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="f52a0-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="f52a0-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="f52a0-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="f52a0-120">Define la ruta que se usa para el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f52a0-120">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="f52a0-121">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="f52a0-121">The default is SMTP.</span></span> <span data-ttu-id="f52a0-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="f52a0-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="f52a0-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="f52a0-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="f52a0-124">Define el tipo de buzón de correo de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f52a0-124">Defines the mailbox type of a mailbox user.</span></span> <span data-ttu-id="f52a0-125">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="f52a0-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="f52a0-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="f52a0-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="f52a0-127">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="f52a0-127">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder.</span></span> <span data-ttu-id="f52a0-128">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="f52a0-128">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f52a0-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f52a0-129">Parent elements</span></span>

|<span data-ttu-id="f52a0-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="f52a0-130">**Element**</span></span>|<span data-ttu-id="f52a0-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f52a0-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f52a0-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="f52a0-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="f52a0-133">Contiene los criterios para los tipos de mensajes para buscar.</span><span class="sxs-lookup"><span data-stu-id="f52a0-133">Contains criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f52a0-134">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f52a0-134">Text value</span></span>

<span data-ttu-id="f52a0-135">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f52a0-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f52a0-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f52a0-136">Remarks</span></span>

<span data-ttu-id="f52a0-137">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f52a0-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f52a0-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f52a0-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f52a0-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f52a0-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f52a0-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f52a0-140">Schema Name</span></span>  <br/> |<span data-ttu-id="f52a0-141">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f52a0-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f52a0-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f52a0-142">Validation File</span></span>  <br/> |<span data-ttu-id="f52a0-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f52a0-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f52a0-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f52a0-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="f52a0-145">False</span><span class="sxs-lookup"><span data-stu-id="f52a0-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f52a0-146">Ver también</span><span class="sxs-lookup"><span data-stu-id="f52a0-146">See also</span></span>



- [<span data-ttu-id="f52a0-147">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f52a0-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

