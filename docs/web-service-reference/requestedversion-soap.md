---
title: RequestedVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 962036c9-9b13-4669-bed2-2502c0f5aabe
description: El elemento RequestedVersion especifica la versión de servicio mínimo que el cliente desea recibir la solicitud que va a procesar en.
ms.openlocfilehash: 0d8682c33790d2d26001512ad9e2191ae52074d0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837134"
---
# <a name="requestedversion-soap"></a><span data-ttu-id="bb3a3-103">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bb3a3-103">RequestedVersion (SOAP)</span></span>

<span data-ttu-id="bb3a3-104">El elemento **RequestedVersion** especifica la versión de servicio mínimo que el cliente desea recibir la solicitud que va a procesar en.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-104">The **RequestedVersion** element specifies the minimum service version that the client wants the request to be processed on.</span></span> 
  
```XML
<RequestedVersion/>
```

 <span data-ttu-id="bb3a3-105">**ExchangeVersion**</span><span class="sxs-lookup"><span data-stu-id="bb3a3-105">**ExchangeVersion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bb3a3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bb3a3-106">Attributes and elements</span></span>

<span data-ttu-id="bb3a3-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb3a3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="bb3a3-108">Attributes</span></span>

<span data-ttu-id="bb3a3-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bb3a3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bb3a3-110">Child elements</span></span>

<span data-ttu-id="bb3a3-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bb3a3-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bb3a3-112">Parent elements</span></span>

|<span data-ttu-id="bb3a3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bb3a3-113">**Element**</span></span>|<span data-ttu-id="bb3a3-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb3a3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb3a3-115">Solicitud (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bb3a3-115">Request (SOAP)</span></span>](request-soap.md) <br/> |<span data-ttu-id="bb3a3-116">Contiene las opciones de configuración solicitado y los usuarios de destino.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-116">Contains the requested configuration settings and the target users.</span></span>  <br/> |
|[<span data-ttu-id="bb3a3-117">Solicitud (SOAP) (GetDomainSettings)</span><span class="sxs-lookup"><span data-stu-id="bb3a3-117">Request (GetDomainSettings) (SOAP)</span></span>](request-getdomainsettingssoap.md) <br/> |<span data-ttu-id="bb3a3-118">Representa una solicitud para obtener la configuración de dominio.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-118">Represents a request to get domain settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bb3a3-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="bb3a3-119">Text value</span></span>

<span data-ttu-id="bb3a3-120">El valor de texto para el elemento **RequestedVersion** puede ser Exchange2010, Exchange2010_SP1, Exchange2010_SP2 o Exchange2013.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-120">The text value for the **RequestedVersion** element can be Exchange2010, Exchange2010_SP1, Exchange2010_SP2, or Exchange2013.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bb3a3-121">Notas</span><span class="sxs-lookup"><span data-stu-id="bb3a3-121">Remarks</span></span>

<span data-ttu-id="bb3a3-122">Si este elemento no está presente, se utiliza la versión más reciente del servicio.</span><span class="sxs-lookup"><span data-stu-id="bb3a3-122">If this element is not present, the latest service version is used.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bb3a3-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bb3a3-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb3a3-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bb3a3-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="bb3a3-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bb3a3-125">Schema Name</span></span>  <br/> |<span data-ttu-id="bb3a3-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="bb3a3-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="bb3a3-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bb3a3-127">Validation File</span></span>  <br/> |<span data-ttu-id="bb3a3-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bb3a3-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bb3a3-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bb3a3-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="bb3a3-130">False</span><span class="sxs-lookup"><span data-stu-id="bb3a3-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb3a3-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="bb3a3-131">See also</span></span>



[<span data-ttu-id="bb3a3-132">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bb3a3-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="bb3a3-133">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bb3a3-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

