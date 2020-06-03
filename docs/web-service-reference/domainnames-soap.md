---
title: DomainNames (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 79ffc3f9-25c4-40b5-84ce-09a3c5f892fa
description: El elemento DomainNames representa la colección de nombres de dominio. El elemento DomainNames es solo para uso interno. Los clientes no usan este elemento.
ms.openlocfilehash: 0b425b3cd4c0e7cb2427920d61feb04010a3b123
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458421"
---
# <a name="domainnames-soap"></a><span data-ttu-id="458e5-105">DomainNames (SOAP)</span><span class="sxs-lookup"><span data-stu-id="458e5-105">DomainNames (SOAP)</span></span>

<span data-ttu-id="458e5-106">El elemento **DomainNames** representa la colección de nombres de dominio.</span><span class="sxs-lookup"><span data-stu-id="458e5-106">The **DomainNames** element represents the domain names collection.</span></span> <span data-ttu-id="458e5-107">El elemento **DomainNames** es solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="458e5-107">The **DomainNames** element is for internal use only.</span></span> <span data-ttu-id="458e5-108">Los clientes no usan este elemento.</span><span class="sxs-lookup"><span data-stu-id="458e5-108">This element is not used by clients.</span></span> 
  
```XML
<DomainNames>
    <Domains/>
</DomainNames>
```

 <span data-ttu-id="458e5-109">**DomainNames**</span><span class="sxs-lookup"><span data-stu-id="458e5-109">**DomainNames**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="458e5-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="458e5-110">Attributes and elements</span></span>

<span data-ttu-id="458e5-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="458e5-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="458e5-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="458e5-112">Attributes</span></span>

<span data-ttu-id="458e5-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="458e5-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="458e5-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="458e5-114">Child elements</span></span>

|<span data-ttu-id="458e5-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="458e5-115">**Element**</span></span>|<span data-ttu-id="458e5-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="458e5-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="458e5-117">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="458e5-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="458e5-118">Representa una colección de dominios que se devuelven desde la [operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md), la [operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)o la [operación GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md).</span><span class="sxs-lookup"><span data-stu-id="458e5-118">Represents a collection of domains that are returned from the [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md), or the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="458e5-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="458e5-119">Parent elements</span></span>

|<span data-ttu-id="458e5-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="458e5-120">**Element**</span></span>|<span data-ttu-id="458e5-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="458e5-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="458e5-122">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="458e5-122">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="458e5-123">Representa una lista de relaciones de organización para una sola organización.</span><span class="sxs-lookup"><span data-stu-id="458e5-123">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="458e5-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="458e5-124">Text value</span></span>

<span data-ttu-id="458e5-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="458e5-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="458e5-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="458e5-126">Remarks</span></span>

<span data-ttu-id="458e5-127">Este elemento representa los dominios SMTP de las organizaciones externas.</span><span class="sxs-lookup"><span data-stu-id="458e5-127">This element represents the SMTP domains of the external organizations.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="458e5-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="458e5-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="458e5-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="458e5-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="458e5-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="458e5-130">Schema Name</span></span>  <br/> |<span data-ttu-id="458e5-131">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="458e5-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="458e5-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="458e5-132">Validation File</span></span>  <br/> |<span data-ttu-id="458e5-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="458e5-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="458e5-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="458e5-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="458e5-135">Verdadero</span><span class="sxs-lookup"><span data-stu-id="458e5-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="458e5-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="458e5-136">See also</span></span>

- [<span data-ttu-id="458e5-137">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="458e5-137">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

