---
title: base64FolderId (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- base64FolderId
api_type:
- schema
ms.assetid: 662f8f2f-49a7-4c7a-9065-98a02a49cfcd
description: El elemento base64FolderId contiene el identificador de la carpeta que se va a especificar como carpeta de correo electrónico predeterminada desde la que la mensajería unificada lee mensajes por teléfono en una solicitud de operación SetTelephoneAccessFolderEmail (servicio web de mensajería unificada).
ms.openlocfilehash: 149ad55d0ab09f57b0dc3ace7eb0e17c96265e3f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518941"
---
# <a name="base64folderid-um-web-service"></a>base64FolderId (servicio web de mensajería unificada)

El **elemento base64FolderId** contiene el identificador de la carpeta que se va a especificar como carpeta de correo electrónico predeterminada desde la que la mensajería unificada lee mensajes por teléfono en una solicitud de operación [SetTelephoneAccessFolderEmail (servicio web](settelephoneaccessfolderemail-operation-um-web-service.md) de mensajería unificada). 
  
[SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)](settelephoneaccessfolderemail-um-web-service.md)
  
[base64FolderId (servicio web de mensajería unificada)](base64folderid-um-web-service.md)
  
```xml
<base64FolderId/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)](settelephoneaccessfolderemail-um-web-service.md) <br/> |Define la solicitud para establecer la carpeta de correo electrónico de acceso telefónico.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor de texto representa el identificador MAPI de la carpeta.
  
## <a name="remarks"></a>Comentarios

Para establecer la carpeta de correo electrónico de acceso telefónico, use la [operación SetTelephoneAccessFolderEmail (servicio web de](settelephoneaccessfolderemail-operation-um-web-service.md)mensajería unificada).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)](settelephoneaccessfolderemail-um-web-service.md)
  
[Operación SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)](settelephoneaccessfolderemail-operation-um-web-service.md)
  
[Operación FindFolder](findfolder-operation.md)
  
[Operación FindItem](finditem-operation.md)

