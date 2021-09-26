---
title: SharedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SharedFolderId
api_type:
- schema
ms.assetid: 21181ba3-9626-4284-9717-0b1c16948e8f
description: El elemento SharedFolderId representa el identificador de la carpeta compartida cuyo identificador de carpeta local debe devolver una solicitud de operación GetSharingFolder.
ms.openlocfilehash: 7e47ba49abed99bdb3cfd00eb43d2ef276d4ef37
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545975"
---
# <a name="sharedfolderid"></a>SharedFolderId

El **elemento SharedFolderId** representa el identificador de la carpeta compartida cuyo identificador de carpeta local debe devolver una solicitud de [operación GetSharingFolder.](getsharingfolder-operation.md) 
  
```xml
<SharedFolderId/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetSharingFolder](getsharingfolder.md) <br/> |Define una solicitud para obtener el identificador de carpeta local de una carpeta compartida especificada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es una cadena que representa el identificador de la carpeta compartida cuyo identificador de carpeta local debe devolver una solicitud de [operación GetSharingFolder.](getsharingfolder-operation.md) 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



[Operación GetSharingFolder](getsharingfolder-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

