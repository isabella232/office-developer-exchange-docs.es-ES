---
title: Identificador (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Id
api_type:
- schema
ms.assetid: 3e1e37b5-5469-4447-ad1f-c2c6d4e0482f
description: El elemento Id identifica una sala de reuniones dentro de la organización de Exchange server.
ms.openlocfilehash: 5cd62f6f4e5912d2ecccda352be15c6a3b24e06c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835847"
---
# <a name="id-emailaddresstype"></a><span data-ttu-id="f3377-103">Identificador (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="f3377-103">Id (EmailAddressType)</span></span>

<span data-ttu-id="f3377-104">El elemento **Id** identifica una sala de reuniones dentro de la organización de Exchange server.</span><span class="sxs-lookup"><span data-stu-id="f3377-104">The **Id** element identifies a meeting room within the Exchange server organization.</span></span> 
  
[<span data-ttu-id="f3377-105">Salón</span><span class="sxs-lookup"><span data-stu-id="f3377-105">Room</span></span>](room.md)
  
[<span data-ttu-id="f3377-106">Identificador (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="f3377-106">Id (EmailAddressType)</span></span>](id-emailaddresstype.md)
  
```xml
<Id>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Id>
```

 <span data-ttu-id="f3377-107">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="f3377-107">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f3377-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f3377-108">Attributes and elements</span></span>

<span data-ttu-id="f3377-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f3377-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3377-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="f3377-110">Attributes</span></span>

<span data-ttu-id="f3377-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f3377-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f3377-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f3377-112">Child elements</span></span>

|<span data-ttu-id="f3377-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f3377-113">**Element**</span></span>|<span data-ttu-id="f3377-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f3377-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3377-115">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="f3377-115">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="f3377-116">Define el nombre de la sala de reuniones.</span><span class="sxs-lookup"><span data-stu-id="f3377-116">Defines the name of the meeting room.</span></span> <span data-ttu-id="f3377-117">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="f3377-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="f3377-118">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="f3377-118">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="f3377-119">Define la dirección de Protocolo Simple de transferencia de correo (SMTP) de una sala de reuniones.</span><span class="sxs-lookup"><span data-stu-id="f3377-119">Defines the Simple Mail Transfer Protocol (SMTP) address of a meeting room.</span></span> <span data-ttu-id="f3377-120">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="f3377-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="f3377-121">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="f3377-121">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="f3377-122">Define la ruta que se usa para el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f3377-122">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="f3377-123">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="f3377-123">The default is SMTP.</span></span> <span data-ttu-id="f3377-124">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="f3377-124">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="f3377-125">MailboxType</span><span class="sxs-lookup"><span data-stu-id="f3377-125">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="f3377-126">Define el tipo de buzón de correo de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f3377-126">Defines the mailbox type of a mailbox user.</span></span> <span data-ttu-id="f3377-127">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="f3377-127">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="f3377-128">ItemId</span><span class="sxs-lookup"><span data-stu-id="f3377-128">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="f3377-129">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="f3377-129">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder.</span></span> <span data-ttu-id="f3377-130">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="f3377-130">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f3377-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f3377-131">Parent elements</span></span>

|<span data-ttu-id="f3377-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="f3377-132">**Element**</span></span>|<span data-ttu-id="f3377-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f3377-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3377-134">Salón</span><span class="sxs-lookup"><span data-stu-id="f3377-134">Room</span></span>](room.md) <br/> |<span data-ttu-id="f3377-135">Define una sala de reuniones en la organización de Exchange server.</span><span class="sxs-lookup"><span data-stu-id="f3377-135">Defines a meeting room in the Exchange server organization.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3377-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3377-136">Remarks</span></span>

<span data-ttu-id="f3377-137">El esquema que describe este elemento se encuentra en el directorio EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f3377-137">The schema that describes this element is located in the EWS directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f3377-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f3377-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3377-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f3377-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f3377-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f3377-140">Schema Name</span></span>  <br/> |<span data-ttu-id="f3377-141">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f3377-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="f3377-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f3377-142">Validation File</span></span>  <br/> |<span data-ttu-id="f3377-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f3377-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f3377-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f3377-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="f3377-145">False</span><span class="sxs-lookup"><span data-stu-id="f3377-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f3377-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3377-146">See also</span></span>



[<span data-ttu-id="f3377-147">Operación GetRooms</span><span class="sxs-lookup"><span data-stu-id="f3377-147">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="f3377-148">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f3377-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

