---
title: AlternateMailbox (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: d913a70d-5a85-4b6e-becc-2fb9334b6088
description: El elemento AlternateMailbox representa un buzón de alternativo.
ms.openlocfilehash: 8eb53e4846ad55916e2c5876606c00c0f2e371ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19763483"
---
# <a name="alternatemailbox-soap"></a><span data-ttu-id="0d61c-103">AlternateMailbox (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0d61c-103">AlternateMailbox (SOAP)</span></span>

<span data-ttu-id="0d61c-104">El elemento **AlternateMailbox** representa un buzón de alternativo.</span><span class="sxs-lookup"><span data-stu-id="0d61c-104">The **AlternateMailbox** element represents an alternate mailbox.</span></span> 
  
```XML
<AlternateMailbox>
   <Type/>
   <DisplayName/>
   <LegacyDN/>
   <Server/>
   <SmtpAddress/>
</AlternateMailbox>
```

 <span data-ttu-id="0d61c-105">**AlternateMailbox**</span><span class="sxs-lookup"><span data-stu-id="0d61c-105">**AlternateMailbox**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0d61c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0d61c-106">Attributes and elements</span></span>

<span data-ttu-id="0d61c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0d61c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d61c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0d61c-108">Attributes</span></span>

<span data-ttu-id="0d61c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0d61c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d61c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0d61c-110">Child elements</span></span>

|<span data-ttu-id="0d61c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d61c-111">**Element**</span></span>|<span data-ttu-id="0d61c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0d61c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d61c-113">Tipo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0d61c-113">Type (SOAP)</span></span>](type-soap.md) <br/> |<span data-ttu-id="0d61c-114">Representa el tipo de buzón de correo alternativas.</span><span class="sxs-lookup"><span data-stu-id="0d61c-114">Represents the alternate mailbox type.</span></span>  <br/> |
|[<span data-ttu-id="0d61c-115">DisplayName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0d61c-115">DisplayName (SOAP)</span></span>](displayname-soap.md) <br/> |<span data-ttu-id="0d61c-116">Representa el nombre para mostrar de buzón de correo alternativas.</span><span class="sxs-lookup"><span data-stu-id="0d61c-116">Represents the alternate mailbox display name.</span></span>  <br/> |
|[<span data-ttu-id="0d61c-117">LegacyDN (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0d61c-117">LegacyDN (SOAP)</span></span>](legacydn-soap.md) <br/> |<span data-ttu-id="0d61c-118">Representa el nombre distintivo heredado de buzón de correo alternativas.</span><span class="sxs-lookup"><span data-stu-id="0d61c-118">Represents the alternate mailbox legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="0d61c-119">Servidor (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0d61c-119">Server (SOAP)</span></span>](server-soap.md) <br/> |<span data-ttu-id="0d61c-120">Representa el servidor de buzones alternativas.</span><span class="sxs-lookup"><span data-stu-id="0d61c-120">Represents the alternate mailbox server.</span></span>  <br/> |
|[<span data-ttu-id="0d61c-121">SmtpAddress (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0d61c-121">SmtpAddress (SOAP)</span></span>](smtpaddress-soap.md) <br/> |<span data-ttu-id="0d61c-122">Representa la dirección SMTP del buzón de correo alternativa.</span><span class="sxs-lookup"><span data-stu-id="0d61c-122">Represents the alternate mailbox SMTP address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0d61c-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0d61c-123">Parent elements</span></span>

|<span data-ttu-id="0d61c-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d61c-124">**Element**</span></span>|<span data-ttu-id="0d61c-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0d61c-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d61c-126">AlternateMailboxes (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0d61c-126">AlternateMailboxes (SOAP)</span></span>](alternatemailboxes-soap.md) <br/> |<span data-ttu-id="0d61c-127">Representa una colección de buzones de correo alternativas.</span><span class="sxs-lookup"><span data-stu-id="0d61c-127">Represents a collection of alternate mailboxes.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0d61c-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0d61c-128">Text value</span></span>

<span data-ttu-id="0d61c-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0d61c-129">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d61c-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0d61c-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d61c-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0d61c-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="0d61c-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0d61c-132">Schema Name</span></span>  <br/> |<span data-ttu-id="0d61c-133">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="0d61c-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="0d61c-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0d61c-134">Validation File</span></span>  <br/> |<span data-ttu-id="0d61c-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0d61c-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0d61c-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0d61c-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="0d61c-137">Verdadero</span><span class="sxs-lookup"><span data-stu-id="0d61c-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d61c-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="0d61c-138">See also</span></span>

- [<span data-ttu-id="0d61c-139">AlternateMailboxCollectionSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0d61c-139">AlternateMailboxCollectionSetting (SOAP)</span></span>](alternatemailboxcollectionsetting-soap.md)
