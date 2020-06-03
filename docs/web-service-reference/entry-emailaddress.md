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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459647"
---
# <a name="entry-emailaddress"></a><span data-ttu-id="d625e-103">Entrada (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="d625e-103">Entry (EmailAddress)</span></span>

<span data-ttu-id="d625e-104">El elemento **entry** representa una sola dirección de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="d625e-104">The **Entry** element represents a single e-mail address for a contact.</span></span> 
  
```XML
<Entry Key="" Name="" RoutingType="" MailboxType="" />
```

<span data-ttu-id="d625e-105">**EmailAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="d625e-105">**EmailAddressDictionaryEntryType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d625e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d625e-106">Attributes and elements</span></span>

<span data-ttu-id="d625e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d625e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d625e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d625e-108">Attributes</span></span>

|<span data-ttu-id="d625e-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="d625e-109">**Attribute**</span></span>|<span data-ttu-id="d625e-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d625e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d625e-111">**Key**</span><span class="sxs-lookup"><span data-stu-id="d625e-111">**Key**</span></span> <br/> | <span data-ttu-id="d625e-112">Identifica la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="d625e-112">Identifies the e-mail address.</span></span><br/><br/><span data-ttu-id="d625e-113">A continuación se muestran los valores posibles para este atributo:</span><span class="sxs-lookup"><span data-stu-id="d625e-113">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="d625e-114">- EmailAddress1</span><span class="sxs-lookup"><span data-stu-id="d625e-114">-  EmailAddress1</span></span>  <br/><span data-ttu-id="d625e-115">- EmailAddress2</span><span class="sxs-lookup"><span data-stu-id="d625e-115">-  EmailAddress2</span></span>  <br/><span data-ttu-id="d625e-116">- EmailAddress3</span><span class="sxs-lookup"><span data-stu-id="d625e-116">-  EmailAddress3</span></span> <br/><br/>  <span data-ttu-id="d625e-117">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d625e-117">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="d625e-118">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d625e-118">**Name**</span></span> <br/> |<span data-ttu-id="d625e-119">Define el nombre del usuario del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d625e-119">Defines the name of the mailbox user.</span></span> <span data-ttu-id="d625e-120">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="d625e-120">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="d625e-121">**RoutingType**</span><span class="sxs-lookup"><span data-stu-id="d625e-121">**RoutingType**</span></span> <br/> |<span data-ttu-id="d625e-122">Define la ruta que se usa para el buzón.</span><span class="sxs-lookup"><span data-stu-id="d625e-122">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="d625e-123">El valor predeterminado es SMTP.</span><span class="sxs-lookup"><span data-stu-id="d625e-123">The default is SMTP.</span></span> <span data-ttu-id="d625e-124">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="d625e-124">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="d625e-125">**MailboxType**</span><span class="sxs-lookup"><span data-stu-id="d625e-125">**MailboxType**</span></span> <br/> |<span data-ttu-id="d625e-126">Define el tipo de buzón de un usuario de buzón.</span><span class="sxs-lookup"><span data-stu-id="d625e-126">Defines the mailbox type of a mailbox user.</span></span> <span data-ttu-id="d625e-127">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="d625e-127">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d625e-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d625e-128">Child elements</span></span>

<span data-ttu-id="d625e-129">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d625e-129">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d625e-130">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d625e-130">Parent elements</span></span>

|<span data-ttu-id="d625e-131">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d625e-131">**Element**</span></span>|<span data-ttu-id="d625e-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d625e-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d625e-133">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="d625e-133">EmailAddresses</span></span>](emailaddresses.md) <br/> |<span data-ttu-id="d625e-134">Representa una colección de direcciones de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="d625e-134">Represents a collection of e-mail addresses for a contact.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d625e-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d625e-135">Remarks</span></span>

<span data-ttu-id="d625e-136">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d625e-136">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d625e-137">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d625e-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d625e-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d625e-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d625e-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="d625e-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d625e-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d625e-140">Schema name</span></span>  <br/> |<span data-ttu-id="d625e-141">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d625e-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="d625e-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d625e-142">Validation file</span></span>  <br/> |<span data-ttu-id="d625e-143">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d625e-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d625e-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d625e-144">Can be empty</span></span>  <br/> |<span data-ttu-id="d625e-145">Falso</span><span class="sxs-lookup"><span data-stu-id="d625e-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d625e-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="d625e-146">See also</span></span>

- [<span data-ttu-id="d625e-147">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d625e-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

