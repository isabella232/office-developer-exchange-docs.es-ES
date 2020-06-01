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
description: El elemento SetUserOofSettingsRequest contiene los argumentos usados para establecer la configuración de fuera de la oficina (OOF) de un usuario de buzón.
ms.openlocfilehash: 10edc9809fd72f80c316de1c6688eaedec4f93df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466153"
---
# <a name="setuseroofsettingsrequest"></a><span data-ttu-id="20efe-103">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="20efe-103">SetUserOofSettingsRequest</span></span>

<span data-ttu-id="20efe-104">El elemento **SetUserOofSettingsRequest** contiene los argumentos usados para establecer la configuración de fuera de la oficina (OOF) de un usuario de buzón.</span><span class="sxs-lookup"><span data-stu-id="20efe-104">The **SetUserOofSettingsRequest** element contains the arguments used to set a mailbox user's Out of Office (OOF) settings.</span></span> 
  
```xml
<SetUserOofSettingsRequest>
   <Mailbox>...</Mailbox>
   <UserOofSettings>...</UserOofSettings>
<SetUserOofSettingsRequest>
```

 <span data-ttu-id="20efe-105">**SetUserOofSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="20efe-105">**SetUserOofSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="20efe-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="20efe-106">Attributes and elements</span></span>

<span data-ttu-id="20efe-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="20efe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20efe-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="20efe-108">Attributes</span></span>

<span data-ttu-id="20efe-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="20efe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="20efe-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="20efe-110">Child elements</span></span>

|<span data-ttu-id="20efe-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="20efe-111">**Element**</span></span>|<span data-ttu-id="20efe-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="20efe-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="20efe-113">Buzón de correo (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="20efe-113">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> |<span data-ttu-id="20efe-114">Identifica al usuario del buzón de correo para una solicitud de SetUserOofSettings o GetUserOofSettings.</span><span class="sxs-lookup"><span data-stu-id="20efe-114">Identifies the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/> |
|[<span data-ttu-id="20efe-115">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="20efe-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="20efe-116">Especifica la configuración de OOF.</span><span class="sxs-lookup"><span data-stu-id="20efe-116">Specifies the OOF settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="20efe-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="20efe-117">Parent elements</span></span>

<span data-ttu-id="20efe-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="20efe-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20efe-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20efe-119">Remarks</span></span>

<span data-ttu-id="20efe-120">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="20efe-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="20efe-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="20efe-121">Example</span></span>

<span data-ttu-id="20efe-122">El siguiente ejemplo de una solicitud SetUserOofSettings establece un valor OOF para diez días.</span><span class="sxs-lookup"><span data-stu-id="20efe-122">The following example of a SetUserOofSettings request sets an OOF setting for ten days.</span></span>
  
```xml
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

## <a name="element-information"></a><span data-ttu-id="20efe-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="20efe-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20efe-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="20efe-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="20efe-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="20efe-125">Schema Name</span></span>  <br/> |<span data-ttu-id="20efe-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="20efe-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="20efe-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="20efe-127">Validation File</span></span>  <br/> |<span data-ttu-id="20efe-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="20efe-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="20efe-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="20efe-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="20efe-130">Falso</span><span class="sxs-lookup"><span data-stu-id="20efe-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20efe-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="20efe-131">See also</span></span>



[<span data-ttu-id="20efe-132">Operación SetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="20efe-132">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

