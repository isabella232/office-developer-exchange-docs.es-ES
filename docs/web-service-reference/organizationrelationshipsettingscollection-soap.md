---
title: OrganizationRelationshipSettingsCollection (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33456abf-a1b6-46da-a864-3ec8af2780de
description: El elemento OrganizationRelationshipSettingsCollection representa una lista de relaciones de organización que coinciden con la consulta. El elemento OrganizationRelationshipSettingsCollection es sólo para uso interno. Este elemento no se usa en los clientes.
ms.openlocfilehash: 18e71ce39d48598868d677a37d5ba439fa6d59c4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836663"
---
# <a name="organizationrelationshipsettingscollection-soap"></a><span data-ttu-id="63630-105">OrganizationRelationshipSettingsCollection (SOAP)</span><span class="sxs-lookup"><span data-stu-id="63630-105">OrganizationRelationshipSettingsCollection (SOAP)</span></span>

<span data-ttu-id="63630-106">El elemento **OrganizationRelationshipSettingsCollection** representa una lista de relaciones de organización que coinciden con la consulta.</span><span class="sxs-lookup"><span data-stu-id="63630-106">The **OrganizationRelationshipSettingsCollection** element represents a list of organization relationships that match the query.</span></span> <span data-ttu-id="63630-107">El elemento **OrganizationRelationshipSettingsCollection** es sólo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="63630-107">The **OrganizationRelationshipSettingsCollection** element is for internal use only.</span></span> <span data-ttu-id="63630-108">Este elemento no se usa en los clientes.</span><span class="sxs-lookup"><span data-stu-id="63630-108">This element is not used by clients.</span></span> 
  
```XML
<OrganizationRelationshipSettingsCollection>
   <OrganizationRelationshipSettings/>
</OrganizationRelationshipSettingsCollection>
```

 <span data-ttu-id="63630-109">**OrganizationRelationshipSettingsCollection**</span><span class="sxs-lookup"><span data-stu-id="63630-109">**OrganizationRelationshipSettingsCollection**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="63630-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="63630-110">Attributes and elements</span></span>

<span data-ttu-id="63630-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="63630-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63630-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="63630-112">Attributes</span></span>

<span data-ttu-id="63630-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="63630-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="63630-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="63630-114">Child elements</span></span>

|<span data-ttu-id="63630-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="63630-115">**Element**</span></span>|<span data-ttu-id="63630-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="63630-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63630-117">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="63630-117">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="63630-118">Representa la lista de relaciones de organización para la organización seleccionada y direcciones SMTP.</span><span class="sxs-lookup"><span data-stu-id="63630-118">Represents the list of organization relationships for the selected organization and SMTP addresses.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="63630-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="63630-119">Parent elements</span></span>

|<span data-ttu-id="63630-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="63630-120">**Element**</span></span>|<span data-ttu-id="63630-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="63630-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63630-122">Respuesta (GetOrganizationRelationship) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="63630-122">Response (GetOrganizationRelationship) (SOAP)</span></span>](response-getorganizationrelationshipsoap.md) <br/> |<span data-ttu-id="63630-123">Contiene la información de respuesta de la [operación de GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="63630-123">Contains the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) response information.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="63630-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="63630-124">Text value</span></span>

<span data-ttu-id="63630-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="63630-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="63630-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="63630-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63630-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="63630-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="63630-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="63630-128">Schema Name</span></span>  <br/> |<span data-ttu-id="63630-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="63630-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="63630-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="63630-130">Validation File</span></span>  <br/> |<span data-ttu-id="63630-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="63630-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="63630-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="63630-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="63630-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="63630-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63630-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="63630-134">See also</span></span>



[<span data-ttu-id="63630-135">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="63630-135">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

