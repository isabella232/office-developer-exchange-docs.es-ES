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
description: El elemento RoomList representa una dirección de correo electrónico que identifica una lista de salas de reuniones.
ms.openlocfilehash: 0444475cb9fffbb89ba2861096baee0c7e645995
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460522"
---
# <a name="roomlist"></a><span data-ttu-id="44742-103">RoomList</span><span class="sxs-lookup"><span data-stu-id="44742-103">RoomList</span></span>

<span data-ttu-id="44742-104">El elemento **RoomList** representa una dirección de correo electrónico que identifica una lista de salas de reuniones.</span><span class="sxs-lookup"><span data-stu-id="44742-104">The **RoomList** element represents an e-mail address that identifies a list of meeting rooms.</span></span> 
  
[<span data-ttu-id="44742-105">GetRooms</span><span class="sxs-lookup"><span data-stu-id="44742-105">GetRooms</span></span>](getrooms.md)
  
[<span data-ttu-id="44742-106">RoomList</span><span class="sxs-lookup"><span data-stu-id="44742-106">RoomList</span></span>](roomlist.md)
  
```XML
<RoomList>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</RoomList>
```

 <span data-ttu-id="44742-107">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="44742-107">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44742-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="44742-108">Attributes and elements</span></span>

<span data-ttu-id="44742-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="44742-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44742-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="44742-110">Attributes</span></span>

<span data-ttu-id="44742-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="44742-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44742-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="44742-112">Child elements</span></span>

|<span data-ttu-id="44742-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="44742-113">**Element**</span></span>|<span data-ttu-id="44742-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44742-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44742-115">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="44742-115">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="44742-116">Define el nombre para mostrar de la lista de salas.</span><span class="sxs-lookup"><span data-stu-id="44742-116">Defines the display name of the room list.</span></span> <span data-ttu-id="44742-117">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="44742-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="44742-118">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="44742-118">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="44742-119">Define la dirección del Protocolo simple de transferencia de correo (SMTP) de una lista de salas.</span><span class="sxs-lookup"><span data-stu-id="44742-119">Defines the Simple Mail Transfer Protocol (SMTP) address of a room list.</span></span> <span data-ttu-id="44742-120">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="44742-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="44742-121">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="44742-121">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="44742-122">Define la ruta que se usa para el buzón.</span><span class="sxs-lookup"><span data-stu-id="44742-122">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="44742-123">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="44742-123">The default is SMTP.</span></span> <span data-ttu-id="44742-124">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="44742-124">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="44742-125">MailboxType</span><span class="sxs-lookup"><span data-stu-id="44742-125">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="44742-126">Define el tipo de buzón de un usuario de buzón.</span><span class="sxs-lookup"><span data-stu-id="44742-126">Defines the mailbox type of a mailbox user.</span></span> <span data-ttu-id="44742-127">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="44742-127">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="44742-128">ItemId</span><span class="sxs-lookup"><span data-stu-id="44742-128">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="44742-129">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="44742-129">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder.</span></span> <span data-ttu-id="44742-130">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="44742-130">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="44742-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="44742-131">Parent elements</span></span>

|<span data-ttu-id="44742-132">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="44742-132">**Element**</span></span>|<span data-ttu-id="44742-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44742-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44742-134">GetRooms</span><span class="sxs-lookup"><span data-stu-id="44742-134">GetRooms</span></span>](getrooms.md) <br/> |<span data-ttu-id="44742-135">El elemento raíz de una solicitud para obtener una lista de salas dentro de una lista de salas determinada.</span><span class="sxs-lookup"><span data-stu-id="44742-135">The root element in a request to get a list of rooms within a particular room list.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="44742-136">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="44742-136">Text value</span></span>

<span data-ttu-id="44742-137">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="44742-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44742-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="44742-138">Remarks</span></span>

<span data-ttu-id="44742-139">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="44742-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44742-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="44742-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44742-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="44742-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="44742-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="44742-142">Schema Name</span></span>  <br/> |<span data-ttu-id="44742-143">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="44742-143">Messages schema</span></span>  <br/> |
|<span data-ttu-id="44742-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="44742-144">Validation File</span></span>  <br/> |<span data-ttu-id="44742-145">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="44742-145">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="44742-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="44742-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="44742-147">Falso</span><span class="sxs-lookup"><span data-stu-id="44742-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44742-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="44742-148">See also</span></span>



[<span data-ttu-id="44742-149">Operación GetRooms</span><span class="sxs-lookup"><span data-stu-id="44742-149">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="44742-150">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="44742-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

