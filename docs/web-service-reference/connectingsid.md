---
title: ConnectingSID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectingSID
api_type:
- schema
ms.assetid: 56d6aa52-8fa6-4773-9046-44a6f4f5d97c
description: El elemento ConnectingSID representa una cuenta que se suplanta cuando se usa el encabezado SOAP ExchangeImpersonation.
ms.openlocfilehash: f4edf63f129fc769f4a2d710a505b40da4057fab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459282"
---
# <a name="connectingsid"></a><span data-ttu-id="76322-103">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="76322-103">ConnectingSID</span></span>

<span data-ttu-id="76322-104">El elemento **ConnectingSID** representa una cuenta que se suplanta cuando se usa el encabezado SOAP ExchangeImpersonation.</span><span class="sxs-lookup"><span data-stu-id="76322-104">The **ConnectingSID** element represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span> 
  
- [<span data-ttu-id="76322-105">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="76322-105">ExchangeImpersonation</span></span>](exchangeimpersonation.md) 
- [<span data-ttu-id="76322-106">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="76322-106">ConnectingSID</span></span>](connectingsid.md)
  
```xml
<ConnectingSID>
   <PrincipalName/>
</ConnectingSID>
```

```xml
<ConnectingSID>
   <SmtpAddress/>
</ConnectingSID>
```

```xml
<ConnectingSID>
    <SID/> 
</ConnectingSID>
```

```xml
<ConnectingSID>
   <PrimarySmtpAddress/>
</ConnectingSID>
```

<span data-ttu-id="76322-107">**ConnectingSIDType**</span><span class="sxs-lookup"><span data-stu-id="76322-107">**ConnectingSIDType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="76322-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="76322-108">Attributes and elements</span></span>

<span data-ttu-id="76322-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="76322-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76322-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="76322-110">Attributes</span></span>

<span data-ttu-id="76322-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="76322-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="76322-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="76322-112">Child elements</span></span>

|<span data-ttu-id="76322-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="76322-113">**Element**</span></span>|<span data-ttu-id="76322-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="76322-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76322-115">PrincipalName</span><span class="sxs-lookup"><span data-stu-id="76322-115">PrincipalName</span></span>](principalname.md) <br/> |<span data-ttu-id="76322-116">Representa el nombre principal de usuario (UPN) de la cuenta que se va a usar para la suplantación.</span><span class="sxs-lookup"><span data-stu-id="76322-116">Represents the user principal name (UPN) of the account to use for impersonation.</span></span> <span data-ttu-id="76322-117">Debe ser el UPN del dominio en el que se encuentra la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="76322-117">This should be the UPN for the domain where the user account exists.</span></span>  <br/> |
|[<span data-ttu-id="76322-118">SID</span><span class="sxs-lookup"><span data-stu-id="76322-118">SID</span></span>](sid.md) <br/> |<span data-ttu-id="76322-119">Representa el formato de lenguaje de definición de descriptores de seguridad (SDDL) del identificador de seguridad (SID) de la cuenta que se va a usar para la suplantación.</span><span class="sxs-lookup"><span data-stu-id="76322-119">Represents the security descriptor definition language (SDDL) form of the security identifier (SID) for the account to use for impersonation.</span></span>  <br/> |
|[<span data-ttu-id="76322-120">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="76322-120">PrimarySmtpAddress</span></span>](primarysmtpaddress.md) <br/> |<span data-ttu-id="76322-121">Representa la dirección de Protocolo simple de transferencia de correo (SMTP) principal de la cuenta que se va a usar para la suplantación de Exchange.</span><span class="sxs-lookup"><span data-stu-id="76322-121">Represents the primary Simple Mail Transfer Protocol (SMTP) address of the account to use for Exchange impersonation.</span></span> <span data-ttu-id="76322-122">Si se proporciona la dirección SMTP principal, la búsqueda del servicio de directorio de Active Directory adicional será más costosa para obtener el SID del usuario.</span><span class="sxs-lookup"><span data-stu-id="76322-122">If the primary SMTP address is supplied, it will cost an extra Active Directory directory service lookup in order to obtain the SID of the user.</span></span> <span data-ttu-id="76322-123">Le recomendamos que use el SID o el UPN si están disponibles.</span><span class="sxs-lookup"><span data-stu-id="76322-123">We recommend that you use the SID or UPN if they are available.</span></span>  <br/> |
|[<span data-ttu-id="76322-124">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="76322-124">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="76322-125">Representa la dirección del Protocolo simple de transferencia de correo (SMTP) de la cuenta que se va a usar para la suplantación de Exchange.</span><span class="sxs-lookup"><span data-stu-id="76322-125">Represents the Simple Mail Transfer Protocol (SMTP) address of the account to use for Exchange Impersonation.</span></span> <span data-ttu-id="76322-126">Si se proporciona la dirección SMTP, el costo de la búsqueda en Active Directory será mayor para obtener el SID del usuario.</span><span class="sxs-lookup"><span data-stu-id="76322-126">If the SMTP address is supplied, it will cost an extra Active Directory lookup in order to obtain the SID of the user.</span></span> <span data-ttu-id="76322-127">Le recomendamos que use el SID o el UPN si están disponibles.</span><span class="sxs-lookup"><span data-stu-id="76322-127">We recommend that you use the SID or UPN if they are available.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="76322-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="76322-128">Parent elements</span></span>

|<span data-ttu-id="76322-129">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="76322-129">**Element**</span></span>|<span data-ttu-id="76322-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="76322-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76322-131">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="76322-131">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="76322-132">Se usa en el encabezado SOAP de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="76322-132">Used in the SOAP header of a request.</span></span> <span data-ttu-id="76322-133">Cuando este elemento está presente, el autor de la llamada está intentando suplantar la cuenta contenida en el elemento **ExchangeImpersonation** .</span><span class="sxs-lookup"><span data-stu-id="76322-133">When this element is present, the caller is trying to impersonate the account that is contained within the **ExchangeImpersonation** element.</span></span>  <br/> <span data-ttu-id="76322-134">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="76322-134">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76322-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="76322-135">Remarks</span></span>

<span data-ttu-id="76322-136">La cuenta de llamada debe tener el derecho **MS-Exch-Impersonation** en el servidor de acceso de cliente y el derecho **MS-Exch-MayImpersonate** en la base de datos de buzones de correo que contiene el buzón de correo para la suplantación o el objeto de contacto o de usuario de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="76322-136">The calling account must have the **ms-exch-impersonation** right on the Client Access server and the **ms-exch-MayImpersonate** right on either the mailbox database that contains the mailbox to impersonate or the Active Directory user or contact object.</span></span> 
  
<span data-ttu-id="76322-137">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="76322-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="76322-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="76322-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76322-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="76322-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="76322-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="76322-140">Schema name</span></span>  <br/> |<span data-ttu-id="76322-141">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="76322-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="76322-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="76322-142">Validation file</span></span>  <br/> |<span data-ttu-id="76322-143">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="76322-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="76322-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="76322-144">Can be empty</span></span>  <br/> |<span data-ttu-id="76322-145">Falso</span><span class="sxs-lookup"><span data-stu-id="76322-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76322-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="76322-146">See also</span></span>

- [<span data-ttu-id="76322-147">Autorización de servidor a servidor en EWS</span><span class="sxs-lookup"><span data-stu-id="76322-147">Server-to-server authorization in EWS</span></span>](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

