---
title: TargetSharingEpr (SOAP)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0115a740-9264-4e57-a410-197bb39e6c81
description: El elemento TargetSharingEpr representa la propiedad TargetSharingEpr. El elemento TargetSharingEpr es solo para uso interno.
ms.openlocfilehash: 8cb8d114ae43dfc8ad76aebe87e0e920c16477f2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457084"
---
# <a name="targetsharingepr-soap"></a><span data-ttu-id="630b5-104">TargetSharingEpr (SOAP)</span><span class="sxs-lookup"><span data-stu-id="630b5-104">TargetSharingEpr (SOAP)</span></span>
 
<span data-ttu-id="630b5-105">El elemento **TargetSharingEpr** representa la propiedad **TargetSharingEpr** .</span><span class="sxs-lookup"><span data-stu-id="630b5-105">The **TargetSharingEpr** element represents the **TargetSharingEpr** property.</span></span> <span data-ttu-id="630b5-106">El elemento **TargetSharingEpr** es solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="630b5-106">The **TargetSharingEpr** element is for internal use only.</span></span> <span data-ttu-id="630b5-107">Los clientes no usan este elemento.</span><span class="sxs-lookup"><span data-stu-id="630b5-107">This element is not used by clients.</span></span> 
  
```XML
<TargetSharingEpr/>
```

<span data-ttu-id="630b5-108">**anyURI**</span><span class="sxs-lookup"><span data-stu-id="630b5-108">**anyURI**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="630b5-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="630b5-109">Attributes and elements</span></span>

<span data-ttu-id="630b5-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="630b5-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="630b5-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="630b5-111">Attributes</span></span>

<span data-ttu-id="630b5-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="630b5-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="630b5-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="630b5-113">Child elements</span></span>

<span data-ttu-id="630b5-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="630b5-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="630b5-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="630b5-115">Parent elements</span></span>

|<span data-ttu-id="630b5-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="630b5-116">**Element**</span></span>|<span data-ttu-id="630b5-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="630b5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="630b5-118">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="630b5-118">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="630b5-119">Representa una lista de relaciones de organización para una sola organización.</span><span class="sxs-lookup"><span data-stu-id="630b5-119">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="630b5-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="630b5-120">Remarks</span></span>

<span data-ttu-id="630b5-121">Este elemento especifica la dirección URL del servidor de destino para la organización externa.</span><span class="sxs-lookup"><span data-stu-id="630b5-121">This element specifies the URL of the target server for the external organization.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="630b5-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="630b5-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="630b5-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="630b5-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="630b5-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="630b5-124">Schema Name</span></span>  <br/> |<span data-ttu-id="630b5-125">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="630b5-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="630b5-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="630b5-126">Validation File</span></span>  <br/> |<span data-ttu-id="630b5-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="630b5-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="630b5-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="630b5-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="630b5-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="630b5-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="630b5-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="630b5-130">See also</span></span>

- [<span data-ttu-id="630b5-131">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="630b5-131">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

