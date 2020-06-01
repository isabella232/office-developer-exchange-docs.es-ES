---
title: GetOrganizationRelationshipSettingsRequest (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e8aa3b3-4bfc-40c3-b96b-9f7062b09309
description: El elemento GetOrganizationRelationshipSettingsRequest representa los parámetros de una llamada a la operación GetOrganizationRelationshipSettings (SOAP). El elemento GetOrganizationRelationshipSettingsRequest es solo para uso interno. Los clientes no usan este elemento.
ms.openlocfilehash: 053bbb8cbe2ccdcf6d544ab1fc92bb81765997e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452737"
---
# <a name="getorganizationrelationshipsettingsrequest-soap"></a><span data-ttu-id="333a9-105">GetOrganizationRelationshipSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="333a9-105">GetOrganizationRelationshipSettingsRequest (SOAP)</span></span>

<span data-ttu-id="333a9-106">El elemento **GetOrganizationRelationshipSettingsRequest** representa los parámetros de una llamada a la operación [GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="333a9-106">The **GetOrganizationRelationshipSettingsRequest** element represents the parameters of a call to the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) operation.</span></span> <span data-ttu-id="333a9-107">El elemento **GetOrganizationRelationshipSettingsRequest** es solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="333a9-107">The **GetOrganizationRelationshipSettingsRequest** element is for internal use only.</span></span> <span data-ttu-id="333a9-108">Los clientes no usan este elemento.</span><span class="sxs-lookup"><span data-stu-id="333a9-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingsRequest>
   <Domains/>
</GetOrganizationRelationshipSettingsRequest>
```

 <span data-ttu-id="333a9-109">**GetOrganizationRelationshipSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="333a9-109">**GetOrganizationRelationshipSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="333a9-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="333a9-110">Attributes and elements</span></span>

<span data-ttu-id="333a9-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="333a9-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="333a9-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="333a9-112">Attributes</span></span>

<span data-ttu-id="333a9-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="333a9-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="333a9-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="333a9-114">Child elements</span></span>

|<span data-ttu-id="333a9-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="333a9-115">**Element**</span></span>|<span data-ttu-id="333a9-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="333a9-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="333a9-117">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="333a9-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="333a9-118">Representa una colección de identificadores de dominio.</span><span class="sxs-lookup"><span data-stu-id="333a9-118">Represents a collection of domain identifiers.</span></span>  <br/> |
|||
   
### <a name="parent-elements"></a><span data-ttu-id="333a9-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="333a9-119">Parent elements</span></span>

<span data-ttu-id="333a9-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="333a9-120">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="333a9-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="333a9-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="333a9-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="333a9-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="333a9-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="333a9-123">Schema Name</span></span>  <br/> |<span data-ttu-id="333a9-124">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="333a9-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="333a9-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="333a9-125">Validation File</span></span>  <br/> |<span data-ttu-id="333a9-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="333a9-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="333a9-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="333a9-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="333a9-128">Verdadero</span><span class="sxs-lookup"><span data-stu-id="333a9-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="333a9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="333a9-129">See also</span></span>



[<span data-ttu-id="333a9-130">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="333a9-130">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

