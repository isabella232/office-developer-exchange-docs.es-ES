---
title: ExternalAudience
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExternalAudience
api_type:
- schema
ms.assetid: 79dc2a4c-f7dd-46d1-8f31-149116e1f76e
description: El elemento ExternalAudience establece o contiene un valor que determina a quienes se envían los mensajes externos de fuera de oficina (OOF).
ms.openlocfilehash: 836b0f6a5140a37e1584f571cb8e26534fe7a25f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764542"
---
# <a name="externalaudience"></a><span data-ttu-id="3eb65-103">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="3eb65-103">ExternalAudience</span></span>

<span data-ttu-id="3eb65-104">El elemento **ExternalAudience** establece o contiene un valor que determina a quienes se envían los mensajes externos de fuera de oficina (OOF).</span><span class="sxs-lookup"><span data-stu-id="3eb65-104">The **ExternalAudience** element sets or contains a value that determines to whom external Out of Office (OOF) messages are sent.</span></span> 
  
```xml
<ExternalAudience>None or Known or All</ExternalAudience>
```

 <span data-ttu-id="3eb65-105">**ExternalAudience**</span><span class="sxs-lookup"><span data-stu-id="3eb65-105">**ExternalAudience**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3eb65-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3eb65-106">Attributes and elements</span></span>

<span data-ttu-id="3eb65-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3eb65-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3eb65-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3eb65-108">Attributes</span></span>

<span data-ttu-id="3eb65-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3eb65-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3eb65-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3eb65-110">Child elements</span></span>

<span data-ttu-id="3eb65-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3eb65-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3eb65-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3eb65-112">Parent elements</span></span>

|<span data-ttu-id="3eb65-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3eb65-113">**Element**</span></span>|<span data-ttu-id="3eb65-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3eb65-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3eb65-115">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="3eb65-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="3eb65-116">Especifica la configuración de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="3eb65-116">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="3eb65-117">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="3eb65-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="3eb65-118">OofSettings</span><span class="sxs-lookup"><span data-stu-id="3eb65-118">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="3eb65-119">Contiene la configuración de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="3eb65-119">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="3eb65-120">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="3eb65-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3eb65-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3eb65-121">Text value</span></span>

<span data-ttu-id="3eb65-122">Un valor de texto es necesario para este elemento.</span><span class="sxs-lookup"><span data-stu-id="3eb65-122">A text value is required for this element.</span></span> <span data-ttu-id="3eb65-123">En la siguiente tabla se enumera los valores posibles para este elemento.</span><span class="sxs-lookup"><span data-stu-id="3eb65-123">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="3eb65-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3eb65-124">**Value**</span></span>|<span data-ttu-id="3eb65-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3eb65-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3eb65-126">**None**</span><span class="sxs-lookup"><span data-stu-id="3eb65-126">**None**</span></span> <br/> |<span data-ttu-id="3eb65-127">Los remitentes de correo electrónico fuera de la organización del usuario de buzón de correo que envían mensajes al usuario no recibirá una respuesta de mensaje de fuera de la oficina externa.</span><span class="sxs-lookup"><span data-stu-id="3eb65-127">E-mail senders outside the mailbox user's organization who send messages to the user will not receive an external OOF message response.</span></span>  <br/> |
|<span data-ttu-id="3eb65-128">**Conocidos**</span><span class="sxs-lookup"><span data-stu-id="3eb65-128">**Known**</span></span> <br/> |<span data-ttu-id="3eb65-129">Los remitentes de correo electrónico fuera de la organización del usuario de buzón de correo que envían mensajes al usuario sólo recibirá una respuesta de mensaje de fuera de la oficina externa si el remitente está en Exchange del usuario almacenan la lista de contactos.</span><span class="sxs-lookup"><span data-stu-id="3eb65-129">E-mail senders outside the mailbox user's organization who send messages to the user will only receive an external OOF message response if the sender is in the user's Exchange store contact list.</span></span>  <br/> |
|<span data-ttu-id="3eb65-130">**All**</span><span class="sxs-lookup"><span data-stu-id="3eb65-130">**All**</span></span> <br/> |<span data-ttu-id="3eb65-131">Los remitentes de correo electrónico fuera de la organización del usuario de buzón de correo que envían mensajes al usuario recibirá una respuesta de mensaje de fuera de la oficina externa.</span><span class="sxs-lookup"><span data-stu-id="3eb65-131">E-mail senders outside the mailbox user's organization who send messages to the user will receive an external OOF message response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3eb65-132">Notas</span><span class="sxs-lookup"><span data-stu-id="3eb65-132">Remarks</span></span>

<span data-ttu-id="3eb65-133">Este elemento comparte el mismo tipo que el elemento [AllowExternalOof](allowexternaloof.md) .</span><span class="sxs-lookup"><span data-stu-id="3eb65-133">This element shares the same type as the [AllowExternalOof](allowexternaloof.md) element.</span></span> 
  
<span data-ttu-id="3eb65-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3eb65-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="3eb65-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3eb65-135">Example</span></span>

<span data-ttu-id="3eb65-136">El siguiente ejemplo de una solicitud de SetUserOofSettings la OoFState establece en **habilitado**, la audiencia externa establece en **todos los**, Establece la duración de OOF a 10 días y establece los mensajes de fuera de la oficina internos y externos.</span><span class="sxs-lookup"><span data-stu-id="3eb65-136">The following example of a SetUserOofSettings request sets the OoFState to **Enabled**, sets the external audience to **All**, sets the duration of OOF to 10 days, and sets the internal and external OOF messages.</span></span>
  
```
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

## <a name="element-information"></a><span data-ttu-id="3eb65-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3eb65-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3eb65-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3eb65-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3eb65-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3eb65-139">Schema Name</span></span>  <br/> |<span data-ttu-id="3eb65-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3eb65-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="3eb65-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3eb65-141">Validation File</span></span>  <br/> |<span data-ttu-id="3eb65-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3eb65-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3eb65-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3eb65-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="3eb65-144">False</span><span class="sxs-lookup"><span data-stu-id="3eb65-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3eb65-145">Ver también</span><span class="sxs-lookup"><span data-stu-id="3eb65-145">See also</span></span>



[<span data-ttu-id="3eb65-146">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="3eb65-146">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="3eb65-147">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="3eb65-147">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

