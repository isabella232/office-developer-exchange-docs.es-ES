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
description: El elemento PurportedSender contiene información de contacto para el remitente presunta de un mensaje de correo electrónico.
ms.openlocfilehash: 1e5b74d60d824c06834cf988557ef64fb84d70c4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836937"
---
# <a name="purportedsender"></a><span data-ttu-id="3bc48-103">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="3bc48-103">PurportedSender</span></span>

<span data-ttu-id="3bc48-104">El elemento **PurportedSender** contiene información de contacto para el remitente presunta de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="3bc48-104">The **PurportedSender** element contains contact information for the alleged sender of an e-mail message.</span></span> 
  
```XML
<PurportedSender>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</PurportedSender>
```

 <span data-ttu-id="3bc48-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="3bc48-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3bc48-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3bc48-106">Attributes and elements</span></span>

<span data-ttu-id="3bc48-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3bc48-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3bc48-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3bc48-108">Attributes</span></span>

<span data-ttu-id="3bc48-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3bc48-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3bc48-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3bc48-110">Child elements</span></span>

|<span data-ttu-id="3bc48-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3bc48-111">**Element**</span></span>|<span data-ttu-id="3bc48-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3bc48-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3bc48-113">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="3bc48-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="3bc48-114">Representa el nombre del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="3bc48-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="3bc48-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="3bc48-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3bc48-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="3bc48-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="3bc48-117">Define la dirección de Protocolo Simple de transferencia de correo (SMTP) de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="3bc48-117">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="3bc48-118">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="3bc48-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3bc48-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="3bc48-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="3bc48-120">Representa el protocolo de enrutamiento para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="3bc48-120">Represents the routing protocol for the recipient.</span></span> <span data-ttu-id="3bc48-121">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="3bc48-121">The default value is SMTP.</span></span> <span data-ttu-id="3bc48-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="3bc48-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3bc48-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="3bc48-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="3bc48-124">Representa el tipo de buzón de correo que está representada por la dirección de correo electrónico..</span><span class="sxs-lookup"><span data-stu-id="3bc48-124">Represents the type of mailbox that is represented by the e-mail address..</span></span> <span data-ttu-id="3bc48-125">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="3bc48-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3bc48-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="3bc48-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="3bc48-127">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="3bc48-127">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder.</span></span> <span data-ttu-id="3bc48-128">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="3bc48-128">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3bc48-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3bc48-129">Parent elements</span></span>

|<span data-ttu-id="3bc48-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="3bc48-130">**Element**</span></span>|<span data-ttu-id="3bc48-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3bc48-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3bc48-132">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="3bc48-132">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="3bc48-133">Especifica los criterios para los tipos de mensajes para buscar.</span><span class="sxs-lookup"><span data-stu-id="3bc48-133">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="3bc48-134">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="3bc48-134">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="3bc48-135">Contiene un solo mensaje que se devuelve en una [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="3bc48-135">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="3bc48-136">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="3bc48-136">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="3bc48-137">Contiene un resultado de mensaje único para un elemento [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="3bc48-137">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3bc48-138">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3bc48-138">Text value</span></span>

<span data-ttu-id="3bc48-139">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3bc48-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3bc48-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3bc48-140">Remarks</span></span>

<span data-ttu-id="3bc48-141">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3bc48-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3bc48-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3bc48-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3bc48-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3bc48-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3bc48-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3bc48-144">Schema Name</span></span>  <br/> |<span data-ttu-id="3bc48-145">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3bc48-145">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3bc48-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3bc48-146">Validation File</span></span>  <br/> |<span data-ttu-id="3bc48-147">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3bc48-147">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3bc48-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3bc48-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="3bc48-149">False</span><span class="sxs-lookup"><span data-stu-id="3bc48-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3bc48-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bc48-150">See also</span></span>



[<span data-ttu-id="3bc48-151">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="3bc48-151">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="3bc48-152">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3bc48-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

