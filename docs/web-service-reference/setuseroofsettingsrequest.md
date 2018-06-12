---
title: SetUserOofSettingsRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetUserOofSettingsRequest
api_type:
- schema
ms.assetid: 628acf0b-3ebc-42f1-8ce2-7a02b4c8141f
description: El elemento SetUserOofSettingsRequest contiene los argumentos que se usa para establecer la configuración del usuario fuera de la oficina (OOF) de un buzón de correo.
ms.openlocfilehash: ed54bb1d066da7b15605fb81931a6ef75dfc61bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837474"
---
# <a name="setuseroofsettingsrequest"></a><span data-ttu-id="ae5c8-103">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="ae5c8-103">SetUserOofSettingsRequest</span></span>

<span data-ttu-id="ae5c8-104">El elemento **SetUserOofSettingsRequest** contiene los argumentos que se usa para establecer la configuración del usuario fuera de la oficina (OOF) de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="ae5c8-104">The **SetUserOofSettingsRequest** element contains the arguments used to set a mailbox user's Out of Office (OOF) settings.</span></span> 
  
```xml
<SetUserOofSettingsRequest>
   <Mailbox>...</Mailbox>
   <UserOofSettings>...</UserOofSettings>
<SetUserOofSettingsRequest>
```

 <span data-ttu-id="ae5c8-105">**SetUserOofSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="ae5c8-105">**SetUserOofSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae5c8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ae5c8-106">Attributes and elements</span></span>

<span data-ttu-id="ae5c8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ae5c8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae5c8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ae5c8-108">Attributes</span></span>

<span data-ttu-id="ae5c8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ae5c8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae5c8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ae5c8-110">Child elements</span></span>

|<span data-ttu-id="ae5c8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ae5c8-111">**Element**</span></span>|<span data-ttu-id="ae5c8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae5c8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae5c8-113">Buzón de correo (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="ae5c8-113">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> |<span data-ttu-id="ae5c8-114">Identifica el usuario del buzón para una solicitud SetUserOofSettings o GetUserOofSettings.</span><span class="sxs-lookup"><span data-stu-id="ae5c8-114">Identifies the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/> |
|[<span data-ttu-id="ae5c8-115">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="ae5c8-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="ae5c8-116">Especifica la configuración de fuera de la oficina.</span><span class="sxs-lookup"><span data-stu-id="ae5c8-116">Specifies the OOF settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ae5c8-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ae5c8-117">Parent elements</span></span>

<span data-ttu-id="ae5c8-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ae5c8-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ae5c8-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae5c8-119">Remarks</span></span>

<span data-ttu-id="ae5c8-120">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ae5c8-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="ae5c8-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ae5c8-121">Example</span></span>

<span data-ttu-id="ae5c8-122">El siguiente ejemplo de una solicitud de SetUserOofSettings establece un valor de OOF para diez días.</span><span class="sxs-lookup"><span data-stu-id="ae5c8-122">The following example of a SetUserOofSettings request sets an OOF setting for ten days.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="ae5c8-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ae5c8-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae5c8-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ae5c8-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ae5c8-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ae5c8-125">Schema Name</span></span>  <br/> |<span data-ttu-id="ae5c8-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ae5c8-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ae5c8-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ae5c8-127">Validation File</span></span>  <br/> |<span data-ttu-id="ae5c8-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ae5c8-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ae5c8-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ae5c8-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="ae5c8-130">False</span><span class="sxs-lookup"><span data-stu-id="ae5c8-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae5c8-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="ae5c8-131">See also</span></span>



[<span data-ttu-id="ae5c8-132">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="ae5c8-132">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

