---
title: ParentItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ParentItemId
api_type:
- schema
ms.assetid: 72dc4391-72db-44d2-85d9-4718d59886a7
description: El elemento ParentItemId identifica el elemento primario que vincula a un archivo adjunto asociado.
ms.openlocfilehash: d8072e86d8bd989d4baf6b0f29385dc955b83de8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515365"
---
# <a name="parentitemid"></a>ParentItemId

El **elemento ParentItemId** identifica el elemento primario que vincula a un archivo adjunto asociado. 
  
- [CreateAttachment](createattachment.md)
  
- [ParentItemId](parentitemid.md)
  
```xml
<ParentItemId Id="" ChangeKey="" />
```

**ItemIdType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Id** <br/> |Identifica un único elemento del almacén de Exchange para asociarlo con datos adjuntos. Este valor es una cadena. Este atributo es obligatorio.  <br/> |
|**ChangeKey** <br/> |Identifica una versión no especificada de un elemento que se identifica mediante el atributo **Id** en el Exchange almacén. Esto se usa para asegurarse de que se usa un elemento actual cuando se actualiza con datos adjuntos. Este valor es una cadena. Este atributo es opcional.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CreateAttachment](createattachment.md) <br/> |Define una solicitud para crear datos adjuntos a un elemento en un buzón.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/CreateAttachment` <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento es necesario en la [operación CreateAttachment](createattachment-operation.md). Este elemento es básicamente el mismo que el [elemento ItemId.](itemid.md) 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |[https://schemas.microsoft.com/exchange/services/2006/messages](https://schemas.microsoft.com/exchange/services/2006/messages) <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación CreateAttachment](createattachment-operation.md)

