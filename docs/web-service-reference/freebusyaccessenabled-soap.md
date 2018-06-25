---
title: FreeBusyAccessEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8d2d3276-b180-424e-a707-7256d14a1776
description: El elemento FreeBusyAccessEnabled representa la marca FreeBusyAccessEnabled(). El elemento FreeBusyAccessEnabled es sólo para uso interno. Este elemento no se usa en los clientes.
ms.openlocfilehash: 4727e7054c02a4b5d454cb880691ecc01a075327
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764715"
---
# <a name="freebusyaccessenabled-soap"></a><span data-ttu-id="084b2-105">FreeBusyAccessEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="084b2-105">FreeBusyAccessEnabled (SOAP)</span></span>

<span data-ttu-id="084b2-106">El elemento **FreeBusyAccessEnabled** representa la marca **FreeBusyAccessEnabled()** .</span><span class="sxs-lookup"><span data-stu-id="084b2-106">The **FreeBusyAccessEnabled** element represents the **FreeBusyAccessEnabled()** flag.</span></span> <span data-ttu-id="084b2-107">El elemento **FreeBusyAccessEnabled** es sólo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="084b2-107">The **FreeBusyAccessEnabled** element is for internal use only.</span></span> <span data-ttu-id="084b2-108">Este elemento no se usa en los clientes.</span><span class="sxs-lookup"><span data-stu-id="084b2-108">This element is not used by clients.</span></span> 
  
```XML
<FreeBusyAccessEnabled>true | false</FreeBusyAccessEnabled>
```

 <span data-ttu-id="084b2-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="084b2-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="084b2-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="084b2-110">Attributes and elements</span></span>

<span data-ttu-id="084b2-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="084b2-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="084b2-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="084b2-112">Attributes</span></span>

<span data-ttu-id="084b2-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="084b2-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="084b2-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="084b2-114">Child elements</span></span>

<span data-ttu-id="084b2-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="084b2-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="084b2-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="084b2-116">Parent elements</span></span>

|<span data-ttu-id="084b2-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="084b2-117">**Element**</span></span>|<span data-ttu-id="084b2-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="084b2-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="084b2-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="084b2-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="084b2-120">Representa una lista de relaciones de organización para una sola organización.</span><span class="sxs-lookup"><span data-stu-id="084b2-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="084b2-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="084b2-121">Text value</span></span>

<span data-ttu-id="084b2-122">Un valor de texto de **true** para el elemento **FreeBusyAccessEnabled** indica que debe usarse la relación de uso compartida para recuperar información de disponibilidad de los usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="084b2-122">A text value of **true** for the **FreeBusyAccessEnabled** element indicates that the sharing relationship should be used to retrieve free busy information from users in the organization.</span></span> <span data-ttu-id="084b2-123">Un valor de **false** indica que se debe suprimir la relación de uso compartida.</span><span class="sxs-lookup"><span data-stu-id="084b2-123">A value of **false** indicates that the sharing relationship should be suppressed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="084b2-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="084b2-124">Remarks</span></span>

<span data-ttu-id="084b2-125">Use este elemento para permitir o suprimir la información de libre/ocupado desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="084b2-125">Use this element to allow or suppress free/busy information from the server.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="084b2-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="084b2-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="084b2-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="084b2-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="084b2-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="084b2-128">Schema Name</span></span>  <br/> |<span data-ttu-id="084b2-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="084b2-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="084b2-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="084b2-130">Validation File</span></span>  <br/> |<span data-ttu-id="084b2-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="084b2-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="084b2-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="084b2-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="084b2-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="084b2-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="084b2-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="084b2-134">See also</span></span>



[<span data-ttu-id="084b2-135">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="084b2-135">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

