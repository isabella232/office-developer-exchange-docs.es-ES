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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764921"
---
# <a name="getorganizationrelationshipsettingsrequest-soap"></a><span data-ttu-id="41a48-105">GetOrganizationRelationshipSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41a48-105">GetOrganizationRelationshipSettingsRequest (SOAP)</span></span>

<span data-ttu-id="41a48-106">El elemento **GetOrganizationRelationshipSettingsRequest** representa los parámetros de una llamada a la operación de la [operación de GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="41a48-106">The **GetOrganizationRelationshipSettingsRequest** element represents the parameters of a call to the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) operation.</span></span> <span data-ttu-id="41a48-107">El elemento **GetOrganizationRelationshipSettingsRequest** es sólo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="41a48-107">The **GetOrganizationRelationshipSettingsRequest** element is for internal use only.</span></span> <span data-ttu-id="41a48-108">Este elemento no se usa en los clientes.</span><span class="sxs-lookup"><span data-stu-id="41a48-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingsRequest>
   <Domains/>
</GetOrganizationRelationshipSettingsRequest>
```

 <span data-ttu-id="41a48-109">**GetOrganizationRelationshipSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="41a48-109">**GetOrganizationRelationshipSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="41a48-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="41a48-110">Attributes and elements</span></span>

<span data-ttu-id="41a48-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="41a48-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41a48-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="41a48-112">Attributes</span></span>

<span data-ttu-id="41a48-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="41a48-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41a48-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="41a48-114">Child elements</span></span>

|<span data-ttu-id="41a48-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="41a48-115">**Element**</span></span>|<span data-ttu-id="41a48-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="41a48-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41a48-117">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41a48-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="41a48-118">Representa una colección de identificadores de dominio.</span><span class="sxs-lookup"><span data-stu-id="41a48-118">Represents a collection of domain identifiers.</span></span>  <br/> |
|||
   
### <a name="parent-elements"></a><span data-ttu-id="41a48-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="41a48-119">Parent elements</span></span>

<span data-ttu-id="41a48-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="41a48-120">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="41a48-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="41a48-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41a48-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="41a48-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="41a48-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="41a48-123">Schema Name</span></span>  <br/> |<span data-ttu-id="41a48-124">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="41a48-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="41a48-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="41a48-125">Validation File</span></span>  <br/> |<span data-ttu-id="41a48-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="41a48-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="41a48-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="41a48-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="41a48-128">Verdadero</span><span class="sxs-lookup"><span data-stu-id="41a48-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41a48-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="41a48-129">See also</span></span>



[<span data-ttu-id="41a48-130">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41a48-130">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

