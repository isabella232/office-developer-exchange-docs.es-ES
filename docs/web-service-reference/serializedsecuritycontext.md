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
description: El elemento de SerializedSecurityContext se usa en el encabezado de protocolo de acceso de objeto Simple (SOAP) para la serialización de token de autenticación de servidor a servidor. No se admite la serialización de token.
ms.openlocfilehash: c5590551dc0780d918b05902e4f48fb9d1390b59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837363"
---
# <a name="serializedsecuritycontext"></a><span data-ttu-id="84fbe-104">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="84fbe-104">SerializedSecurityContext</span></span>

<span data-ttu-id="84fbe-105">El elemento de **SerializedSecurityContext** se usa en el encabezado de protocolo de acceso de objeto Simple (SOAP) para la serialización de token de autenticación de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="84fbe-105">The **SerializedSecurityContext** element is used in the Simple Object Access Protocol (SOAP) header for token serialization in server-to-server authentication.</span></span> <span data-ttu-id="84fbe-106">No se admite la serialización de token.</span><span class="sxs-lookup"><span data-stu-id="84fbe-106">Token serialization is not supported.</span></span> 
  
```xml
<SerializedSecurityContext>
   <UserSid/>
   <GroupSids/>
   <RestrictedGroupSids/>
   <PrimarySmtpAddress/>
</SerializedSecurityContext>
```

 <span data-ttu-id="84fbe-107">**SerializedSecurityContextType**</span><span class="sxs-lookup"><span data-stu-id="84fbe-107">**SerializedSecurityContextType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="84fbe-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="84fbe-108">Attributes and elements</span></span>

<span data-ttu-id="84fbe-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="84fbe-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84fbe-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="84fbe-110">Attributes</span></span>

<span data-ttu-id="84fbe-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="84fbe-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="84fbe-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="84fbe-112">Child elements</span></span>

|<span data-ttu-id="84fbe-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="84fbe-113">**Element**</span></span>|<span data-ttu-id="84fbe-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="84fbe-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84fbe-115">UserSid</span><span class="sxs-lookup"><span data-stu-id="84fbe-115">UserSid</span></span>](usersid.md) <br/> |<span data-ttu-id="84fbe-116">Representa el formato de idioma (SDDL) de definición de descriptor de seguridad del identificador de seguridad de usuario en un encabezado SOAP de contexto de seguridad serializado.</span><span class="sxs-lookup"><span data-stu-id="84fbe-116">Represents the security descriptor definition language (SDDL) form of the user security identifier in a serialized security context SOAP header.</span></span>  <br/> |
|[<span data-ttu-id="84fbe-117">GroupSids</span><span class="sxs-lookup"><span data-stu-id="84fbe-117">GroupSids</span></span>](groupsids.md) <br/> |<span data-ttu-id="84fbe-118">Representa una colección de identificadores de seguridad de objeto de grupo servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="84fbe-118">Represents a collection of Active Directory directory service group object security identifiers.</span></span>  <br/> |
|[<span data-ttu-id="84fbe-119">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="84fbe-119">RestrictedGroupSids</span></span>](restrictedgroupsids.md) <br/> |<span data-ttu-id="84fbe-120">Representa el identificador del grupo de seguridad y los atributos de un grupo restringido.</span><span class="sxs-lookup"><span data-stu-id="84fbe-120">Represents the group security identifier and attributes for a restricted group.</span></span>  <br/> |
|[<span data-ttu-id="84fbe-121">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="84fbe-121">PrimarySmtpAddress</span></span>](primarysmtpaddress.md) <br/> |<span data-ttu-id="84fbe-122">Representa la dirección de Protocolo Simple de transferencia de correo (SMTP) principal de una cuenta que se usará para la autorización de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="84fbe-122">Represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for server-to-server authorization.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="84fbe-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="84fbe-123">Parent elements</span></span>

<span data-ttu-id="84fbe-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="84fbe-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="84fbe-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84fbe-125">Remarks</span></span>

<span data-ttu-id="84fbe-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor (CAS) de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="84fbe-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server (CAS) role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="84fbe-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="84fbe-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84fbe-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="84fbe-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="84fbe-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="84fbe-129">Schema Name</span></span>  <br/> |<span data-ttu-id="84fbe-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="84fbe-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="84fbe-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="84fbe-131">Validation File</span></span>  <br/> |<span data-ttu-id="84fbe-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="84fbe-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="84fbe-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="84fbe-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="84fbe-134">False</span><span class="sxs-lookup"><span data-stu-id="84fbe-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84fbe-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="84fbe-135">See also</span></span>



- [<span data-ttu-id="84fbe-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="84fbe-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="84fbe-137">Autorización de servidor a servidor en EWS</span><span class="sxs-lookup"><span data-stu-id="84fbe-137">Server-to-server authorization in EWS</span></span>](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

