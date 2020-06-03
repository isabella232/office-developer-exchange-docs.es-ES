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
description: El elemento InternalReply contiene la respuesta de fuera de la oficina (OOF) enviada a otros usuarios en el dominio del usuario o en los dominios de confianza.
ms.openlocfilehash: 24c278ebd3acf83e87fbf72650eb3d5d438d5c22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465586"
---
# <a name="internalreply"></a><span data-ttu-id="de6f6-103">InternalReply</span><span class="sxs-lookup"><span data-stu-id="de6f6-103">InternalReply</span></span>

<span data-ttu-id="de6f6-104">El elemento **InternalReply** contiene la respuesta de fuera de la oficina (OOF) enviada a otros usuarios en el dominio del usuario o en los dominios de confianza.</span><span class="sxs-lookup"><span data-stu-id="de6f6-104">The **InternalReply** element contains the out of office (OOF) response sent to other users in the user's domain or trusted domains.</span></span> 
  
```XML
<InternalReply>
   <Message/> 
</InternalReply>
```

 <span data-ttu-id="de6f6-105">**ReplyBody**</span><span class="sxs-lookup"><span data-stu-id="de6f6-105">**ReplyBody**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="de6f6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="de6f6-106">Attributes and elements</span></span>

<span data-ttu-id="de6f6-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="de6f6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de6f6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="de6f6-108">Attributes</span></span>

|<span data-ttu-id="de6f6-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="de6f6-109">**Attribute**</span></span>|<span data-ttu-id="de6f6-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de6f6-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="de6f6-111">XML: lang</span><span class="sxs-lookup"><span data-stu-id="de6f6-111">xml:lang</span></span>  <br/> |<span data-ttu-id="de6f6-112">Especifica el idioma usado en el mensaje **InternalReply** .</span><span class="sxs-lookup"><span data-stu-id="de6f6-112">Specifies the language used in the **InternalReply** message.</span></span> <span data-ttu-id="de6f6-113">Los valores posibles de este atributo los define el documento RFC 3066 de IETF.</span><span class="sxs-lookup"><span data-stu-id="de6f6-113">The possible values of this attribute are defined by IETF RFC 3066.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="de6f6-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="de6f6-114">Child elements</span></span>

|<span data-ttu-id="de6f6-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="de6f6-115">**Element**</span></span>|<span data-ttu-id="de6f6-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de6f6-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de6f6-117">Mensaje (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="de6f6-117">Message (Availability)</span></span>](message-availability.md) <br/> |<span data-ttu-id="de6f6-118">Contiene la respuesta OOF.</span><span class="sxs-lookup"><span data-stu-id="de6f6-118">Contains the OOF response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="de6f6-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="de6f6-119">Parent elements</span></span>

|<span data-ttu-id="de6f6-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="de6f6-120">**Element**</span></span>|<span data-ttu-id="de6f6-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de6f6-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de6f6-122">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="de6f6-122">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="de6f6-123">Especifica la configuración de OOF.</span><span class="sxs-lookup"><span data-stu-id="de6f6-123">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="de6f6-124">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="de6f6-124">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="de6f6-125">OofSettings</span><span class="sxs-lookup"><span data-stu-id="de6f6-125">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="de6f6-126">Contiene la configuración de OOF.</span><span class="sxs-lookup"><span data-stu-id="de6f6-126">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="de6f6-127">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="de6f6-127">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de6f6-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de6f6-128">Remarks</span></span>

<span data-ttu-id="de6f6-129">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="de6f6-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="de6f6-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="de6f6-130">Example</span></span>

<span data-ttu-id="de6f6-131">El siguiente ejemplo de una solicitud SetUserOofSettings establece la [OofState](oofstate.md) en **habilitada**, establece la duración de OOF durante 10 días y establece los mensajes OOF internos y externos.</span><span class="sxs-lookup"><span data-stu-id="de6f6-131">The following example of a SetUserOofSettings request sets the [OofState](oofstate.md) to **Enabled**, sets the duration of OOF for 10 days, and sets the internal and external OOF messages.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="de6f6-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="de6f6-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de6f6-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="de6f6-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="de6f6-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="de6f6-134">Schema Name</span></span>  <br/> |<span data-ttu-id="de6f6-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="de6f6-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="de6f6-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="de6f6-136">Validation File</span></span>  <br/> |<span data-ttu-id="de6f6-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="de6f6-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="de6f6-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="de6f6-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="de6f6-139">Falso</span><span class="sxs-lookup"><span data-stu-id="de6f6-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de6f6-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="de6f6-140">See also</span></span>



[<span data-ttu-id="de6f6-141">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="de6f6-141">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="de6f6-142">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="de6f6-142">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

