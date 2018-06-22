---
title: Acción (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a3462c6b-453c-462a-830d-f29ee4a2babb
description: El elemento de acción proporciona información que se utiliza para determinar si se requiere otra solicitud de detección automática para devolver la información de configuración de usuario.
ms.openlocfilehash: 118bb59f2c929e3c74683dbf3f073da34d67a3e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764557"
---
# <a name="action-pox"></a><span data-ttu-id="f01e4-103">Acción (POX)</span><span class="sxs-lookup"><span data-stu-id="f01e4-103">Action (POX)</span></span>

<span data-ttu-id="f01e4-104">El elemento de **acción** proporciona información que se utiliza para determinar si se requiere otra solicitud de detección automática para devolver la información de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="f01e4-104">The **Action** element provides information that is used to determine whether another Autodiscover request is required to return the user configuration information.</span></span> 
  
- [<span data-ttu-id="f01e4-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="f01e4-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="f01e4-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="f01e4-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="f01e4-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="f01e4-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="f01e4-108">Acción (POX)</span><span class="sxs-lookup"><span data-stu-id="f01e4-108">Action (POX)</span></span>](action-pox.md)
  
```xml
<Action>redirectUrl or redirectAddr or settings</Action>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="f01e4-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f01e4-109">Attributes and elements</span></span>

<span data-ttu-id="f01e4-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f01e4-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f01e4-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="f01e4-111">Attributes</span></span>

<span data-ttu-id="f01e4-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f01e4-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f01e4-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f01e4-113">Child elements</span></span>

<span data-ttu-id="f01e4-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f01e4-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f01e4-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f01e4-115">Parent elements</span></span>

|<span data-ttu-id="f01e4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f01e4-116">**Element**</span></span>|<span data-ttu-id="f01e4-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f01e4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f01e4-118">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="f01e4-118">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="f01e4-119">Especifica la configuración de cuenta para el usuario.</span><span class="sxs-lookup"><span data-stu-id="f01e4-119">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f01e4-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f01e4-120">Text value</span></span>

<span data-ttu-id="f01e4-121">El valor de texto representa si otra solicitud de detección automática es necesario para recuperar información de configuración del usuario.</span><span class="sxs-lookup"><span data-stu-id="f01e4-121">The text value represents whether another Autodiscover request is necessary to retrieve the user's configuration information.</span></span> <span data-ttu-id="f01e4-122">En la siguiente tabla se enumera los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="f01e4-122">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="f01e4-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f01e4-123">**Value**</span></span>|<span data-ttu-id="f01e4-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f01e4-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f01e4-125">redirectUrl</span><span class="sxs-lookup"><span data-stu-id="f01e4-125">redirectUrl</span></span>  <br/> |<span data-ttu-id="f01e4-126">Si se especifica este valor, el elemento [RedirectUrl (POX)](redirecturl-pox.md) especifique la dirección URL del servidor acceso de cliente que se utilizará en la siguiente solicitud de detección automática.</span><span class="sxs-lookup"><span data-stu-id="f01e4-126">If this value is specified, the [RedirectUrl (POX)](redirecturl-pox.md) element will specify the Client Access server URL to be used in the subsequent Autodiscover request.</span></span> <span data-ttu-id="f01e4-127">La aplicación cliente debe dejar de redirigir después de 10 redirecciones.</span><span class="sxs-lookup"><span data-stu-id="f01e4-127">The client application should stop redirecting after 10 redirects.</span></span>  <br/> |
|<span data-ttu-id="f01e4-128">redirectAddr</span><span class="sxs-lookup"><span data-stu-id="f01e4-128">redirectAddr</span></span>  <br/> |<span data-ttu-id="f01e4-129">Si se especifica este valor, el elemento [RedirectAddr (POX)](redirectaddr-pox.md) especifique la dirección de correo electrónico que se debe usar para una solicitud de detección automática subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="f01e4-129">If this value is specified, the [RedirectAddr (POX)](redirectaddr-pox.md) element will specify the e-mail address that should be used for a subsequent Autodiscover request.</span></span>  <br/> |
|<span data-ttu-id="f01e4-130">settings</span><span class="sxs-lookup"><span data-stu-id="f01e4-130">settings</span></span>  <br/> |<span data-ttu-id="f01e4-131">Si se especifica este valor, la respuesta de detección automática contiene la configuración que se usa para configurar la cuenta.</span><span class="sxs-lookup"><span data-stu-id="f01e4-131">If this value is specified, the Autodiscover response contains settings that are used to configure the account.</span></span> <span data-ttu-id="f01e4-132">La mayoría de las opciones se encuentran en el elemento de [Protocolo (POX)](protocol-pox.md) .</span><span class="sxs-lookup"><span data-stu-id="f01e4-132">Most of the settings will be found in the [Protocol (POX)](protocol-pox.md) element.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f01e4-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="f01e4-133">See also</span></span>

- [<span data-ttu-id="f01e4-134">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="f01e4-134">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

