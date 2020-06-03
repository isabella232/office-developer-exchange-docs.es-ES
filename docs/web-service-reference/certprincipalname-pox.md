---
title: CertPrincipalName (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a24092c9-58be-4008-92c4-68ec5c6c0fa6
description: El elemento CertPrincipalName especifica el nombre principal del certificado de capa de sockets seguros (SSL) que se necesita para conectarse a la organización de Microsoft Exchange Server 2007 mediante SSL.
ms.openlocfilehash: fb2a1c8577bce41945b669be56f2a94a2c4dca26
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463345"
---
# <a name="certprincipalname-pox"></a>CertPrincipalName (POX)

El elemento **CertPrincipalName** especifica el nombre principal del certificado de capa de sockets seguros (SSL) que se necesita para conectarse a la organización de Microsoft Exchange Server 2007 mediante SSL. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[CertPrincipalName (POX)](certprincipalname-pox.md)
  
```xml
<CertPrincipalName>none or servername</CertPrinicpalName>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al equipo que ejecuta Exchange 2007 y que tiene instalado el rol de servidor acceso de clientes.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto especifica el nombre de entidad de certificación SSL necesario para conectarse a la organización de Microsoft Exchange mediante SSL.
  
## <a name="remarks"></a>Comentarios

Si no se especifica el elemento **CertPrincipalName** , se establece el valor predeterminado en MSSTD: Server, donde servidor es el valor que se especifica en el elemento [servidor (POX)](server-pox.md) . Por ejemplo, si el servidor se especifica como example.com y **CertPrincipalName** se deja en blanco con [SSL (POX)](ssl-pox.md) activado, el valor predeterminado de **CertPrincipalName** sería msstd:example. com. 
  
Si no se especifica **ninguna** , Windows validará el nombre principal del certificado de acuerdo con la información que se encuentra en el tema [nombres principales](https://go.microsoft.com/fwlink/?LinkId=93417) de MSDN. 
  
## <a name="see-also"></a>Vea también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

