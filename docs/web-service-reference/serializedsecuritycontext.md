---
title: SerializedSecurityContext
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SerializedSecurityContext
api_type:
- schema
ms.assetid: a02c4fc1-ed1a-40d9-a18e-6cfdae21a690
description: El elemento SerializedSecurityContext se usa en el encabezado del Protocolo simple de acceso a objetos (SOAP) para la serialización de tokens en la autenticación de servidor a servidor. No se admite la serialización de tokens.
ms.openlocfilehash: 58fea1c7f613315d59e81935561f92f318afc769
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462055"
---
# <a name="serializedsecuritycontext"></a><span data-ttu-id="04136-104">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="04136-104">SerializedSecurityContext</span></span>

<span data-ttu-id="04136-105">El elemento **SerializedSecurityContext** se usa en el encabezado del Protocolo simple de acceso a objetos (SOAP) para la serialización de tokens en la autenticación de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="04136-105">The **SerializedSecurityContext** element is used in the Simple Object Access Protocol (SOAP) header for token serialization in server-to-server authentication.</span></span> <span data-ttu-id="04136-106">No se admite la serialización de tokens.</span><span class="sxs-lookup"><span data-stu-id="04136-106">Token serialization is not supported.</span></span> 
  
```xml
<SerializedSecurityContext>
   <UserSid/>
   <GroupSids/>
   <RestrictedGroupSids/>
   <PrimarySmtpAddress/>
</SerializedSecurityContext>
```

 <span data-ttu-id="04136-107">**SerializedSecurityContextType**</span><span class="sxs-lookup"><span data-stu-id="04136-107">**SerializedSecurityContextType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="04136-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="04136-108">Attributes and elements</span></span>

<span data-ttu-id="04136-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="04136-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04136-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="04136-110">Attributes</span></span>

<span data-ttu-id="04136-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="04136-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="04136-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="04136-112">Child elements</span></span>

|<span data-ttu-id="04136-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="04136-113">**Element**</span></span>|<span data-ttu-id="04136-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="04136-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="04136-115">UserSid</span><span class="sxs-lookup"><span data-stu-id="04136-115">UserSid</span></span>](usersid.md) <br/> |<span data-ttu-id="04136-116">Representa el formato de lenguaje de definición de descriptores de seguridad (SDDL) del identificador de seguridad de usuario en un encabezado SOAP de contexto de seguridad serializado.</span><span class="sxs-lookup"><span data-stu-id="04136-116">Represents the security descriptor definition language (SDDL) form of the user security identifier in a serialized security context SOAP header.</span></span>  <br/> |
|[<span data-ttu-id="04136-117">GroupSids</span><span class="sxs-lookup"><span data-stu-id="04136-117">GroupSids</span></span>](groupsids.md) <br/> |<span data-ttu-id="04136-118">Representa una colección de identificadores de seguridad de objetos de grupo del servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="04136-118">Represents a collection of Active Directory directory service group object security identifiers.</span></span>  <br/> |
|[<span data-ttu-id="04136-119">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="04136-119">RestrictedGroupSids</span></span>](restrictedgroupsids.md) <br/> |<span data-ttu-id="04136-120">Representa el identificador de seguridad de grupo y los atributos de un grupo restringido.</span><span class="sxs-lookup"><span data-stu-id="04136-120">Represents the group security identifier and attributes for a restricted group.</span></span>  <br/> |
|[<span data-ttu-id="04136-121">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="04136-121">PrimarySmtpAddress</span></span>](primarysmtpaddress.md) <br/> |<span data-ttu-id="04136-122">Representa la dirección de Protocolo simple de transferencia de correo (SMTP) principal de una cuenta que se va a usar para la autorización de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="04136-122">Represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for server-to-server authorization.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="04136-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="04136-123">Parent elements</span></span>

<span data-ttu-id="04136-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="04136-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="04136-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04136-125">Remarks</span></span>

<span data-ttu-id="04136-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor de acceso de cliente (CAS).</span><span class="sxs-lookup"><span data-stu-id="04136-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server (CAS) role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="04136-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="04136-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04136-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="04136-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="04136-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="04136-129">Schema Name</span></span>  <br/> |<span data-ttu-id="04136-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="04136-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="04136-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="04136-131">Validation File</span></span>  <br/> |<span data-ttu-id="04136-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="04136-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="04136-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="04136-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="04136-134">Falso</span><span class="sxs-lookup"><span data-stu-id="04136-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="04136-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="04136-135">See also</span></span>



- [<span data-ttu-id="04136-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="04136-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="04136-137">Autorización de servidor a servidor en EWS</span><span class="sxs-lookup"><span data-stu-id="04136-137">Server-to-server authorization in EWS</span></span>](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

