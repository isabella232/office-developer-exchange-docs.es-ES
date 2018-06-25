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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837363"
---
# <a name="serializedsecuritycontext"></a>SerializedSecurityContext

El elemento de **SerializedSecurityContext** se usa en el encabezado de protocolo de acceso de objeto Simple (SOAP) para la serialización de token de autenticación de servidor a servidor. No se admite la serialización de token. 
  
```xml
<SerializedSecurityContext>
   <UserSid/>
   <GroupSids/>
   <RestrictedGroupSids/>
   <PrimarySmtpAddress/>
</SerializedSecurityContext>
```

 **SerializedSecurityContextType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[UserSid](usersid.md) <br/> |Representa el formato de idioma (SDDL) de definición de descriptor de seguridad del identificador de seguridad de usuario en un encabezado SOAP de contexto de seguridad serializado.  <br/> |
|[GroupSids](groupsids.md) <br/> |Representa una colección de identificadores de seguridad de objeto de grupo servicio de directorio de Active Directory.  <br/> |
|[RestrictedGroupSids](restrictedgroupsids.md) <br/> |Representa el identificador del grupo de seguridad y los atributos de un grupo restringido.  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Representa la dirección de Protocolo Simple de transferencia de correo (SMTP) principal de una cuenta que se usará para la autorización de servidor a servidor.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor (CAS) de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


[Autorización de servidor a servidor en EWS](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

