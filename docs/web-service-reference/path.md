---
title: Ruta
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
description: El elemento path es el tipo de esquema base para todos los identificadores de propiedad. Este tipo es abstracto y nunca se producirá directamente en documentos de instancia.
ms.openlocfilehash: 5ba18084243e9720a76b9ac28023778c6d546bc4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529017"
---
# <a name="path"></a>Ruta

El elemento **path** es el tipo de esquema base para todos los identificadores de propiedad. Este tipo es abstracto y nunca se producirá directamente en documentos de instancia. 
  
```xml
<Path/>
```

 **BasePathToElementType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Los siguientes elementos se usan para sustituir al elemento **path** : 
  
- [FieldURI](fielduri.md)
    
- [IndexedFieldURI](indexedfielduri.md)
    
- [ExceptionFieldURI](exceptionfielduri.md)
    
- [ExtendedFieldURI](extendedfielduri.md)
    
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

