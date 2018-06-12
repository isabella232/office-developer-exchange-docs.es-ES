---
title: RequestType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequestType
api_type:
- schema
ms.assetid: 4e657e57-528f-4250-a99c-f9850bbbcec5
description: El elemento RequestType identifica si una solicitud de proxy es una solicitud de entre bosques o entre sitios.
ms.openlocfilehash: 96a4d57432b15aa54fff2618df458fc75cb227f3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837139"
---
# <a name="requesttype"></a><span data-ttu-id="0c2c5-103">RequestType</span><span class="sxs-lookup"><span data-stu-id="0c2c5-103">RequestType</span></span>

<span data-ttu-id="0c2c5-104">El elemento **RequestType** identifica si una solicitud de proxy es una solicitud de entre bosques o entre sitios.</span><span class="sxs-lookup"><span data-stu-id="0c2c5-104">The **RequestType** element identifies whether a proxy request is a cross-site or a cross-forest request.</span></span> 
  
```xml
<RequestType>CrossSite or CrossForest</RequestType>
```

 <span data-ttu-id="0c2c5-105">**AvailabilityProxyRequestType**</span><span class="sxs-lookup"><span data-stu-id="0c2c5-105">**AvailabilityProxyRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0c2c5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0c2c5-106">Attributes and elements</span></span>

<span data-ttu-id="0c2c5-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0c2c5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c2c5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0c2c5-108">Attributes</span></span>

<span data-ttu-id="0c2c5-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0c2c5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0c2c5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0c2c5-110">Child elements</span></span>

<span data-ttu-id="0c2c5-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0c2c5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0c2c5-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0c2c5-112">Parent elements</span></span>

<span data-ttu-id="0c2c5-113">Este elemento no tiene un elemento primario en el esquema.</span><span class="sxs-lookup"><span data-stu-id="0c2c5-113">This element does not have a parent in the schema.</span></span> <span data-ttu-id="0c2c5-114">Este elemento se usa en el encabezado SOAP.</span><span class="sxs-lookup"><span data-stu-id="0c2c5-114">This element is used in the SOAP header.</span></span> <span data-ttu-id="0c2c5-115">Para obtener más información acerca de cómo se usa este elemento, consulte el archivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="0c2c5-115">For more information about how this element is used, see the WSDL file.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="0c2c5-116">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0c2c5-116">Text value</span></span>

<span data-ttu-id="0c2c5-117">Un valor de texto es necesario para este elemento.</span><span class="sxs-lookup"><span data-stu-id="0c2c5-117">A text value is required for this element.</span></span> <span data-ttu-id="0c2c5-118">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="0c2c5-118">The following are the possible values:</span></span>
  
- <span data-ttu-id="0c2c5-119">CrossSite</span><span class="sxs-lookup"><span data-stu-id="0c2c5-119">CrossSite</span></span>
    
- <span data-ttu-id="0c2c5-120">CrossForest</span><span class="sxs-lookup"><span data-stu-id="0c2c5-120">CrossForest</span></span>
    
## <a name="element-information"></a><span data-ttu-id="0c2c5-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0c2c5-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c2c5-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0c2c5-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0c2c5-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0c2c5-123">Schema name</span></span>  <br/> |<span data-ttu-id="0c2c5-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0c2c5-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="0c2c5-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0c2c5-125">Validation file</span></span>  <br/> |<span data-ttu-id="0c2c5-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0c2c5-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0c2c5-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0c2c5-127">Can be empty</span></span>  <br/> |<span data-ttu-id="0c2c5-128">False</span><span class="sxs-lookup"><span data-stu-id="0c2c5-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c2c5-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="0c2c5-129">See also</span></span>



- [<span data-ttu-id="0c2c5-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0c2c5-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

