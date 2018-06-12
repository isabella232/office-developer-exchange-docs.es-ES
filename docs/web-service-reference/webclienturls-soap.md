---
title: WebClientUrls (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: fdfe6059-a861-4fa2-a20e-ee6ab820bee9
description: El elemento WebClientUrls representa una configuración de usuario que contiene una colección de elementos de WebClientUrl (SOAP).
ms.openlocfilehash: 8d5d6aec67ab183743d7aae9f5d1f303d2949cd0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840985"
---
# <a name="webclienturls-soap"></a><span data-ttu-id="30013-103">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="30013-103">WebClientUrls (SOAP)</span></span>

<span data-ttu-id="30013-104">El elemento **WebClientUrls** representa una configuración de usuario que contiene una colección de elementos de [WebClientUrl (SOAP)](webclienturl-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="30013-104">The **WebClientUrls** element represents a user setting that contains a collection of [WebClientUrl (SOAP)](webclienturl-soap.md) elements.</span></span> 
  
[<span data-ttu-id="30013-105">UserSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="30013-105">UserSetting (SOAP)</span></span>](usersetting-soap.md)
  
[<span data-ttu-id="30013-106">WebClientUrls (SOAP)</span><span class="sxs-lookup"><span data-stu-id="30013-106">WebClientUrls (SOAP)</span></span>](webclienturls-soap.md)
  
[<span data-ttu-id="30013-107">WebClientUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="30013-107">WebClientUrl (SOAP)</span></span>](webclienturl-soap.md)
  
```XML
<WebClientUrls>
     <WebClientUrl/>
</WebClientUrls>

```

 <span data-ttu-id="30013-108">**WebClientUrls**</span><span class="sxs-lookup"><span data-stu-id="30013-108">**WebClientUrls**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="30013-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="30013-109">Attributes and elements</span></span>

<span data-ttu-id="30013-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="30013-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="30013-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="30013-111">Attributes</span></span>

<span data-ttu-id="30013-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="30013-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="30013-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="30013-113">Child elements</span></span>

|<span data-ttu-id="30013-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="30013-114">**Element**</span></span>|<span data-ttu-id="30013-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="30013-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30013-116">WebClientUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="30013-116">WebClientUrl (SOAP)</span></span>](webclienturl-soap.md) <br/> |<span data-ttu-id="30013-117">Representa una dirección URL de cliente de Exchange.</span><span class="sxs-lookup"><span data-stu-id="30013-117">Represents an Exchange client URL.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="30013-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="30013-118">Parent elements</span></span>

|<span data-ttu-id="30013-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="30013-119">**Element**</span></span>|<span data-ttu-id="30013-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="30013-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30013-121">UserSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="30013-121">UserSetting (SOAP)</span></span>](usersetting-soap.md) <br/> |<span data-ttu-id="30013-122">Representa una respuesta a una solicitud de GetUserSettings.</span><span class="sxs-lookup"><span data-stu-id="30013-122">Represents a response to a GetUserSettings request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="30013-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="30013-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30013-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="30013-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="30013-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="30013-125">Schema Name</span></span>  <br/> |<span data-ttu-id="30013-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="30013-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="30013-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="30013-127">Validation File</span></span>  <br/> |<span data-ttu-id="30013-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="30013-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="30013-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="30013-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="30013-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="30013-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30013-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="30013-131">See also</span></span>



[<span data-ttu-id="30013-132">WebClientUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="30013-132">WebClientUrl (SOAP)</span></span>](webclienturl-soap.md)

