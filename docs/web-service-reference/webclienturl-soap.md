---
title: WebClientUrl (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 7f8cb6d6-4aac-4a1f-8bec-2dcb90fc1df6
description: El elemento WebClientUrl representa la dirección URL de un cliente web de Exchange.
ms.openlocfilehash: 649845018acee1706a96f9e37475a6d5c5fa0aa7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840990"
---
# <a name="webclienturl-soap"></a><span data-ttu-id="523ac-103">WebClientUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="523ac-103">WebClientUrl (SOAP)</span></span>

<span data-ttu-id="523ac-104">El elemento **WebClientUrl** representa la dirección URL de un cliente web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="523ac-104">The **WebClientUrl** element represents the URL of an Exchange web client.</span></span> 
  
[<span data-ttu-id="523ac-105">UserSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="523ac-105">UserSetting (SOAP)</span></span>](usersetting-soap.md)
  
[<span data-ttu-id="523ac-106">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="523ac-106">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md)
  
[<span data-ttu-id="523ac-107">WebClientUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="523ac-107">WebClientUrl (SOAP)</span></span>](webclienturl-soap.md)
  
```XML
<WebClientUrl>
    <AuthenticationMethods/>
    <Url/>
</WebClientUrl>
```

 <span data-ttu-id="523ac-108">**WebClientUrl**</span><span class="sxs-lookup"><span data-stu-id="523ac-108">**WebClientUrl**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="523ac-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="523ac-109">Attributes and elements</span></span>

<span data-ttu-id="523ac-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="523ac-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="523ac-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="523ac-111">Attributes</span></span>

<span data-ttu-id="523ac-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="523ac-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="523ac-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="523ac-113">Child elements</span></span>

|<span data-ttu-id="523ac-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="523ac-114">**Element**</span></span>|<span data-ttu-id="523ac-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="523ac-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="523ac-116">AuthenticationMethods (SOAP)</span><span class="sxs-lookup"><span data-stu-id="523ac-116">AuthenticationMethods (SOAP)</span></span>](authenticationmethods-soap.md) <br/> |<span data-ttu-id="523ac-117">Representa el método de autenticación que se utilizará al obtener acceso a la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="523ac-117">Represents the authentication method to use when accessing the specified URL.</span></span>  <br/> |
|[<span data-ttu-id="523ac-118">Dirección URL (SOAP)</span><span class="sxs-lookup"><span data-stu-id="523ac-118">Url (SOAP)</span></span>](url-soap.md) <br/> |<span data-ttu-id="523ac-119">Representa la dirección web para la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="523ac-119">Represents the web address for the URL.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="523ac-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="523ac-120">Parent elements</span></span>

|<span data-ttu-id="523ac-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="523ac-121">**Element**</span></span>|<span data-ttu-id="523ac-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="523ac-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="523ac-123">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="523ac-123">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md) <br/> |<span data-ttu-id="523ac-124">Representa una configuración de usuario que contiene una colección de elementos de **WebClientUrl** .</span><span class="sxs-lookup"><span data-stu-id="523ac-124">Represents a user setting that contains a collection of **WebClientUrl** elements.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="523ac-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="523ac-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="523ac-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="523ac-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="523ac-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="523ac-127">Schema Name</span></span>  <br/> |<span data-ttu-id="523ac-128">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="523ac-128">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="523ac-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="523ac-129">Validation File</span></span>  <br/> |<span data-ttu-id="523ac-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="523ac-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="523ac-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="523ac-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="523ac-132">Verdadero</span><span class="sxs-lookup"><span data-stu-id="523ac-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="523ac-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="523ac-133">See also</span></span>



[<span data-ttu-id="523ac-134">Dirección URL (SOAP)</span><span class="sxs-lookup"><span data-stu-id="523ac-134">Url (SOAP)</span></span>](url-soap.md)
  
[<span data-ttu-id="523ac-135">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="523ac-135">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md)

