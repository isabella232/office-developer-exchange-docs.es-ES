---
title: AutodiscoverResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 203a5ac3-ebd0-4514-acbe-bc1c74638127
description: El elemento AutodiscoverResponse (SOAP) representa el elemento base para todas las respuestas devueltas por el servicio Detección automática.
ms.openlocfilehash: 81fd557578bde9552d07e24386c93903e44a9afa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463968"
---
# <a name="autodiscoverresponse-soap"></a><span data-ttu-id="15205-103">AutodiscoverResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="15205-103">AutodiscoverResponse (SOAP)</span></span>

<span data-ttu-id="15205-104">El elemento **AutodiscoverResponse (SOAP)** representa el elemento base para todas las respuestas devueltas por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="15205-104">The **AutodiscoverResponse (SOAP)** element represents the base element for all responses that are returned by the Autodiscover service.</span></span> 
  
- [<span data-ttu-id="15205-105">AutodiscoverResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="15205-105">AutodiscoverResponse (SOAP)</span></span>](autodiscoverresponse-soap.md)
  
```XML
<AutodiscoverResponse>
    <UserResponses/>
    <UserSettingErrors/>
    <UserSettings/>
</AutodiscoverResponse>

```

 <span data-ttu-id="15205-106">**AutodiscoverResponse**</span><span class="sxs-lookup"><span data-stu-id="15205-106">**AutodiscoverResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15205-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="15205-107">Attributes and elements</span></span>

<span data-ttu-id="15205-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="15205-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15205-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="15205-109">Attributes</span></span>

<span data-ttu-id="15205-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="15205-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="15205-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="15205-111">Child elements</span></span>

|<span data-ttu-id="15205-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="15205-112">**Element**</span></span>|<span data-ttu-id="15205-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="15205-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15205-114">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="15205-114">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="15205-115">Representa una colección de elementos [UserResponse (SOAP)](userresponse-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="15205-115">Represents a collection of [UserResponse (SOAP)](userresponse-soap.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="15205-116">UserSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="15205-116">UserSettingErrors (SOAP)</span></span>](usersettingerrors-soap.md) <br/> |<span data-ttu-id="15205-117">Representa una colección de elementos [UserSettingError (SOAP)](usersettingerror-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="15205-117">Represents a collection of [UserSettingError (SOAP)](usersettingerror-soap.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="15205-118">UserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="15205-118">UserSettings (SOAP)</span></span>](usersettings-soap.md) <br/> |<span data-ttu-id="15205-119">Representa una colección de elementos [UserSetting (SOAP)](usersetting-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="15205-119">Represents a collection of [UserSetting (SOAP)](usersetting-soap.md) elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="15205-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="15205-120">Parent elements</span></span>

<span data-ttu-id="15205-121">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="15205-121">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="15205-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="15205-122">Text value</span></span>

<span data-ttu-id="15205-123">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="15205-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15205-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="15205-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15205-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="15205-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="15205-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="15205-126">Schema Name</span></span>  <br/> |<span data-ttu-id="15205-127">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="15205-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="15205-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="15205-128">Validation File</span></span>  <br/> |<span data-ttu-id="15205-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="15205-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="15205-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="15205-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="15205-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="15205-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15205-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="15205-132">See also</span></span>

- [<span data-ttu-id="15205-133">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="15205-133">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="15205-134">Operación GetFederationInformation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="15205-134">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)
- [<span data-ttu-id="15205-135">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="15205-135">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

