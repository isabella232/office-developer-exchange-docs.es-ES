---
title: UserOofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserOofSettings
api_type:
- schema
ms.assetid: 0a95ca63-660e-4cc0-82e4-3f74fb4ae21c
description: El elemento UserOofSettings especifica la configuración de fuera de oficina (OOF).
ms.openlocfilehash: a035fd89387ece632d83f5f72a564e4896bc6753
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840921"
---
# <a name="useroofsettings"></a><span data-ttu-id="47ffd-103">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="47ffd-103">UserOofSettings</span></span>

<span data-ttu-id="47ffd-104">El elemento **UserOofSettings** especifica la configuración de fuera de oficina (OOF).</span><span class="sxs-lookup"><span data-stu-id="47ffd-104">The **UserOofSettings** element specifies the Out of Office (OOF) settings.</span></span> 
  
[<span data-ttu-id="47ffd-105">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="47ffd-105">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md)
  
[<span data-ttu-id="47ffd-106">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="47ffd-106">UserOofSettings</span></span>](useroofsettings.md)
  
```xml
<UserOofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</UserOofSettings>
```

 <span data-ttu-id="47ffd-107">**UserOofSettings**</span><span class="sxs-lookup"><span data-stu-id="47ffd-107">**UserOofSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="47ffd-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="47ffd-108">Attributes and elements</span></span>

<span data-ttu-id="47ffd-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="47ffd-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47ffd-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="47ffd-110">Attributes</span></span>

<span data-ttu-id="47ffd-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="47ffd-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="47ffd-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="47ffd-112">Child elements</span></span>

|<span data-ttu-id="47ffd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="47ffd-113">**Element**</span></span>|<span data-ttu-id="47ffd-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="47ffd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="47ffd-115">OofState</span><span class="sxs-lookup"><span data-stu-id="47ffd-115">OofState</span></span>](oofstate.md) <br/> |<span data-ttu-id="47ffd-116">Establece el estado de fuera de la oficina del usuario.</span><span class="sxs-lookup"><span data-stu-id="47ffd-116">Sets the user's OOF state.</span></span>  <br/> |
|[<span data-ttu-id="47ffd-117">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="47ffd-117">ExternalAudience</span></span>](externalaudience.md) <br/> |<span data-ttu-id="47ffd-118">Establece o contiene un valor que determina a quienes se envían los mensajes externos de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="47ffd-118">Sets or contains a value that determines to whom external OOF messages are sent.</span></span>  <br/> |
|[<span data-ttu-id="47ffd-119">Duración (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="47ffd-119">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> |<span data-ttu-id="47ffd-120">Especifica la duración para la que está habilitado el estado de fuera de la oficina si el elemento [OofState](oofstate.md) está establecido en **programado**.</span><span class="sxs-lookup"><span data-stu-id="47ffd-120">Specifies the duration for which the OOF status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span> <span data-ttu-id="47ffd-121">Si el elemento de [OofState](oofstate.md) se establece en **habilitada** o **deshabilitada**, se ignora el valor de este elemento.</span><span class="sxs-lookup"><span data-stu-id="47ffd-121">If the [OofState](oofstate.md) element is set to **Enabled** or **Disabled**, the value of this element is ignored.</span></span>  <br/> |
|[<span data-ttu-id="47ffd-122">InternalReply</span><span class="sxs-lookup"><span data-stu-id="47ffd-122">InternalReply</span></span>](internalreply.md) <br/> |<span data-ttu-id="47ffd-123">Contiene la respuesta OOF enviada a otros usuarios de dominio o los dominios de confianza del usuario.</span><span class="sxs-lookup"><span data-stu-id="47ffd-123">Contains the OOF response sent to other users in the user's domain or trusted domains.</span></span>  <br/> |
|[<span data-ttu-id="47ffd-124">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="47ffd-124">ExternalReply</span></span>](externalreply.md) <br/> |<span data-ttu-id="47ffd-125">Contiene la respuesta OOF enviada a direcciones fuera del destinatario dominio o dominios de confianza.</span><span class="sxs-lookup"><span data-stu-id="47ffd-125">Contains the OOF response sent to addresses outside the recipient's domain or trusted domains.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="47ffd-126">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="47ffd-126">Parent elements</span></span>

|<span data-ttu-id="47ffd-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="47ffd-127">**Element**</span></span>|<span data-ttu-id="47ffd-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="47ffd-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="47ffd-129">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="47ffd-129">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md) <br/> |<span data-ttu-id="47ffd-130">Contiene los argumentos que se usa para establecer la configuración de fuera de la oficina y los mensajes de un usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="47ffd-130">Contains the arguments used to set a mailbox user's OOF settings and messages.</span></span>  <br/> <span data-ttu-id="47ffd-131">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="47ffd-131">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47ffd-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="47ffd-132">Remarks</span></span>

<span data-ttu-id="47ffd-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="47ffd-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="47ffd-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="47ffd-134">Example</span></span>

<span data-ttu-id="47ffd-135">El siguiente ejemplo de una solicitud de SetUserOofSettings la OoFState establece en **habilitado**, Establece la duración de OOF para 10 días y establece los mensajes de fuera de la oficina internos y externos.</span><span class="sxs-lookup"><span data-stu-id="47ffd-135">The following example of a SetUserOofSettings request sets the OoFState to **Enabled**, sets the duration of OOF for 10 days, and sets the internal and external OOF messages.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2005-10-05T00:00:00</StartTime>
          <EndTime>2005-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="47ffd-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="47ffd-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47ffd-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="47ffd-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="47ffd-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="47ffd-138">Schema Name</span></span>  <br/> |<span data-ttu-id="47ffd-139">esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="47ffd-139">messages schema</span></span>  <br/> |
|<span data-ttu-id="47ffd-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="47ffd-140">Validation File</span></span>  <br/> |<span data-ttu-id="47ffd-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="47ffd-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="47ffd-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="47ffd-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="47ffd-143">False</span><span class="sxs-lookup"><span data-stu-id="47ffd-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="47ffd-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="47ffd-144">See also</span></span>

- [<span data-ttu-id="47ffd-145">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="47ffd-145">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

