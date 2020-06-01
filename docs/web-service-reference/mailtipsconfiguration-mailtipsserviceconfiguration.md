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
description: El elemento MailTipsConfiguration contiene información de configuración del servicio para el servicio de sugerencias de correo.
ms.openlocfilehash: 9128ee99545066899c3b27b624f10a9f1bd36c9d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467791"
---
# <a name="mailtipsconfiguration-mailtipsserviceconfiguration"></a><span data-ttu-id="de6a3-103">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="de6a3-103">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>

<span data-ttu-id="de6a3-104">El elemento **MailTipsConfiguration** contiene información de configuración del servicio para el servicio de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="de6a3-104">The **MailTipsConfiguration** element contains service configuration information for the mail tips service.</span></span> 
  
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

 <span data-ttu-id="de6a3-105">**MailTipsServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="de6a3-105">**MailTipsServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="de6a3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="de6a3-106">Attributes and elements</span></span>

<span data-ttu-id="de6a3-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="de6a3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de6a3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="de6a3-108">Attributes</span></span>

<span data-ttu-id="de6a3-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="de6a3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="de6a3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="de6a3-110">Child elements</span></span>

|<span data-ttu-id="de6a3-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="de6a3-111">**Element**</span></span>|<span data-ttu-id="de6a3-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de6a3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de6a3-113">MailTipsEnabled</span><span class="sxs-lookup"><span data-stu-id="de6a3-113">MailTipsEnabled</span></span>](mailtipsenabled.md) <br/> |<span data-ttu-id="de6a3-114">Indica si el servicio de sugerencias de correo está disponible.</span><span class="sxs-lookup"><span data-stu-id="de6a3-114">Indicates whether the mail tips service is available.</span></span> <span data-ttu-id="de6a3-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="de6a3-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="de6a3-116">MaxRecipientsPerGetMailTipsRequest</span><span class="sxs-lookup"><span data-stu-id="de6a3-116">MaxRecipientsPerGetMailTipsRequest</span></span>](maxrecipientspergetmailtipsrequest.md) <br/> |<span data-ttu-id="de6a3-117">Indica el número máximo de destinatarios que se pueden pasar a la [operación GetMailTips](getmailtips-operation.md).</span><span class="sxs-lookup"><span data-stu-id="de6a3-117">Indicates the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span> <span data-ttu-id="de6a3-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="de6a3-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="de6a3-119">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="de6a3-119">MaxMessageSize</span></span>](maxmessagesize.md) <br/> |<span data-ttu-id="de6a3-120">Representa el tamaño máximo de mensaje que puede aceptar un destinatario.</span><span class="sxs-lookup"><span data-stu-id="de6a3-120">Represents the maximum message size a recipient can accept.</span></span> <span data-ttu-id="de6a3-121">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="de6a3-121">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="de6a3-122">LargeAudienceThreshold</span><span class="sxs-lookup"><span data-stu-id="de6a3-122">LargeAudienceThreshold</span></span>](largeaudiencethreshold.md) <br/> |<span data-ttu-id="de6a3-123">Representa el umbral de gran audiencia para un cliente.</span><span class="sxs-lookup"><span data-stu-id="de6a3-123">Represents the large audience threshold for a client.</span></span> <span data-ttu-id="de6a3-124">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="de6a3-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="de6a3-125">ShowExternalRecipientCount</span><span class="sxs-lookup"><span data-stu-id="de6a3-125">ShowExternalRecipientCount</span></span>](showexternalrecipientcount.md) <br/> |<span data-ttu-id="de6a3-126">Indica si los consumidores de la [operación GetMailTips](getmailtips-operation.md) tienen que Mostrar sugerencias de correo que indican el número de destinatarios externos a los que se dirige un mensaje.</span><span class="sxs-lookup"><span data-stu-id="de6a3-126">Indicates whether consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> <span data-ttu-id="de6a3-127">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="de6a3-127">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="de6a3-128">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="de6a3-128">InternalDomains (SmtpDomainList)</span></span>](internaldomains-smtpdomainlist.md) <br/> |<span data-ttu-id="de6a3-129">Identifica la lista de dominios SMTP internos de la organización.</span><span class="sxs-lookup"><span data-stu-id="de6a3-129">Identifies the list of internal SMTP domains of the organization.</span></span> <span data-ttu-id="de6a3-130">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="de6a3-130">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="de6a3-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="de6a3-131">Parent elements</span></span>

|<span data-ttu-id="de6a3-132">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="de6a3-132">**Element**</span></span>|<span data-ttu-id="de6a3-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de6a3-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de6a3-134">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="de6a3-134">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="de6a3-135">Contiene las opciones de configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="de6a3-135">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="de6a3-136">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="de6a3-136">Text value</span></span>

<span data-ttu-id="de6a3-137">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="de6a3-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="de6a3-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de6a3-138">Remarks</span></span>

<span data-ttu-id="de6a3-139">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="de6a3-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de6a3-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="de6a3-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de6a3-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="de6a3-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="de6a3-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="de6a3-142">Schema Name</span></span>  <br/> |<span data-ttu-id="de6a3-143">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="de6a3-143">Messages schema</span></span>  <br/> |
|<span data-ttu-id="de6a3-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="de6a3-144">Validation File</span></span>  <br/> |<span data-ttu-id="de6a3-145">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="de6a3-145">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="de6a3-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="de6a3-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="de6a3-147">Falso</span><span class="sxs-lookup"><span data-stu-id="de6a3-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de6a3-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="de6a3-148">See also</span></span>



- [<span data-ttu-id="de6a3-149">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="de6a3-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

