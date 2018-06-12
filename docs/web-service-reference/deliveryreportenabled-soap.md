---
title: DeliveryReportEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ab522bc-40ea-4e43-aa57-6d2562db35e9
description: El elemento DeliveryReportEnabled representa la marca DeliveryReportEnabled(). El elemento DeliveryReportEnabled es sólo para uso interno. Este elemento no se usa en los clientes.
ms.openlocfilehash: 089256a5f75ad92a4f11c5aaf3d175382eeee456
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764123"
---
# <a name="deliveryreportenabled-soap"></a><span data-ttu-id="18bab-105">DeliveryReportEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="18bab-105">DeliveryReportEnabled (SOAP)</span></span>

<span data-ttu-id="18bab-106">El elemento **DeliveryReportEnabled** representa la marca **DeliveryReportEnabled()** .</span><span class="sxs-lookup"><span data-stu-id="18bab-106">The **DeliveryReportEnabled** element represents the **DeliveryReportEnabled()** flag.</span></span> <span data-ttu-id="18bab-107">El elemento **DeliveryReportEnabled** es sólo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="18bab-107">The **DeliveryReportEnabled** element is for internal use only.</span></span> <span data-ttu-id="18bab-108">Este elemento no se usa en los clientes.</span><span class="sxs-lookup"><span data-stu-id="18bab-108">This element is not used by clients.</span></span> 
  
```XML
<DeliveryReportEnabled>true | false</DeliveryReportEnabled>
```

 <span data-ttu-id="18bab-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="18bab-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18bab-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="18bab-110">Attributes and elements</span></span>

<span data-ttu-id="18bab-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="18bab-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18bab-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="18bab-112">Attributes</span></span>

<span data-ttu-id="18bab-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="18bab-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="18bab-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="18bab-114">Child elements</span></span>

<span data-ttu-id="18bab-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="18bab-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="18bab-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="18bab-116">Parent elements</span></span>

|<span data-ttu-id="18bab-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="18bab-117">**Element**</span></span>|<span data-ttu-id="18bab-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="18bab-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18bab-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="18bab-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="18bab-120">Representa una lista de relaciones de organización para una sola organización.</span><span class="sxs-lookup"><span data-stu-id="18bab-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="18bab-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="18bab-121">Text value</span></span>

<span data-ttu-id="18bab-122">Un valor de texto de true para el elemento DeliveryReportEnabled indica que se pueden usar los informes de entrega de los usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="18bab-122">A text value of true for the DeliveryReportEnabled element indicates that the delivery reports from users in the organization can be used.</span></span> <span data-ttu-id="18bab-123">Un valor de false indica que se debe suprimir los informes de entrega.</span><span class="sxs-lookup"><span data-stu-id="18bab-123">A value of false indicates that the delivery reports should suppressed.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="18bab-124">Notas</span><span class="sxs-lookup"><span data-stu-id="18bab-124">Remarks</span></span>

<span data-ttu-id="18bab-125">Use este elemento para permitir o suprimir informes de entrega desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="18bab-125">Use this element to allow or suppress delivery reports from the server.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18bab-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="18bab-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18bab-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="18bab-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="18bab-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="18bab-128">Schema Name</span></span>  <br/> |<span data-ttu-id="18bab-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="18bab-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="18bab-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="18bab-130">Validation File</span></span>  <br/> |<span data-ttu-id="18bab-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="18bab-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="18bab-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="18bab-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="18bab-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="18bab-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18bab-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="18bab-134">See also</span></span>

- [<span data-ttu-id="18bab-135">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="18bab-135">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

