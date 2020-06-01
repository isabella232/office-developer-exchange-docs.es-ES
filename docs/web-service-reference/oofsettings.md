---
title: OofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OofSettings
api_type:
- schema
ms.assetid: 8f37d174-db11-427c-bbed-fdde754a60c7
description: El elemento OofSettings contiene la configuración de fuera de la oficina (OOF).
ms.openlocfilehash: c1b214fd8bfab5b7a82d41a5187cf6e0fc4ba79c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467196"
---
# <a name="oofsettings"></a><span data-ttu-id="ec193-103">OofSettings</span><span class="sxs-lookup"><span data-stu-id="ec193-103">OofSettings</span></span>

<span data-ttu-id="ec193-104">El elemento **OofSettings** contiene la configuración de fuera de la oficina (OOF).</span><span class="sxs-lookup"><span data-stu-id="ec193-104">The **OofSettings** element contains the Out of Office (OOF) settings.</span></span> 
  
[<span data-ttu-id="ec193-105">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="ec193-105">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
  
[<span data-ttu-id="ec193-106">OofSettings</span><span class="sxs-lookup"><span data-stu-id="ec193-106">OofSettings</span></span>](oofsettings.md)
  
```xml
<OofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</OofSettings>
```

 <span data-ttu-id="ec193-107">**UserOofSettings**</span><span class="sxs-lookup"><span data-stu-id="ec193-107">**UserOofSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec193-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ec193-108">Attributes and elements</span></span>

<span data-ttu-id="ec193-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ec193-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec193-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="ec193-110">Attributes</span></span>

<span data-ttu-id="ec193-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ec193-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ec193-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ec193-112">Child elements</span></span>

|<span data-ttu-id="ec193-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ec193-113">**Element**</span></span>|<span data-ttu-id="ec193-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ec193-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec193-115">OofState</span><span class="sxs-lookup"><span data-stu-id="ec193-115">OofState</span></span>](oofstate.md) <br/> |<span data-ttu-id="ec193-116">Contiene el estado de OOF del usuario.</span><span class="sxs-lookup"><span data-stu-id="ec193-116">Contains the user's OOF state.</span></span>  <br/> |
|[<span data-ttu-id="ec193-117">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="ec193-117">ExternalAudience</span></span>](externalaudience.md) <br/> |<span data-ttu-id="ec193-118">Contiene un valor que determina a quién se envían los mensajes de OOF externos.</span><span class="sxs-lookup"><span data-stu-id="ec193-118">Contains a value that determines to whom external OOF messages are sent.</span></span>  <br/> |
|[<span data-ttu-id="ec193-119">Duración (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="ec193-119">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> |<span data-ttu-id="ec193-120">Contiene la duración para la que está habilitado el estado OOF si el elemento [OofState](oofstate.md) está establecido en **programado**.</span><span class="sxs-lookup"><span data-stu-id="ec193-120">Contains the duration for which the OOF status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span> <span data-ttu-id="ec193-121">Si el elemento [OofState](oofstate.md) está establecido en **habilitado** o **deshabilitado**, se omite el valor de este elemento.</span><span class="sxs-lookup"><span data-stu-id="ec193-121">If the [OofState](oofstate.md) element is set to **Enabled** or **Disabled**, the value of this element is ignored.</span></span>  <br/> |
|[<span data-ttu-id="ec193-122">InternalReply</span><span class="sxs-lookup"><span data-stu-id="ec193-122">InternalReply</span></span>](internalreply.md) <br/> |<span data-ttu-id="ec193-123">Contiene la respuesta OOF enviada a otros usuarios en el dominio del usuario o en un dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="ec193-123">Contains the OOF response sent to other users in the user's domain or trusted domain.</span></span>  <br/> |
|[<span data-ttu-id="ec193-124">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="ec193-124">ExternalReply</span></span>](externalreply.md) <br/> |<span data-ttu-id="ec193-125">Contiene la respuesta OOF enviada a direcciones fuera del dominio del destinatario o de dominios de confianza.</span><span class="sxs-lookup"><span data-stu-id="ec193-125">Contains the OOF response sent to addresses outside the recipient's domain or trusted domains.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ec193-126">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ec193-126">Parent elements</span></span>

|<span data-ttu-id="ec193-127">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ec193-127">**Element**</span></span>|<span data-ttu-id="ec193-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ec193-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec193-129">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="ec193-129">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="ec193-130">Contiene los resultados de la respuesta y la configuración de OOF para un usuario.</span><span class="sxs-lookup"><span data-stu-id="ec193-130">Contains the response results and the OOF settings for a user.</span></span>  <br/> <span data-ttu-id="ec193-131">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="ec193-131">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec193-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ec193-132">Remarks</span></span>

<span data-ttu-id="ec193-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ec193-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec193-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ec193-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec193-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec193-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ec193-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ec193-136">Schema Name</span></span>  <br/> |<span data-ttu-id="ec193-137">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ec193-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ec193-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ec193-138">Validation File</span></span>  <br/> |<span data-ttu-id="ec193-139">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ec193-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ec193-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ec193-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="ec193-141">Falso</span><span class="sxs-lookup"><span data-stu-id="ec193-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec193-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec193-142">See also</span></span>



[<span data-ttu-id="ec193-143">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="ec193-143">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="ec193-144">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="ec193-144">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

