---
title: UserResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd
description: El elemento UserResponse representa una respuesta a una solicitud de GetUserSettings para un usuario individual.
ms.openlocfilehash: 6fcd82e06916df5acdd317cb44161c1b69e58574
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19840924"
---
# <a name="userresponse-soap"></a><span data-ttu-id="f50e2-103">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f50e2-103">UserResponse (SOAP)</span></span>

<span data-ttu-id="f50e2-104">El elemento **UserResponse** representa una respuesta a una solicitud de GetUserSettings para un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="f50e2-104">The **UserResponse** element represents a response to a GetUserSettings request for an individual user.</span></span> 
  
```XML
<UserResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <RedirectTarget/>
   <UserSettingErrors/>
   <UserSettings/>
</UserResponse>
```

 <span data-ttu-id="f50e2-105">**UserResponse**</span><span class="sxs-lookup"><span data-stu-id="f50e2-105">**UserResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f50e2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f50e2-106">Attributes and elements</span></span>

<span data-ttu-id="f50e2-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f50e2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f50e2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f50e2-108">Attributes</span></span>

<span data-ttu-id="f50e2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f50e2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f50e2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f50e2-110">Child elements</span></span>

|<span data-ttu-id="f50e2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f50e2-111">**Element**</span></span>|<span data-ttu-id="f50e2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f50e2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f50e2-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f50e2-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="f50e2-114">Representa un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="f50e2-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="f50e2-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f50e2-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="f50e2-116">Representa un mensaje en el que está asociado con un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="f50e2-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="f50e2-117">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f50e2-117">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md) <br/> |<span data-ttu-id="f50e2-118">Contiene el destino de la dirección de correo electrónico o dirección URL de redirección.</span><span class="sxs-lookup"><span data-stu-id="f50e2-118">Contains the target of the redirection URL or email address.</span></span>  <br/> |
|[<span data-ttu-id="f50e2-119">UserSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f50e2-119">UserSettingErrors (SOAP)</span></span>](usersettingerrors-soap.md) <br/> |<span data-ttu-id="f50e2-120">Representa una colección de información sobre la configuración que no se pudo devolver.</span><span class="sxs-lookup"><span data-stu-id="f50e2-120">Represents a collection of information about settings that could not be returned.</span></span>  <br/> |
|[<span data-ttu-id="f50e2-121">UserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f50e2-121">UserSettings (SOAP)</span></span>](usersettings-soap.md) <br/> |<span data-ttu-id="f50e2-122">La configuración solicitada para el usuario.</span><span class="sxs-lookup"><span data-stu-id="f50e2-122">The requested settings for the user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f50e2-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f50e2-123">Parent elements</span></span>

|<span data-ttu-id="f50e2-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="f50e2-124">**Element**</span></span>|<span data-ttu-id="f50e2-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f50e2-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f50e2-126">ArrayOfUserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f50e2-126">ArrayOfUserResponse (SOAP)</span></span>](arrayofuserresponse-soap.md) <br/> |<span data-ttu-id="f50e2-127">Contiene una matriz de las respuestas del usuario.</span><span class="sxs-lookup"><span data-stu-id="f50e2-127">Contains an array of user responses.</span></span>  <br/> |
|[<span data-ttu-id="f50e2-128">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f50e2-128">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="f50e2-129">Contiene las opciones de configuración para cada usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="f50e2-129">Contains the configuration settings for each requested user.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="f50e2-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f50e2-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f50e2-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f50e2-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="f50e2-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f50e2-132">Schema Name</span></span>  <br/> |<span data-ttu-id="f50e2-133">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="f50e2-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="f50e2-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f50e2-134">Validation File</span></span>  <br/> |<span data-ttu-id="f50e2-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f50e2-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f50e2-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f50e2-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="f50e2-137">Verdadero</span><span class="sxs-lookup"><span data-stu-id="f50e2-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f50e2-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="f50e2-138">See also</span></span>



[<span data-ttu-id="f50e2-139">Elementos de Autodiscover XML SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="f50e2-139">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

