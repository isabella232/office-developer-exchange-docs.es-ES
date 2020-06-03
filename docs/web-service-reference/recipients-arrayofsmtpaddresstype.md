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
description: El elemento Recipients especifica una matriz de destinatarios de un mensaje.
ms.openlocfilehash: 4c2478a81836c2e52baad9c928d112108679b837
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465509"
---
# <a name="recipients-arrayofsmtpaddresstype"></a><span data-ttu-id="67154-103">Recipients (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="67154-103">Recipients (ArrayOfSmtpAddressType)</span></span>

<span data-ttu-id="67154-104">El elemento **Recipients** especifica una matriz de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="67154-104">The **Recipients** element specifies an array of recipients of a message.</span></span> 
  
```xml
<Recipients>   <SmtpAddress/></Recipients>
```

 <span data-ttu-id="67154-105">**ArrayOfSmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="67154-105">**ArrayOfSmtpAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="67154-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="67154-106">Attributes and elements</span></span>

<span data-ttu-id="67154-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="67154-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67154-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="67154-108">Attributes</span></span>

<span data-ttu-id="67154-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="67154-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="67154-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="67154-110">Child elements</span></span>

|<span data-ttu-id="67154-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="67154-111">**Element**</span></span>|<span data-ttu-id="67154-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="67154-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67154-113">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="67154-113">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="67154-114">Representa la dirección del destinatario del Protocolo simple de transferencia de correo (SMTP) de una solicitud de uso compartido de contactos o calendario.</span><span class="sxs-lookup"><span data-stu-id="67154-114">Represents the Simple Mail Transfer Protocol (SMTP) recipient address of a calendar or contact sharing request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="67154-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="67154-115">Parent elements</span></span>

|<span data-ttu-id="67154-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="67154-116">**Element**</span></span>|<span data-ttu-id="67154-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="67154-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67154-118">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="67154-118">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="67154-119">Define una solicitud para obtener un token de autenticación opaco que identifique la invitación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="67154-119">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67154-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="67154-120">Remarks</span></span>

<span data-ttu-id="67154-121">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="67154-121">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67154-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="67154-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67154-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="67154-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="67154-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="67154-124">Schema Name</span></span>  <br/> |<span data-ttu-id="67154-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="67154-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="67154-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="67154-126">Validation File</span></span>  <br/> |<span data-ttu-id="67154-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="67154-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="67154-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="67154-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="67154-129">Falso</span><span class="sxs-lookup"><span data-stu-id="67154-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="67154-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="67154-130">See also</span></span>



[<span data-ttu-id="67154-131">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="67154-131">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="67154-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="67154-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

