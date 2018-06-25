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
description: El elemento CertPrincipalName especifica el nombre de entidad de seguridad de certificado de capa de Sockets seguros (SSL) que es necesario para conectarse a la organización de Microsoft Exchange Server 2007 mediante el uso de SSL.
ms.openlocfilehash: d2766b16a3e8a1bcd013de332d9c07f709fcf949
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763734"
---
# <a name="certprincipalname-pox"></a>CertPrincipalName (POX)

El elemento **CertPrincipalName** especifica el nombre de entidad de seguridad de certificado de capa de Sockets seguros (SSL) que es necesario para conectarse a la organización de Microsoft Exchange Server 2007 mediante el uso de SSL. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[CertPrincipalName (POX)](certprincipalname-pox.md)
  
```xml
<CertPrincipalName>none or servername</CertPrinicpalName>
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
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Exchange 2007 que tenga instalado el rol de servidor de acceso de cliente.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto especifica el nombre de entidad de seguridad de certificados SSL que se necesita para conectarse a la organización de Microsoft Exchange mediante el uso de SSL.
  
## <a name="remarks"></a>Comentarios

Si no se especifica el elemento **CertPrincipalName** , el valor predeterminado se establece en msstd:SERVER, donde servidor es el valor que se especifica en el elemento de [Servidor (POX)](server-pox.md) . Por ejemplo, si el servidor especificado como example.com y **CertPrincipalName** se deja en blanco con [SSL (POX)](ssl-pox.md) activado, el valor predeterminado de **CertPrincipalName** sería msstd:example.com. 
  
Si no se especifica **ninguna** , Windows validará el nombre de entidad de seguridad del certificado según la información que se encuentra en el tema de [Los nombres de entidad de seguridad](http://go.microsoft.com/fwlink/?LinkId=93417) en MSDN. 
  
## <a name="see-also"></a>Vea también



[Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

