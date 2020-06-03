---
title: DeliveryReportEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ab522bc-40ea-4e43-aa57-6d2562db35e9
description: El elemento DeliveryReportEnabled representa la marca DeliveryReportEnabled (). El elemento DeliveryReportEnabled es solo para uso interno. Los clientes no usan este elemento.
ms.openlocfilehash: 2a163b3e6ceaa169cc8f76f395b7d501419a31ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458477"
---
# <a name="deliveryreportenabled-soap"></a><span data-ttu-id="5c294-105">DeliveryReportEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5c294-105">DeliveryReportEnabled (SOAP)</span></span>

<span data-ttu-id="5c294-106">El elemento **DeliveryReportEnabled** representa la marca **DeliveryReportEnabled ()** .</span><span class="sxs-lookup"><span data-stu-id="5c294-106">The **DeliveryReportEnabled** element represents the **DeliveryReportEnabled()** flag.</span></span> <span data-ttu-id="5c294-107">El elemento **DeliveryReportEnabled** es solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="5c294-107">The **DeliveryReportEnabled** element is for internal use only.</span></span> <span data-ttu-id="5c294-108">Los clientes no usan este elemento.</span><span class="sxs-lookup"><span data-stu-id="5c294-108">This element is not used by clients.</span></span> 
  
```XML
<DeliveryReportEnabled>true | false</DeliveryReportEnabled>
```

 <span data-ttu-id="5c294-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="5c294-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5c294-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5c294-110">Attributes and elements</span></span>

<span data-ttu-id="5c294-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5c294-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c294-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="5c294-112">Attributes</span></span>

<span data-ttu-id="5c294-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5c294-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5c294-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5c294-114">Child elements</span></span>

<span data-ttu-id="5c294-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5c294-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5c294-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5c294-116">Parent elements</span></span>

|<span data-ttu-id="5c294-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5c294-117">**Element**</span></span>|<span data-ttu-id="5c294-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c294-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c294-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5c294-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="5c294-120">Representa una lista de relaciones de organización para una sola organización.</span><span class="sxs-lookup"><span data-stu-id="5c294-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5c294-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5c294-121">Text value</span></span>

<span data-ttu-id="5c294-122">Un valor de texto de true para el elemento DeliveryReportEnabled indica que se pueden usar los informes de entrega de los usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="5c294-122">A text value of true for the DeliveryReportEnabled element indicates that the delivery reports from users in the organization can be used.</span></span> <span data-ttu-id="5c294-123">Un valor de False indica que deben suprimirse los informes de entrega.</span><span class="sxs-lookup"><span data-stu-id="5c294-123">A value of false indicates that the delivery reports should suppressed.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5c294-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5c294-124">Remarks</span></span>

<span data-ttu-id="5c294-125">Use este elemento para permitir o suprimir informes de entrega del servidor.</span><span class="sxs-lookup"><span data-stu-id="5c294-125">Use this element to allow or suppress delivery reports from the server.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c294-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5c294-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c294-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c294-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="5c294-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5c294-128">Schema Name</span></span>  <br/> |<span data-ttu-id="5c294-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="5c294-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="5c294-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5c294-130">Validation File</span></span>  <br/> |<span data-ttu-id="5c294-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5c294-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5c294-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5c294-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="5c294-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="5c294-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c294-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c294-134">See also</span></span>

- [<span data-ttu-id="5c294-135">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="5c294-135">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

