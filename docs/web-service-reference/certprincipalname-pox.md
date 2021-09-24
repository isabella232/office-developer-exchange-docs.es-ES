---
title: CertPrincipalName (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a24092c9-58be-4008-92c4-68ec5c6c0fa6
description: El elemento CertPrincipalName especifica el nombre de entidad de seguridad del certificado capa de sockets seguros (SSL) necesario para conectarse a la organización de Microsoft Exchange Server 2007 mediante SSL.
ms.openlocfilehash: 69ee49cdad09032c269ffbbcc918044daf61cb9b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523254"
---
# <a name="certprincipalname-pox"></a>CertPrincipalName (POX)

El **elemento CertPrincipalName** especifica el nombre de entidad de seguridad del certificado capa de sockets seguros (SSL) necesario para conectarse a la organización de Microsoft Exchange Server 2007 mediante SSL. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[CertPrincipalName (POX)](certprincipalname-pox.md)
  
```xml
<CertPrincipalName>none or servername</CertPrinicpalName>
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
|[Protocol (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al equipo que se ejecuta Exchange 2007 que tiene instalada la función de servidor Acceso de cliente.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto especifica el nombre principal del certificado SSL necesario para conectarse a la organización de Microsoft Exchange mediante SSL.
  
## <a name="remarks"></a>Comentarios

Si no se especifica el elemento **CertPrincipalName,** el valor predeterminado se establece en msstd:SERVER, donde SERVER es el valor especificado en el elemento [Server (POX).](server-pox.md) Por ejemplo, si SERVER se especifica como example.com y **CertPrincipalName** se deja en blanco con [SSL (POX)](ssl-pox.md) activado, el valor predeterminado de **CertPrincipalName** sería msstd:example.com. 
  
Si **no** se especifica ninguno, Windows validará el nombre principal del certificado de acuerdo con la información que se encuentra en el tema [Nombres](https://go.microsoft.com/fwlink/?LinkId=93417) principales de MSDN. 
  
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

