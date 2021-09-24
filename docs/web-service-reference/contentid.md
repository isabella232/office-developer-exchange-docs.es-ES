---
title: ContentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ContentId
api_type:
- schema
ms.assetid: bc59100d-6079-414b-a6e0-7c15feaa3184
description: El elemento ContentId representa un identificador del contenido de los datos adjuntos. ContentId se puede establecer en cualquier valor de cadena. Las aplicaciones pueden usar ContentId para implementar sus propios mecanismos de identificación.
ms.openlocfilehash: 786a76d312e4b8f276a9b5c7082754b873b0061c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519915"
---
# <a name="contentid"></a>ContentId

El **elemento ContentId** representa un identificador del contenido de los datos adjuntos. **ContentId** se puede establecer en cualquier valor de cadena. Las aplicaciones pueden usar **ContentId** para implementar sus propios mecanismos de identificación. 
  
```xml
<ContentId/>
```

 **String**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemAttachment](itemattachment.md) <br/> |Representa un Exchange que se adjunta a otro Exchange elemento.  <br/> |
|[FileAttachment](fileattachment.md) <br/> |Representa un archivo adjunto a un elemento del Exchange almacén.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de cadena representa el identificador del contenido de un archivo adjunto.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

