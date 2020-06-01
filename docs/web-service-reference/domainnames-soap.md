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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458421"
---
# <a name="domainnames-soap"></a><span data-ttu-id="1d324-105">DomainNames (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1d324-105">DomainNames (SOAP)</span></span>

<span data-ttu-id="1d324-106">El elemento **DomainNames** representa la colección de nombres de dominio.</span><span class="sxs-lookup"><span data-stu-id="1d324-106">The **DomainNames** element represents the domain names collection.</span></span> <span data-ttu-id="1d324-107">El elemento **DomainNames** es solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="1d324-107">The **DomainNames** element is for internal use only.</span></span> <span data-ttu-id="1d324-108">Los clientes no usan este elemento.</span><span class="sxs-lookup"><span data-stu-id="1d324-108">This element is not used by clients.</span></span> 
  
```XML
<DomainNames>
    <Domains/>
</DomainNames>
```

 <span data-ttu-id="1d324-109">**DomainNames**</span><span class="sxs-lookup"><span data-stu-id="1d324-109">**DomainNames**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d324-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1d324-110">Attributes and elements</span></span>

<span data-ttu-id="1d324-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1d324-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d324-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="1d324-112">Attributes</span></span>

<span data-ttu-id="1d324-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1d324-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1d324-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1d324-114">Child elements</span></span>

|<span data-ttu-id="1d324-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1d324-115">**Element**</span></span>|<span data-ttu-id="1d324-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d324-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d324-117">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1d324-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="1d324-118">Representa una colección de dominios que se devuelven desde la [operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md), la [operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)o la [operación GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md).</span><span class="sxs-lookup"><span data-stu-id="1d324-118">Represents a collection of domains that are returned from the [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md), or the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1d324-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1d324-119">Parent elements</span></span>

|<span data-ttu-id="1d324-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1d324-120">**Element**</span></span>|<span data-ttu-id="1d324-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d324-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d324-122">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1d324-122">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="1d324-123">Representa una lista de relaciones de organización para una sola organización.</span><span class="sxs-lookup"><span data-stu-id="1d324-123">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1d324-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1d324-124">Text value</span></span>

<span data-ttu-id="1d324-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1d324-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1d324-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d324-126">Remarks</span></span>

<span data-ttu-id="1d324-127">Este elemento representa los dominios SMTP de las organizaciones externas.</span><span class="sxs-lookup"><span data-stu-id="1d324-127">This element represents the SMTP domains of the external organizations.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d324-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1d324-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d324-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d324-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="1d324-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1d324-130">Schema Name</span></span>  <br/> |<span data-ttu-id="1d324-131">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="1d324-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="1d324-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1d324-132">Validation File</span></span>  <br/> |<span data-ttu-id="1d324-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="1d324-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1d324-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1d324-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="1d324-135">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1d324-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d324-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d324-136">See also</span></span>

- [<span data-ttu-id="1d324-137">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1d324-137">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

