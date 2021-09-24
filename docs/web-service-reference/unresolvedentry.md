---
title: UnresolvedEntry
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UnresolvedEntry
api_type:
- schema
ms.assetid: 5ac6116a-3b24-40f8-a877-dbe9a6935919
description: El elemento UnresolvedEntry contiene el nombre de una lista de contactos o distribución que se debe resolver.
ms.openlocfilehash: 77074d5aed0a799d355fd176a8c9c06f2dffec5a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538676"
---
# <a name="unresolvedentry"></a>UnresolvedEntry

El **elemento UnresolvedEntry** contiene el nombre de una lista de contactos o distribución que se debe resolver. 
  
[ResolveNames](resolvenames.md)
  
[UnresolvedEntry](unresolvedentry.md)
  
```xml
<UnresolvedEntry/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ResolveNames](resolvenames.md) <br/> |Define una solicitud para resolver nombres ambiguos.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el nombre de un contacto público o una lista de distribución. La longitud mínima de la cadena es de un carácter.
  
## <a name="remarks"></a>Comentarios

El valor de texto de este elemento se usa para resolver nombres en los campos siguientes:
  
- Nombre
    
- Apellidos
    
- Nombre para mostrar
    
- Nombre completo
    
- Office
    
- Alias
    
- Dirección SMTP
    
Las direcciones de correo electrónico con tipos de enrutamiento con prefijo, como smtp o sip, se guardan en una matriz de varios valores. La [operación ResolveNames](resolvenames-operation.md) realiza una coincidencia parcial con cada valor de esa matriz cuando se agrega el tipo de enrutamiento al principio del nombre no resuelto, como "sip:User1@Contoso.com". Si no especifica un tipo de enrutamiento, la operación **ResolveNames** tendrá como valor predeterminado el tipo de enrutamiento smtp, lo coincidirá con una propiedad de dirección SMTP principal y no buscará en la matriz de varios valores. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación ResolveNames](resolvenames-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

