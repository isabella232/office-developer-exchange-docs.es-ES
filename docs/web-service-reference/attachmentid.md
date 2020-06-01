---
title: AttachmentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentId
api_type:
- schema
ms.assetid: 55a5fd77-60d1-40fa-8144-770600cedc6a
description: El elemento AttachmentId identifica un elemento o datos adjuntos de archivo. Este elemento se usa en las respuestas de CreateAttachment.
ms.openlocfilehash: b5dc9299b615f0fc01b8afcbaabf0ec7996e53d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459114"
---
# <a name="attachmentid"></a>AttachmentId

El elemento **AttachmentId** identifica un elemento o datos adjuntos de archivo. Este elemento se usa en las respuestas de CreateAttachment. 
  
```xml
<AttachmentId Id="" RootItemId="" RootItemChangeKey="" />
```

 **AttachmentIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Id** <br/> |Identifica el identificador único de los datos adjuntos.  <br/> |
|**RootItemId** <br/> |Identifica el identificador único del elemento de almacén raíz al que se adjuntan los datos adjuntos.  <br/> |
|**RootItemChangeKey** <br/> |Identifica la clave de cambio del elemento de almacén raíz al que se adjuntan los datos adjuntos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemAttachment](itemattachment.md) <br/> |Representa un elemento de Exchange que está adjunto a otro elemento de Exchange.  <br/> |
|[FileAttachment](fileattachment.md) <br/> |Representa un archivo que está adjunto a un elemento en el almacén de Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

Es importante tener en cuenta que cuando se crea un archivo adjunto, se modifica la clave de cambio del elemento raíz.
  
El elemento [AttachmentId (GetAttachment y DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md) se usa en solicitudes DeleteAttachment y GetAttachment. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

