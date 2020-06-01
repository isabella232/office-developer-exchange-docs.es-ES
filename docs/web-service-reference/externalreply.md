---
title: ExternalReply
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExternalReply
api_type:
- schema
ms.assetid: cbcfa469-242c-4f98-8f4f-2c9bcbe69f5a
description: El elemento ExternalReply contiene la respuesta de fuera de la oficina (OOF) que se envía a las direcciones fuera del dominio del destinatario o de los dominios de confianza.
ms.openlocfilehash: c3381979e5e6aad51f9ae2bb3e661003ef793be6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458764"
---
# <a name="externalreply"></a><span data-ttu-id="7a8a8-103">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="7a8a8-103">ExternalReply</span></span>

<span data-ttu-id="7a8a8-104">El elemento **ExternalReply** contiene la respuesta de fuera de la oficina (OOF) que se envía a las direcciones fuera del dominio del destinatario o de los dominios de confianza.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-104">The **ExternalReply** element contains the out of office (OOF) response that is sent to addresses outside the recipient's domain or trusted domains.</span></span> 
  
```XML
<ExternalReply>
   <Message/>
</ExternalReply>
```

 <span data-ttu-id="7a8a8-105">**ReplyBody**</span><span class="sxs-lookup"><span data-stu-id="7a8a8-105">**ReplyBody**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7a8a8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7a8a8-106">Attributes and elements</span></span>

<span data-ttu-id="7a8a8-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a8a8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7a8a8-108">Attributes</span></span>

|<span data-ttu-id="7a8a8-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7a8a8-109">**Attribute**</span></span>|<span data-ttu-id="7a8a8-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7a8a8-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7a8a8-111">XML: lang</span><span class="sxs-lookup"><span data-stu-id="7a8a8-111">xml:lang</span></span>  <br/> |<span data-ttu-id="7a8a8-112">Especifica el idioma usado en el mensaje **ExternalReply** .</span><span class="sxs-lookup"><span data-stu-id="7a8a8-112">Specifies the language used in the **ExternalReply** message.</span></span> <span data-ttu-id="7a8a8-113">Los valores posibles para este atributo los define el documento RFC 3066 de IETF.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-113">The possible values for this attribute are defined by IETF RFC 3066.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7a8a8-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7a8a8-114">Child elements</span></span>

|<span data-ttu-id="7a8a8-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7a8a8-115">**Element**</span></span>|<span data-ttu-id="7a8a8-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7a8a8-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a8a8-117">Mensaje (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="7a8a8-117">Message (Availability)</span></span>](message-availability.md) <br/> |<span data-ttu-id="7a8a8-118">Contiene la respuesta OOF.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-118">Contains the OOF response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7a8a8-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7a8a8-119">Parent elements</span></span>

|<span data-ttu-id="7a8a8-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7a8a8-120">**Element**</span></span>|<span data-ttu-id="7a8a8-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7a8a8-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a8a8-122">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="7a8a8-122">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="7a8a8-123">Especifica la configuración de OOF.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-123">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="7a8a8-124">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="7a8a8-124">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="7a8a8-125">OofSettings</span><span class="sxs-lookup"><span data-stu-id="7a8a8-125">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="7a8a8-126">Contiene la configuración de OOF.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-126">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="7a8a8-127">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="7a8a8-127">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a8a8-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7a8a8-128">Remarks</span></span>

<span data-ttu-id="7a8a8-129">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="7a8a8-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7a8a8-130">Example</span></span>

<span data-ttu-id="7a8a8-131">El siguiente ejemplo de una solicitud SetUserOofSettings establece la [OofState](oofstate.md) en **habilitada**, establece la duración de OOF en 10 días y establece los mensajes internos y externos de OOF.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-131">The following example of a SetUserOofSettings request sets the [OofState](oofstate.md) to **Enabled**, sets the duration of OOF to 10 days, and sets the internal and external OOF messages.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="7a8a8-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7a8a8-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a8a8-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a8a8-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7a8a8-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7a8a8-134">Schema Name</span></span>  <br/> |<span data-ttu-id="7a8a8-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7a8a8-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="7a8a8-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7a8a8-136">Validation File</span></span>  <br/> |<span data-ttu-id="7a8a8-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="7a8a8-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7a8a8-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7a8a8-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="7a8a8-139">Falso</span><span class="sxs-lookup"><span data-stu-id="7a8a8-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a8a8-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a8a8-140">See also</span></span>



[<span data-ttu-id="7a8a8-141">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="7a8a8-141">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

