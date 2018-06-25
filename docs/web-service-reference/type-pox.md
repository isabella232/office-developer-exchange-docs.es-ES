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
description: El elemento de tipo identifica el tipo de la cuenta de correo configurada.
ms.openlocfilehash: 6e1349769c6a5349304f576419e0c609d3edd9a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840735"
---
# <a name="type-pox"></a>Tipo (POX)

El elemento de **tipo** identifica el tipo de la cuenta de correo configurada. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[Tipo (POX)](type-pox.md)
  
```XML
<Type>WEB or EXCH or EXPR or EXHTTP</Type>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente con el servidor de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el tipo de cuenta de correo. En la siguiente tabla se enumera los valores posibles.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|EXCH  <br/> |El protocolo que se usa para conectarse al servidor es RPC de Exchange.  <br/> |
|EXHTTP  <br/> |El protocolo que se usa para conectarse a las conexiones RPC/HTTP del servidor.  <br/> |
|EXPR  <br/> |El protocolo que se usa para conectarse al servidor es RPC de Exchange a través de HTTP, utilizando un servidor proxy RPC.  <br/> Esto solo es aplicable cuando el elemento [AccountType (POX)](accounttype-pox.md) está establecido en correo electrónico.  <br/> |
|WEB  <br/> |Correo electrónico se obtiene acceso desde un explorador Web mediante el uso de la dirección URL que se especifica en el elemento de [Servidor (POX)](server-pox.md) .  <br/> Esto solo es aplicable cuando el elemento [AccountType (POX)](accounttype-pox.md) está establecido en correo electrónico.  <br/> |
   
### <a name="version-differences"></a>Diferencias de versión

Office 365, Exchange Online y versiones locales de inicio de Exchange con creación 15.00.0995.014 devuelto un valor de "EXHTTP" sólo si el servidor está configurado para aceptar conexiones RPC/HTTP y el cliente incluye un encabezado [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) que contiene "ExHttpInfo". 
  
## <a name="see-also"></a>Vea también



[Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

