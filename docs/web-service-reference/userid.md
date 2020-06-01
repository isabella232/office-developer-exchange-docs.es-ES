---
title: UserId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserId
api_type:
- schema
ms.assetid: 244af9e0-bf3c-46b4-8bfa-9719a1ed3107
description: El elemento UserId identifica un usuario delegado o un usuario que tiene permisos de acceso a la carpeta.
ms.openlocfilehash: 68075e335383835ddce9575d85ba5fa945ed305c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455544"
---
# <a name="userid"></a>UserId

El elemento **userid** identifica un usuario delegado o un usuario que tiene permisos de acceso a la carpeta. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SID](sid.md) <br/> |Representa el formato de lenguaje de definición de descriptores de seguridad (SDDL) del identificador de seguridad (SID).  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Representa la dirección de Protocolo simple de transferencia de correo (SMTP) principal de una cuenta que se va a usar para el acceso delegado.  <br/> |
|[DisplayName (cadena)](displayname-string.md) <br/> |Define el nombre para mostrar de una carpeta, un contacto, una lista de distribución o un usuario delegado.  <br/> |
|[DistinguishedUser](distinguisheduser.md) <br/> |Identifica cuentas de usuario anónimas y predeterminadas para el acceso delegado.  <br/> |
|[ExternalUserIdentity](externaluseridentity.md) <br/> |Identifica un usuario delegado externo o un usuario externo que tiene permisos de acceso a la carpeta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DelegateUser](delegateuser.md) <br/> |Identifica un único delegado para agregar o actualizar en un buzón.  <br/> |
|[Permiso](permission.md) <br/> |Define el acceso que un usuario tiene a una carpeta.  <br/> |
|[CalendarPermission](calendarpermission.md) <br/> |Define el acceso que tiene un usuario a una carpeta de calendario.  <br/> |
|[UserIds](userids.md) <br/> |Contiene una matriz de usuarios delegados para obtener o quitar del buzón de la entidad de la identidad.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación AddDelegate](adddelegate-operation.md)
  
[Operación UpdateDelegate](updatedelegate-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


[Adición de delegados](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

