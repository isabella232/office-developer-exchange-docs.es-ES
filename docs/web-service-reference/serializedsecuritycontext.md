---
title: SerializedSecurityContext
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SerializedSecurityContext
api_type:
- schema
ms.assetid: a02c4fc1-ed1a-40d9-a18e-6cfdae21a690
description: El elemento SerializedSecurityContext se usa en el encabezado SOAP (Protocolo simple de acceso a objetos) para la serialización de tokens en la autenticación de servidor a servidor. No se admite la serialización de tokens.
ms.openlocfilehash: 55fe752813fc2d7e3ed5416401ff46b5e00516e3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546045"
---
# <a name="serializedsecuritycontext"></a>SerializedSecurityContext

El **elemento SerializedSecurityContext** se usa en el encabezado SOAP (Protocolo simple de acceso a objetos) para la serialización de tokens en la autenticación de servidor a servidor. No se admite la serialización de tokens. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UserSid](usersid.md) <br/> |Representa el formato de lenguaje de definición de descriptor de seguridad (SDDL) del identificador de seguridad del usuario en un encabezado SOAP de contexto de seguridad serializado.  <br/> |
|[GroupSids](groupsids.md) <br/> |Representa una colección de identificadores de seguridad de objetos de grupo de servicio de directorio de Active Directory.  <br/> |
|[RestrictedGroupSids](restrictedgroupsids.md) <br/> |Representa el identificador de seguridad del grupo y los atributos de un grupo restringido.  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Representa la dirección principal del Protocolo simple de transferencia de correo (SMTP) de una cuenta que se usará para la autorización de servidor a servidor.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol servidor de acceso de cliente (CAS).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Autorización de servidor a servidor en EWS](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

