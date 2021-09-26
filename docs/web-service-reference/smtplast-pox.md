---
title: SMTPLast (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: f1aa8bd9-c6ac-41ac-8d2d-56fb20006005
description: El elemento SMTPLast especifica si el servidor del Protocolo simple de transferencia de correo (SMTP) requiere que el correo electrónico se descargue antes de enviar correo electrónico mediante el servidor SMTP.
ms.openlocfilehash: ff1e47fa1e3ebd0267879cd596a3a559f2702943
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544685"
---
# <a name="smtplast-pox"></a>SMTPLast (POX)

El **elemento SMTPLast** especifica si el servidor del Protocolo simple de transferencia de correo (SMTP) requiere que el correo electrónico se descargue antes de enviar correo electrónico mediante el servidor SMTP. 
  
- [AutoDiscover (POX)](autodiscover-pox.md)
  
- [Response (POX)](response-pox.md)
  
- [Account (POX)](account-pox.md)
  
- [Protocol (POX)](protocol-pox.md)
  
- [SMTPLast (POX)](smtplast-pox.md)
  
```xml
<SMTPLast>on or off</SMTPLast>
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

El valor de texto especifica si el servidor SMTP requiere que el correo electrónico se descargue antes de enviar correo electrónico mediante el servidor SMTP. Los valores posibles **están on** y **off**. El valor predeterminado es **off**.
  
## <a name="see-also"></a>Consulte también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

