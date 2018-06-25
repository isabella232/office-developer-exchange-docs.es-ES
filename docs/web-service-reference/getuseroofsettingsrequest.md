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
description: El elemento GetUserOofSettingsRequest es el elemento raíz que contiene los argumentos que se usa para obtener la configuración del usuario fuera de la oficina (OOF) de un buzón de correo.
ms.openlocfilehash: e64818961283f90e447e2044cf7f918eccd21f06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835692"
---
# <a name="getuseroofsettingsrequest"></a><span data-ttu-id="b4980-103">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="b4980-103">GetUserOofSettingsRequest</span></span>

<span data-ttu-id="b4980-104">El elemento **GetUserOofSettingsRequest** es el elemento raíz que contiene los argumentos que se usa para obtener la configuración del usuario fuera de la oficina (OOF) de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="b4980-104">The **GetUserOofSettingsRequest** element is the root element that contains the arguments used to get a mailbox user's Out of Office (OOF) settings.</span></span> 
  
```xml
<GetUserOofSettingsRequest>
   <Mailbox>...</Mailbox>
</GetUserOofSettingsRequest>
```

 <span data-ttu-id="b4980-105">**GetUserOofSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="b4980-105">**GetUserOofSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b4980-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b4980-106">Attributes and elements</span></span>

<span data-ttu-id="b4980-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b4980-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4980-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b4980-108">Attributes</span></span>

<span data-ttu-id="b4980-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b4980-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b4980-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b4980-110">Child elements</span></span>

|<span data-ttu-id="b4980-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b4980-111">**Element**</span></span>|<span data-ttu-id="b4980-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b4980-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b4980-113">Buzón de correo (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="b4980-113">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> |<span data-ttu-id="b4980-114">Identifica el usuario del buzón para una solicitud SetUserOofSettings o GetUserOofSettings.</span><span class="sxs-lookup"><span data-stu-id="b4980-114">Identifies the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b4980-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b4980-115">Parent elements</span></span>

<span data-ttu-id="b4980-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b4980-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b4980-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b4980-117">Remarks</span></span>

<span data-ttu-id="b4980-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b4980-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="b4980-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b4980-119">Example</span></span>

<span data-ttu-id="b4980-120">El siguiente es un ejemplo de una solicitud de GetUserOofSettings que obtiene información de fuera de la oficina de un único usuario.</span><span class="sxs-lookup"><span data-stu-id="b4980-120">The following is an example of a GetUserOofSettings request that gets a single user's OOF information.</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
    </GetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="b4980-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b4980-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4980-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b4980-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b4980-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b4980-123">Schema Name</span></span>  <br/> |<span data-ttu-id="b4980-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b4980-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b4980-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b4980-125">Validation File</span></span>  <br/> |<span data-ttu-id="b4980-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b4980-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b4980-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b4980-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="b4980-128">False</span><span class="sxs-lookup"><span data-stu-id="b4980-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4980-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4980-129">See also</span></span>



[<span data-ttu-id="b4980-130">Operación GetUserOofSettings</span><span class="sxs-lookup"><span data-stu-id="b4980-130">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)

