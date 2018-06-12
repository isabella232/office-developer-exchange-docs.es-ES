---
title: AuthRequired (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 241a23ee-d2a2-4724-b794-d0d523d480a2
description: El elemento AuthRequired especifica si se requiere autenticación.
ms.openlocfilehash: b747f53766b6b914955c5e41b63462b9b44bff4e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763589"
---
# <a name="authrequired-pox"></a>AuthRequired (POX)

El elemento **AuthRequired** especifica si se requiere autenticación. 
  
- [Detección automática (POX)](autodiscover-pox.md)
  
- [Respuesta (POX)](response-pox.md)
  
- [Cuenta (POX)](account-pox.md)
  
- [Protocolo (POX)](protocol-pox.md)
  
- [AuthRequired (POX)](authrequired-pox.md)
  
```xml
<AuthRequired>on or off</AuthRequired>
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

El valor de texto especifica si se requiere autenticación. Los valores posibles son **encendido** y **apagado**. Si no se especifica un valor, el valor predeterminado es **en**. 
  
## <a name="see-also"></a>Ver también

- [Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

