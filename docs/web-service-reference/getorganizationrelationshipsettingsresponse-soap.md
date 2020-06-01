---
title: GetOrganizationRelationshipSettingsResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f43b817-92c2-4e04-8095-479d790f768c
description: El elemento GetOrganizationRelationshipSettingsResponse contiene la respuesta de operación GetOrganizationRelationshipSettings (SOAP). El elemento GetOrganizationRelationshipSettingsResponse es solo para uso interno. Los clientes no usan este elemento.
ms.openlocfilehash: 0f34fbc6577b379dd0ac379564c5e6bbd940d379
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457924"
---
# <a name="getorganizationrelationshipsettingsresponse-soap"></a><span data-ttu-id="e2a21-105">GetOrganizationRelationshipSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e2a21-105">GetOrganizationRelationshipSettingsResponse (SOAP)</span></span>

<span data-ttu-id="e2a21-106">El elemento **GetOrganizationRelationshipSettingsResponse** contiene la respuesta de [operación GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="e2a21-106">The **GetOrganizationRelationshipSettingsResponse** element contains the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) response.</span></span> <span data-ttu-id="e2a21-107">El elemento **GetOrganizationRelationshipSettingsResponse** es solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="e2a21-107">The **GetOrganizationRelationshipSettingsResponse** element is for internal use only.</span></span> <span data-ttu-id="e2a21-108">Los clientes no usan este elemento.</span><span class="sxs-lookup"><span data-stu-id="e2a21-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <OrganizationRelationshipSettingsCollection/>
</GetOrganizationRelationshipSettingResponse>
```

 <span data-ttu-id="e2a21-109">**GetOrganizationRelationshipSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="e2a21-109">**GetOrganizationRelationshipSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e2a21-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e2a21-110">Attributes and elements</span></span>

<span data-ttu-id="e2a21-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e2a21-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2a21-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="e2a21-112">Attributes</span></span>

<span data-ttu-id="e2a21-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e2a21-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e2a21-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e2a21-114">Child elements</span></span>

|<span data-ttu-id="e2a21-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e2a21-115">**Element**</span></span>|<span data-ttu-id="e2a21-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e2a21-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2a21-117">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e2a21-117">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="e2a21-118">Representa un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="e2a21-118">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="e2a21-119">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e2a21-119">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="e2a21-120">Representa un mensaje que está asociado con un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="e2a21-120">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="e2a21-121">OrganizationRelationshipSettingsCollection (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e2a21-121">OrganizationRelationshipSettingsCollection (SOAP)</span></span>](organizationrelationshipsettingscollection-soap.md) <br/> |<span data-ttu-id="e2a21-122">Representa una colección de relaciones de organización que coinciden con la consulta.</span><span class="sxs-lookup"><span data-stu-id="e2a21-122">Represents a collection of organization relationships that match the query.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e2a21-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e2a21-123">Parent elements</span></span>

<span data-ttu-id="e2a21-124">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e2a21-124">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="e2a21-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e2a21-125">Text value</span></span>

<span data-ttu-id="e2a21-126">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e2a21-126">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2a21-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e2a21-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2a21-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2a21-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="e2a21-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e2a21-129">Schema Name</span></span>  <br/> |<span data-ttu-id="e2a21-130">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="e2a21-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="e2a21-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e2a21-131">Validation File</span></span>  <br/> |<span data-ttu-id="e2a21-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e2a21-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e2a21-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e2a21-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="e2a21-134">Verdadero</span><span class="sxs-lookup"><span data-stu-id="e2a21-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2a21-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2a21-135">See also</span></span>



[<span data-ttu-id="e2a21-136">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e2a21-136">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

