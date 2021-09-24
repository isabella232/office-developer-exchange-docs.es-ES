---
title: NetworkRequirements (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 1555fd2e-05b6-4b94-907b-dae9174049d9
description: El elemento NetworkRequirements contiene los criterios que se usan para determinar si el equipo cliente está en una red que cumple los requisitos del proveedor de servicios de Internet (ISP) para conectarse al servidor.
ms.openlocfilehash: 07a258ad48b74c614ce367db0f893ed884cf3f75
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509526"
---
# <a name="networkrequirements-pox"></a>NetworkRequirements (POX)

El **elemento NetworkRequirements** contiene los criterios que se usan para determinar si el equipo cliente está en una red que cumple los requisitos del proveedor de servicios de Internet (ISP) para conectarse al servidor. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[IPv4Start (POX)](ipv4start-pox.md) <br/> |Identifica el inicio de un intervalo de direcciones IP de la versión 4 (IPv4) que se usan para identificar un equipo en una red.  <br/> |
|[IPv4End (POX)](ipv4end-pox.md) <br/> |Identifica el final de un intervalo de direcciones IP de la versión 4 (IPv4) que se usan para identificar un equipo en la red.  <br/> |
|[IPv6Start (POX)](ipv6start-pox.md) <br/> |Identifica el inicio de un intervalo de direcciones IP de la versión 6 (IPv6) que se usan para identificar un equipo en una red.  <br/> |
|[IPv6End (POX)](ipv6end-pox.md) <br/> |Identifica el final de un intervalo de direcciones IP de la versión 6 (IPv6) que se usan para identificar un equipo en una red.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al equipo que se ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si el cliente de correo electrónico no coincide con los requisitos de red, debe probar otros tipos de protocolo. Los ISP pueden proporcionar un conjunto de servidores con etiquetas de protocolo [(POX)](protocol-pox.md) que no requieren autenticación, pero que deben estar en la red isp. Los ISP pueden enumerar otro conjunto de servidores que requieren autenticación, pero que no son necesarios para estar en una red específica. 
  
El **elemento NetworkRequirements** es opcional. 
  
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

