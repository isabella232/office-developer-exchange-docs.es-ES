---
title: RecipientFilter
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientFilter
api_type:
- schema
ms.assetid: 956c287a-a38a-49a7-a877-6d2088dfbc06
description: El elemento RecipientFilter representa una dirección de destinatario para usar con el informe de seguimiento de mensajes especificado.
ms.openlocfilehash: c31ed469132b110a690416b112d5e4e96e44c501
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836972"
---
# <a name="recipientfilter"></a><span data-ttu-id="3c17f-103">RecipientFilter</span><span class="sxs-lookup"><span data-stu-id="3c17f-103">RecipientFilter</span></span>

<span data-ttu-id="3c17f-104">El elemento **RecipientFilter** representa una dirección de destinatario para usar con el informe de seguimiento de mensajes especificado.</span><span class="sxs-lookup"><span data-stu-id="3c17f-104">The **RecipientFilter** element represents a recipient address to use with the specified message tracking report.</span></span> 
  
```XML
 <RecipientFilter>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</RecipientFilter>
```

 <span data-ttu-id="3c17f-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="3c17f-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3c17f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3c17f-106">Attributes and elements</span></span>

<span data-ttu-id="3c17f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3c17f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c17f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3c17f-108">Attributes</span></span>

<span data-ttu-id="3c17f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3c17f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3c17f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3c17f-110">Child elements</span></span>

|<span data-ttu-id="3c17f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c17f-111">**Element**</span></span>|<span data-ttu-id="3c17f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3c17f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c17f-113">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="3c17f-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="3c17f-114">Representa el nombre del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="3c17f-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="3c17f-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="3c17f-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3c17f-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="3c17f-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="3c17f-117">Define la dirección de Protocolo Simple de transferencia de correo (SMTP) principal de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="3c17f-117">Defines the primary Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="3c17f-118">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="3c17f-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3c17f-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="3c17f-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="3c17f-120">Representa el protocolo de enrutamiento para este destinatario.</span><span class="sxs-lookup"><span data-stu-id="3c17f-120">Represents the routing protocol for this recipient.</span></span> <span data-ttu-id="3c17f-121">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="3c17f-121">The default value is SMTP.</span></span> <span data-ttu-id="3c17f-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="3c17f-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3c17f-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="3c17f-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="3c17f-124">Representa el tipo de buzón de correo que está representada por la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="3c17f-124">Represents the type of mailbox that is represented by the e-mail address.</span></span> <span data-ttu-id="3c17f-125">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="3c17f-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="3c17f-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="3c17f-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="3c17f-127">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="3c17f-127">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder.</span></span> <span data-ttu-id="3c17f-128">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="3c17f-128">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3c17f-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3c17f-129">Parent elements</span></span>

|<span data-ttu-id="3c17f-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c17f-130">**Element**</span></span>|<span data-ttu-id="3c17f-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3c17f-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c17f-132">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="3c17f-132">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="3c17f-133">Contiene la solicitud para la [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md) recuperar el mensaje completo informe de seguimiento para el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="3c17f-133">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3c17f-134">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3c17f-134">Text value</span></span>

<span data-ttu-id="3c17f-135">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3c17f-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3c17f-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3c17f-136">Remarks</span></span>

<span data-ttu-id="3c17f-137">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3c17f-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c17f-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3c17f-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c17f-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3c17f-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3c17f-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3c17f-140">Schema Name</span></span>  <br/> |<span data-ttu-id="3c17f-141">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3c17f-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3c17f-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3c17f-142">Validation File</span></span>  <br/> |<span data-ttu-id="3c17f-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3c17f-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3c17f-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3c17f-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="3c17f-145">False</span><span class="sxs-lookup"><span data-stu-id="3c17f-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c17f-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c17f-146">See also</span></span>



[<span data-ttu-id="3c17f-147">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="3c17f-147">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="3c17f-148">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3c17f-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

