---
title: GetUserSettingsResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: e7cd470d-5861-41e7-9e66-73ef7a59700b
description: El elemento GetUserSettingsResponse representa una respuesta a una solicitud de operación (SOAP) GetUserSettings.
ms.openlocfilehash: 24dbfb1582f628fd0130aa82ea5f1beedd31b156
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835705"
---
# <a name="getusersettingsresponse-soap"></a><span data-ttu-id="e6c6f-103">GetUserSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e6c6f-103">GetUserSettingsResponse (SOAP)</span></span>

<span data-ttu-id="e6c6f-104">El elemento **GetUserSettingsResponse** representa una respuesta a una solicitud de [operación GetUserSettings (SOAP)](getusersettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="e6c6f-104">The **GetUserSettingsResponse** element represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span> 
  
```XML
<GetUserSettingsResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <UserResponses/>
</GetUserSettingsResponse>
```

 <span data-ttu-id="e6c6f-105">**GetUserSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-105">**GetUserSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e6c6f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e6c6f-106">Attributes and elements</span></span>

<span data-ttu-id="e6c6f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6c6f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e6c6f-108">Attributes</span></span>

<span data-ttu-id="e6c6f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e6c6f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e6c6f-110">Child elements</span></span>

|<span data-ttu-id="e6c6f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-111">**Element**</span></span>|<span data-ttu-id="e6c6f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e6c6f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6c6f-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e6c6f-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="e6c6f-114">Representa un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="e6c6f-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e6c6f-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="e6c6f-116">Representa un mensaje en el que está asociado con un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="e6c6f-117">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e6c6f-117">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="e6c6f-118">Contiene las opciones de configuración para cada usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-118">Contains the configuration settings for each requested user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e6c6f-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e6c6f-119">Parent elements</span></span>

<span data-ttu-id="e6c6f-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="e6c6f-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e6c6f-121">Text value</span></span>

<span data-ttu-id="e6c6f-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e6c6f-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e6c6f-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e6c6f-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6c6f-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e6c6f-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="e6c6f-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e6c6f-125">Schema Name</span></span>  <br/> |<span data-ttu-id="e6c6f-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="e6c6f-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="e6c6f-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e6c6f-127">Validation File</span></span>  <br/> |<span data-ttu-id="e6c6f-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e6c6f-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e6c6f-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e6c6f-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="e6c6f-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="e6c6f-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6c6f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6c6f-131">See also</span></span>



[<span data-ttu-id="e6c6f-132">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e6c6f-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

