---
title: Response (GetOrganizationRelationship) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e6bbe800-3cbc-48b2-87b3-2043f575e88b
description: El elemento Response contiene la información de respuesta de la operación GetOrganizationRelationshipSettings (SOAP). El elemento Response es solo para uso interno. Los clientes no usan este elemento.
ms.openlocfilehash: 55f8cd549f40b780b2e7438634a851a2c3854f40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467945"
---
# <a name="response-getorganizationrelationship-soap"></a><span data-ttu-id="92842-105">Response (GetOrganizationRelationship) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="92842-105">Response (GetOrganizationRelationship) (SOAP)</span></span>

<span data-ttu-id="92842-106">El elemento **Response** contiene la información de respuesta de la [operación GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="92842-106">The **Response** element contains the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) response information.</span></span> <span data-ttu-id="92842-107">El elemento **Response** es solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="92842-107">The **Response** element is for internal use only.</span></span> <span data-ttu-id="92842-108">Los clientes no usan este elemento.</span><span class="sxs-lookup"><span data-stu-id="92842-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingsResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <OrganizationRelationshipSettingsCollection/>
</GetOrganizationRelationshipSettingResponse>
```

 <span data-ttu-id="92842-109">**GetOrganizationRelationshipSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="92842-109">**GetOrganizationRelationshipSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="92842-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="92842-110">Attributes and elements</span></span>

<span data-ttu-id="92842-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="92842-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="92842-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="92842-112">Attributes</span></span>

<span data-ttu-id="92842-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="92842-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="92842-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="92842-114">Child elements</span></span>

|<span data-ttu-id="92842-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="92842-115">**Element**</span></span>|<span data-ttu-id="92842-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="92842-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92842-117">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="92842-117">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="92842-118">Representa un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="92842-118">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="92842-119">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="92842-119">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="92842-120">Representa un mensaje que está asociado con un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="92842-120">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="92842-121">OrganizationRelationshipSettingsCollection (SOAP)</span><span class="sxs-lookup"><span data-stu-id="92842-121">OrganizationRelationshipSettingsCollection (SOAP)</span></span>](organizationrelationshipsettingscollection-soap.md) <br/> |<span data-ttu-id="92842-122">Representa una lista de relaciones de organización que coinciden con la consulta.</span><span class="sxs-lookup"><span data-stu-id="92842-122">Represents a list of organization relationships that match the query.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="92842-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="92842-123">Parent elements</span></span>

<span data-ttu-id="92842-124">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="92842-124">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="92842-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="92842-125">Text value</span></span>

<span data-ttu-id="92842-126">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="92842-126">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="92842-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="92842-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92842-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="92842-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="92842-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="92842-129">Schema Name</span></span>  <br/> |<span data-ttu-id="92842-130">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="92842-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="92842-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="92842-131">Validation File</span></span>  <br/> |<span data-ttu-id="92842-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="92842-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="92842-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="92842-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="92842-134">Verdadero</span><span class="sxs-lookup"><span data-stu-id="92842-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="92842-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="92842-135">See also</span></span>



[<span data-ttu-id="92842-136">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="92842-136">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

