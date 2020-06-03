---
title: TargetApplicationUri (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e13c0edd-2ab1-49bb-a993-54a8db2dfbb9
description: El elemento TargetApplicationUri define el URI de la aplicación de destino. El elemento TargetApplicationUri es solo para uso interno. Los clientes no usan este elemento.
ms.openlocfilehash: 88968aac604b77cd057dbc69c396227a489ac9a8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457091"
---
# <a name="targetapplicationuri-soap"></a><span data-ttu-id="99675-105">TargetApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="99675-105">TargetApplicationUri (SOAP)</span></span>

<span data-ttu-id="99675-106">El elemento **TargetApplicationUri** define el URI de la aplicación de destino.</span><span class="sxs-lookup"><span data-stu-id="99675-106">The **TargetApplicationUri** element defines the target application URI.</span></span> <span data-ttu-id="99675-107">El elemento **TargetApplicationUri** es solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="99675-107">The **TargetApplicationUri** element is for internal use only.</span></span> <span data-ttu-id="99675-108">Los clientes no usan este elemento.</span><span class="sxs-lookup"><span data-stu-id="99675-108">This element is not used by clients.</span></span> 
  
```XML
<TargetApplicationUri/>
```

 <span data-ttu-id="99675-109">**anyURI**</span><span class="sxs-lookup"><span data-stu-id="99675-109">**anyURI**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="99675-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="99675-110">Attributes and elements</span></span>

<span data-ttu-id="99675-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="99675-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99675-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="99675-112">Attributes</span></span>

<span data-ttu-id="99675-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="99675-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="99675-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="99675-114">Child elements</span></span>

<span data-ttu-id="99675-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="99675-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="99675-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="99675-116">Parent elements</span></span>

|<span data-ttu-id="99675-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99675-117">**Element**</span></span>|<span data-ttu-id="99675-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99675-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99675-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="99675-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="99675-120">Representa una lista de relaciones de organización para una sola organización</span><span class="sxs-lookup"><span data-stu-id="99675-120">Represents a list of organization relationships for a single organization</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99675-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99675-121">Remarks</span></span>

<span data-ttu-id="99675-122">Este elemento define el URI de destino de la organización externa.</span><span class="sxs-lookup"><span data-stu-id="99675-122">This element defines the target URI of the external organization.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99675-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="99675-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99675-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="99675-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="99675-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="99675-125">Schema Name</span></span>  <br/> |<span data-ttu-id="99675-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="99675-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="99675-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="99675-127">Validation File</span></span>  <br/> |<span data-ttu-id="99675-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="99675-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="99675-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="99675-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="99675-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="99675-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99675-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="99675-131">See also</span></span>



[<span data-ttu-id="99675-132">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="99675-132">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

