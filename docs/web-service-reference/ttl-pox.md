---
title: TTL (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 178eefa1-995c-4bea-930b-e51293961191
description: El elemento TTL especifica el período de vida, en horas, durante el cual la configuración permanece válida.
ms.openlocfilehash: 5fecf3103553a82ed2aeeecfc1e4e1b9fe38583c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840733"
---
# <a name="ttl-pox"></a>TTL (POX)

El elemento **TTL** especifica el período de vida, en horas, durante el cual la configuración permanece válida. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[TTL (POX)](ttl-pox.md)
  
```xml
<TTL/>
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
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente con el equipo de Exchange Server 2007 en la que está instalado el rol de servidor de acceso de cliente.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el período de vida, en horas, durante el cual la configuración permanece válida. Un valor de cero indica que redescubrimiento no es necesario. Si no se especifica ningún valor, el valor predeterminado para este elemento es 1 hora.
  
## <a name="remarks"></a>Comentarios

Una vez transcurrido el tiempo que está representado por el elemento de **período de Vida** , la configuración se debe redescubrir mediante el uso de una solicitud de detección automática. 
  
## <a name="see-also"></a>Vea también



[Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

