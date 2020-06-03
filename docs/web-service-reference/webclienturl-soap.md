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
ms.openlocfilehash: bcf9c8d4fe80de8af4c9500e5e850558a8451d4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464976"
---
# <a name="webclienturl-soap"></a><span data-ttu-id="728b6-103">WebClientUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="728b6-103">WebClientUrl (SOAP)</span></span>

<span data-ttu-id="728b6-104">El elemento **WebClientUrl** representa la dirección URL de un cliente web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="728b6-104">The **WebClientUrl** element represents the URL of an Exchange web client.</span></span> 
  
[<span data-ttu-id="728b6-105">UserSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="728b6-105">UserSetting (SOAP)</span></span>](usersetting-soap.md)
  
[<span data-ttu-id="728b6-106">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="728b6-106">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md)
  
[<span data-ttu-id="728b6-107">WebClientUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="728b6-107">WebClientUrl (SOAP)</span></span>](webclienturl-soap.md)
  
```XML
<WebClientUrl>
    <AuthenticationMethods/>
    <Url/>
</WebClientUrl>
```

 <span data-ttu-id="728b6-108">**WebClientUrl**</span><span class="sxs-lookup"><span data-stu-id="728b6-108">**WebClientUrl**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="728b6-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="728b6-109">Attributes and elements</span></span>

<span data-ttu-id="728b6-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="728b6-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="728b6-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="728b6-111">Attributes</span></span>

<span data-ttu-id="728b6-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="728b6-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="728b6-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="728b6-113">Child elements</span></span>

|<span data-ttu-id="728b6-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="728b6-114">**Element**</span></span>|<span data-ttu-id="728b6-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="728b6-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="728b6-116">AuthenticationMethods (SOAP)</span><span class="sxs-lookup"><span data-stu-id="728b6-116">AuthenticationMethods (SOAP)</span></span>](authenticationmethods-soap.md) <br/> |<span data-ttu-id="728b6-117">Representa el método de autenticación que se va a usar para obtener acceso a la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="728b6-117">Represents the authentication method to use when accessing the specified URL.</span></span>  <br/> |
|[<span data-ttu-id="728b6-118">URL (SOAP)</span><span class="sxs-lookup"><span data-stu-id="728b6-118">Url (SOAP)</span></span>](url-soap.md) <br/> |<span data-ttu-id="728b6-119">Representa la dirección Web de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="728b6-119">Represents the web address for the URL.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="728b6-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="728b6-120">Parent elements</span></span>

|<span data-ttu-id="728b6-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="728b6-121">**Element**</span></span>|<span data-ttu-id="728b6-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="728b6-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="728b6-123">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="728b6-123">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md) <br/> |<span data-ttu-id="728b6-124">Representa una configuración de usuario que contiene una colección de elementos **WebClientUrl** .</span><span class="sxs-lookup"><span data-stu-id="728b6-124">Represents a user setting that contains a collection of **WebClientUrl** elements.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="728b6-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="728b6-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="728b6-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="728b6-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="728b6-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="728b6-127">Schema Name</span></span>  <br/> |<span data-ttu-id="728b6-128">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="728b6-128">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="728b6-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="728b6-129">Validation File</span></span>  <br/> |<span data-ttu-id="728b6-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="728b6-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="728b6-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="728b6-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="728b6-132">Verdadero</span><span class="sxs-lookup"><span data-stu-id="728b6-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="728b6-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="728b6-133">See also</span></span>



[<span data-ttu-id="728b6-134">URL (SOAP)</span><span class="sxs-lookup"><span data-stu-id="728b6-134">Url (SOAP)</span></span>](url-soap.md)
  
[<span data-ttu-id="728b6-135">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="728b6-135">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md)

