---
title: Remitente (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Sender
api_type:
- schema
ms.assetid: 717eb6d0-d167-4b20-92e2-5d08b96186c4
description: El elemento Sender representa la dirección de correo electrónico del remitente del mensaje.
ms.openlocfilehash: 23a487f216a110796d40f3d3e86224c691acc004
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455327"
---
# <a name="sender-emailaddresstype"></a><span data-ttu-id="5d5d1-103">Remitente (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="5d5d1-103">Sender (EmailAddressType)</span></span>

<span data-ttu-id="5d5d1-104">El elemento **Sender** representa la dirección de correo electrónico del remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-104">The **Sender** element represents the e-mail address for the sender of the message.</span></span> 
  
```XML
<Sender>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Sender>
```

 <span data-ttu-id="5d5d1-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="5d5d1-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5d5d1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5d5d1-106">Attributes and elements</span></span>

<span data-ttu-id="5d5d1-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d5d1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5d5d1-108">Attributes</span></span>

<span data-ttu-id="5d5d1-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5d5d1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5d5d1-110">Child elements</span></span>

|<span data-ttu-id="5d5d1-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5d5d1-111">**Element**</span></span>|<span data-ttu-id="5d5d1-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d5d1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d5d1-113">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="5d5d1-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="5d5d1-114">Representa el nombre del usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="5d5d1-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="5d5d1-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="5d5d1-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="5d5d1-117">Define la dirección principal del Protocolo simple de transferencia de correo (SMTP) de un usuario de buzón.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="5d5d1-118">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="5d5d1-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="5d5d1-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="5d5d1-120">Representa el protocolo de enrutamiento para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-120">Represents the routing protocol for the recipient.</span></span> <span data-ttu-id="5d5d1-121">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-121">The default value is SMTP.</span></span> <span data-ttu-id="5d5d1-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="5d5d1-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="5d5d1-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="5d5d1-124">Representa el tipo de buzón que se representa mediante la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-124">Represents the type of mailbox that is represented by the e-mail address.</span></span> <span data-ttu-id="5d5d1-125">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="5d5d1-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="5d5d1-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="5d5d1-127">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-127">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder.</span></span> <span data-ttu-id="5d5d1-128">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-128">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5d5d1-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5d5d1-129">Parent elements</span></span>

|<span data-ttu-id="5d5d1-130">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5d5d1-130">**Element**</span></span>|<span data-ttu-id="5d5d1-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d5d1-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d5d1-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="5d5d1-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="5d5d1-133">Especifica los criterios para los tipos de mensajes que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-133">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="5d5d1-134">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="5d5d1-134">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="5d5d1-135">Contiene un único resultado de mensaje para un elemento [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="5d5d1-135">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
|[<span data-ttu-id="5d5d1-136">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="5d5d1-136">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="5d5d1-137">Contiene un solo mensaje que se devuelve en una [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="5d5d1-137">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5d5d1-138">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5d5d1-138">Text value</span></span>

<span data-ttu-id="5d5d1-139">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5d5d1-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d5d1-140">Remarks</span></span>

<span data-ttu-id="5d5d1-141">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5d5d1-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5d5d1-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5d5d1-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d5d1-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d5d1-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5d5d1-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5d5d1-144">Schema Name</span></span>  <br/> |<span data-ttu-id="5d5d1-145">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5d5d1-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="5d5d1-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5d5d1-146">Validation File</span></span>  <br/> |<span data-ttu-id="5d5d1-147">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5d5d1-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5d5d1-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5d5d1-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="5d5d1-149">Falso</span><span class="sxs-lookup"><span data-stu-id="5d5d1-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d5d1-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d5d1-150">See also</span></span>



[<span data-ttu-id="5d5d1-151">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="5d5d1-151">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="5d5d1-152">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5d5d1-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

