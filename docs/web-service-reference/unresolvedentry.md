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
description: El elemento UnresolvedEntry contiene el nombre de un contacto o una lista de distribución para resolverlos.
ms.openlocfilehash: 0f157c1be6c327187456a795c4c1000b8c35b620
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459843"
---
# <a name="unresolvedentry"></a>UnresolvedEntry

El elemento **UnresolvedEntry** contiene el nombre de un contacto o una lista de distribución para resolverlos. 
  
[ResolveNames](resolvenames.md)
  
[UnresolvedEntry](unresolvedentry.md)
  
```xml
<UnresolvedEntry/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ResolveNames](resolvenames.md) <br/> |Define una solicitud para resolver nombres ambiguos.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el nombre de un contacto público o una lista de distribución. La longitud mínima de la cadena es un carácter.
  
## <a name="remarks"></a>Comentarios

El valor de texto de este elemento se usa para resolver nombres con los siguientes campos:
  
- Nombre
    
- Apellidos
    
- Nombre completo (DN)
    
- Nombre completo
    
- Office
    
- Alias
    
- Dirección SMTP
    
Las direcciones de correo electrónico con tipos de enrutamiento prefijados, como SMTP o SIP, se guardan en una matriz de varios valores. La [operación ResolveNames](resolvenames-operation.md) realiza una coincidencia parcial con cada valor de la matriz cuando se agrega el tipo de enrutamiento al principio del nombre sin resolver, como "SIP:user1@Contoso.com". Si no especifica un tipo de enrutamiento, la operación **ResolveNames** se establecerá de forma predeterminada en el tipo de enrutamiento de SMTP, lo hará coincidir con una propiedad de dirección SMTP principal y no buscará en la matriz de varios valores. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación ResolveNames](resolvenames-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

