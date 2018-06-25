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
description: El elemento UserId identifica un usuario delegado o un usuario que tiene permisos de acceso de la carpeta.
ms.openlocfilehash: 8e9867f5a8cdd62dd2dae55fbf527595ac14f46d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840909"
---
# <a name="userid"></a>UserId

El elemento **UserId** identifica un usuario delegado o un usuario que tiene permisos de acceso de la carpeta. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[SID](sid.md) <br/> |Representa el formato de idioma (SDDL) de definición de descriptor de seguridad del identificador de seguridad (SID).  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Representa la dirección de Protocolo Simple de transferencia de correo (SMTP) principal de una cuenta que se utilizará para el acceso de delegado.  <br/> |
|[DisplayName (cadena)](displayname-string.md) <br/> |Define el nombre para mostrar de una carpeta, contacto, lista de distribución o un usuario delegado.  <br/> |
|[DistinguishedUser](distinguisheduser.md) <br/> |Identifica las cuentas de usuario anónimo y predeterminado para el acceso de delegado.  <br/> |
|[ExternalUserIdentity](externaluseridentity.md) <br/> |Identifica un usuario delegado externo o un usuario externo que tiene permisos de acceso de la carpeta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[UsuarioDelegado](delegateuser.md) <br/> |Identifica un único delegado para agregar o actualizar en un buzón de correo.  <br/> |
|[Permission](permission.md) <br/> |Define el acceso que tiene un usuario a una carpeta.  <br/> |
|[CalendarPermission](calendarpermission.md) <br/> |Define el acceso que tiene un usuario a una carpeta de calendario.  <br/> |
|[Identificadores de usuario](userids.md) <br/> |Contiene una matriz de delegado a los usuarios obtener o quitar de buzón de una entidad de seguridad.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación AddDelegate](adddelegate-operation.md)
  
[Operación UpdateDelegate](updatedelegate-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


[Adición de delegados](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

