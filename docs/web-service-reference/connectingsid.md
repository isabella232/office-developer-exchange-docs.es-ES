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
description: El elemento ConnectingSID representa una cuenta para suplantar a cuando se usa el encabezado SOAP ExchangeImpersonation.
ms.openlocfilehash: a30f11721506989a84f52dd04c328974f4483956
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354340"
---
# <a name="connectingsid"></a><span data-ttu-id="682d5-103">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="682d5-103">ConnectingSID</span></span>

<span data-ttu-id="682d5-104">El elemento **ConnectingSID** representa una cuenta para suplantar a cuando se usa el encabezado SOAP ExchangeImpersonation.</span><span class="sxs-lookup"><span data-stu-id="682d5-104">The **ConnectingSID** element represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span> 
  
- [<span data-ttu-id="682d5-105">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="682d5-105">ExchangeImpersonation</span></span>](exchangeimpersonation.md) 
- [<span data-ttu-id="682d5-106">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="682d5-106">ConnectingSID</span></span>](connectingsid.md)
  
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

<span data-ttu-id="682d5-107">**ConnectingSIDType**</span><span class="sxs-lookup"><span data-stu-id="682d5-107">**ConnectingSIDType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="682d5-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="682d5-108">Attributes and elements</span></span>

<span data-ttu-id="682d5-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="682d5-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="682d5-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="682d5-110">Attributes</span></span>

<span data-ttu-id="682d5-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="682d5-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="682d5-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="682d5-112">Child elements</span></span>

|<span data-ttu-id="682d5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="682d5-113">**Element**</span></span>|<span data-ttu-id="682d5-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="682d5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="682d5-115">PrincipalName</span><span class="sxs-lookup"><span data-stu-id="682d5-115">PrincipalName</span></span>](principalname.md) <br/> |<span data-ttu-id="682d5-116">Representa el nombre principal de usuario (UPN) de la cuenta a utilizar para la suplantación.</span><span class="sxs-lookup"><span data-stu-id="682d5-116">Represents the user principal name (UPN) of the account to use for impersonation.</span></span> <span data-ttu-id="682d5-117">Debe ser el UPN para el dominio donde se encuentra la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="682d5-117">This should be the UPN for the domain where the user account exists.</span></span>  <br/> |
|[<span data-ttu-id="682d5-118">SID</span><span class="sxs-lookup"><span data-stu-id="682d5-118">SID</span></span>](sid.md) <br/> |<span data-ttu-id="682d5-119">Representa el formulario de idioma (SDDL) de definición de descriptor de seguridad del identificador de seguridad (SID) para que la cuenta a utilizar para la suplantación.</span><span class="sxs-lookup"><span data-stu-id="682d5-119">Represents the security descriptor definition language (SDDL) form of the security identifier (SID) for the account to use for impersonation.</span></span>  <br/> |
|[<span data-ttu-id="682d5-120">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="682d5-120">PrimarySmtpAddress</span></span>](primarysmtpaddress.md) <br/> |<span data-ttu-id="682d5-121">Representa la dirección de Protocolo Simple de transferencia de correo (SMTP) principal de la cuenta que se usará para la suplantación de Exchange.</span><span class="sxs-lookup"><span data-stu-id="682d5-121">Represents the primary Simple Mail Transfer Protocol (SMTP) address of the account to use for Exchange impersonation.</span></span> <span data-ttu-id="682d5-122">Si se proporciona la dirección SMTP principal, costo una búsqueda de servicio de directorio de Active Directory adicional con el fin de obtener al SID del usuario.</span><span class="sxs-lookup"><span data-stu-id="682d5-122">If the primary SMTP address is supplied, it will cost an extra Active Directory directory service lookup in order to obtain the SID of the user.</span></span> <span data-ttu-id="682d5-123">Se recomienda usar el SID o el UPN si están disponibles.</span><span class="sxs-lookup"><span data-stu-id="682d5-123">We recommend that you use the SID or UPN if they are available.</span></span>  <br/> |
|[<span data-ttu-id="682d5-124">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="682d5-124">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="682d5-125">Representa la dirección de Protocolo Simple de transferencia de correo (SMTP) de la cuenta que se usará para la suplantación de Exchange.</span><span class="sxs-lookup"><span data-stu-id="682d5-125">Represents the Simple Mail Transfer Protocol (SMTP) address of the account to use for Exchange Impersonation.</span></span> <span data-ttu-id="682d5-126">Si se proporciona la dirección SMTP, costo una búsqueda de Active Directory adicional con el fin de obtener al SID del usuario.</span><span class="sxs-lookup"><span data-stu-id="682d5-126">If the SMTP address is supplied, it will cost an extra Active Directory lookup in order to obtain the SID of the user.</span></span> <span data-ttu-id="682d5-127">Se recomienda usar el SID o el UPN si están disponibles.</span><span class="sxs-lookup"><span data-stu-id="682d5-127">We recommend that you use the SID or UPN if they are available.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="682d5-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="682d5-128">Parent elements</span></span>

|<span data-ttu-id="682d5-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="682d5-129">**Element**</span></span>|<span data-ttu-id="682d5-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="682d5-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="682d5-131">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="682d5-131">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="682d5-132">Se usa en el encabezado SOAP de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="682d5-132">Used in the SOAP header of a request.</span></span> <span data-ttu-id="682d5-133">Cuando este elemento está presente, el autor de la llamada está intentando suplantar la cuenta que está incluida dentro del elemento **ExchangeImpersonation** .</span><span class="sxs-lookup"><span data-stu-id="682d5-133">When this element is present, the caller is trying to impersonate the account that is contained within the **ExchangeImpersonation** element.</span></span>  <br/> <span data-ttu-id="682d5-134">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="682d5-134">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="682d5-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="682d5-135">Remarks</span></span>

<span data-ttu-id="682d5-136">La cuenta que realiza la llamada debe tener la **ms-exch-impersonation** derecha en el servidor de acceso de cliente y el **ms-exch-MayImpersonate** derecho en ya sea la base de datos de buzón de correo que contiene el buzón de correo para suplantar o el usuario de Active Directory o contacto objeto.</span><span class="sxs-lookup"><span data-stu-id="682d5-136">The calling account must have the **ms-exch-impersonation** right on the Client Access server and the **ms-exch-MayImpersonate** right on either the mailbox database that contains the mailbox to impersonate or the Active Directory user or contact object.</span></span> 
  
<span data-ttu-id="682d5-137">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="682d5-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="682d5-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="682d5-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="682d5-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="682d5-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="682d5-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="682d5-140">Schema name</span></span>  <br/> |<span data-ttu-id="682d5-141">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="682d5-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="682d5-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="682d5-142">Validation file</span></span>  <br/> |<span data-ttu-id="682d5-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="682d5-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="682d5-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="682d5-144">Can be empty</span></span>  <br/> |<span data-ttu-id="682d5-145">False</span><span class="sxs-lookup"><span data-stu-id="682d5-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="682d5-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="682d5-146">See also</span></span>

- [<span data-ttu-id="682d5-147">Autorización de servidor a servidor en EWS</span><span class="sxs-lookup"><span data-stu-id="682d5-147">Server-to-server authorization in EWS</span></span>](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

