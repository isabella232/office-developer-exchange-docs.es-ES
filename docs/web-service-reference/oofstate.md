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
description: El elemento OofState se usa para obtener o establecer el estado de fuera de oficina (OOF) del usuario.
ms.openlocfilehash: f97c050aec102b384fa4d98e6dee43befd4dc9ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836651"
---
# <a name="oofstate"></a><span data-ttu-id="bab49-103">OofState</span><span class="sxs-lookup"><span data-stu-id="bab49-103">OofState</span></span>

<span data-ttu-id="bab49-104">El elemento **OofState** se usa para obtener o establecer el estado de fuera de oficina (OOF) del usuario.</span><span class="sxs-lookup"><span data-stu-id="bab49-104">The **OofState** element is used to get or set the user's Out of Office (OOF) state.</span></span> 
  
```xml
<OofState>Disabled or Enabled or Scheduled</OofState>
```

 <span data-ttu-id="bab49-105">**OofState**</span><span class="sxs-lookup"><span data-stu-id="bab49-105">**OofState**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bab49-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bab49-106">Attributes and elements</span></span>

<span data-ttu-id="bab49-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bab49-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bab49-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="bab49-108">Attributes</span></span>

<span data-ttu-id="bab49-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bab49-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bab49-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bab49-110">Child elements</span></span>

<span data-ttu-id="bab49-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bab49-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bab49-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bab49-112">Parent elements</span></span>

|<span data-ttu-id="bab49-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bab49-113">**Element**</span></span>|<span data-ttu-id="bab49-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bab49-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bab49-115">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="bab49-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="bab49-116">Especifica la configuración de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="bab49-116">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="bab49-117">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="bab49-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="bab49-118">OofSettings</span><span class="sxs-lookup"><span data-stu-id="bab49-118">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="bab49-119">Contiene la configuración de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="bab49-119">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="bab49-120">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="bab49-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bab49-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="bab49-121">Text value</span></span>

<span data-ttu-id="bab49-122">Un valor de texto es necesario para el elemento **OofState** .</span><span class="sxs-lookup"><span data-stu-id="bab49-122">A text value is required for the **OofState** element.</span></span> <span data-ttu-id="bab49-123">En la lista siguiente contiene los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="bab49-123">The following list contains the possible values for this element:</span></span> 
  
- <span data-ttu-id="bab49-124">**Deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="bab49-124">**Disabled**</span></span>
    
- <span data-ttu-id="bab49-125">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="bab49-125">**Enabled**</span></span>
    
- <span data-ttu-id="bab49-126">**Programado**</span><span class="sxs-lookup"><span data-stu-id="bab49-126">**Scheduled**</span></span>
    
<span data-ttu-id="bab49-127">Un valor de **programada** indica que el estado de fuera de la oficina se establece en **habilitado** durante un período de tiempo identificado por el elemento de [duración (UserOofSettings)](duration-useroofsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="bab49-127">A value of **Scheduled** indicates that the OOF status is set to **Enabled** during a time period identified by the [Duration (UserOofSettings)](duration-useroofsettings.md) element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bab49-128">Notas</span><span class="sxs-lookup"><span data-stu-id="bab49-128">Remarks</span></span>

<span data-ttu-id="bab49-129">Este elemento es necesario en el mensaje de SetUsersOofSettingRequest y el mensaje GetUserOofSettingResponse.</span><span class="sxs-lookup"><span data-stu-id="bab49-129">This element is required in both the SetUsersOofSettingRequest message and the GetUserOofSettingResponse message.</span></span>
  
<span data-ttu-id="bab49-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="bab49-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="bab49-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bab49-131">Example</span></span>

<span data-ttu-id="bab49-132">El siguiente ejemplo de una solicitud de SetUserOofSettings permite la **OofState**.</span><span class="sxs-lookup"><span data-stu-id="bab49-132">The following example of a SetUserOofSettings request enables the **OofState**.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="bab49-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bab49-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bab49-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bab49-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bab49-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bab49-135">Schema Name</span></span>  <br/> |<span data-ttu-id="bab49-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="bab49-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="bab49-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bab49-137">Validation File</span></span>  <br/> |<span data-ttu-id="bab49-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bab49-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bab49-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bab49-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="bab49-140">False</span><span class="sxs-lookup"><span data-stu-id="bab49-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bab49-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="bab49-141">See also</span></span>



[<span data-ttu-id="bab49-142">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="bab49-142">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="bab49-143">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="bab49-143">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

