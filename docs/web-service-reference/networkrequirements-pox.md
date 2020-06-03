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
description: El elemento NetworkRequirements contiene los criterios que se usan para determinar si el equipo cliente está en una red que cumple con los requisitos del proveedor de servicios de Internet (ISP) para conectarse al servidor.
ms.openlocfilehash: d588f7eb12a445fba9c997c4b9db0a6842105b4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462727"
---
# <a name="networkrequirements-pox"></a>NetworkRequirements (POX)

El elemento **NetworkRequirements** contiene los criterios que se usan para determinar si el equipo cliente está en una red que cumple con los requisitos del proveedor de servicios de Internet (ISP) para conectarse al servidor. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[IPv4Start (POX)](ipv4start-pox.md) <br/> |Identifica el inicio de un intervalo de direcciones IP de la versión 4 (IPv4) que se usan para identificar un equipo en una red.  <br/> |
|[IPv4End (POX)](ipv4end-pox.md) <br/> |Identifica el final de un intervalo de direcciones IP de la versión 4 (IPv4) que se usan para identificar un equipo en la red.  <br/> |
|[IPv6Start (POX)](ipv6start-pox.md) <br/> |Identifica el inicio de un intervalo de direcciones IP versión 6 (IPv6) que se usan para identificar un equipo en una red.  <br/> |
|[IPv6End (POX)](ipv6end-pox.md) <br/> |Identifica el final de un intervalo de direcciones IP versión 6 (IPv6) que se usan para identificar un equipo en una red.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si el cliente de correo electrónico no cumple los requisitos de red, debe probar otros tipos de protocolo. Los ISP pueden proporcionar un conjunto de servidores con etiquetas de [Protocolo (POX)](protocol-pox.md) que no requieran autenticación pero que necesiten estar en la red del ISP. Los ISP pueden enumerar otro conjunto de servidores que requieran autenticación pero que no necesiten estar en una red específica. 
  
El elemento **NetworkRequirements** es opcional. 
  
## <a name="see-also"></a>Vea también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

