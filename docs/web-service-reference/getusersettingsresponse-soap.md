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
description: El elemento GetUserSettingsResponse representa una respuesta a una solicitud de operación GetUserSettings (SOAP).
ms.openlocfilehash: a41a195a003789ddaef81f844e47aad689df0937
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530151"
---
# <a name="getusersettingsresponse-soap"></a><span data-ttu-id="64bf4-103">GetUserSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="64bf4-103">GetUserSettingsResponse (SOAP)</span></span>

<span data-ttu-id="64bf4-104">El elemento **GetUserSettingsResponse** representa una respuesta a una solicitud de [operación GetUserSettings (SOAP)](getusersettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="64bf4-104">The **GetUserSettingsResponse** element represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span> 
  
```XML
<GetUserSettingsResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <UserResponses/>
</GetUserSettingsResponse>
```

 <span data-ttu-id="64bf4-105">**GetUserSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="64bf4-105">**GetUserSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="64bf4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="64bf4-106">Attributes and elements</span></span>

<span data-ttu-id="64bf4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="64bf4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64bf4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="64bf4-108">Attributes</span></span>

<span data-ttu-id="64bf4-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="64bf4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="64bf4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="64bf4-110">Child elements</span></span>

|<span data-ttu-id="64bf4-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="64bf4-111">**Element**</span></span>|<span data-ttu-id="64bf4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="64bf4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64bf4-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="64bf4-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="64bf4-114">Representa un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="64bf4-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="64bf4-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="64bf4-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="64bf4-116">Representa un mensaje que está asociado con un código de error devuelto por el servicio de detección automática.</span><span class="sxs-lookup"><span data-stu-id="64bf4-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="64bf4-117">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="64bf4-117">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="64bf4-118">Contiene las opciones de configuración para cada usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="64bf4-118">Contains the configuration settings for each requested user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="64bf4-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="64bf4-119">Parent elements</span></span>

<span data-ttu-id="64bf4-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="64bf4-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="64bf4-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="64bf4-121">Text value</span></span>

<span data-ttu-id="64bf4-122">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="64bf4-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="64bf4-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="64bf4-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64bf4-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="64bf4-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="64bf4-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="64bf4-125">Schema Name</span></span>  <br/> |<span data-ttu-id="64bf4-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="64bf4-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="64bf4-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="64bf4-127">Validation File</span></span>  <br/> |<span data-ttu-id="64bf4-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="64bf4-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="64bf4-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="64bf4-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="64bf4-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="64bf4-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="64bf4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="64bf4-131">See also</span></span>



[<span data-ttu-id="64bf4-132">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="64bf4-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

