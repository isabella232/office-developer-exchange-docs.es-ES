---
title: AddBlankTargetToLinks
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 30180298-2501-4369-9b8f-2f7663f02336
description: El elemento AddBlankTargetToLinks especifica que el atributo de destino de los vínculos HTML se establece para abrir una nueva ventana.
ms.openlocfilehash: c8d7a5973e60e43638472b0da29842ce1caacc98
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543831"
---
# <a name="addblanktargettolinks"></a>AddBlankTargetToLinks

El **elemento AddBlankTargetToLinks** especifica que el atributo de destino de los vínculos HTML se establece para abrir una nueva ventana. 
  
```XML
<AddBlankTargetToLinks> true | false </AddBlankTargetToLinks>
```

**xs:Boolean**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> | Identifica las propiedades y el contenido del elemento que se incluirán en una respuesta **GetItem**, **FindItem**, **GetConversationItems** o **SyncFolderItems.**<br/><br/>  Las siguientes son las expresiones XPath de este elemento:<br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/>  `/GetConversationItems/ItemShape` <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento AddBlankTargetToLinks** indica que todos los vínculos HTML se establecerán para abrir una nueva ventana. Un valor de **false** indica que los vínculos HTML se abrirán en la ventana actual. 
  
## <a name="remarks"></a>Comentarios

Este elemento es opcional.
  
Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Consulte también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

