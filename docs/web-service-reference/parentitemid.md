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
description: El elemento ParentItemId identifica el elemento primario que se vincula a un dato adjunto asociado.
ms.openlocfilehash: 4f3e33da0af2438948313f0e335cd03e076d135a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465747"
---
# <a name="parentitemid"></a>ParentItemId

El elemento **ParentItemId** identifica el elemento primario que se vincula a un dato adjunto asociado. 
  
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
|**Id** <br/> |Identifica un solo elemento del almacén de Exchange para asociarlo a datos adjuntos. Este valor es una cadena. Este atributo es obligatorio.  <br/> |
|**ChangeKey** <br/> |Identifica una versión no especificada de un elemento que se identifica mediante el atributo **ID** en el almacén de Exchange. Se usa para asegurarse de que se usa un elemento actual cuando se actualiza con datos adjuntos. Este valor es una cadena. Este atributo es opcional.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CreateAttachment](createattachment.md) <br/> |Define una solicitud para crear datos adjuntos a un elemento en un buzón.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/CreateAttachment` <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento es obligatorio en la [operación CreateAttachment](createattachment-operation.md). Este elemento es básicamente el mismo que el elemento [Itemid](itemid.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |[https://schemas.microsoft.com/exchange/services/2006/messages](https://schemas.microsoft.com/exchange/services/2006/messages) <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación CreateAttachment](createattachment-operation.md)

