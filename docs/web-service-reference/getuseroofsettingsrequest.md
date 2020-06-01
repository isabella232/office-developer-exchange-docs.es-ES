---
title: GetUserOofSettingsRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserOofSettingsRequest
api_type:
- schema
ms.assetid: 15dea99c-7f5d-4af1-82ff-4255127fe567
description: El elemento GetUserOofSettingsRequest es el elemento raíz que contiene los argumentos usados para obtener la configuración de fuera de la oficina (OOF) del usuario de un buzón.
ms.openlocfilehash: f515e8cf016d3aff6c652ae92a0da71a8f0a5f6b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457833"
---
# <a name="getuseroofsettingsrequest"></a><span data-ttu-id="001a7-103">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="001a7-103">GetUserOofSettingsRequest</span></span>

<span data-ttu-id="001a7-104">El elemento **GetUserOofSettingsRequest** es el elemento raíz que contiene los argumentos usados para obtener la configuración de fuera de la oficina (OOF) del usuario de un buzón.</span><span class="sxs-lookup"><span data-stu-id="001a7-104">The **GetUserOofSettingsRequest** element is the root element that contains the arguments used to get a mailbox user's Out of Office (OOF) settings.</span></span> 
  
```xml
<GetUserOofSettingsRequest>
   <Mailbox>...</Mailbox>
</GetUserOofSettingsRequest>
```

 <span data-ttu-id="001a7-105">**GetUserOofSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="001a7-105">**GetUserOofSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="001a7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="001a7-106">Attributes and elements</span></span>

<span data-ttu-id="001a7-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="001a7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="001a7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="001a7-108">Attributes</span></span>

<span data-ttu-id="001a7-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="001a7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="001a7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="001a7-110">Child elements</span></span>

|<span data-ttu-id="001a7-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="001a7-111">**Element**</span></span>|<span data-ttu-id="001a7-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="001a7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="001a7-113">Buzón de correo (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="001a7-113">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> |<span data-ttu-id="001a7-114">Identifica al usuario del buzón de correo para una solicitud de SetUserOofSettings o GetUserOofSettings.</span><span class="sxs-lookup"><span data-stu-id="001a7-114">Identifies the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="001a7-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="001a7-115">Parent elements</span></span>

<span data-ttu-id="001a7-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="001a7-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="001a7-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="001a7-117">Remarks</span></span>

<span data-ttu-id="001a7-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="001a7-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="001a7-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="001a7-119">Example</span></span>

<span data-ttu-id="001a7-120">El siguiente es un ejemplo de una solicitud de GetUserOofSettings que obtiene la información de OOF de un solo usuario.</span><span class="sxs-lookup"><span data-stu-id="001a7-120">The following is an example of a GetUserOofSettings request that gets a single user's OOF information.</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
    </GetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="001a7-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="001a7-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="001a7-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="001a7-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="001a7-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="001a7-123">Schema Name</span></span>  <br/> |<span data-ttu-id="001a7-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="001a7-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="001a7-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="001a7-125">Validation File</span></span>  <br/> |<span data-ttu-id="001a7-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="001a7-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="001a7-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="001a7-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="001a7-128">Falso</span><span class="sxs-lookup"><span data-stu-id="001a7-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="001a7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="001a7-129">See also</span></span>



[<span data-ttu-id="001a7-130">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="001a7-130">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)

