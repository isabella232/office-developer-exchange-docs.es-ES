---
title: OofState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OofState
api_type:
- schema
ms.assetid: 3c486a38-06da-4382-ad20-664d067d76ac
description: El elemento OofState se usa para obtener o establecer el estado fuera de la oficina del usuario (OOF).
ms.openlocfilehash: 6aef7d989ee6978019a483f2673895e68a88a7c5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459738"
---
# <a name="oofstate"></a><span data-ttu-id="dcca4-103">OofState</span><span class="sxs-lookup"><span data-stu-id="dcca4-103">OofState</span></span>

<span data-ttu-id="dcca4-104">El elemento **OofState** se usa para obtener o establecer el estado fuera de la oficina del usuario (OOF).</span><span class="sxs-lookup"><span data-stu-id="dcca4-104">The **OofState** element is used to get or set the user's Out of Office (OOF) state.</span></span> 
  
```xml
<OofState>Disabled or Enabled or Scheduled</OofState>
```

 <span data-ttu-id="dcca4-105">**OofState**</span><span class="sxs-lookup"><span data-stu-id="dcca4-105">**OofState**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dcca4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dcca4-106">Attributes and elements</span></span>

<span data-ttu-id="dcca4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dcca4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dcca4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dcca4-108">Attributes</span></span>

<span data-ttu-id="dcca4-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="dcca4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dcca4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dcca4-110">Child elements</span></span>

<span data-ttu-id="dcca4-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="dcca4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dcca4-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dcca4-112">Parent elements</span></span>

|<span data-ttu-id="dcca4-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dcca4-113">**Element**</span></span>|<span data-ttu-id="dcca4-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dcca4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dcca4-115">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="dcca4-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="dcca4-116">Especifica la configuración de OOF.</span><span class="sxs-lookup"><span data-stu-id="dcca4-116">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="dcca4-117">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="dcca4-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="dcca4-118">OofSettings</span><span class="sxs-lookup"><span data-stu-id="dcca4-118">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="dcca4-119">Contiene la configuración de OOF.</span><span class="sxs-lookup"><span data-stu-id="dcca4-119">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="dcca4-120">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="dcca4-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dcca4-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="dcca4-121">Text value</span></span>

<span data-ttu-id="dcca4-122">Se requiere un valor de texto para el elemento **OofState** .</span><span class="sxs-lookup"><span data-stu-id="dcca4-122">A text value is required for the **OofState** element.</span></span> <span data-ttu-id="dcca4-123">La lista siguiente contiene los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="dcca4-123">The following list contains the possible values for this element:</span></span> 
  
- <span data-ttu-id="dcca4-124">**Disabled**</span><span class="sxs-lookup"><span data-stu-id="dcca4-124">**Disabled**</span></span>
    
- <span data-ttu-id="dcca4-125">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="dcca4-125">**Enabled**</span></span>
    
- <span data-ttu-id="dcca4-126">**Scheduled**</span><span class="sxs-lookup"><span data-stu-id="dcca4-126">**Scheduled**</span></span>
    
<span data-ttu-id="dcca4-127">Un valor de **programado** indica que el estado de OOF se establece en **habilitado** durante un período de tiempo identificado por el elemento [Duration (UserOofSettings)](duration-useroofsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="dcca4-127">A value of **Scheduled** indicates that the OOF status is set to **Enabled** during a time period identified by the [Duration (UserOofSettings)](duration-useroofsettings.md) element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dcca4-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dcca4-128">Remarks</span></span>

<span data-ttu-id="dcca4-129">Este elemento es obligatorio tanto en el mensaje SetUsersOofSettingRequest como en el mensaje GetUserOofSettingResponse.</span><span class="sxs-lookup"><span data-stu-id="dcca4-129">This element is required in both the SetUsersOofSettingRequest message and the GetUserOofSettingResponse message.</span></span>
  
<span data-ttu-id="dcca4-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="dcca4-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="dcca4-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dcca4-131">Example</span></span>

<span data-ttu-id="dcca4-132">El siguiente ejemplo de una solicitud SetUserOofSettings habilita el **OofState**.</span><span class="sxs-lookup"><span data-stu-id="dcca4-132">The following example of a SetUserOofSettings request enables the **OofState**.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="dcca4-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dcca4-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dcca4-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="dcca4-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dcca4-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dcca4-135">Schema Name</span></span>  <br/> |<span data-ttu-id="dcca4-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="dcca4-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="dcca4-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dcca4-137">Validation File</span></span>  <br/> |<span data-ttu-id="dcca4-138">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="dcca4-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dcca4-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dcca4-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="dcca4-140">Falso</span><span class="sxs-lookup"><span data-stu-id="dcca4-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dcca4-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcca4-141">See also</span></span>



[<span data-ttu-id="dcca4-142">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="dcca4-142">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="dcca4-143">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="dcca4-143">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

