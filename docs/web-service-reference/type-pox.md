---
title: Type (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 9a627244-554f-4223-b9d8-a601b81a4a1a
description: El elemento Type identifica el tipo de la cuenta de correo configurada.
ms.openlocfilehash: bb92913071509fec46736341bce56b1a00730f6b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517528"
---
# <a name="type-pox"></a>Type (POX)

El **elemento Type** identifica el tipo de la cuenta de correo configurada. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[Type (POX)](type-pox.md)
  
```XML
<Type>WEB or EXCH or EXPR or EXHTTP</Type>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al Exchange servidor.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el tipo de cuenta de correo. En la tabla siguiente se enumeran los valores posibles.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|EXCH  <br/> |El protocolo que se usa para conectarse al servidor es Exchange RPC.  <br/> |
|EXHTTP  <br/> |Protocolo que se usa para conectarse a las conexiones RPC/HTTP del servidor.  <br/> |
|EXPR  <br/> |El protocolo que se usa para conectarse al servidor es Exchange RPC sobre HTTP, mediante un servidor proxy RPC.  <br/> Esto solo es aplicable cuando el [elemento AccountType (POX)](accounttype-pox.md) se establece en correo electrónico.  <br/> |
|WEB  <br/> |Se tiene acceso al correo electrónico desde un explorador web mediante la dirección URL especificada en el [elemento Servidor (POX).](server-pox.md)  <br/> Esto solo es aplicable cuando el [elemento AccountType (POX)](accounttype-pox.md) se establece en correo electrónico.  <br/> |
   
### <a name="version-differences"></a>Diferencias de versión

Office 365, Exchange Online y las versiones locales de Exchange a partir de la compilación 15.00.0995.014 devuelven un valor de "EXHTTP" solo si el servidor está configurado para aceptar conexiones RPC/HTTP y el cliente incluye un encabezado [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) que contiene "ExHttpInfo". 
  
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

