---
title: SharedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharedFolderId
api_type:
- schema
ms.assetid: 21181ba3-9626-4284-9717-0b1c16948e8f
description: El elemento SharedFolderId representa el identificador de la carpeta compartida cuyo identificador de carpeta local debe ser devuelto por una solicitud de operación GetSharingFolder.
ms.openlocfilehash: 546e148540708725bcf335f39bf69d193124d210
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466125"
---
# <a name="sharedfolderid"></a>SharedFolderId

El elemento **SharedFolderId** representa el identificador de la carpeta compartida cuyo identificador de carpeta local debe ser devuelto por una solicitud de [operación GetSharingFolder](getsharingfolder-operation.md) . 
  
```xml
<SharedFolderId/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetSharingFolder](getsharingfolder.md) <br/> |Define una solicitud para obtener el identificador de carpeta local de una carpeta compartida especificada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es una cadena que representa el identificador de la carpeta compartida cuyo identificador de carpeta local debe ser devuelto por una solicitud de [operación GetSharingFolder](getsharingfolder-operation.md) . 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetSharingFolder](getsharingfolder-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

