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
description: El elemento FederatedDeliveryMailbox representa el buzón de correo al que se envió un mensaje entre locales.
ms.openlocfilehash: d493ed81e82237b7257e8c469f4552d931b73aa6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461950"
---
# <a name="federateddeliverymailbox"></a><span data-ttu-id="afdbb-103">FederatedDeliveryMailbox</span><span class="sxs-lookup"><span data-stu-id="afdbb-103">FederatedDeliveryMailbox</span></span>

<span data-ttu-id="afdbb-104">El elemento **FederatedDeliveryMailbox** representa el buzón de correo al que se envió un mensaje entre locales.</span><span class="sxs-lookup"><span data-stu-id="afdbb-104">The **FederatedDeliveryMailbox** element represents the mailbox to which a cross-premise message was sent.</span></span> 
  
```XML
<FederatedDeliveryMailbox>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</FederatedDeliveryMailbox>
```

 <span data-ttu-id="afdbb-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="afdbb-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="afdbb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="afdbb-106">Attributes and elements</span></span>

<span data-ttu-id="afdbb-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="afdbb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="afdbb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="afdbb-108">Attributes</span></span>

<span data-ttu-id="afdbb-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="afdbb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="afdbb-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="afdbb-110">Child elements</span></span>

|<span data-ttu-id="afdbb-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="afdbb-111">**Element**</span></span>|<span data-ttu-id="afdbb-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="afdbb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afdbb-113">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="afdbb-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="afdbb-114">Define el nombre del usuario del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="afdbb-114">Defines the name of the mailbox user.</span></span> <span data-ttu-id="afdbb-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="afdbb-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="afdbb-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="afdbb-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="afdbb-117">Define la dirección del Protocolo simple de transferencia de correo (SMTP) de un usuario de buzón.</span><span class="sxs-lookup"><span data-stu-id="afdbb-117">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="afdbb-118">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="afdbb-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="afdbb-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="afdbb-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="afdbb-120">Define la ruta que se usa para el buzón.</span><span class="sxs-lookup"><span data-stu-id="afdbb-120">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="afdbb-121">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="afdbb-121">The default is SMTP.</span></span> <span data-ttu-id="afdbb-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="afdbb-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="afdbb-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="afdbb-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="afdbb-124">Define el tipo de buzón de un usuario de buzón.</span><span class="sxs-lookup"><span data-stu-id="afdbb-124">Defines the mailbox type of a mailbox user.</span></span> <span data-ttu-id="afdbb-125">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="afdbb-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="afdbb-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="afdbb-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="afdbb-127">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="afdbb-127">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder.</span></span> <span data-ttu-id="afdbb-128">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="afdbb-128">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="afdbb-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="afdbb-129">Parent elements</span></span>

|<span data-ttu-id="afdbb-130">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="afdbb-130">**Element**</span></span>|<span data-ttu-id="afdbb-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="afdbb-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afdbb-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="afdbb-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="afdbb-133">Contiene los criterios para los tipos de mensajes que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="afdbb-133">Contains criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="afdbb-134">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="afdbb-134">Text value</span></span>

<span data-ttu-id="afdbb-135">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="afdbb-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="afdbb-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="afdbb-136">Remarks</span></span>

<span data-ttu-id="afdbb-137">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="afdbb-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="afdbb-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="afdbb-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="afdbb-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="afdbb-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="afdbb-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="afdbb-140">Schema Name</span></span>  <br/> |<span data-ttu-id="afdbb-141">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="afdbb-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="afdbb-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="afdbb-142">Validation File</span></span>  <br/> |<span data-ttu-id="afdbb-143">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="afdbb-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="afdbb-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="afdbb-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="afdbb-145">Falso</span><span class="sxs-lookup"><span data-stu-id="afdbb-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="afdbb-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="afdbb-146">See also</span></span>



- [<span data-ttu-id="afdbb-147">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="afdbb-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

