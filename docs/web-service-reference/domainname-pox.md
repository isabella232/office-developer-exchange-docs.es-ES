---
title: Nombredominio (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2b4af2b2-58b5-4f28-9cb3-c07a11377747
description: El elemento DomainName especifica el dominio del usuario.
ms.openlocfilehash: ff38d6a876e396317dedece0a81a9f9f0db0f587
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458428"
---
# <a name="domainname-pox"></a>Nombredominio (POX)

El elemento **domainname** especifica el dominio del usuario. 
  
- [Detección automática (POX)](autodiscover-pox.md)  
- [Respuesta (POX)](response-pox.md)  
- [Cuenta (POX)](account-pox.md) 
- [Protocolo (POX)](protocol-pox.md) 
- [Nombredominio (POX)](domainname-pox.md)
  
```xml
<DomainName/>
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
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto especifica el dominio del usuario.
  
## <a name="remarks"></a>Comentarios

Si no se especifica ningún valor, la autenticación predeterminada es usar la dirección de correo electrónico como un formato de nombre principal de usuario (UPN). Por ejemplo: \<Username\> @ \<Domain\> .
  
## <a name="see-also"></a>Vea también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

