---
title: Ignore
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Ignore
api_type:
- schema
ms.assetid: 7789eec5-ceec-43f2-84d5-d0d15b734076
description: El elemento ignore identifica los elementos que se deben omitir durante la sincronización.
ms.openlocfilehash: b65d11d8c7655279dac0e7d3cbd13f8a9317540c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458575"
---
# <a name="ignore"></a>Ignore

El elemento **Ignore** identifica los elementos que se deben omitir durante la sincronización. 
  
[SyncFolderItems](syncfolderitems.md)
  
[Ignore](ignore.md)
  
```xml
<Ignore>
   <ItemId/>
</Ignore>
```

 **ArrayOfBaseItemIdsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SyncFolderItems](syncfolderitems.md) <br/> |Define una solicitud para sincronizar elementos en una carpeta de almacén de Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
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

