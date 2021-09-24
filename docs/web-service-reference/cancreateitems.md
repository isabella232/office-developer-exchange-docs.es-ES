---
title: CanCreateItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CanCreateItems
api_type:
- schema
ms.assetid: c4574e9a-3c42-40a1-a5f9-79b6560e9b30
description: El elemento CanCreateItems indica si un usuario tiene permiso para crear elementos en una carpeta. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: b2d426e103bf50536d72c47d9fc62d062847e62f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526739"
---
# <a name="cancreateitems"></a>CanCreateItems

El **elemento CanCreateItems** indica si un usuario tiene permiso para crear elementos en una carpeta. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<CanCreateItems/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Permiso](permission.md) <br/> |Define el acceso que un usuario tiene a una carpeta. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[CalendarPermission](calendarpermission.md) <br/> |Define el acceso que un usuario tiene a una carpeta Calendar. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** indica que el usuario puede crear elementos en la carpeta. Un valor de **false** indica que el usuario no puede crear elementos en la carpeta. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Configuración Folder-Level permisos](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

