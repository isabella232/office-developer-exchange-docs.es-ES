---
title: base64FolderId (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- base64FolderId
api_type:
- schema
ms.assetid: 662f8f2f-49a7-4c7a-9065-98a02a49cfcd
description: El elemento base64FolderId contiene el identificador de la carpeta para especificar como la carpeta de correo electrónico predeterminada desde la que mensajería unificada lee los mensajes a través del teléfono en una solicitud de SetTelephoneAccessFolderEmail operación (servicio web de mensajería unificada).
ms.openlocfilehash: 7d710542418a717c6fcad243a22682e5840ebbd2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763604"
---
# <a name="base64folderid-um-web-service"></a>base64FolderId (servicio web de mensajería unificada)

El elemento **base64FolderId** contiene el identificador de la carpeta para especificar como la carpeta de correo electrónico predeterminada desde la que mensajería unificada lee los mensajes a través del teléfono en una solicitud de [operación SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)](settelephoneaccessfolderemail-operation-um-web-service.md) . 
  
[SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)](settelephoneaccessfolderemail-um-web-service.md)
  
[base64FolderId (servicio web de mensajería unificada)](base64folderid-um-web-service.md)
  
```xml
<base64FolderId/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)](settelephoneaccessfolderemail-um-web-service.md) <br/> |Define la solicitud para establecer la carpeta de correo electrónico de acceso telefónico.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor de texto representa el identificador de MAPI de la carpeta.
  
## <a name="remarks"></a>Comentarios

Para establecer la carpeta de correo electrónico de acceso telefónico, use la [operación de SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)](settelephoneaccessfolderemail-operation-um-web-service.md).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)](settelephoneaccessfolderemail-um-web-service.md)
  
[Operación SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)](settelephoneaccessfolderemail-operation-um-web-service.md)
  
[Operación FindFolder](findfolder-operation.md)
  
[Operación FindItem](finditem-operation.md)

