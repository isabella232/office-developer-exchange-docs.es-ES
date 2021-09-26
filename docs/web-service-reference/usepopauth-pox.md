---
title: UsePOPAuth (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 28f552d8-6bb8-49b4-a45c-b2053670f1cc
description: El elemento UsePOPAuth indica si la información de autenticación que se proporciona para un tipo de cuenta POP3 también se usa para el Protocolo simple de transferencia de correo (SMTP).
ms.openlocfilehash: 354c027bf40ddf30cda472eb4ca0d018dca64f9c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542627"
---
# <a name="usepopauth-pox"></a>UsePOPAuth (POX)

El **elemento UsePOPAuth** indica si la información de autenticación que se proporciona para un tipo de cuenta POP3 también se usa para el Protocolo simple de transferencia de correo (SMTP). 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[UsePOPAuth (POX)](usepopauth-pox.md)
  
```xml
<UsePOPAuth>on or off</UsePOPAuth>
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
|[Protocol (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al equipo que se ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto indica si la información de autenticación que se proporciona para un tipo de cuenta POP3 también se usa para SMTP. Los valores posibles **están on** y **off**.
  
## <a name="remarks"></a>Comentarios

El **elemento UsePOPAuth** solo se usa cuando [Type (POX)](type-pox.md) es SMTP. 
  
## <a name="see-also"></a>Consulte también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

