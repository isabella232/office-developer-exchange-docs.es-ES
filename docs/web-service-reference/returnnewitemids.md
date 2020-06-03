---
title: ReturnNewItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aeef79e4-31e1-4213-b627-9bac676be018
description: El elemento ReturnNewItemIds indica si los identificadores de elemento de los elementos nuevos se devuelven en la respuesta.
ms.openlocfilehash: 003676c4c034454aa551e42bf3af976183117b8c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465117"
---
# <a name="returnnewitemids"></a>ReturnNewItemIds

El elemento **ReturnNewItemIds** indica si los identificadores de elemento de los elementos nuevos se devuelven en la respuesta. 
  
```XML
<ReturnNewItemIds/>
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
|[CopyItem](copyitem.md) <br/> |Define una solicitud para copiar un elemento en un buzón de correo en el almacén de Exchange.  <br/> |
|[MoveItem](moveitem.md) <br/> |Define una solicitud para mover un elemento en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** para el elemento **ReturnNewItemIds** indica que los nuevos identificadores de elemento se devuelven en la respuesta. Un valor de **false** indica que los nuevos identificadores de elemento no se devuelven en la respuesta. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   

