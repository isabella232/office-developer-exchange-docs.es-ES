---
title: SMTPLast (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f1aa8bd9-c6ac-41ac-8d2d-56fb20006005
description: El elemento SMTPLast especifica si el servidor de Protocolo Simple de transferencia de correo (SMTP) requiere que el correo electrónico se descargue antes de enviar correo electrónico mediante el servidor SMTP.
ms.openlocfilehash: 5359f20b33855f4ef48566058bc46bd618e3b2ff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837505"
---
# <a name="smtplast-pox"></a>SMTPLast (POX)

El elemento **SMTPLast** especifica si el servidor de Protocolo Simple de transferencia de correo (SMTP) requiere que el correo electrónico se descargue antes de enviar correo electrónico mediante el servidor SMTP. 
  
- [Detección automática (POX)](autodiscover-pox.md)
  
- [Respuesta (POX)](response-pox.md)
  
- [Cuenta (POX)](account-pox.md)
  
- [Protocolo (POX)](protocol-pox.md)
  
- [SMTPLast (POX)](smtplast-pox.md)
  
```xml
<SMTPLast>on or off</SMTPLast>
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
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto especifica si el servidor SMTP requiere que el correo electrónico se descargue antes de enviar correo electrónico mediante el servidor SMTP. Los valores posibles son **encendido** y **apagado**. El valor predeterminado es **desactivado**.
  
## <a name="see-also"></a>Ver también

- [Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

