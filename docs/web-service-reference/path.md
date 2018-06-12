---
title: Ruta de acceso
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Path
api_type:
- schema
ms.assetid: 5829149e-7bfe-4820-bcc6-910e9264acc9
description: El elemento de ruta de acceso es el tipo de esquema de base para todos los identificadores de propiedad. Este tipo es abstracto y no se producirá nunca directamente dentro de los documentos de instancia.
ms.openlocfilehash: a5a1ca5179ccf339e5a1f15621c92e2870f4f2d9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836700"
---
# <a name="path"></a>Ruta de acceso

El elemento de **ruta de acceso** es el tipo de esquema de base para todos los identificadores de propiedad. Este tipo es abstracto y no se producirá nunca directamente dentro de los documentos de instancia. 
  
```xml
<Path/>
```

 **BasePathToElementType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Observaciones

Los siguientes elementos se usan para sustituir para el elemento de **ruta de acceso** : 
  
- [FieldURI](fielduri.md)
    
- [IndexedFieldURI](indexedfielduri.md)
    
- [ExceptionFieldURI](exceptionfielduri.md)
    
- [ExtendedFieldURI](extendedfielduri.md)
    
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

