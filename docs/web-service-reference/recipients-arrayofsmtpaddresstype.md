---
title: Recipients (ArrayOfSmtpAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recipients
api_type:
- schema
ms.assetid: cf68417d-85cf-49e0-857a-f987d3675344
description: El elemento de destinatarios especifica una matriz de destinatarios de un mensaje.
ms.openlocfilehash: 8490988043b1e06fd3a8f553fcefaeb2e90e9d31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836988"
---
# <a name="recipients-arrayofsmtpaddresstype"></a><span data-ttu-id="514df-103">Recipients (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="514df-103">Recipients (ArrayOfSmtpAddressType)</span></span>

<span data-ttu-id="514df-104">El elemento de **destinatarios de** especifica una matriz de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="514df-104">The **Recipients** element specifies an array of recipients of a message.</span></span> 
  
```xml
<Recipients>   <SmtpAddress/></Recipients>
```

 <span data-ttu-id="514df-105">**ArrayOfSmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="514df-105">**ArrayOfSmtpAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="514df-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="514df-106">Attributes and elements</span></span>

<span data-ttu-id="514df-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="514df-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="514df-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="514df-108">Attributes</span></span>

<span data-ttu-id="514df-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="514df-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="514df-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="514df-110">Child elements</span></span>

|<span data-ttu-id="514df-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="514df-111">**Element**</span></span>|<span data-ttu-id="514df-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="514df-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="514df-113">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="514df-113">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="514df-114">Representa la dirección del destinatario de Protocolo Simple de transferencia de correo (SMTP) de un calendario o un contacto solicitud para compartir.</span><span class="sxs-lookup"><span data-stu-id="514df-114">Represents the Simple Mail Transfer Protocol (SMTP) recipient address of a calendar or contact sharing request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="514df-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="514df-115">Parent elements</span></span>

|<span data-ttu-id="514df-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="514df-116">**Element**</span></span>|<span data-ttu-id="514df-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="514df-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="514df-118">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="514df-118">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="514df-119">Define una solicitud para obtener un token de autenticación opaco que identifica la invitación para compartir.</span><span class="sxs-lookup"><span data-stu-id="514df-119">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="514df-120">Notas</span><span class="sxs-lookup"><span data-stu-id="514df-120">Remarks</span></span>

<span data-ttu-id="514df-121">El esquema que describe este elemento se encuentra en el directorio Virtual de IIS que hospeda los servicios Web Exchange del equipo que ejecuta a Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="514df-121">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="514df-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="514df-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="514df-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="514df-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="514df-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="514df-124">Schema Name</span></span>  <br/> |<span data-ttu-id="514df-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="514df-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="514df-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="514df-126">Validation File</span></span>  <br/> |<span data-ttu-id="514df-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="514df-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="514df-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="514df-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="514df-129">False</span><span class="sxs-lookup"><span data-stu-id="514df-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="514df-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="514df-130">See also</span></span>



[<span data-ttu-id="514df-131">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="514df-131">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="514df-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="514df-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

