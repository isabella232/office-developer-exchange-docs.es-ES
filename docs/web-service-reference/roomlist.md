---
title: RoomList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoomList
api_type:
- schema
ms.assetid: cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2
description: El elemento RoomList representa una dirección de correo electrónico que identifica una lista de las salas de reuniones.
ms.openlocfilehash: 7de2c67f8001387abf463186933f0b81ee45a58a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837262"
---
# <a name="roomlist"></a><span data-ttu-id="59522-103">RoomList</span><span class="sxs-lookup"><span data-stu-id="59522-103">RoomList</span></span>

<span data-ttu-id="59522-104">El elemento **RoomList** representa una dirección de correo electrónico que identifica una lista de las salas de reuniones.</span><span class="sxs-lookup"><span data-stu-id="59522-104">The **RoomList** element represents an e-mail address that identifies a list of meeting rooms.</span></span> 
  
[<span data-ttu-id="59522-105">GetRooms</span><span class="sxs-lookup"><span data-stu-id="59522-105">GetRooms</span></span>](getrooms.md)
  
[<span data-ttu-id="59522-106">RoomList</span><span class="sxs-lookup"><span data-stu-id="59522-106">RoomList</span></span>](roomlist.md)
  
```XML
<RoomList>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</RoomList>
```

 <span data-ttu-id="59522-107">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="59522-107">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="59522-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="59522-108">Attributes and elements</span></span>

<span data-ttu-id="59522-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="59522-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="59522-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="59522-110">Attributes</span></span>

<span data-ttu-id="59522-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="59522-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="59522-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="59522-112">Child elements</span></span>

|<span data-ttu-id="59522-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="59522-113">**Element**</span></span>|<span data-ttu-id="59522-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="59522-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59522-115">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="59522-115">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="59522-116">Define el nombre para mostrar de la lista de salas.</span><span class="sxs-lookup"><span data-stu-id="59522-116">Defines the display name of the room list.</span></span> <span data-ttu-id="59522-117">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="59522-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="59522-118">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="59522-118">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="59522-119">Define la dirección de Protocolo Simple de transferencia de correo (SMTP) de una lista de salas.</span><span class="sxs-lookup"><span data-stu-id="59522-119">Defines the Simple Mail Transfer Protocol (SMTP) address of a room list.</span></span> <span data-ttu-id="59522-120">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="59522-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="59522-121">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="59522-121">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="59522-122">Define la ruta que se usa para el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="59522-122">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="59522-123">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="59522-123">The default is SMTP.</span></span> <span data-ttu-id="59522-124">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="59522-124">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="59522-125">MailboxType</span><span class="sxs-lookup"><span data-stu-id="59522-125">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="59522-126">Define el tipo de buzón de correo de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="59522-126">Defines the mailbox type of a mailbox user.</span></span> <span data-ttu-id="59522-127">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="59522-127">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="59522-128">ItemId</span><span class="sxs-lookup"><span data-stu-id="59522-128">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="59522-129">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="59522-129">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder.</span></span> <span data-ttu-id="59522-130">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="59522-130">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="59522-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="59522-131">Parent elements</span></span>

|<span data-ttu-id="59522-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="59522-132">**Element**</span></span>|<span data-ttu-id="59522-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="59522-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59522-134">GetRooms</span><span class="sxs-lookup"><span data-stu-id="59522-134">GetRooms</span></span>](getrooms.md) <br/> |<span data-ttu-id="59522-135">El elemento raíz en una solicitud para obtener una lista de salas dentro de una lista de salas determinado.</span><span class="sxs-lookup"><span data-stu-id="59522-135">The root element in a request to get a list of rooms within a particular room list.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="59522-136">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="59522-136">Text value</span></span>

<span data-ttu-id="59522-137">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="59522-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="59522-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="59522-138">Remarks</span></span>

<span data-ttu-id="59522-139">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="59522-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59522-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="59522-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59522-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="59522-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="59522-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="59522-142">Schema Name</span></span>  <br/> |<span data-ttu-id="59522-143">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="59522-143">Messages schema</span></span>  <br/> |
|<span data-ttu-id="59522-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="59522-144">Validation File</span></span>  <br/> |<span data-ttu-id="59522-145">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="59522-145">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="59522-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="59522-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="59522-147">False</span><span class="sxs-lookup"><span data-stu-id="59522-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59522-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="59522-148">See also</span></span>



[<span data-ttu-id="59522-149">Operación GetRooms</span><span class="sxs-lookup"><span data-stu-id="59522-149">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="59522-150">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="59522-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

