---
title: ContentLocation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContentLocation
api_type:
- schema
ms.assetid: d91cf587-24e3-4c13-8784-5ca29787cca7
description: El elemento ContentLocation contiene el identificador uniforme de recursos (URI) que corresponde a la ubicación del contenido de los datos adjuntos.
ms.openlocfilehash: 01bb95da5f620fddc8777f88b1d3eb1a7e6069b1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461488"
---
# <a name="contentlocation"></a>ContentLocation

El elemento **ContentLocation** contiene el identificador uniforme de recursos (URI) que corresponde a la ubicación del contenido de los datos adjuntos. 
  
```xml
<ContentLocation/>
```

 **String**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemAttachment](itemattachment.md) <br/> |Representa un elemento de Exchange que está adjunto a otro elemento de Exchange.  <br/> |
|[FileAttachment](fileattachment.md) <br/> |Representa un archivo que está adjunto a un elemento en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es un valor de cadena que representa un identificador URI.
  
## <a name="remarks"></a>Comentarios

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

