---
title: Domain (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1f26b691-7331-4c7f-a92b-dfcc66c26963
description: El elemento Domain indica si el dominio es necesario para la autenticación.
ms.openlocfilehash: f314b9d27d1b4ee472d249ec49af1a785ff9ac25
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764262"
---
# <a name="domainrequired-pox"></a>Domain (POX)

El elemento **Domain** indica si el dominio es necesario para la autenticación. 
  
- [Detección automática (POX)](autodiscover-pox.md)  
- [Respuesta (POX)](response-pox.md) 
- [Cuenta (POX)](account-pox.md)  
- [Protocolo (POX)](protocol-pox.md)  
- [Domain (POX)](domainrequired-pox.md)
  
```xml
<DomainRequired>on or off</DomainRequired>
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

El valor de texto indica si el dominio es necesario para la autenticación. Los valores posibles son **encendido** y **apagado**. Si **el valor está habilitado,** la siguiente solicitud debe contener el dominio de la cuenta de usuario.
  
## <a name="remarks"></a>Comentarios

Si el dominio no está especificado en el elemento [LoginName (POX)](loginname-pox.md) , o no se ha especificado el elemento **LoginName** , el usuario debe escribir el dominio antes de que la autenticación se realizará correctamente. 
  
## <a name="see-also"></a>Vea también

- [Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

