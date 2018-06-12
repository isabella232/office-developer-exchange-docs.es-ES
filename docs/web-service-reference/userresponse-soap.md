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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840924"
---
# <a name="userresponse-soap"></a><span data-ttu-id="c04db-103">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c04db-103">UserResponse (SOAP)</span></span>

<span data-ttu-id="c04db-104">El elemento **UserResponse** representa una respuesta a una solicitud de GetUserSettings para un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="c04db-104">The **UserResponse** element represents a response to a GetUserSettings request for an individual user.</span></span> 
  
```XML
<UserResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <RedirectTarget/>
   <UserSettingErrors/>
   <UserSettings/>
</UserResponse>
```

 <span data-ttu-id="c04db-105">**UserResponse**</span><span class="sxs-lookup"><span data-stu-id="c04db-105">**UserResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c04db-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c04db-106">Attributes and elements</span></span>

<span data-ttu-id="c04db-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c04db-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c04db-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c04db-108">Attributes</span></span>

<span data-ttu-id="c04db-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c04db-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c04db-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c04db-110">Child elements</span></span>

|<span data-ttu-id="c04db-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c04db-111">**Element**</span></span>|<span data-ttu-id="c04db-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c04db-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c04db-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c04db-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="c04db-114">Representa un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="c04db-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="c04db-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c04db-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="c04db-116">Representa un mensaje en el que está asociado con un código de error devuelto por el servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="c04db-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="c04db-117">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c04db-117">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md) <br/> |<span data-ttu-id="c04db-118">Contiene el destino de la dirección de correo electrónico o dirección URL de redirección.</span><span class="sxs-lookup"><span data-stu-id="c04db-118">Contains the target of the redirection URL or email address.</span></span>  <br/> |
|[<span data-ttu-id="c04db-119">UserSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c04db-119">UserSettingErrors (SOAP)</span></span>](usersettingerrors-soap.md) <br/> |<span data-ttu-id="c04db-120">Representa una colección de información sobre la configuración que no se pudo devolver.</span><span class="sxs-lookup"><span data-stu-id="c04db-120">Represents a collection of information about settings that could not be returned.</span></span>  <br/> |
|[<span data-ttu-id="c04db-121">UserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c04db-121">UserSettings (SOAP)</span></span>](usersettings-soap.md) <br/> |<span data-ttu-id="c04db-122">La configuración solicitada para el usuario.</span><span class="sxs-lookup"><span data-stu-id="c04db-122">The requested settings for the user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c04db-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c04db-123">Parent elements</span></span>

|<span data-ttu-id="c04db-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="c04db-124">**Element**</span></span>|<span data-ttu-id="c04db-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c04db-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c04db-126">ArrayOfUserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c04db-126">ArrayOfUserResponse (SOAP)</span></span>](arrayofuserresponse-soap.md) <br/> |<span data-ttu-id="c04db-127">Contiene una matriz de las respuestas del usuario.</span><span class="sxs-lookup"><span data-stu-id="c04db-127">Contains an array of user responses.</span></span>  <br/> |
|[<span data-ttu-id="c04db-128">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c04db-128">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="c04db-129">Contiene las opciones de configuración para cada usuario solicitado.</span><span class="sxs-lookup"><span data-stu-id="c04db-129">Contains the configuration settings for each requested user.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="c04db-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c04db-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c04db-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c04db-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="c04db-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c04db-132">Schema Name</span></span>  <br/> |<span data-ttu-id="c04db-133">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="c04db-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="c04db-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c04db-134">Validation File</span></span>  <br/> |<span data-ttu-id="c04db-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c04db-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c04db-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c04db-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="c04db-137">Verdadero</span><span class="sxs-lookup"><span data-stu-id="c04db-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c04db-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="c04db-138">See also</span></span>



[<span data-ttu-id="c04db-139">Elementos de Autodiscover XML SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="c04db-139">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

