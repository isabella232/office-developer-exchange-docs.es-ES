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
description: El elemento SyncScope especifica si solo los elementos o elementos y la información asociada a la carpeta se devuelven en una respuesta de sincronización.
ms.openlocfilehash: 5ede26204c823a452189222075c784f24e98d188
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463037"
---
# <a name="syncscope"></a>SyncScope

El elemento **SyncScope** especifica si solo los elementos o elementos y la información asociada a la carpeta se devuelven en una respuesta de sincronización. 
  
```xml
<SyncScope>NormalItems or NormalAndAssociatedItems</SyncScope>
```

 **SyncFolderItemsScopeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SyncFolderItems](syncfolderitems.md) <br/> |Elemento que define una solicitud para sincronizar elementos en una carpeta de almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:  <br/> /SyncFolderItems  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumeran los valores posibles para el elemento **SyncScope** . 
  
**Valores del elemento SyncScope**

|**Valor**|**Descripción**|
|:-----|:-----|
|NormalItems  <br/> |Especifica que sólo los elementos de la carpeta se devuelven en una respuesta de sincronización.  <br/> |
|NormalAndAssociatedItems  <br/> |Especifica que ambos elementos de la carpeta y la información asociada a la carpeta se devuelven en una respuesta de sincronización.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación SyncFolderItems](syncfolderitems-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

