---
title: MailTipsConfiguration (MailTipsServiceConfiguration)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsConfiguration
api_type:
- schema
ms.assetid: 9a34515e-815b-4c61-b118-d5f66b80238f
description: El elemento MailTipsConfiguration contiene información de configuración de servicio para el servicio de sugerencias de correo.
ms.openlocfilehash: ea92af3ebb2d2f720e5823c5317d09d5bcdb3978
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836321"
---
# <a name="mailtipsconfiguration-mailtipsserviceconfiguration"></a><span data-ttu-id="28b3c-103">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="28b3c-103">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>

<span data-ttu-id="28b3c-104">El elemento **MailTipsConfiguration** contiene información de configuración de servicio para el servicio de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="28b3c-104">The **MailTipsConfiguration** element contains service configuration information for the mail tips service.</span></span> 
  
```XML
<MailTipsConfiguration>
   <MailTipsEnabled/>
   <MaxRecipientsPerGetMailTipsRequest/>
   <MaxMessageSize/>
   <LargeAudienceThreshold/>
   <ShowExternalRecipientCount/>
   <InternalDomains/>
</MailTipsConfiguration>
```

 <span data-ttu-id="28b3c-105">**MailTipsServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="28b3c-105">**MailTipsServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28b3c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="28b3c-106">Attributes and elements</span></span>

<span data-ttu-id="28b3c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="28b3c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28b3c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="28b3c-108">Attributes</span></span>

<span data-ttu-id="28b3c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="28b3c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="28b3c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="28b3c-110">Child elements</span></span>

|<span data-ttu-id="28b3c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="28b3c-111">**Element**</span></span>|<span data-ttu-id="28b3c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28b3c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28b3c-113">MailTipsEnabled</span><span class="sxs-lookup"><span data-stu-id="28b3c-113">MailTipsEnabled</span></span>](mailtipsenabled.md) <br/> |<span data-ttu-id="28b3c-114">Indica si el servicio de sugerencias de correo está disponible.</span><span class="sxs-lookup"><span data-stu-id="28b3c-114">Indicates whether the mail tips service is available.</span></span> <span data-ttu-id="28b3c-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="28b3c-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="28b3c-116">MaxRecipientsPerGetMailTipsRequest</span><span class="sxs-lookup"><span data-stu-id="28b3c-116">MaxRecipientsPerGetMailTipsRequest</span></span>](maxrecipientspergetmailtipsrequest.md) <br/> |<span data-ttu-id="28b3c-117">Indica el número máximo de destinatarios que se pueden pasar a la [operación de GetMailTips](getmailtips-operation.md).</span><span class="sxs-lookup"><span data-stu-id="28b3c-117">Indicates the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span> <span data-ttu-id="28b3c-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="28b3c-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="28b3c-119">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="28b3c-119">MaxMessageSize</span></span>](maxmessagesize.md) <br/> |<span data-ttu-id="28b3c-120">Representa el tamaño máximo de mensaje que puede aceptar un destinatario.</span><span class="sxs-lookup"><span data-stu-id="28b3c-120">Represents the maximum message size a recipient can accept.</span></span> <span data-ttu-id="28b3c-121">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="28b3c-121">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="28b3c-122">LargeAudienceThreshold</span><span class="sxs-lookup"><span data-stu-id="28b3c-122">LargeAudienceThreshold</span></span>](largeaudiencethreshold.md) <br/> |<span data-ttu-id="28b3c-123">Representa el umbral de audiencia grande para un cliente.</span><span class="sxs-lookup"><span data-stu-id="28b3c-123">Represents the large audience threshold for a client.</span></span> <span data-ttu-id="28b3c-124">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="28b3c-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="28b3c-125">ShowExternalRecipientCount</span><span class="sxs-lookup"><span data-stu-id="28b3c-125">ShowExternalRecipientCount</span></span>](showexternalrecipientcount.md) <br/> |<span data-ttu-id="28b3c-126">Indica si los consumidores de la [operación de GetMailTips](getmailtips-operation.md) tienen que mostrar sugerencias de correo que indican el número de destinatarios externos a la que se envía un mensaje.</span><span class="sxs-lookup"><span data-stu-id="28b3c-126">Indicates whether consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> <span data-ttu-id="28b3c-127">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="28b3c-127">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="28b3c-128">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="28b3c-128">InternalDomains (SmtpDomainList)</span></span>](internaldomains-smtpdomainlist.md) <br/> |<span data-ttu-id="28b3c-129">Identifica la lista de dominios SMTP internos de la organización.</span><span class="sxs-lookup"><span data-stu-id="28b3c-129">Identifies the list of internal SMTP domains of the organization.</span></span> <span data-ttu-id="28b3c-130">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="28b3c-130">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="28b3c-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="28b3c-131">Parent elements</span></span>

|<span data-ttu-id="28b3c-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="28b3c-132">**Element**</span></span>|<span data-ttu-id="28b3c-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28b3c-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28b3c-134">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="28b3c-134">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="28b3c-135">Contiene la configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="28b3c-135">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="28b3c-136">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="28b3c-136">Text value</span></span>

<span data-ttu-id="28b3c-137">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="28b3c-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28b3c-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="28b3c-138">Remarks</span></span>

<span data-ttu-id="28b3c-139">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="28b3c-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28b3c-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="28b3c-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28b3c-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="28b3c-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="28b3c-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="28b3c-142">Schema Name</span></span>  <br/> |<span data-ttu-id="28b3c-143">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="28b3c-143">Messages schema</span></span>  <br/> |
|<span data-ttu-id="28b3c-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="28b3c-144">Validation File</span></span>  <br/> |<span data-ttu-id="28b3c-145">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="28b3c-145">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="28b3c-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="28b3c-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="28b3c-147">False</span><span class="sxs-lookup"><span data-stu-id="28b3c-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28b3c-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="28b3c-148">See also</span></span>



- [<span data-ttu-id="28b3c-149">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="28b3c-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

