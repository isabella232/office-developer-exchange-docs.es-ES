---
title: UserId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UserId
api_type:
- schema
ms.assetid: 244af9e0-bf3c-46b4-8bfa-9719a1ed3107
description: El elemento UserId identifica un usuario delegado o un usuario que tiene permisos de acceso a carpetas.
ms.openlocfilehash: f03914745f8f7f47c64685b3e7c52eefece5ff6d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510760"
---
# <a name="userid"></a>UserId

El **elemento UserId** identifica un usuario delegado o un usuario que tiene permisos de acceso a carpetas. 
  
```xml
<UserId>
   <SID/>
   <PrimarySmtpAddress/>
   <DisplayName/>
   <DistinguishedUser/>
   <ExternalUserIdentity/>
</UserId>
```

 **UserIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SID](sid.md) <br/> |Representa el formato de lenguaje de definición de descriptor de seguridad (SDDL) del identificador de seguridad (SID).  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Representa la dirección principal del Protocolo simple de transferencia de correo (SMTP) de una cuenta que se usará para el acceso delegado.  <br/> |
|[DisplayName (cadena)](displayname-string.md) <br/> |Define el nombre para mostrar de una carpeta, contacto, lista de distribución o usuario delegado.  <br/> |
|[DistinguishedUser](distinguisheduser.md) <br/> |Identifica cuentas de usuario anónimas y predeterminadas para el acceso delegado.  <br/> |
|[ExternalUserIdentity](externaluseridentity.md) <br/> |Identifica un usuario delegado externo o un usuario externo que tiene permisos de acceso a carpetas.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DelegateUser](delegateuser.md) <br/> |Identifica un único delegado para agregar o actualizar en un buzón.  <br/> |
|[Permiso](permission.md) <br/> |Define el acceso que un usuario tiene a una carpeta.  <br/> |
|[CalendarPermission](calendarpermission.md) <br/> |Define el acceso que un usuario tiene a una carpeta Calendar.  <br/> |
|[UserIds](userids.md) <br/> |Contiene una matriz de usuarios delegados para obtener o quitar del buzón de una entidad de seguridad.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación AddDelegate](adddelegate-operation.md)
  
[Operación UpdateDelegate](updatedelegate-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Agregar delegados](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

