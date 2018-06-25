---
title: RequestedSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 8d713d22-580c-49a5-99f5-ee532443e89a
description: El elemento RequestedSettings contiene los nombres de las opciones de configuración solicitado.
ms.openlocfilehash: 025f86d417ea2041a3247ac67b065d75c8f75599
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837136"
---
# <a name="requestedsettings-soap"></a><span data-ttu-id="6d0d4-103">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6d0d4-103">RequestedSettings (SOAP)</span></span>

<span data-ttu-id="6d0d4-104">El elemento **RequestedSettings** contiene los nombres de las opciones de configuración solicitado.</span><span class="sxs-lookup"><span data-stu-id="6d0d4-104">The **RequestedSettings** element contains the names of the requested configuration settings.</span></span> 
  
```XML
<RequestedSettings>
   <Setting/>
</RequestedSettings>
```

 <span data-ttu-id="6d0d4-105">**RequestedSettings**</span><span class="sxs-lookup"><span data-stu-id="6d0d4-105">**RequestedSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6d0d4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6d0d4-106">Attributes and elements</span></span>

<span data-ttu-id="6d0d4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6d0d4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d0d4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6d0d4-108">Attributes</span></span>

<span data-ttu-id="6d0d4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6d0d4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6d0d4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6d0d4-110">Child elements</span></span>

|<span data-ttu-id="6d0d4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6d0d4-111">**Element**</span></span>|<span data-ttu-id="6d0d4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6d0d4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d0d4-113">Configuración (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6d0d4-113">Setting (SOAP)</span></span>](setting-soap.md) <br/> |<span data-ttu-id="6d0d4-114">Representa una opción de configuración que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="6d0d4-114">Represents a configuration setting to be returned.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6d0d4-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6d0d4-115">Parent elements</span></span>

|<span data-ttu-id="6d0d4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="6d0d4-116">**Element**</span></span>|<span data-ttu-id="6d0d4-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6d0d4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d0d4-118">GetUserSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6d0d4-118">GetUserSettingsRequest (SOAP)</span></span>](getusersettingsrequest-soap.md) <br/> |<span data-ttu-id="6d0d4-119">Representa una solicitud para recuperar la configuración especificada para uno o varios usuarios.</span><span class="sxs-lookup"><span data-stu-id="6d0d4-119">Represents a request to retrieve specified settings for one or more users.</span></span>  <br/> |
|[<span data-ttu-id="6d0d4-120">Solicitud (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6d0d4-120">Request (SOAP)</span></span>](request-soap.md) <br/> |<span data-ttu-id="6d0d4-121">Contiene las opciones de configuración solicitado y los usuarios de destino.</span><span class="sxs-lookup"><span data-stu-id="6d0d4-121">Contains the requested configuration settings and the target users.</span></span>  <br/> |
|[<span data-ttu-id="6d0d4-122">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6d0d4-122">GetDomainSettingsRequest (SOAP)</span></span>](getdomainsettingsrequest-soap.md) <br/> |<span data-ttu-id="6d0d4-123">Representa una solicitud de [operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="6d0d4-123">Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="6d0d4-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6d0d4-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d0d4-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6d0d4-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="6d0d4-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6d0d4-126">Schema Name</span></span>  <br/> |<span data-ttu-id="6d0d4-127">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="6d0d4-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="6d0d4-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6d0d4-128">Validation File</span></span>  <br/> |<span data-ttu-id="6d0d4-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6d0d4-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6d0d4-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6d0d4-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="6d0d4-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="6d0d4-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6d0d4-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d0d4-132">See also</span></span>



[<span data-ttu-id="6d0d4-133">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6d0d4-133">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="6d0d4-134">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6d0d4-134">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

