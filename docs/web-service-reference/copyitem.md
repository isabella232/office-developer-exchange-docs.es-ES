---
title: CopyItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CopyItem
api_type:
- schema
ms.assetid: ffb4c13e-e7ea-4e6b-87a0-509ce5371100
description: El elemento CopyItem define una solicitud para copiar un elemento en un buzón del Exchange almacén.
ms.openlocfilehash: 7f083f09a587b4788180711039e1cfdbbe6a10cd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529179"
---
# <a name="copyitem"></a>CopyItem

El **elemento CopyItem** define una solicitud para copiar un elemento en un buzón en el Exchange almacén. 
  
```XML
<CopyItem>
   <ToFolderId/>
   <ItemIds/>
   <ReturnNewItemIds/>
</CopyItem>
```

 **CopyItemType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ToFolderId](tofolderid.md) <br/> |Representa la carpeta de destino de un elemento copiado.  <br/> |
|[ItemIds](itemids.md) <br/> |Contiene una matriz de elementos identificados que se copian en la carpeta representada por el [elemento ToFolderId.](tofolderid.md)  <br/> |
|[ReturnNewItemIds](returnnewitemids.md) <br/> |Indica si los identificadores de elementos nuevos se devuelven en la respuesta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación CopyItem](copyitem-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

