---
title: ParentItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentItemId
api_type:
- schema
ms.assetid: 72dc4391-72db-44d2-85d9-4718d59886a7
description: El elemento ParentItemId identifica el elemento primario que contiene vínculos a los datos adjuntos asociados.
ms.openlocfilehash: 9bd875ee5ead8b87996288a640e1bb14e3a5e8b8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836703"
---
# <a name="parentitemid"></a>ParentItemId

El elemento **ParentItemId** identifica el elemento primario que contiene vínculos a los datos adjuntos asociados. 
  
- [CreateAttachment](createattachment.md)
  
- [ParentItemId](parentitemid.md)
  
```xml
<ParentItemId Id="" ChangeKey="" />
```

**ItemIdType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**Id** <br/> |Identifica un elemento único en el almacén de Exchange para asociar con datos adjuntos. Este valor es una cadena. Este atributo es necesario.  <br/> |
|**ChangeKey** <br/> |Identifica una versión de un elemento que se identifica con el atributo **Id** en el almacén de Exchange no especificada. Esto se usa para asegurarse de que un elemento actual se usa cuando se actualizan con datos adjuntos. Este valor es una cadena. Este atributo es opcional.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CreateAttachment](createattachment.md) <br/> |Define una solicitud para crear un archivo adjunto a un elemento en un buzón de correo.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/CreateAttachment` <br/> |
   
## <a name="remarks"></a>Notas

Este elemento es necesario en la [operación CreateAttachment](createattachment-operation.md). Este elemento es básicamente el mismo que el elemento [ItemId](itemid.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |[http://schemas.microsoft.com/exchange/services/2006/messages](http://schemas.microsoft.com/exchange/services/2006/messages) <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación CreateAttachment](createattachment-operation.md)

