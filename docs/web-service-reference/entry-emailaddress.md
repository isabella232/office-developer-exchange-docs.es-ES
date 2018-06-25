---
title: Entrada (EmailAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Entry
api_type:
- schema
ms.assetid: b028c5c7-3494-4ecd-96d1-78783daa660f
description: El elemento de entrada representa una dirección de correo electrónico única para un contacto.
ms.openlocfilehash: 1852584e507c38da030815c37f85f7c4af4e2ba4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764424"
---
# <a name="entry-emailaddress"></a><span data-ttu-id="bb662-103">Entrada (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="bb662-103">Entry (EmailAddress)</span></span>

<span data-ttu-id="bb662-104">El elemento de **entrada** representa una dirección de correo electrónico única para un contacto.</span><span class="sxs-lookup"><span data-stu-id="bb662-104">The **Entry** element represents a single e-mail address for a contact.</span></span> 
  
```XML
<Entry Key="" Name="" RoutingType="" MailboxType="" />
```

<span data-ttu-id="bb662-105">**EmailAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="bb662-105">**EmailAddressDictionaryEntryType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="bb662-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bb662-106">Attributes and elements</span></span>

<span data-ttu-id="bb662-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bb662-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb662-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="bb662-108">Attributes</span></span>

|<span data-ttu-id="bb662-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="bb662-109">**Attribute**</span></span>|<span data-ttu-id="bb662-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb662-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb662-111">**Clave**</span><span class="sxs-lookup"><span data-stu-id="bb662-111">**Key**</span></span> <br/> | <span data-ttu-id="bb662-112">Identifica la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="bb662-112">Identifies the e-mail address.</span></span><br/><br/><span data-ttu-id="bb662-113">Los siguientes son los valores posibles para este atributo:</span><span class="sxs-lookup"><span data-stu-id="bb662-113">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="bb662-114">-EmailAddress1</span><span class="sxs-lookup"><span data-stu-id="bb662-114">-  EmailAddress1</span></span>  <br/><span data-ttu-id="bb662-115">-EmailAddress2</span><span class="sxs-lookup"><span data-stu-id="bb662-115">-  EmailAddress2</span></span>  <br/><span data-ttu-id="bb662-116">-EmailAddress3</span><span class="sxs-lookup"><span data-stu-id="bb662-116">-  EmailAddress3</span></span> <br/><br/>  <span data-ttu-id="bb662-117">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="bb662-117">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="bb662-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="bb662-118">**Name**</span></span> <br/> |<span data-ttu-id="bb662-119">Define el nombre del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="bb662-119">Defines the name of the mailbox user.</span></span> <span data-ttu-id="bb662-120">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="bb662-120">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="bb662-121">**RoutingType**</span><span class="sxs-lookup"><span data-stu-id="bb662-121">**RoutingType**</span></span> <br/> |<span data-ttu-id="bb662-122">Define la ruta que se usa para el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="bb662-122">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="bb662-123">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="bb662-123">The default is SMTP.</span></span> <span data-ttu-id="bb662-124">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="bb662-124">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="bb662-125">**MailboxType**</span><span class="sxs-lookup"><span data-stu-id="bb662-125">**MailboxType**</span></span> <br/> |<span data-ttu-id="bb662-126">Define el tipo de buzón de correo de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="bb662-126">Defines the mailbox type of a mailbox user.</span></span> <span data-ttu-id="bb662-127">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="bb662-127">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bb662-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bb662-128">Child elements</span></span>

<span data-ttu-id="bb662-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bb662-129">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bb662-130">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bb662-130">Parent elements</span></span>

|<span data-ttu-id="bb662-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="bb662-131">**Element**</span></span>|<span data-ttu-id="bb662-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb662-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb662-133">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="bb662-133">EmailAddresses</span></span>](emailaddresses.md) <br/> |<span data-ttu-id="bb662-134">Representa una colección de direcciones de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="bb662-134">Represents a collection of e-mail addresses for a contact.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb662-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb662-135">Remarks</span></span>

<span data-ttu-id="bb662-136">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bb662-136">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="bb662-137">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="bb662-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bb662-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bb662-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb662-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bb662-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bb662-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bb662-140">Schema name</span></span>  <br/> |<span data-ttu-id="bb662-141">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="bb662-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="bb662-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bb662-142">Validation file</span></span>  <br/> |<span data-ttu-id="bb662-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bb662-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bb662-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bb662-144">Can be empty</span></span>  <br/> |<span data-ttu-id="bb662-145">False</span><span class="sxs-lookup"><span data-stu-id="bb662-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb662-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb662-146">See also</span></span>

- [<span data-ttu-id="bb662-147">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="bb662-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

