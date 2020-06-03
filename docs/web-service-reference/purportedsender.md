---
title: PurportedSender
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PurportedSender
api_type:
- schema
ms.assetid: eb7a54ec-2e48-4030-bbcf-50a31609691b
description: El elemento PurportedSender contiene información de contacto del remitente de un mensaje de correo electrónico.
ms.openlocfilehash: 5ecf352484a423e3955736620bf5a65c4e98099a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468337"
---
# <a name="purportedsender"></a><span data-ttu-id="28a51-103">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="28a51-103">PurportedSender</span></span>

<span data-ttu-id="28a51-104">El elemento **PurportedSender** contiene información de contacto del remitente de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="28a51-104">The **PurportedSender** element contains contact information for the alleged sender of an e-mail message.</span></span> 
  
```XML
<PurportedSender>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</PurportedSender>
```

 <span data-ttu-id="28a51-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="28a51-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28a51-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="28a51-106">Attributes and elements</span></span>

<span data-ttu-id="28a51-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="28a51-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28a51-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="28a51-108">Attributes</span></span>

<span data-ttu-id="28a51-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="28a51-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="28a51-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="28a51-110">Child elements</span></span>

|<span data-ttu-id="28a51-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="28a51-111">**Element**</span></span>|<span data-ttu-id="28a51-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28a51-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28a51-113">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="28a51-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="28a51-114">Representa el nombre del usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="28a51-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="28a51-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="28a51-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="28a51-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="28a51-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="28a51-117">Define la dirección del Protocolo simple de transferencia de correo (SMTP) de un usuario de buzón.</span><span class="sxs-lookup"><span data-stu-id="28a51-117">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="28a51-118">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="28a51-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="28a51-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="28a51-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="28a51-120">Representa el protocolo de enrutamiento para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="28a51-120">Represents the routing protocol for the recipient.</span></span> <span data-ttu-id="28a51-121">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="28a51-121">The default value is SMTP.</span></span> <span data-ttu-id="28a51-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="28a51-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="28a51-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="28a51-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="28a51-124">Representa el tipo de buzón que se representa mediante la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="28a51-124">Represents the type of mailbox that is represented by the e-mail address..</span></span> <span data-ttu-id="28a51-125">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="28a51-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="28a51-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="28a51-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="28a51-127">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="28a51-127">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder.</span></span> <span data-ttu-id="28a51-128">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="28a51-128">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="28a51-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="28a51-129">Parent elements</span></span>

|<span data-ttu-id="28a51-130">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="28a51-130">**Element**</span></span>|<span data-ttu-id="28a51-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28a51-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28a51-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="28a51-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="28a51-133">Especifica los criterios para los tipos de mensajes que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="28a51-133">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="28a51-134">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="28a51-134">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="28a51-135">Contiene un solo mensaje que se devuelve en una [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="28a51-135">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="28a51-136">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="28a51-136">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="28a51-137">Contiene un único resultado de mensaje para un elemento [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="28a51-137">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="28a51-138">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="28a51-138">Text value</span></span>

<span data-ttu-id="28a51-139">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="28a51-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28a51-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="28a51-140">Remarks</span></span>

<span data-ttu-id="28a51-141">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="28a51-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28a51-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="28a51-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28a51-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="28a51-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="28a51-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="28a51-144">Schema Name</span></span>  <br/> |<span data-ttu-id="28a51-145">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="28a51-145">Messages schema</span></span>  <br/> |
|<span data-ttu-id="28a51-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="28a51-146">Validation File</span></span>  <br/> |<span data-ttu-id="28a51-147">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="28a51-147">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="28a51-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="28a51-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="28a51-149">Falso</span><span class="sxs-lookup"><span data-stu-id="28a51-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28a51-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="28a51-150">See also</span></span>



[<span data-ttu-id="28a51-151">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="28a51-151">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="28a51-152">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="28a51-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

