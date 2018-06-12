---
title: RecipientAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientAddress
api_type:
- schema
ms.assetid: 9ae6351a-2c60-4715-a489-5681a13641f9
description: El elemento RecipientAddress representa el buzón de correo del destinatario.
ms.openlocfilehash: 10928ac206227cfc21bd83ab5bfa9a55aad354e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836974"
---
# <a name="recipientaddress"></a><span data-ttu-id="4a87a-103">RecipientAddress</span><span class="sxs-lookup"><span data-stu-id="4a87a-103">RecipientAddress</span></span>

<span data-ttu-id="4a87a-104">El elemento **RecipientAddress** representa el buzón de correo del destinatario.</span><span class="sxs-lookup"><span data-stu-id="4a87a-104">The **RecipientAddress** element represents the mailbox of the recipient.</span></span> 
  
```xml
<RecipientAddress>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</RecipientAddress>
```

 <span data-ttu-id="4a87a-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="4a87a-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4a87a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4a87a-106">Attributes and elements</span></span>

<span data-ttu-id="4a87a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4a87a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4a87a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4a87a-108">Attributes</span></span>

<span data-ttu-id="4a87a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4a87a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4a87a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4a87a-110">Child elements</span></span>

|<span data-ttu-id="4a87a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4a87a-111">**Element**</span></span>|<span data-ttu-id="4a87a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4a87a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a87a-113">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="4a87a-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="4a87a-114">Representa el nombre del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="4a87a-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="4a87a-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="4a87a-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="4a87a-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="4a87a-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="4a87a-117">Define la dirección de Protocolo Simple de transferencia de correo (SMTP) de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="4a87a-117">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user.</span></span> <span data-ttu-id="4a87a-118">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="4a87a-118">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="4a87a-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="4a87a-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="4a87a-120">Representa el protocolo de enrutamiento para el destinatario.</span><span class="sxs-lookup"><span data-stu-id="4a87a-120">Represents the routing protocol for the recipient.</span></span> <span data-ttu-id="4a87a-121">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="4a87a-121">The default is SMTP.</span></span> <span data-ttu-id="4a87a-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="4a87a-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="4a87a-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="4a87a-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="4a87a-124">Representa el tipo de buzón de correo que está representada por la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4a87a-124">Represents the type of mailbox that is represented by the e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="4a87a-125">ItemId</span><span class="sxs-lookup"><span data-stu-id="4a87a-125">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="4a87a-126">Define el identificador de elemento de un contacto o una lista de distribución privada para los destinatarios de la carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="4a87a-126">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder.</span></span> <span data-ttu-id="4a87a-127">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="4a87a-127">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4a87a-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4a87a-128">Parent elements</span></span>

|<span data-ttu-id="4a87a-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="4a87a-129">**Element**</span></span>|<span data-ttu-id="4a87a-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4a87a-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a87a-131">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="4a87a-131">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="4a87a-132">Representa los valores de distintos tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="4a87a-132">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a87a-133">Notas</span><span class="sxs-lookup"><span data-stu-id="4a87a-133">Remarks</span></span>

<span data-ttu-id="4a87a-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="4a87a-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4a87a-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4a87a-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a87a-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4a87a-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4a87a-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4a87a-137">Schema Name</span></span>  <br/> |<span data-ttu-id="4a87a-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4a87a-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="4a87a-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4a87a-139">Validation File</span></span>  <br/> |<span data-ttu-id="4a87a-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4a87a-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4a87a-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4a87a-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="4a87a-142">False</span><span class="sxs-lookup"><span data-stu-id="4a87a-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4a87a-143">Ver también</span><span class="sxs-lookup"><span data-stu-id="4a87a-143">See also</span></span>



- [<span data-ttu-id="4a87a-144">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4a87a-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

