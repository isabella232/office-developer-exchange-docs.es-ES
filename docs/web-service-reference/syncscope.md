---
title: SyncScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncScope
api_type:
- schema
ms.assetid: e0ca231f-0374-4844-8d4c-ada8da167920
description: El elemento SyncScope especifica si se devuelven sólo los elementos o elementos y la carpeta asociada información en una respuesta de sincronización.
ms.openlocfilehash: 847c0244a8847364e29ea584b0c0b721f00d3064
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840618"
---
# <a name="syncscope"></a>SyncScope

El elemento **SyncScope** especifica si se devuelven sólo los elementos o elementos y la carpeta asociada información en una respuesta de sincronización. 
  
```xml
<SyncScope>NormalItems or NormalAndAssociatedItems</SyncScope>
```

 **SyncFolderItemsScopeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[SyncFolderItems](syncfolderitems.md) <br/> |El elemento que define una solicitud para sincronizar los elementos en una carpeta de almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/> / SyncFolderItems  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumera los valores posibles para el elemento **SyncScope** . 
  
**Valores de elemento SyncScope**

|**Valor**|**Descripción**|
|:-----|:-----|
|NormalItems  <br/> |Especifica que sólo los elementos de la carpeta se devuelven en una respuesta de sincronización.  <br/> |
|NormalAndAssociatedItems  <br/> |Especifica que se devuelven ambos elementos en la carpeta y la información de la carpeta asociada en una respuesta de sincronización.  <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación SyncFolderItems](syncfolderitems-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

