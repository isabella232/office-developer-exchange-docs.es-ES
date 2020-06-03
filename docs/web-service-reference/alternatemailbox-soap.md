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
description: El elemento AlternateMailbox representa un buzón de correo alternativo.
ms.openlocfilehash: 9019f85a373cc186cc9dadddceee3dc9d11b3854
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466160"
---
# <a name="alternatemailbox-soap"></a><span data-ttu-id="28ece-103">AlternateMailbox (SOAP)</span><span class="sxs-lookup"><span data-stu-id="28ece-103">AlternateMailbox (SOAP)</span></span>

<span data-ttu-id="28ece-104">El elemento **AlternateMailbox** representa un buzón de correo alternativo.</span><span class="sxs-lookup"><span data-stu-id="28ece-104">The **AlternateMailbox** element represents an alternate mailbox.</span></span> 
  
```XML
<AlternateMailbox>
   <Type/>
   <DisplayName/>
   <LegacyDN/>
   <Server/>
   <SmtpAddress/>
</AlternateMailbox>
```

 <span data-ttu-id="28ece-105">**AlternateMailbox**</span><span class="sxs-lookup"><span data-stu-id="28ece-105">**AlternateMailbox**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28ece-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="28ece-106">Attributes and elements</span></span>

<span data-ttu-id="28ece-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="28ece-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28ece-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="28ece-108">Attributes</span></span>

<span data-ttu-id="28ece-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="28ece-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="28ece-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="28ece-110">Child elements</span></span>

|<span data-ttu-id="28ece-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="28ece-111">**Element**</span></span>|<span data-ttu-id="28ece-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28ece-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28ece-113">Tipo (SOAP)</span><span class="sxs-lookup"><span data-stu-id="28ece-113">Type (SOAP)</span></span>](type-soap.md) <br/> |<span data-ttu-id="28ece-114">Representa el tipo de buzón alternativo.</span><span class="sxs-lookup"><span data-stu-id="28ece-114">Represents the alternate mailbox type.</span></span>  <br/> |
|[<span data-ttu-id="28ece-115">DisplayName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="28ece-115">DisplayName (SOAP)</span></span>](displayname-soap.md) <br/> |<span data-ttu-id="28ece-116">Representa el nombre para mostrar del buzón alternativo.</span><span class="sxs-lookup"><span data-stu-id="28ece-116">Represents the alternate mailbox display name.</span></span>  <br/> |
|[<span data-ttu-id="28ece-117">LegacyDN (SOAP)</span><span class="sxs-lookup"><span data-stu-id="28ece-117">LegacyDN (SOAP)</span></span>](legacydn-soap.md) <br/> |<span data-ttu-id="28ece-118">Representa el nombre distintivo heredado de buzón alternativo.</span><span class="sxs-lookup"><span data-stu-id="28ece-118">Represents the alternate mailbox legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="28ece-119">Servidor (SOAP)</span><span class="sxs-lookup"><span data-stu-id="28ece-119">Server (SOAP)</span></span>](server-soap.md) <br/> |<span data-ttu-id="28ece-120">Representa el servidor de buzones de correo alternativo.</span><span class="sxs-lookup"><span data-stu-id="28ece-120">Represents the alternate mailbox server.</span></span>  <br/> |
|[<span data-ttu-id="28ece-121">SmtpAddress (SOAP)</span><span class="sxs-lookup"><span data-stu-id="28ece-121">SmtpAddress (SOAP)</span></span>](smtpaddress-soap.md) <br/> |<span data-ttu-id="28ece-122">Representa la dirección SMTP de buzón alternativa.</span><span class="sxs-lookup"><span data-stu-id="28ece-122">Represents the alternate mailbox SMTP address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="28ece-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="28ece-123">Parent elements</span></span>

|<span data-ttu-id="28ece-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="28ece-124">**Element**</span></span>|<span data-ttu-id="28ece-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28ece-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28ece-126">AlternateMailboxes (SOAP)</span><span class="sxs-lookup"><span data-stu-id="28ece-126">AlternateMailboxes (SOAP)</span></span>](alternatemailboxes-soap.md) <br/> |<span data-ttu-id="28ece-127">Representa una colección de buzones de correo alternativos.</span><span class="sxs-lookup"><span data-stu-id="28ece-127">Represents a collection of alternate mailboxes.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="28ece-128">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="28ece-128">Text value</span></span>

<span data-ttu-id="28ece-129">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="28ece-129">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28ece-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="28ece-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28ece-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="28ece-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="28ece-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="28ece-132">Schema Name</span></span>  <br/> |<span data-ttu-id="28ece-133">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="28ece-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="28ece-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="28ece-134">Validation File</span></span>  <br/> |<span data-ttu-id="28ece-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="28ece-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="28ece-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="28ece-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="28ece-137">Verdadero</span><span class="sxs-lookup"><span data-stu-id="28ece-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28ece-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="28ece-138">See also</span></span>

- [<span data-ttu-id="28ece-139">AlternateMailboxCollectionSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="28ece-139">AlternateMailboxCollectionSetting (SOAP)</span></span>](alternatemailboxcollectionsetting-soap.md)

