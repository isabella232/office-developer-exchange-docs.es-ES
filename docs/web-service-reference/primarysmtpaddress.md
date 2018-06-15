---
title: PrimarySmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PrimarySmtpAddress
api_type:
- schema
ms.assetid: eee79904-9412-4e61-b9b8-aff0ce25fade
description: El elemento PrimarySmtpAddress representa la dirección de Protocolo Simple de transferencia de correo (SMTP) principal de una cuenta que se usará para la autorización de servidor a servidor o acceso delegado.
ms.openlocfilehash: d33bf22af4ddf6b2f6d8d8d434168264acfaea7c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19836881"
---
# <a name="primarysmtpaddress"></a><span data-ttu-id="d2852-103">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="d2852-103">PrimarySmtpAddress</span></span>

<span data-ttu-id="d2852-104">El elemento **PrimarySmtpAddress** representa la dirección de Protocolo Simple de transferencia de correo (SMTP) principal de una cuenta que se usará para la autorización de servidor a servidor o acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="d2852-104">The **PrimarySmtpAddress** element represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for server-to-server authorization or delegate access.</span></span> 
  
```xml
<PrimarySmtpAddress/>
```

 <span data-ttu-id="d2852-105">**PrimarySmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="d2852-105">**PrimarySmtpAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d2852-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d2852-106">Attributes and elements</span></span>

<span data-ttu-id="d2852-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d2852-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2852-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d2852-108">Attributes</span></span>

<span data-ttu-id="d2852-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d2852-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d2852-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d2852-110">Child elements</span></span>

<span data-ttu-id="d2852-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d2852-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d2852-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d2852-112">Parent elements</span></span>

|<span data-ttu-id="d2852-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d2852-113">**Element**</span></span>|<span data-ttu-id="d2852-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d2852-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2852-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="d2852-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="d2852-116">Representa una cuenta para suplantar a cuando se usa el encabezado SOAP ExchangeImpersonation.</span><span class="sxs-lookup"><span data-stu-id="d2852-116">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="d2852-117">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="d2852-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="d2852-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="d2852-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="d2852-119">Se usa en el encabezado SOAP para la serialización de token de autenticación de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="d2852-119">Used in the SOAP header for token serialization in server- to-server authentication.</span></span>  <br/> |
|[<span data-ttu-id="d2852-120">UserId</span><span class="sxs-lookup"><span data-stu-id="d2852-120">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="d2852-121">Identifica un usuario delegado o un usuario que tiene permisos de acceso de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d2852-121">Identifies a delegate user or a user who has folder access permissions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d2852-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d2852-122">Text value</span></span>

<span data-ttu-id="d2852-123">Se requiere un valor de texto que representa una dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="d2852-123">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2852-124">Notas</span><span class="sxs-lookup"><span data-stu-id="d2852-124">Remarks</span></span>

<span data-ttu-id="d2852-125">Servicios Web de Exchange requiere que los buzones de correo se identificado por la dirección SMTP principal del buzón.</span><span class="sxs-lookup"><span data-stu-id="d2852-125">Exchange Web Services requires that mailboxes be identified by the primary SMTP address of the mailbox.</span></span> <span data-ttu-id="d2852-126">No se aceptan direcciones alternativas o proxy.</span><span class="sxs-lookup"><span data-stu-id="d2852-126">Proxy or alternative addresses are not accepted.</span></span>
  
<span data-ttu-id="d2852-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d2852-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d2852-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d2852-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2852-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d2852-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d2852-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d2852-130">Schema Name</span></span>  <br/> |<span data-ttu-id="d2852-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d2852-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="d2852-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d2852-132">Validation File</span></span>  <br/> |<span data-ttu-id="d2852-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d2852-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d2852-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d2852-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="d2852-135">False</span><span class="sxs-lookup"><span data-stu-id="d2852-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2852-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="d2852-136">See also</span></span>



- [<span data-ttu-id="d2852-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d2852-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="d2852-138">Autorización de servidor a servidor en EWS</span><span class="sxs-lookup"><span data-stu-id="d2852-138">Server-to-server authorization in EWS</span></span>](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)
  
[<span data-ttu-id="d2852-139">Trabajar con el acceso delegado</span><span class="sxs-lookup"><span data-stu-id="d2852-139">Working with Delegate Access</span></span>](http://msdn.microsoft.com/library/dfd6b4a3-8fd3-47ba-83c0-52465cb5f3f3%28Office.15%29.aspx)

