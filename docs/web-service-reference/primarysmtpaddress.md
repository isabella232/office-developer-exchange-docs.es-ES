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
description: El elemento PrimarySmtpAddress representa la dirección de Protocolo simple de transferencia de correo (SMTP) principal de una cuenta que se va a usar para la autorización de servidor a servidor o acceso delegado.
ms.openlocfilehash: eea995b3e546d7e94e65cf9b230b639a781c4928
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467966"
---
# <a name="primarysmtpaddress"></a><span data-ttu-id="2e22c-103">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="2e22c-103">PrimarySmtpAddress</span></span>

<span data-ttu-id="2e22c-104">El elemento **PrimarySmtpAddress** representa la dirección de Protocolo simple de transferencia de correo (SMTP) principal de una cuenta que se va a usar para la autorización de servidor a servidor o acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="2e22c-104">The **PrimarySmtpAddress** element represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for server-to-server authorization or delegate access.</span></span> 
  
```xml
<PrimarySmtpAddress/>
```

 <span data-ttu-id="2e22c-105">**PrimarySmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="2e22c-105">**PrimarySmtpAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2e22c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2e22c-106">Attributes and elements</span></span>

<span data-ttu-id="2e22c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2e22c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e22c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2e22c-108">Attributes</span></span>

<span data-ttu-id="2e22c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2e22c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e22c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2e22c-110">Child elements</span></span>

<span data-ttu-id="2e22c-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2e22c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2e22c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2e22c-112">Parent elements</span></span>

|<span data-ttu-id="2e22c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2e22c-113">**Element**</span></span>|<span data-ttu-id="2e22c-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e22c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e22c-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="2e22c-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="2e22c-116">Representa una cuenta que se va a suplantar cuando se usa el encabezado SOAP ExchangeImpersonation.</span><span class="sxs-lookup"><span data-stu-id="2e22c-116">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="2e22c-117">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="2e22c-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="2e22c-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="2e22c-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="2e22c-119">Se usa en el encabezado SOAP para la serialización de tokens en la autenticación de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="2e22c-119">Used in the SOAP header for token serialization in server- to-server authentication.</span></span>  <br/> |
|[<span data-ttu-id="2e22c-120">UserId</span><span class="sxs-lookup"><span data-stu-id="2e22c-120">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="2e22c-121">Identifica un usuario delegado o un usuario que tiene permisos de acceso a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="2e22c-121">Identifies a delegate user or a user who has folder access permissions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2e22c-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2e22c-122">Text value</span></span>

<span data-ttu-id="2e22c-123">Se necesita un valor de texto que represente una dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="2e22c-123">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e22c-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e22c-124">Remarks</span></span>

<span data-ttu-id="2e22c-125">Los servicios web Exchange requieren que los buzones se identifiquen por la dirección SMTP principal del buzón.</span><span class="sxs-lookup"><span data-stu-id="2e22c-125">Exchange Web Services requires that mailboxes be identified by the primary SMTP address of the mailbox.</span></span> <span data-ttu-id="2e22c-126">No se aceptan direcciones proxy ni alternativas.</span><span class="sxs-lookup"><span data-stu-id="2e22c-126">Proxy or alternative addresses are not accepted.</span></span>
  
<span data-ttu-id="2e22c-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="2e22c-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e22c-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2e22c-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e22c-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e22c-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2e22c-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2e22c-130">Schema Name</span></span>  <br/> |<span data-ttu-id="2e22c-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2e22c-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="2e22c-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2e22c-132">Validation File</span></span>  <br/> |<span data-ttu-id="2e22c-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2e22c-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2e22c-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2e22c-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="2e22c-135">Falso</span><span class="sxs-lookup"><span data-stu-id="2e22c-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e22c-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e22c-136">See also</span></span>



- [<span data-ttu-id="2e22c-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2e22c-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="2e22c-138">Autorización de servidor a servidor en EWS</span><span class="sxs-lookup"><span data-stu-id="2e22c-138">Server-to-server authorization in EWS</span></span>](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)
  
[<span data-ttu-id="2e22c-139">Trabajar con acceso delegado</span><span class="sxs-lookup"><span data-stu-id="2e22c-139">Working with Delegate Access</span></span>](https://msdn.microsoft.com/library/dfd6b4a3-8fd3-47ba-83c0-52465cb5f3f3%28Office.15%29.aspx)

