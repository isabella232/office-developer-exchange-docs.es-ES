---
title: GetOrganizationRelationshipSettingsRequest (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e8aa3b3-4bfc-40c3-b96b-9f7062b09309
description: El elemento GetOrganizationRelationshipSettingsRequest representa los parámetros de una llamada a la operación de operación (SOAP) GetOrganizationRelationshipSettings. El elemento GetOrganizationRelationshipSettingsRequest es sólo para uso interno. Este elemento no se usa en los clientes.
ms.openlocfilehash: 451506d53212ddca416f5b797624688f511988d0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764921"
---
# <a name="getorganizationrelationshipsettingsrequest-soap"></a><span data-ttu-id="ad5f9-105">GetOrganizationRelationshipSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad5f9-105">GetOrganizationRelationshipSettingsRequest (SOAP)</span></span>

<span data-ttu-id="ad5f9-106">El elemento **GetOrganizationRelationshipSettingsRequest** representa los parámetros de una llamada a la operación de la [operación de GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="ad5f9-106">The **GetOrganizationRelationshipSettingsRequest** element represents the parameters of a call to the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) operation.</span></span> <span data-ttu-id="ad5f9-107">El elemento **GetOrganizationRelationshipSettingsRequest** es sólo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="ad5f9-107">The **GetOrganizationRelationshipSettingsRequest** element is for internal use only.</span></span> <span data-ttu-id="ad5f9-108">Este elemento no se usa en los clientes.</span><span class="sxs-lookup"><span data-stu-id="ad5f9-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingsRequest>
   <Domains/>
</GetOrganizationRelationshipSettingsRequest>
```

 <span data-ttu-id="ad5f9-109">**GetOrganizationRelationshipSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="ad5f9-109">**GetOrganizationRelationshipSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ad5f9-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ad5f9-110">Attributes and elements</span></span>

<span data-ttu-id="ad5f9-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ad5f9-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad5f9-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad5f9-112">Attributes</span></span>

<span data-ttu-id="ad5f9-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ad5f9-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ad5f9-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ad5f9-114">Child elements</span></span>

|<span data-ttu-id="ad5f9-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad5f9-115">**Element**</span></span>|<span data-ttu-id="ad5f9-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad5f9-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad5f9-117">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad5f9-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="ad5f9-118">Representa una colección de identificadores de dominio.</span><span class="sxs-lookup"><span data-stu-id="ad5f9-118">Represents a collection of domain identifiers.</span></span>  <br/> |
|||
   
### <a name="parent-elements"></a><span data-ttu-id="ad5f9-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ad5f9-119">Parent elements</span></span>

<span data-ttu-id="ad5f9-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ad5f9-120">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad5f9-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ad5f9-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad5f9-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ad5f9-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="ad5f9-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ad5f9-123">Schema Name</span></span>  <br/> |<span data-ttu-id="ad5f9-124">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="ad5f9-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="ad5f9-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ad5f9-125">Validation File</span></span>  <br/> |<span data-ttu-id="ad5f9-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ad5f9-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ad5f9-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ad5f9-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="ad5f9-128">Verdadero</span><span class="sxs-lookup"><span data-stu-id="ad5f9-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad5f9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad5f9-129">See also</span></span>



[<span data-ttu-id="ad5f9-130">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ad5f9-130">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

