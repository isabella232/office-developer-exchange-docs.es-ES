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
description: El elemento Address representa una dirección de correo electrónico completamente resuelta.
ms.openlocfilehash: 591bc675165ec80f69407bd8ee19d16c9ddff15a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464906"
---
# <a name="address-emailaddresstype"></a><span data-ttu-id="7ae92-103">Dirección (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="7ae92-103">Address (EmailAddressType)</span></span>

<span data-ttu-id="7ae92-104">El elemento **Address** representa una dirección de correo electrónico completamente resuelta.</span><span class="sxs-lookup"><span data-stu-id="7ae92-104">The **Address** element represents a fully resolved e-mail address.</span></span> 
  
```XML
<Address>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Address >
```

 <span data-ttu-id="7ae92-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="7ae92-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7ae92-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7ae92-106">Attributes and elements</span></span>

<span data-ttu-id="7ae92-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7ae92-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7ae92-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7ae92-108">Attributes</span></span>

<span data-ttu-id="7ae92-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7ae92-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7ae92-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7ae92-110">Child elements</span></span>

|<span data-ttu-id="7ae92-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7ae92-111">**Element**</span></span>|<span data-ttu-id="7ae92-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7ae92-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ae92-113">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="7ae92-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="7ae92-114">Define el nombre del usuario del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="7ae92-114">Defines the name of the mailbox user.</span></span> <span data-ttu-id="7ae92-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="7ae92-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="7ae92-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="7ae92-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="7ae92-117">Define la dirección del Protocolo simple de transferencia de correo (SMTP) de un usuario de buzón.</span><span class="sxs-lookup"><span data-stu-id="7ae92-117">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="7ae92-118">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="7ae92-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="7ae92-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="7ae92-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="7ae92-120">Define la ruta que se usa para el buzón.</span><span class="sxs-lookup"><span data-stu-id="7ae92-120">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="7ae92-121">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="7ae92-121">The default is SMTP.</span></span> <span data-ttu-id="7ae92-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="7ae92-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="7ae92-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="7ae92-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="7ae92-124">Define el tipo de buzón de un usuario de buzón.</span><span class="sxs-lookup"><span data-stu-id="7ae92-124">Defines the mailbox type of a mailbox user.</span></span> <span data-ttu-id="7ae92-125">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="7ae92-125">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="7ae92-126">ItemId</span><span class="sxs-lookup"><span data-stu-id="7ae92-126">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="7ae92-127">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="7ae92-127">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder.</span></span> <span data-ttu-id="7ae92-128">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="7ae92-128">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7ae92-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7ae92-129">Parent elements</span></span>

|<span data-ttu-id="7ae92-130">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7ae92-130">**Element**</span></span>|<span data-ttu-id="7ae92-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7ae92-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ae92-132">OriginalRecipients</span><span class="sxs-lookup"><span data-stu-id="7ae92-132">OriginalRecipients</span></span>](originalrecipients.md) <br/> |<span data-ttu-id="7ae92-133">Contiene una colección de direcciones de correo electrónico que representan a los destinatarios originales de un mensaje con seguimiento.</span><span class="sxs-lookup"><span data-stu-id="7ae92-133">Contains a collection of e-mail addresses that represent the original recipients of a tracked message.</span></span>  <br/> |
|[<span data-ttu-id="7ae92-134">RoomLists</span><span class="sxs-lookup"><span data-stu-id="7ae92-134">RoomLists</span></span>](roomlists.md) <br/> |<span data-ttu-id="7ae92-135">Contiene una lista de las salas de reuniones de una organización.</span><span class="sxs-lookup"><span data-stu-id="7ae92-135">Contains a list of meeting rooms in an organization.</span></span>  <br/> |
|[<span data-ttu-id="7ae92-136">SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="7ae92-136">SentToAddresses</span></span>](senttoaddresses.md) <br/> |<span data-ttu-id="7ae92-137">Contiene una lista de direcciones de correo electrónico a las que se deben enviar los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="7ae92-137">Contains a list of e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7ae92-138">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7ae92-138">Text value</span></span>

<span data-ttu-id="7ae92-139">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7ae92-139">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7ae92-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ae92-140">Remarks</span></span>

<span data-ttu-id="7ae92-141">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7ae92-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7ae92-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7ae92-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ae92-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="7ae92-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7ae92-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7ae92-144">Schema Name</span></span>  <br/> |<span data-ttu-id="7ae92-145">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7ae92-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="7ae92-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7ae92-146">Validation File</span></span>  <br/> |<span data-ttu-id="7ae92-147">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="7ae92-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7ae92-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7ae92-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="7ae92-149">Falso</span><span class="sxs-lookup"><span data-stu-id="7ae92-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ae92-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ae92-150">See also</span></span>

- [<span data-ttu-id="7ae92-151">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="7ae92-151">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md) 
- [<span data-ttu-id="7ae92-152">Operación GetRoomLists</span><span class="sxs-lookup"><span data-stu-id="7ae92-152">GetRoomLists operation</span></span>](getroomlists-operation.md)
- [<span data-ttu-id="7ae92-153">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7ae92-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

