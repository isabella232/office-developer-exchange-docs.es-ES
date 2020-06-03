---
title: RootItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootItemId
api_type:
- schema
ms.assetid: f613c705-17ce-48ce-aa64-4dc2cea25e31
description: El elemento RootItemId identifica el elemento raíz de los datos adjuntos eliminados.
ms.openlocfilehash: d8badd465fd5a93e1a6354d55ac5c4b080897152
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457098"
---
# <a name="rootitemid"></a>RootItemId

El elemento **RootItemId** identifica el elemento raíz de los datos adjuntos eliminados. 
  
[DeleteAttachmentResponse](deleteattachmentresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md)
  
[RootItemId](rootitemid.md)
  
```xml
<RootItemId RootItemId="" RootItemChangeKey="" />
```

 **RootItemIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**RootItemId** <br/> |Identifica el elemento raíz de un dato adjunto eliminado.  <br/> |
|**RootItemChangeKey** <br/> |Identifica la nueva clave de cambio del elemento raíz de un archivo adjunto eliminado.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud DeleteAttachment.  <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento **RootItemId** solo se usa en respuestas DeleteAttachment. Esto identifica el identificador del elemento raíz y, lo que es más importante, la nueva clave de cambio para el elemento primario. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[DeleteAttachment](deleteattachment.md)
  
[Operación DeleteAttachment](deleteattachment-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

