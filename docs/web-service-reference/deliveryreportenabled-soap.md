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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458477"
---
# <a name="deliveryreportenabled-soap"></a><span data-ttu-id="3b4dc-105">DeliveryReportEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b4dc-105">DeliveryReportEnabled (SOAP)</span></span>

<span data-ttu-id="3b4dc-106">El elemento **DeliveryReportEnabled** representa la marca **DeliveryReportEnabled ()** .</span><span class="sxs-lookup"><span data-stu-id="3b4dc-106">The **DeliveryReportEnabled** element represents the **DeliveryReportEnabled()** flag.</span></span> <span data-ttu-id="3b4dc-107">El elemento **DeliveryReportEnabled** es solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="3b4dc-107">The **DeliveryReportEnabled** element is for internal use only.</span></span> <span data-ttu-id="3b4dc-108">Los clientes no usan este elemento.</span><span class="sxs-lookup"><span data-stu-id="3b4dc-108">This element is not used by clients.</span></span> 
  
```XML
<DeliveryReportEnabled>true | false</DeliveryReportEnabled>
```

 <span data-ttu-id="3b4dc-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3b4dc-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b4dc-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3b4dc-110">Attributes and elements</span></span>

<span data-ttu-id="3b4dc-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3b4dc-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b4dc-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="3b4dc-112">Attributes</span></span>

<span data-ttu-id="3b4dc-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3b4dc-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b4dc-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3b4dc-114">Child elements</span></span>

<span data-ttu-id="3b4dc-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3b4dc-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3b4dc-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3b4dc-116">Parent elements</span></span>

|<span data-ttu-id="3b4dc-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3b4dc-117">**Element**</span></span>|<span data-ttu-id="3b4dc-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3b4dc-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b4dc-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b4dc-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="3b4dc-120">Representa una lista de relaciones de organización para una sola organización.</span><span class="sxs-lookup"><span data-stu-id="3b4dc-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3b4dc-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3b4dc-121">Text value</span></span>

<span data-ttu-id="3b4dc-122">Un valor de texto de true para el elemento DeliveryReportEnabled indica que se pueden usar los informes de entrega de los usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="3b4dc-122">A text value of true for the DeliveryReportEnabled element indicates that the delivery reports from users in the organization can be used.</span></span> <span data-ttu-id="3b4dc-123">Un valor de False indica que deben suprimirse los informes de entrega.</span><span class="sxs-lookup"><span data-stu-id="3b4dc-123">A value of false indicates that the delivery reports should suppressed.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3b4dc-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3b4dc-124">Remarks</span></span>

<span data-ttu-id="3b4dc-125">Use este elemento para permitir o suprimir informes de entrega del servidor.</span><span class="sxs-lookup"><span data-stu-id="3b4dc-125">Use this element to allow or suppress delivery reports from the server.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3b4dc-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3b4dc-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b4dc-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b4dc-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="3b4dc-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3b4dc-128">Schema Name</span></span>  <br/> |<span data-ttu-id="3b4dc-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="3b4dc-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="3b4dc-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3b4dc-130">Validation File</span></span>  <br/> |<span data-ttu-id="3b4dc-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3b4dc-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3b4dc-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3b4dc-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="3b4dc-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="3b4dc-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b4dc-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b4dc-134">See also</span></span>

- [<span data-ttu-id="3b4dc-135">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3b4dc-135">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

