---
title: TTL (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 178eefa1-995c-4bea-930b-e51293961191
description: El elemento TTL especifica el time to live, en horas, durante el cual la configuración permanece válida.
ms.openlocfilehash: 6850f104fe90ae941f9d1d522fa3d3641e433c5f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515106"
---
# <a name="ttl-pox"></a>TTL (POX)

El **elemento TTL** especifica el time to live, en horas, durante el cual la configuración permanece válida. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[TTL (POX)](ttl-pox.md)
  
```xml
<TTL/>
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
|[Protocol (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al equipo Exchange Server 2007 en el que está instalado el rol de servidor Acceso de cliente.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el tiempo de vida, en horas, durante el cual la configuración permanece válida. Un valor de cero indica que la detección no es necesaria. Si no se especifica ningún valor, el valor predeterminado de este elemento es 1 hora.
  
## <a name="remarks"></a>Comentarios

Una vez transcurrido el tiempo representado por el elemento **TTL,** la configuración debe volver a detectarse mediante una solicitud de detección automática. 
  
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

