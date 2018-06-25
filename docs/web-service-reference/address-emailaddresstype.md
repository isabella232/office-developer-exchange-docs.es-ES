---
title: Dirección (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Address
api_type:
- schema
ms.assetid: 518641c8-7f6f-496c-86f9-341e7c1bb44c
description: El elemento de dirección representa una dirección de correo electrónico completa resuelta.
ms.openlocfilehash: 2a2d409edcc3a04bf82c6da0080183becfc9b25b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763481"
---
# <a name="address-emailaddresstype"></a><span data-ttu-id="e9509-103">Dirección (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="e9509-103">Address (EmailAddressType)</span></span>

<span data-ttu-id="e9509-104">El elemento de **dirección** representa una dirección de correo electrónico completa resuelta.</span><span class="sxs-lookup"><span data-stu-id="e9509-104">The **Address** element represents a fully resolved e-mail address.</span></span> 
  
```XML
<Address>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Address >
```

 <span data-ttu-id="e9509-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="e9509-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e9509-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e9509-106">Attributes and elements</span></span>

<span data-ttu-id="e9509-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e9509-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e9509-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e9509-108">Attributes</span></span>

<span data-ttu-id="e9509-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e9509-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e9509-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e9509-110">Child elements</span></span>

|<span data-ttu-id="e9509-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e9509-111">**Element**</span></span>|<span data-ttu-id="e9509-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e9509-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9509-113">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="e9509-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="e9509-114">Define el nombre del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e9509-114">Defines the name of the mailbox user.</span></span> <span data-ttu-id="e9509-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="e9509-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="e9509-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="e9509-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="e9509-117">Define la dirección de Protocolo Simple de transferencia de correo (SMTP) de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e9509-117">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="e9509-118">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="e9509-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="e9509-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="e9509-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="e9509-120">Define la ruta que se usa para el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e9509-120">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="e9509-121">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="e9509-121">The default is SMTP.</span></span> <span data-ttu-id="e9509-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="e9509-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="e9509-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="e9509-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="e9509-124">Define el tipo de buzón de correo de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e9509-124">Defines the mailbox type of a mailbox user.</span></span> <span data-ttu-id="e9509-125">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="e9509-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="e9509-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="e9509-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="e9509-127">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="e9509-127">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder.</span></span> <span data-ttu-id="e9509-128">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="e9509-128">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e9509-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e9509-129">Parent elements</span></span>

|<span data-ttu-id="e9509-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="e9509-130">**Element**</span></span>|<span data-ttu-id="e9509-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e9509-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9509-132">OriginalRecipients</span><span class="sxs-lookup"><span data-stu-id="e9509-132">OriginalRecipients</span></span>](originalrecipients.md) <br/> |<span data-ttu-id="e9509-133">Contiene una colección de direcciones de correo electrónico que representan a los destinatarios originales de un mensaje de marca de revisión.</span><span class="sxs-lookup"><span data-stu-id="e9509-133">Contains a collection of e-mail addresses that represent the original recipients of a tracked message.</span></span>  <br/> |
|[<span data-ttu-id="e9509-134">RoomLists</span><span class="sxs-lookup"><span data-stu-id="e9509-134">RoomLists</span></span>](roomlists.md) <br/> |<span data-ttu-id="e9509-135">Contiene una lista de salas en una organización de reuniones.</span><span class="sxs-lookup"><span data-stu-id="e9509-135">Contains a list of meeting rooms in an organization.</span></span>  <br/> |
|[<span data-ttu-id="e9509-136">SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="e9509-136">SentToAddresses</span></span>](senttoaddresses.md) <br/> |<span data-ttu-id="e9509-137">Contiene una lista de direcciones de correo electrónico que se han enviado en orden para la condición o la excepción que se debe aplicar a los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="e9509-137">Contains a list of e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e9509-138">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e9509-138">Text value</span></span>

<span data-ttu-id="e9509-139">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e9509-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e9509-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e9509-140">Remarks</span></span>

<span data-ttu-id="e9509-141">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e9509-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e9509-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e9509-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e9509-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e9509-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e9509-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e9509-144">Schema Name</span></span>  <br/> |<span data-ttu-id="e9509-145">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e9509-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="e9509-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e9509-146">Validation File</span></span>  <br/> |<span data-ttu-id="e9509-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e9509-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e9509-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e9509-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="e9509-149">False</span><span class="sxs-lookup"><span data-stu-id="e9509-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9509-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9509-150">See also</span></span>

- [<span data-ttu-id="e9509-151">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="e9509-151">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md) 
- [<span data-ttu-id="e9509-152">Operación GetRoomLists</span><span class="sxs-lookup"><span data-stu-id="e9509-152">GetRoomLists operation</span></span>](getroomlists-operation.md)
- [<span data-ttu-id="e9509-153">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e9509-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

