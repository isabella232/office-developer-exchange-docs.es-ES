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
description: El elemento RequestedVersion especifica la versión de servicio mínima en la que el cliente desea que se procese la solicitud.
ms.openlocfilehash: ded276b3eb2c70b6edd39ca12289098de2b3faea
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459170"
---
# <a name="requestedversion-soap"></a><span data-ttu-id="2fa92-103">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2fa92-103">RequestedVersion (SOAP)</span></span>

<span data-ttu-id="2fa92-104">El elemento **RequestedVersion** especifica la versión de servicio mínima en la que el cliente desea que se procese la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2fa92-104">The **RequestedVersion** element specifies the minimum service version that the client wants the request to be processed on.</span></span> 
  
```XML
<RequestedVersion/>
```

 <span data-ttu-id="2fa92-105">**ExchangeVersion**</span><span class="sxs-lookup"><span data-stu-id="2fa92-105">**ExchangeVersion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2fa92-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2fa92-106">Attributes and elements</span></span>

<span data-ttu-id="2fa92-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2fa92-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2fa92-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2fa92-108">Attributes</span></span>

<span data-ttu-id="2fa92-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2fa92-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2fa92-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2fa92-110">Child elements</span></span>

<span data-ttu-id="2fa92-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2fa92-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2fa92-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2fa92-112">Parent elements</span></span>

|<span data-ttu-id="2fa92-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2fa92-113">**Element**</span></span>|<span data-ttu-id="2fa92-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2fa92-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2fa92-115">Solicitud (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2fa92-115">Request (SOAP)</span></span>](request-soap.md) <br/> |<span data-ttu-id="2fa92-116">Contiene las opciones de configuración solicitadas y los usuarios de destino.</span><span class="sxs-lookup"><span data-stu-id="2fa92-116">Contains the requested configuration settings and the target users.</span></span>  <br/> |
|[<span data-ttu-id="2fa92-117">Request (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2fa92-117">Request (GetDomainSettings) (SOAP)</span></span>](request-getdomainsettingssoap.md) <br/> |<span data-ttu-id="2fa92-118">Representa una solicitud para obtener la configuración del dominio.</span><span class="sxs-lookup"><span data-stu-id="2fa92-118">Represents a request to get domain settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2fa92-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2fa92-119">Text value</span></span>

<span data-ttu-id="2fa92-120">El valor de texto del elemento **RequestedVersion** puede ser Exchange2010, Exchange2010_SP1, Exchange2010_SP2 o Exchange2013.</span><span class="sxs-lookup"><span data-stu-id="2fa92-120">The text value for the **RequestedVersion** element can be Exchange2010, Exchange2010_SP1, Exchange2010_SP2, or Exchange2013.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2fa92-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2fa92-121">Remarks</span></span>

<span data-ttu-id="2fa92-122">Si este elemento no está presente, se usa la versión más reciente del servicio.</span><span class="sxs-lookup"><span data-stu-id="2fa92-122">If this element is not present, the latest service version is used.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2fa92-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2fa92-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2fa92-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="2fa92-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="2fa92-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2fa92-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2fa92-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="2fa92-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="2fa92-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2fa92-127">Validation File</span></span>  <br/> |<span data-ttu-id="2fa92-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2fa92-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2fa92-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2fa92-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="2fa92-130">Falso</span><span class="sxs-lookup"><span data-stu-id="2fa92-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2fa92-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fa92-131">See also</span></span>



[<span data-ttu-id="2fa92-132">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2fa92-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="2fa92-133">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2fa92-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

