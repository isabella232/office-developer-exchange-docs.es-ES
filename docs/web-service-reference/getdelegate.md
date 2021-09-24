---
title: GetDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetDelegate
api_type:
- schema
ms.assetid: 6d5efe59-596f-46f8-bdc6-ca9cded9bb8e
description: El elemento GetDelegate define una solicitud para obtener información sobre delegados en un buzón. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 922a1d92856ba92abdc0fba717879b9a9e2687ef
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512971"
---
# <a name="getdelegate"></a>GetDelegate

El **elemento GetDelegate** define una solicitud para obtener información sobre delegados en un buzón. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<GetDelegate IncludePermissions="">
      <Mailbox/>
   <UserIds/>
</GetDelegate>
```

 **GetDelegateType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**IncludePermissions** <br/> |Indica si la respuesta contiene la configuración de permisos para cada usuario delegado.  <br/> |
   
#### <a name="includepermissions-attribute-values"></a>Valores de atributo IncludePermissions

|**Valor**|**Descripción**|
|:-----|:-----|
|**True** <br/> |Los permisos de usuario delegados se devuelven además de la información de usuario delegada que se devuelve en el [elemento UserId.](userid.md)  <br/> |
|**False** <br/> |[Se devuelve información de UserId.](userid.md)  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Buzón](mailbox.md) <br/> |Identifica el buzón de la entidad de seguridad.  <br/> |
|[UserIds](userids.md) <br/> |Contiene una matriz de usuarios delegados para obtener desde el buzón de una entidad de seguridad. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetDelegate](getdelegate-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

