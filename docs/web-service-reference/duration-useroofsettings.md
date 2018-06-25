---
title: Duración (UserOofSettings)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Duration
api_type:
- schema
ms.assetid: 01d67af3-658e-4acd-93e3-441ae827fdd3
description: El elemento de duración Especifica la duración de fuera de la oficina (OOF) está habilitado si se establece el elemento OofState en programado.
ms.openlocfilehash: 62a5492372fd80173d58e965376b7c8c466825a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764293"
---
# <a name="duration-useroofsettings"></a><span data-ttu-id="a59d2-103">Duración (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="a59d2-103">Duration (UserOofSettings)</span></span>

<span data-ttu-id="a59d2-104">El elemento de **duración** especifica la duración de la espera del estado de la oficina (OOF) está habilitada si se establece el elemento [OofState](oofstate.md) en **programado**.</span><span class="sxs-lookup"><span data-stu-id="a59d2-104">The **Duration** element specifies the duration that the out of office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span>
  
```XML
<Duration>
   <StartTime/>
   <EndTime/> 
</Duration>
```

 <span data-ttu-id="a59d2-105">**Duration**</span><span class="sxs-lookup"><span data-stu-id="a59d2-105">**Duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a59d2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a59d2-106">Attributes and elements</span></span>

<span data-ttu-id="a59d2-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a59d2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a59d2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a59d2-108">Attributes</span></span>

<span data-ttu-id="a59d2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a59d2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a59d2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a59d2-110">Child elements</span></span>

|<span data-ttu-id="a59d2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a59d2-111">**Element**</span></span>|<span data-ttu-id="a59d2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a59d2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a59d2-113">StartTime</span><span class="sxs-lookup"><span data-stu-id="a59d2-113">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="a59d2-114">Representa el inicio de un período de tiempo establecido con un estado de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="a59d2-114">Represents the start of the time span set with an OOF status.</span></span> <span data-ttu-id="a59d2-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="a59d2-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="a59d2-116">Hora de finalización</span><span class="sxs-lookup"><span data-stu-id="a59d2-116">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="a59d2-117">Representa el final de un período de tiempo establecido con un estado de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="a59d2-117">Represents the end of the time span set with an OOF status.</span></span> <span data-ttu-id="a59d2-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="a59d2-118">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a59d2-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a59d2-119">Parent elements</span></span>

|<span data-ttu-id="a59d2-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="a59d2-120">**Element**</span></span>|<span data-ttu-id="a59d2-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a59d2-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a59d2-122">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="a59d2-122">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="a59d2-123">Especifica la configuración de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="a59d2-123">Specifies the OOF settings.</span></span>  <br/><br/><span data-ttu-id="a59d2-124">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="a59d2-124">The following is the XPath expression to this element:</span></span><br/><br/>`/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="a59d2-125">OofSettings</span><span class="sxs-lookup"><span data-stu-id="a59d2-125">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="a59d2-126">Contiene la configuración de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="a59d2-126">Contains the OOF settings.</span></span><br/><br/><span data-ttu-id="a59d2-127">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="a59d2-127">The following is the XPath expression to this element:</span></span><br/><br/>`/GetUserOofSettingsResponse/OofSettings` <br/> |
|[<span data-ttu-id="a59d2-128">Fuera de la oficina</span><span class="sxs-lookup"><span data-stu-id="a59d2-128">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="a59d2-129">Define el mensaje de respuesta de fuera de oficina (OOF) y un tiempo de duración para enviar el mensaje de respuesta para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a59d2-129">Defines the Out of Office (OOF) response message and a duration time for sending the response message for a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a59d2-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a59d2-130">Remarks</span></span>

<span data-ttu-id="a59d2-131">El tipo de **duración** también es el tipo de los elementos [DetailedSuggestionsWindow](detailedsuggestionswindow.md), [ventana de tiempo](timewindow.md)y [fuera de la oficina](outofoffice.md) .</span><span class="sxs-lookup"><span data-stu-id="a59d2-131">The **Duration** type is also the type for the [DetailedSuggestionsWindow](detailedsuggestionswindow.md), [TimeWindow](timewindow.md), and [OutOfOffice](outofoffice.md) elements.</span></span> 
  
<span data-ttu-id="a59d2-132">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a59d2-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="a59d2-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a59d2-133">Example</span></span>

<span data-ttu-id="a59d2-134">El siguiente ejemplo de una solicitud de [operación de SetUserOofSettings](setuseroofsettings-operation.md) la [OofState](oofstate.md) establece en **habilitado**, los mensajes de fuera de la oficina internos y externos y establece la duración de OOF durante 10 días.</span><span class="sxs-lookup"><span data-stu-id="a59d2-134">The following example of a [SetUserOofSettings operation](setuseroofsettings-operation.md) request sets the [OofState](oofstate.md) to **Enabled**, the internal and external OOF messages, and sets the duration of OOF for 10 days.</span></span>
  
```XML
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
        <SetByLegacyClient>false</SetByLegacyClient>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="a59d2-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a59d2-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a59d2-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a59d2-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a59d2-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a59d2-137">Schema Name</span></span>  <br/> |<span data-ttu-id="a59d2-138">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a59d2-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="a59d2-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a59d2-139">Validation File</span></span>  <br/> |<span data-ttu-id="a59d2-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a59d2-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a59d2-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a59d2-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="a59d2-142">False</span><span class="sxs-lookup"><span data-stu-id="a59d2-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a59d2-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="a59d2-143">See also</span></span>

- [<span data-ttu-id="a59d2-144">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="a59d2-144">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)  
- [<span data-ttu-id="a59d2-145">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="a59d2-145">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

