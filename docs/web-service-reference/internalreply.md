---
title: InternalReply
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternalReply
api_type:
- schema
ms.assetid: 1d784ded-b874-4eb1-8f6d-2e0e03330e1e
description: El elemento InternalReply contiene la espera de respuesta de la oficina (OOF) enviado a otros usuarios de dominio o los dominios de confianza del usuario.
ms.openlocfilehash: ac5e9eadac7f45c233007ffb05f4d2430875ec52
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835955"
---
# <a name="internalreply"></a><span data-ttu-id="7b7bc-103">InternalReply</span><span class="sxs-lookup"><span data-stu-id="7b7bc-103">InternalReply</span></span>

<span data-ttu-id="7b7bc-104">El elemento **InternalReply** contiene la espera de respuesta de la oficina (OOF) enviado a otros usuarios de dominio o los dominios de confianza del usuario.</span><span class="sxs-lookup"><span data-stu-id="7b7bc-104">The **InternalReply** element contains the out of office (OOF) response sent to other users in the user's domain or trusted domains.</span></span> 
  
```XML
<InternalReply>
   <Message/> 
</InternalReply>
```

 <span data-ttu-id="7b7bc-105">**ReplyBody**</span><span class="sxs-lookup"><span data-stu-id="7b7bc-105">**ReplyBody**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7b7bc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7b7bc-106">Attributes and elements</span></span>

<span data-ttu-id="7b7bc-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7b7bc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b7bc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7b7bc-108">Attributes</span></span>

|<span data-ttu-id="7b7bc-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7b7bc-109">**Attribute**</span></span>|<span data-ttu-id="7b7bc-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7b7bc-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7b7bc-111">XML: lang</span><span class="sxs-lookup"><span data-stu-id="7b7bc-111">xml:lang</span></span>  <br/> |<span data-ttu-id="7b7bc-112">Especifica el lenguaje utilizado en el mensaje **InternalReply** .</span><span class="sxs-lookup"><span data-stu-id="7b7bc-112">Specifies the language used in the **InternalReply** message.</span></span> <span data-ttu-id="7b7bc-113">Los valores posibles de este atributo se definen en IETF RFC 3066.</span><span class="sxs-lookup"><span data-stu-id="7b7bc-113">The possible values of this attribute are defined by IETF RFC 3066.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7b7bc-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7b7bc-114">Child elements</span></span>

|<span data-ttu-id="7b7bc-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="7b7bc-115">**Element**</span></span>|<span data-ttu-id="7b7bc-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7b7bc-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b7bc-117">Mensaje (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="7b7bc-117">Message (Availability)</span></span>](message-availability.md) <br/> |<span data-ttu-id="7b7bc-118">Contiene la respuesta de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="7b7bc-118">Contains the OOF response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7b7bc-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7b7bc-119">Parent elements</span></span>

|<span data-ttu-id="7b7bc-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="7b7bc-120">**Element**</span></span>|<span data-ttu-id="7b7bc-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7b7bc-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b7bc-122">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="7b7bc-122">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="7b7bc-123">Especifica la configuración de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="7b7bc-123">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="7b7bc-124">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="7b7bc-124">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="7b7bc-125">OofSettings</span><span class="sxs-lookup"><span data-stu-id="7b7bc-125">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="7b7bc-126">Contiene la configuración de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="7b7bc-126">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="7b7bc-127">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="7b7bc-127">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b7bc-128">Notas</span><span class="sxs-lookup"><span data-stu-id="7b7bc-128">Remarks</span></span>

<span data-ttu-id="7b7bc-129">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7b7bc-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="7b7bc-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b7bc-130">Example</span></span>

<span data-ttu-id="7b7bc-131">El siguiente ejemplo de una solicitud de SetUserOofSettings la [OofState](oofstate.md) establece en **habilitado**, Establece la duración de OOF para 10 días y establece los mensajes de fuera de la oficina internos y externos.</span><span class="sxs-lookup"><span data-stu-id="7b7bc-131">The following example of a SetUserOofSettings request sets the [OofState](oofstate.md) to **Enabled**, sets the duration of OOF for 10 days, and sets the internal and external OOF messages.</span></span>
  
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
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="7b7bc-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7b7bc-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b7bc-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7b7bc-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7b7bc-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7b7bc-134">Schema Name</span></span>  <br/> |<span data-ttu-id="7b7bc-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7b7bc-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="7b7bc-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7b7bc-136">Validation File</span></span>  <br/> |<span data-ttu-id="7b7bc-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7b7bc-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7b7bc-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7b7bc-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="7b7bc-139">False</span><span class="sxs-lookup"><span data-stu-id="7b7bc-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b7bc-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="7b7bc-140">See also</span></span>



[<span data-ttu-id="7b7bc-141">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="7b7bc-141">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="7b7bc-142">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="7b7bc-142">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

