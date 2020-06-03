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
description: El elemento RequestType identifica si una solicitud de proxy es una solicitud entre sitios o entre bosques.
ms.openlocfilehash: 278a65a1f2ce4cb433ae8099703d70d0a2cafa3b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455971"
---
# <a name="requesttype"></a><span data-ttu-id="70895-103">RequestType</span><span class="sxs-lookup"><span data-stu-id="70895-103">RequestType</span></span>

<span data-ttu-id="70895-104">El elemento **RequestType** identifica si una solicitud de proxy es una solicitud entre sitios o entre bosques.</span><span class="sxs-lookup"><span data-stu-id="70895-104">The **RequestType** element identifies whether a proxy request is a cross-site or a cross-forest request.</span></span> 
  
```xml
<RequestType>CrossSite or CrossForest</RequestType>
```

 <span data-ttu-id="70895-105">**AvailabilityProxyRequestType**</span><span class="sxs-lookup"><span data-stu-id="70895-105">**AvailabilityProxyRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="70895-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="70895-106">Attributes and elements</span></span>

<span data-ttu-id="70895-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="70895-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70895-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="70895-108">Attributes</span></span>

<span data-ttu-id="70895-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="70895-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="70895-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="70895-110">Child elements</span></span>

<span data-ttu-id="70895-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="70895-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="70895-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="70895-112">Parent elements</span></span>

<span data-ttu-id="70895-113">Este elemento no tiene un elemento primario en el esquema.</span><span class="sxs-lookup"><span data-stu-id="70895-113">This element does not have a parent in the schema.</span></span> <span data-ttu-id="70895-114">Este elemento se usa en el encabezado SOAP.</span><span class="sxs-lookup"><span data-stu-id="70895-114">This element is used in the SOAP header.</span></span> <span data-ttu-id="70895-115">Para obtener más información sobre cómo se usa este elemento, vea el archivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="70895-115">For more information about how this element is used, see the WSDL file.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="70895-116">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="70895-116">Text value</span></span>

<span data-ttu-id="70895-117">Se requiere un valor de texto para este elemento.</span><span class="sxs-lookup"><span data-stu-id="70895-117">A text value is required for this element.</span></span> <span data-ttu-id="70895-118">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="70895-118">The following are the possible values:</span></span>
  
- <span data-ttu-id="70895-119">CrossSite</span><span class="sxs-lookup"><span data-stu-id="70895-119">CrossSite</span></span>
    
- <span data-ttu-id="70895-120">CrossForest</span><span class="sxs-lookup"><span data-stu-id="70895-120">CrossForest</span></span>
    
## <a name="element-information"></a><span data-ttu-id="70895-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="70895-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70895-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="70895-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="70895-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="70895-123">Schema name</span></span>  <br/> |<span data-ttu-id="70895-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="70895-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="70895-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="70895-125">Validation file</span></span>  <br/> |<span data-ttu-id="70895-126">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="70895-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="70895-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="70895-127">Can be empty</span></span>  <br/> |<span data-ttu-id="70895-128">Falso</span><span class="sxs-lookup"><span data-stu-id="70895-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="70895-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="70895-129">See also</span></span>



- [<span data-ttu-id="70895-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="70895-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

