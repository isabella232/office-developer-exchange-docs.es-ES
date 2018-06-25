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
description: El elemento OofSettings contiene la configuración de fuera de oficina (OOF).
ms.openlocfilehash: d71f068ff24af22da98b6b4de090ab26d3f74f26
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836649"
---
# <a name="oofsettings"></a><span data-ttu-id="c05f6-103">OofSettings</span><span class="sxs-lookup"><span data-stu-id="c05f6-103">OofSettings</span></span>

<span data-ttu-id="c05f6-104">El elemento **OofSettings** contiene la configuración de fuera de oficina (OOF).</span><span class="sxs-lookup"><span data-stu-id="c05f6-104">The **OofSettings** element contains the Out of Office (OOF) settings.</span></span> 
  
[<span data-ttu-id="c05f6-105">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="c05f6-105">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
  
[<span data-ttu-id="c05f6-106">OofSettings</span><span class="sxs-lookup"><span data-stu-id="c05f6-106">OofSettings</span></span>](oofsettings.md)
  
```xml
<OofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</OofSettings>
```

 <span data-ttu-id="c05f6-107">**UserOofSettings**</span><span class="sxs-lookup"><span data-stu-id="c05f6-107">**UserOofSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c05f6-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c05f6-108">Attributes and elements</span></span>

<span data-ttu-id="c05f6-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c05f6-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c05f6-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="c05f6-110">Attributes</span></span>

<span data-ttu-id="c05f6-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c05f6-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c05f6-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c05f6-112">Child elements</span></span>

|<span data-ttu-id="c05f6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c05f6-113">**Element**</span></span>|<span data-ttu-id="c05f6-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c05f6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c05f6-115">OofState</span><span class="sxs-lookup"><span data-stu-id="c05f6-115">OofState</span></span>](oofstate.md) <br/> |<span data-ttu-id="c05f6-116">Contiene el estado de fuera de la oficina del usuario.</span><span class="sxs-lookup"><span data-stu-id="c05f6-116">Contains the user's OOF state.</span></span>  <br/> |
|[<span data-ttu-id="c05f6-117">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="c05f6-117">ExternalAudience</span></span>](externalaudience.md) <br/> |<span data-ttu-id="c05f6-118">Contiene un valor que determina a quienes se envían los mensajes externos de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="c05f6-118">Contains a value that determines to whom external OOF messages are sent.</span></span>  <br/> |
|[<span data-ttu-id="c05f6-119">Duración (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="c05f6-119">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> |<span data-ttu-id="c05f6-120">Contiene la duración para la que está habilitado el estado de fuera de la oficina si el elemento [OofState](oofstate.md) está establecido en **programado**.</span><span class="sxs-lookup"><span data-stu-id="c05f6-120">Contains the duration for which the OOF status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span> <span data-ttu-id="c05f6-121">Si el elemento de [OofState](oofstate.md) se establece en **habilitada** o **deshabilitada**, se ignora el valor de este elemento.</span><span class="sxs-lookup"><span data-stu-id="c05f6-121">If the [OofState](oofstate.md) element is set to **Enabled** or **Disabled**, the value of this element is ignored.</span></span>  <br/> |
|[<span data-ttu-id="c05f6-122">InternalReply</span><span class="sxs-lookup"><span data-stu-id="c05f6-122">InternalReply</span></span>](internalreply.md) <br/> |<span data-ttu-id="c05f6-123">Contiene la respuesta OOF enviada a otros usuarios de dominio o los dominios de confianza del usuario.</span><span class="sxs-lookup"><span data-stu-id="c05f6-123">Contains the OOF response sent to other users in the user's domain or trusted domain.</span></span>  <br/> |
|[<span data-ttu-id="c05f6-124">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="c05f6-124">ExternalReply</span></span>](externalreply.md) <br/> |<span data-ttu-id="c05f6-125">Contiene la respuesta OOF enviada a direcciones fuera del destinatario dominio o dominios de confianza.</span><span class="sxs-lookup"><span data-stu-id="c05f6-125">Contains the OOF response sent to addresses outside the recipient's domain or trusted domains.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c05f6-126">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c05f6-126">Parent elements</span></span>

|<span data-ttu-id="c05f6-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="c05f6-127">**Element**</span></span>|<span data-ttu-id="c05f6-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c05f6-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c05f6-129">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="c05f6-129">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="c05f6-130">Contiene los resultados de la respuesta y la configuración de fuera de la oficina de un usuario.</span><span class="sxs-lookup"><span data-stu-id="c05f6-130">Contains the response results and the OOF settings for a user.</span></span>  <br/> <span data-ttu-id="c05f6-131">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="c05f6-131">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c05f6-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c05f6-132">Remarks</span></span>

<span data-ttu-id="c05f6-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c05f6-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c05f6-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c05f6-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c05f6-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c05f6-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c05f6-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c05f6-136">Schema Name</span></span>  <br/> |<span data-ttu-id="c05f6-137">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c05f6-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c05f6-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c05f6-138">Validation File</span></span>  <br/> |<span data-ttu-id="c05f6-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c05f6-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c05f6-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c05f6-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="c05f6-141">False</span><span class="sxs-lookup"><span data-stu-id="c05f6-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c05f6-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="c05f6-142">See also</span></span>



[<span data-ttu-id="c05f6-143">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="c05f6-143">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="c05f6-144">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="c05f6-144">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

