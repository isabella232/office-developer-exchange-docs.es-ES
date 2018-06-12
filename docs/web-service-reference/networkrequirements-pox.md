---
title: NetworkRequirements (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1555fd2e-05b6-4b94-907b-dae9174049d9
description: El elemento NetworkRequirements contiene los criterios que se usan para determinar si el equipo cliente está en una red que cumpla los requisitos del proveedor de servicios Internet (ISP) para conectarse al servidor.
ms.openlocfilehash: f3abcff04cd4121b8dcc7ceff7658ad389e6d0b0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836529"
---
# <a name="networkrequirements-pox"></a>NetworkRequirements (POX)

El elemento **NetworkRequirements** contiene los criterios que se usan para determinar si el equipo cliente está en una red que cumpla los requisitos del proveedor de servicios Internet (ISP) para conectarse al servidor. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[NetworkRequirements (POX)](networkrequirements-pox.md)
  
```xml
<NetworkRequirements>
   <IPv4Start/>
   <IPv4End/>
   <IPv6Start/>
   <IPv6End/>
</NetworkRequirements>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[IPv4Start (POX)](ipv4start-pox.md) <br/> |Identifica el inicio de un intervalo de IP versión 4 (IPv4) las direcciones que se usan para identificar un equipo en una red.  <br/> |
|[IPv4End (POX)](ipv4end-pox.md) <br/> |Identifica el final de un intervalo de IP versión 4 (IPv4) las direcciones que se usan para identificar un equipo en la red.  <br/> |
|[IPv6Start (POX)](ipv6start-pox.md) <br/> |Identifica el inicio de un intervalo de IP versión 6 (IPv6) las direcciones que se usan para identificar un equipo en una red.  <br/> |
|[IPv6End (POX)](ipv6end-pox.md) <br/> |Identifica el final de un intervalo de IP versión 6 (IPv6) las direcciones que se usan para identificar un equipo en una red.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.  <br/> |
   
## <a name="remarks"></a>Notas

Si el cliente de correo electrónico no coincide con los requisitos de red, deben intentar otros tipos de protocolo. ISP pueden proporcionar un conjunto de servidores con las etiquetas de [Protocolo (POX)](protocol-pox.md) que no requieren la autenticación pero que son necesarios para estar en la red de ISP. ISP pueden mostrar otro conjunto de servidores que requieren la autenticación pero que no tienen que estar en una red específica. 
  
El elemento **NetworkRequirements** es opcional. 
  
## <a name="see-also"></a>Ver también



[Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

