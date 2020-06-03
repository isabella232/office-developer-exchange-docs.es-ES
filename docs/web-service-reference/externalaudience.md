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
description: El elemento ExternalAudience establece o contiene un valor que determina a quién se envían los mensajes externos de fuera de la oficina (OOF).
ms.openlocfilehash: b3fcebd9042b07bb9a8294196799ef2a13d78bdd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530603"
---
# <a name="externalaudience"></a><span data-ttu-id="d0b61-103">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="d0b61-103">ExternalAudience</span></span>

<span data-ttu-id="d0b61-104">El elemento **ExternalAudience** establece o contiene un valor que determina a quién se envían los mensajes externos de fuera de la oficina (OOF).</span><span class="sxs-lookup"><span data-stu-id="d0b61-104">The **ExternalAudience** element sets or contains a value that determines to whom external Out of Office (OOF) messages are sent.</span></span> 
  
```xml
<ExternalAudience>None or Known or All</ExternalAudience>
```

 <span data-ttu-id="d0b61-105">**ExternalAudience**</span><span class="sxs-lookup"><span data-stu-id="d0b61-105">**ExternalAudience**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0b61-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d0b61-106">Attributes and elements</span></span>

<span data-ttu-id="d0b61-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d0b61-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0b61-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d0b61-108">Attributes</span></span>

<span data-ttu-id="d0b61-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d0b61-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0b61-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d0b61-110">Child elements</span></span>

<span data-ttu-id="d0b61-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d0b61-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d0b61-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d0b61-112">Parent elements</span></span>

|<span data-ttu-id="d0b61-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d0b61-113">**Element**</span></span>|<span data-ttu-id="d0b61-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0b61-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0b61-115">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="d0b61-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="d0b61-116">Especifica la configuración de OOF.</span><span class="sxs-lookup"><span data-stu-id="d0b61-116">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="d0b61-117">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="d0b61-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="d0b61-118">OofSettings</span><span class="sxs-lookup"><span data-stu-id="d0b61-118">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="d0b61-119">Contiene la configuración de OOF.</span><span class="sxs-lookup"><span data-stu-id="d0b61-119">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="d0b61-120">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="d0b61-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d0b61-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d0b61-121">Text value</span></span>

<span data-ttu-id="d0b61-122">Se requiere un valor de texto para este elemento.</span><span class="sxs-lookup"><span data-stu-id="d0b61-122">A text value is required for this element.</span></span> <span data-ttu-id="d0b61-123">En la siguiente tabla se enumeran los valores posibles para este elemento.</span><span class="sxs-lookup"><span data-stu-id="d0b61-123">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="d0b61-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d0b61-124">**Value**</span></span>|<span data-ttu-id="d0b61-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0b61-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d0b61-126">**Ninguno**</span><span class="sxs-lookup"><span data-stu-id="d0b61-126">**None**</span></span> <br/> |<span data-ttu-id="d0b61-127">Los remitentes de correo electrónico que se encuentran fuera de la organización del usuario del buzón que envían mensajes al usuario no recibirán una respuesta de mensaje OOF externa.</span><span class="sxs-lookup"><span data-stu-id="d0b61-127">E-mail senders outside the mailbox user's organization who send messages to the user will not receive an external OOF message response.</span></span>  <br/> |
|<span data-ttu-id="d0b61-128">**Válida**</span><span class="sxs-lookup"><span data-stu-id="d0b61-128">**Known**</span></span> <br/> |<span data-ttu-id="d0b61-129">Los remitentes de correo electrónico que se encuentran fuera de la organización del usuario del buzón de correo que envían mensajes al usuario solo recibirán una respuesta de mensaje de OOF externa si el remitente está en la lista de contactos del almacén de Exchange del usuario.</span><span class="sxs-lookup"><span data-stu-id="d0b61-129">E-mail senders outside the mailbox user's organization who send messages to the user will only receive an external OOF message response if the sender is in the user's Exchange store contact list.</span></span>  <br/> |
|<span data-ttu-id="d0b61-130">**All**</span><span class="sxs-lookup"><span data-stu-id="d0b61-130">**All**</span></span> <br/> |<span data-ttu-id="d0b61-131">Los remitentes de correo electrónico que se encuentran fuera de la organización del usuario del buzón de correo que envían mensajes al usuario recibirán una respuesta de mensaje OOF externa.</span><span class="sxs-lookup"><span data-stu-id="d0b61-131">E-mail senders outside the mailbox user's organization who send messages to the user will receive an external OOF message response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0b61-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d0b61-132">Remarks</span></span>

<span data-ttu-id="d0b61-133">Este elemento comparte el mismo tipo que el elemento [AllowExternalOof](allowexternaloof.md) .</span><span class="sxs-lookup"><span data-stu-id="d0b61-133">This element shares the same type as the [AllowExternalOof](allowexternaloof.md) element.</span></span> 
  
<span data-ttu-id="d0b61-134">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="d0b61-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="d0b61-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0b61-135">Example</span></span>

<span data-ttu-id="d0b61-136">En el siguiente ejemplo de una solicitud de SetUserOofSettings se establece el OoFState en **habilitado**, se establece la audiencia externa en **todos**, se establece la duración de OOF en 10 días y se establecen los mensajes OOF internos y externos.</span><span class="sxs-lookup"><span data-stu-id="d0b61-136">The following example of a SetUserOofSettings request sets the OoFState to **Enabled**, sets the external audience to **All**, sets the duration of OOF to 10 days, and sets the internal and external OOF messages.</span></span>
  
```
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

## <a name="element-information"></a><span data-ttu-id="d0b61-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d0b61-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0b61-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0b61-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d0b61-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d0b61-139">Schema Name</span></span>  <br/> |<span data-ttu-id="d0b61-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d0b61-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="d0b61-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d0b61-141">Validation File</span></span>  <br/> |<span data-ttu-id="d0b61-142">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d0b61-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d0b61-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d0b61-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="d0b61-144">Falso</span><span class="sxs-lookup"><span data-stu-id="d0b61-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0b61-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0b61-145">See also</span></span>



[<span data-ttu-id="d0b61-146">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="d0b61-146">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="d0b61-147">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="d0b61-147">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

