---
title: Tipo (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 9a627244-554f-4223-b9d8-a601b81a4a1a
description: El elemento Type identifica el tipo de cuenta de correo configurada.
ms.openlocfilehash: ad3570094ebe28498dfdc375cf7fc255434ba20d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465103"
---
# <a name="type-pox"></a>Tipo (POX)

El elemento **Type** identifica el tipo de cuenta de correo configurada. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[Tipo (POX)](type-pox.md)
  
```XML
<Type>WEB or EXCH or EXPR or EXHTTP</Type>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al servidor de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el tipo de cuenta de correo. En la siguiente tabla se enumeran los valores posibles.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|EXCH  <br/> |El protocolo que se usa para conectarse al servidor es RPC de Exchange.  <br/> |
|Exhttp  <br/> |Protocolo que se usa para conectarse a las conexiones RPC/HTTP del servidor.  <br/> |
|EXPRESIÓN  <br/> |El protocolo que se usa para conectarse al servidor es Exchange RPC sobre HTTP, mediante un servidor proxy RPC.  <br/> Esto solo es aplicable cuando el elemento [AccountType (POX)](accounttype-pox.md) se establece en email.  <br/> |
|WEB  <br/> |Se obtiene acceso al correo electrónico desde un explorador Web con la dirección URL especificada en el elemento [servidor (POX)](server-pox.md) .  <br/> Esto solo es aplicable cuando el elemento [AccountType (POX)](accounttype-pox.md) se establece en email.  <br/> |
   
### <a name="version-differences"></a>Diferencias de versión

Office 365, Exchange Online y versiones locales de Exchange que comienzan con la compilación 15.00.0995.014 devuelven un valor de "exhttp" solo si el servidor está configurado para aceptar conexiones RPC/HTTP y el cliente incluye un encabezado [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) que contiene "ExHttpInfo". 
  
## <a name="see-also"></a>Vea también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

