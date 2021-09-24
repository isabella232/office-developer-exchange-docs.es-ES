---
title: ReturnNewItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: aeef79e4-31e1-4213-b627-9bac676be018
description: El elemento ReturnNewItemIds indica si los identificadores de elementos nuevos se devuelven en la respuesta.
ms.openlocfilehash: 93ff4e37c56c3583e81711ba7e3582706d9ef940
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512383"
---
# <a name="returnnewitemids"></a>ReturnNewItemIds

El **elemento ReturnNewItemIds** indica si los identificadores de elementos nuevos se devuelven en la respuesta. 
  
```XML
<ReturnNewItemIds/>
```

 **xs:boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CopyItem](copyitem.md) <br/> |Define una solicitud para copiar un elemento en un buzón en el Exchange almacén.  <br/> |
|[MoveItem](moveitem.md) <br/> |Define una solicitud para mover un elemento en el Exchange almacén.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento ReturnNewItemIds** indica que los nuevos identificadores de elemento se devuelven en la respuesta. Un valor de **false** indica que los nuevos identificadores de elemento no se devuelven en la respuesta. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Web Services.Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   

