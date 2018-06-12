---
title: GetDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetDelegate
api_type:
- schema
ms.assetid: 6d5efe59-596f-46f8-bdc6-ca9cded9bb8e
description: El elemento GetDelegate define una solicitud para obtener información acerca de los delegados a un buzón de correo. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: e31d6bd4f4387094beb467fcc4dff31ca7ec5d62
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764803"
---
# <a name="getdelegate"></a>GetDelegate

El elemento **GetDelegate** define una solicitud para obtener información acerca de los delegados a un buzón de correo. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<GetDelegate IncludePermissions="">
      <Mailbox/>
   <UserIds/>
</GetDelegate>
```

 **GetDelegateType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**IncludePermissions** <br/> |Indica si la respuesta contiene la configuración de permisos para cada usuario delegado.  <br/> |
   
#### <a name="includepermissions-attribute-values"></a>Valores de atributo de IncludePermissions

|**Valor**|**Descripción**|
|:-----|:-----|
|**True** <br/> |Delegar permisos se devuelven además de la información del usuario delegado que se devuelve en el elemento [UserId](userid.md) del usuario.  <br/> |
|**False** <br/> |Se devuelve información de [UserId](userid.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Buzón de correo](mailbox.md) <br/> |Identifica el buzón de correo de la entidad de seguridad.  <br/> |
|[Identificadores de usuario](userids.md) <br/> |Contiene una matriz de delegado a los usuarios obtener desde el buzón de correo de una entidad de seguridad. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetDelegate](getdelegate-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

