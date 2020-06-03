---
title: base64FolderId (servicio Web de mensajería unificada)
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
description: El elemento base64FolderId contiene el identificador de la carpeta que se va a especificar como carpeta de correo electrónico predeterminada desde la que la mensajería unificada Lee los mensajes a través del teléfono en una solicitud SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada).
ms.openlocfilehash: ea31c7a0f93188e563bf95c4a3e6e91f0866746c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458050"
---
# <a name="base64folderid-um-web-service"></a>base64FolderId (servicio Web de mensajería unificada)

El elemento **base64FolderId** contiene el identificador de la carpeta que se va a especificar como carpeta de correo electrónico predeterminada desde la que la mensajería unificada Lee los mensajes a través del teléfono en una solicitud [SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)](settelephoneaccessfolderemail-operation-um-web-service.md) . 
  
[SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)](settelephoneaccessfolderemail-um-web-service.md)
  
[base64FolderId (servicio Web de mensajería unificada)](base64folderid-um-web-service.md)
  
```xml
<base64FolderId/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)](settelephoneaccessfolderemail-um-web-service.md) <br/> |Define la solicitud para establecer la carpeta de correo electrónico de acceso telefónico.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor de texto representa el identificador MAPI de la carpeta.
  
## <a name="remarks"></a>Comentarios

Para establecer la carpeta de correo electrónico de acceso telefónico, use la [operación SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)](settelephoneaccessfolderemail-operation-um-web-service.md).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)](settelephoneaccessfolderemail-um-web-service.md)
  
[Operación SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)](settelephoneaccessfolderemail-operation-um-web-service.md)
  
[Operación FindFolder](findfolder-operation.md)
  
[Operación FindItem](finditem-operation.md)

