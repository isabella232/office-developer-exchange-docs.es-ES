---
title: AddBlankTargetToLinks
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 30180298-2501-4369-9b8f-2f7663f02336
description: El elemento AddBlankTargetToLinks especifica que el atributo de destino en vínculos HTML está configurado para abrir una nueva ventana.
ms.openlocfilehash: 1d4d36c1f4b98ebee96baea683c40527d2a9ec27
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465046"
---
# <a name="addblanktargettolinks"></a>AddBlankTargetToLinks

El elemento **AddBlankTargetToLinks** especifica que el atributo de destino en vínculos HTML está configurado para abrir una nueva ventana. 
  
```XML
<AddBlankTargetToLinks> true | false </AddBlankTargetToLinks>
```

**XS: Boolean**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> | Identifica las propiedades de elemento y el contenido que se incluirá en una respuesta de **GetItem**, **FindItem**, **GetConversationItems** o **SyncFolderItems** .<br/><br/>  Las siguientes son las expresiones XPath de este elemento:<br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/>  `/GetConversationItems/ItemShape` <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** para el elemento **AddBlankTargetToLinks** indica que se establecerán todos los vínculos HTML para abrir una nueva ventana. Un valor de **false** indica que los vínculos HTML se abrirán en la ventana actual. 
  
## <a name="remarks"></a>Comentarios

Este elemento es opcional.
  
Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

