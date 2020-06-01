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
description: El elemento entry representa una sola dirección de correo electrónico de un contacto.
ms.openlocfilehash: 766d67cda10b02c07a7677e541fddfc38a4285cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459647"
---
# <a name="entry-emailaddress"></a><span data-ttu-id="d1c98-103">Entrada (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="d1c98-103">Entry (EmailAddress)</span></span>

<span data-ttu-id="d1c98-104">El elemento **entry** representa una sola dirección de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="d1c98-104">The **Entry** element represents a single e-mail address for a contact.</span></span> 
  
```XML
<Entry Key="" Name="" RoutingType="" MailboxType="" />
```

<span data-ttu-id="d1c98-105">**EmailAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="d1c98-105">**EmailAddressDictionaryEntryType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d1c98-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d1c98-106">Attributes and elements</span></span>

<span data-ttu-id="d1c98-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d1c98-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1c98-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d1c98-108">Attributes</span></span>

|<span data-ttu-id="d1c98-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="d1c98-109">**Attribute**</span></span>|<span data-ttu-id="d1c98-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d1c98-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d1c98-111">**Key**</span><span class="sxs-lookup"><span data-stu-id="d1c98-111">**Key**</span></span> <br/> | <span data-ttu-id="d1c98-112">Identifica la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="d1c98-112">Identifies the e-mail address.</span></span><br/><br/><span data-ttu-id="d1c98-113">A continuación se muestran los valores posibles para este atributo:</span><span class="sxs-lookup"><span data-stu-id="d1c98-113">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="d1c98-114">- EmailAddress1</span><span class="sxs-lookup"><span data-stu-id="d1c98-114">-  EmailAddress1</span></span>  <br/><span data-ttu-id="d1c98-115">- EmailAddress2</span><span class="sxs-lookup"><span data-stu-id="d1c98-115">-  EmailAddress2</span></span>  <br/><span data-ttu-id="d1c98-116">- EmailAddress3</span><span class="sxs-lookup"><span data-stu-id="d1c98-116">-  EmailAddress3</span></span> <br/><br/>  <span data-ttu-id="d1c98-117">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d1c98-117">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="d1c98-118">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d1c98-118">**Name**</span></span> <br/> |<span data-ttu-id="d1c98-119">Define el nombre del usuario del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d1c98-119">Defines the name of the mailbox user.</span></span> <span data-ttu-id="d1c98-120">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="d1c98-120">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="d1c98-121">**RoutingType**</span><span class="sxs-lookup"><span data-stu-id="d1c98-121">**RoutingType**</span></span> <br/> |<span data-ttu-id="d1c98-122">Define la ruta que se usa para el buzón.</span><span class="sxs-lookup"><span data-stu-id="d1c98-122">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="d1c98-123">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="d1c98-123">The default is SMTP.</span></span> <span data-ttu-id="d1c98-124">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="d1c98-124">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="d1c98-125">**MailboxType**</span><span class="sxs-lookup"><span data-stu-id="d1c98-125">**MailboxType**</span></span> <br/> |<span data-ttu-id="d1c98-126">Define el tipo de buzón de un usuario de buzón.</span><span class="sxs-lookup"><span data-stu-id="d1c98-126">Defines the mailbox type of a mailbox user.</span></span> <span data-ttu-id="d1c98-127">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="d1c98-127">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d1c98-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d1c98-128">Child elements</span></span>

<span data-ttu-id="d1c98-129">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d1c98-129">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d1c98-130">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d1c98-130">Parent elements</span></span>

|<span data-ttu-id="d1c98-131">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d1c98-131">**Element**</span></span>|<span data-ttu-id="d1c98-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d1c98-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1c98-133">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="d1c98-133">EmailAddresses</span></span>](emailaddresses.md) <br/> |<span data-ttu-id="d1c98-134">Representa una colección de direcciones de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="d1c98-134">Represents a collection of e-mail addresses for a contact.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1c98-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d1c98-135">Remarks</span></span>

<span data-ttu-id="d1c98-136">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d1c98-136">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d1c98-137">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d1c98-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d1c98-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d1c98-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1c98-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1c98-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d1c98-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d1c98-140">Schema name</span></span>  <br/> |<span data-ttu-id="d1c98-141">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d1c98-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="d1c98-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d1c98-142">Validation file</span></span>  <br/> |<span data-ttu-id="d1c98-143">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d1c98-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d1c98-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d1c98-144">Can be empty</span></span>  <br/> |<span data-ttu-id="d1c98-145">Falso</span><span class="sxs-lookup"><span data-stu-id="d1c98-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1c98-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1c98-146">See also</span></span>

- [<span data-ttu-id="d1c98-147">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d1c98-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

