---
title: UnresolvedEntry
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnresolvedEntry
api_type:
- schema
ms.assetid: 5ac6116a-3b24-40f8-a877-dbe9a6935919
description: El elemento UnresolvedEntry contiene el nombre de un contacto o lista de distribución para resolver.
ms.openlocfilehash: 98b447cd49685b49f73f75f12d921a65749be245
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840788"
---
# <a name="unresolvedentry"></a>UnresolvedEntry

El elemento **UnresolvedEntry** contiene el nombre de un contacto o lista de distribución para resolver. 
  
[ResolveNames](resolvenames.md)
  
[UnresolvedEntry](unresolvedentry.md)
  
```xml
<UnresolvedEntry/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ResolveNames](resolvenames.md) <br/> |Define una solicitud para resolver nombres ambiguos.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el nombre de una lista de contactos o de distribución pública. La longitud mínima de la cadena es un carácter.
  
## <a name="remarks"></a>Notas

El valor de texto de este elemento se utiliza para resolver nombres de los campos siguientes:
  
- Nombre propio
    
- Apellido
    
- Nombre para mostrar
    
- Nombre completo
    
- Office
    
- Alias
    
- dirección SMTP
    
Direcciones de correo electrónico con tipos de enrutamiento de prefijo, como smtp o sip, se guardan en una matriz con varios valores. La [operación ResolveNames](resolvenames-operation.md) lleva a cabo a una coincidencia parcial con respecto a cada valor de dicha matriz al agregar el tipo de distribución al principio del nombre sin resolver, como "sip:User1@Contoso.com". Si no especifica un tipo de enrutamiento, la operación **ResolveNames** de forma predeterminada en el tipo de distribución de smtp, match a una propiedad de dirección SMTP principal y no buscar en la matriz con varios valores. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación ResolveNames](resolvenames-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

