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
# <a name="serializedsecuritycontext"></a>SerializedSecurityContext

El elemento **SerializedSecurityContext** se usa en el encabezado del Protocolo simple de acceso a objetos (SOAP) para la serialización de tokens en la autenticación de servidor a servidor. No se admite la serialización de tokens. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UserSid](usersid.md) <br/> |Representa el formato de lenguaje de definición de descriptores de seguridad (SDDL) del identificador de seguridad de usuario en un encabezado SOAP de contexto de seguridad serializado.  <br/> |
|[GroupSids](groupsids.md) <br/> |Representa una colección de identificadores de seguridad de objetos de grupo del servicio de directorio de Active Directory.  <br/> |
|[RestrictedGroupSids](restrictedgroupsids.md) <br/> |Representa el identificador de seguridad de grupo y los atributos de un grupo restringido.  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Representa la dirección de Protocolo simple de transferencia de correo (SMTP) principal de una cuenta que se va a usar para la autorización de servidor a servidor.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor de acceso de cliente (CAS).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


[Autorización de servidor a servidor en EWS](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

