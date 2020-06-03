---
title: OrganizationRelationshipSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 917481bb-46fc-4b88-8683-4cf812dcb0ab
description: El elemento OrganizationRelationshipSettings representa una lista de relaciones de organización para una sola organización. El elemento OrganizationRelationshipSettings es solo para uso interno. Los clientes no usan este elemento.
ms.openlocfilehash: 383b3635e1435c6597ccf793a7990c411c02d36d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462461"
---
# <a name="organizationrelationshipsettings-soap"></a><span data-ttu-id="62c2d-105">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="62c2d-105">OrganizationRelationshipSettings (SOAP)</span></span>

<span data-ttu-id="62c2d-106">El elemento **OrganizationRelationshipSettings** representa una lista de relaciones de organización para una sola organización.</span><span class="sxs-lookup"><span data-stu-id="62c2d-106">The **OrganizationRelationshipSettings** element represents a list of organization relationships for a single organization.</span></span> <span data-ttu-id="62c2d-107">El elemento **OrganizationRelationshipSettings** es solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="62c2d-107">The **OrganizationRelationshipSettings** element is for internal use only.</span></span> <span data-ttu-id="62c2d-108">Los clientes no usan este elemento.</span><span class="sxs-lookup"><span data-stu-id="62c2d-108">This element is not used by clients.</span></span> 
  
```XML
<OrganizationRelationshipSettings>
    <DeliveryReportEnabled/>
    <DomainNames/>
    <FreeBusyAccessEnabled/>
    <FreeBusyAccessLevel/>
    <MailTipsAccessEnabled/>
    <MailTipsAccessLevel/>
    <MailboxMoveEnabled/>
    <Name/>
    <TargetApplicationUri/>
    <TargetAudodiscoverEpr/>
    <TargetSharingEpr/>
</OrganizationRelationshipSettings>
```

 <span data-ttu-id="62c2d-109">**OrganizationRelationshipSettings**</span><span class="sxs-lookup"><span data-stu-id="62c2d-109">**OrganizationRelationshipSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="62c2d-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="62c2d-110">Attributes and elements</span></span>

<span data-ttu-id="62c2d-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="62c2d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="62c2d-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="62c2d-112">Attributes</span></span>

<span data-ttu-id="62c2d-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="62c2d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="62c2d-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="62c2d-114">Child elements</span></span>

|<span data-ttu-id="62c2d-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="62c2d-115">**Element**</span></span>|<span data-ttu-id="62c2d-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="62c2d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62c2d-117">DeliveryReportEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="62c2d-117">DeliveryReportEnabled (SOAP)</span></span>](deliveryreportenabled-soap.md) <br/> |<span data-ttu-id="62c2d-118">Representa la marca [DeliveryReportEnabled ()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.DeliveryReportEnabled.aspx) .</span><span class="sxs-lookup"><span data-stu-id="62c2d-118">Represents the [DeliveryReportEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.DeliveryReportEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="62c2d-119">DomainNames (SOAP)</span><span class="sxs-lookup"><span data-stu-id="62c2d-119">DomainNames (SOAP)</span></span>](domainnames-soap.md) <br/> |<span data-ttu-id="62c2d-120">Representa la colección de nombres de dominio.</span><span class="sxs-lookup"><span data-stu-id="62c2d-120">Represents the domain names collection.</span></span>  <br/> |
|[<span data-ttu-id="62c2d-121">FreeBusyAccessEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="62c2d-121">FreeBusyAccessEnabled (SOAP)</span></span>](freebusyaccessenabled-soap.md) <br/> |<span data-ttu-id="62c2d-122">Representa la marca [FreeBusyAccessEnabled ()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.FreeBusyAccessEnabled.aspx) .</span><span class="sxs-lookup"><span data-stu-id="62c2d-122">Represents the [FreeBusyAccessEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.FreeBusyAccessEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="62c2d-123">FreeBusyAccessLevel (SOAP)</span><span class="sxs-lookup"><span data-stu-id="62c2d-123">FreeBusyAccessLevel (SOAP)</span></span>](freebusyaccesslevel-soap.md) <br/> |<span data-ttu-id="62c2d-124">Representa la propiedad [FreeBusyAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.FreeBusyAccessLevel.aspx) .</span><span class="sxs-lookup"><span data-stu-id="62c2d-124">Represents the [FreeBusyAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.FreeBusyAccessLevel.aspx) property.</span></span>  <br/> |
|[<span data-ttu-id="62c2d-125">MailTipsAccessEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="62c2d-125">MailTipsAccessEnabled (SOAP)</span></span>](mailtipsaccessenabled-soap.md) <br/> |<span data-ttu-id="62c2d-126">Representa la marca [MailTipsAccessEnabled ()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailTipsAccessEnabled.aspx) .</span><span class="sxs-lookup"><span data-stu-id="62c2d-126">Represents the [MailTipsAccessEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailTipsAccessEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="62c2d-127">MailTipsAccessLevel (SOAP)</span><span class="sxs-lookup"><span data-stu-id="62c2d-127">MailTipsAccessLevel (SOAP)</span></span>](mailtipsaccesslevel-soap.md) <br/> |<span data-ttu-id="62c2d-128">Representa la propiedad [MailTipsAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.MailTipsAccessLevel.aspx) .</span><span class="sxs-lookup"><span data-stu-id="62c2d-128">Represents the [MailTipsAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.MailTipsAccessLevel.aspx) property.</span></span>  <br/> |
|[<span data-ttu-id="62c2d-129">MailboxMoveEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="62c2d-129">MailboxMoveEnabled (SOAP)</span></span>](mailboxmoveenabled-soap.md) <br/> |<span data-ttu-id="62c2d-130">Representa la marca [MailboxMoveEnabled ()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailboxMoveEnabled.aspx) .</span><span class="sxs-lookup"><span data-stu-id="62c2d-130">Represents the [MailboxMoveEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailboxMoveEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="62c2d-131">Name (SOAP)</span><span class="sxs-lookup"><span data-stu-id="62c2d-131">Name (SOAP)</span></span>](name-soap.md) <br/> |<span data-ttu-id="62c2d-132">Representa el nombre de la relación de la organización.</span><span class="sxs-lookup"><span data-stu-id="62c2d-132">Represents the name of the organization relationship.</span></span>  <br/> |
|[<span data-ttu-id="62c2d-133">TargetApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="62c2d-133">TargetApplicationUri (SOAP)</span></span>](targetapplicationuri-soap.md) <br/> |<span data-ttu-id="62c2d-134">Define el URI de la aplicación de destino.</span><span class="sxs-lookup"><span data-stu-id="62c2d-134">Defines the target application URI.</span></span>  <br/> |
|[<span data-ttu-id="62c2d-135">TargetAutodiscoverEpr (SOAP)</span><span class="sxs-lookup"><span data-stu-id="62c2d-135">TargetAutodiscoverEpr (SOAP)</span></span>](targetautodiscoverepr-soap.md) <br/> |<span data-ttu-id="62c2d-136">Representa la propiedad [TargetAutodiscoverEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetAutodiscoverEpr.aspx) .</span><span class="sxs-lookup"><span data-stu-id="62c2d-136">Represents the [TargetAutodiscoverEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetAutodiscoverEpr.aspx) property.</span></span>  <br/> |
|[<span data-ttu-id="62c2d-137">TargetSharingEpr (SOAP)</span><span class="sxs-lookup"><span data-stu-id="62c2d-137">TargetSharingEpr (SOAP)</span></span>](targetsharingepr-soap.md) <br/> |<span data-ttu-id="62c2d-138">Representa la propiedad [TargetSharingEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetSharingEpr.aspx) .</span><span class="sxs-lookup"><span data-stu-id="62c2d-138">Represents the [TargetSharingEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetSharingEpr.aspx) property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="62c2d-139">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="62c2d-139">Parent elements</span></span>

|<span data-ttu-id="62c2d-140">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="62c2d-140">**Element**</span></span>|<span data-ttu-id="62c2d-141">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="62c2d-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62c2d-142">OrganizationRelationshipSettingsCollection (SOAP)</span><span class="sxs-lookup"><span data-stu-id="62c2d-142">OrganizationRelationshipSettingsCollection (SOAP)</span></span>](organizationrelationshipsettingscollection-soap.md) <br/> |<span data-ttu-id="62c2d-143">Representa una lista de relaciones de organización que coinciden con la consulta.</span><span class="sxs-lookup"><span data-stu-id="62c2d-143">Represents a list of organization relationships that match the query.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="62c2d-144">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="62c2d-144">Text value</span></span>

<span data-ttu-id="62c2d-145">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="62c2d-145">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="62c2d-146">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="62c2d-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62c2d-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="62c2d-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="62c2d-148">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="62c2d-148">Schema Name</span></span>  <br/> |<span data-ttu-id="62c2d-149">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="62c2d-149">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="62c2d-150">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="62c2d-150">Validation File</span></span>  <br/> |<span data-ttu-id="62c2d-151">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="62c2d-151">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="62c2d-152">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="62c2d-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="62c2d-153">Verdadero</span><span class="sxs-lookup"><span data-stu-id="62c2d-153">True</span></span>  <br/> |
   

