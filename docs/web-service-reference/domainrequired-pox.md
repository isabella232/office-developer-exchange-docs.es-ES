---
title: DomainRequired (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1f26b691-7331-4c7f-a92b-dfcc66c26963
description: El elemento DomainRequired indica si el dominio es necesario para la autenticación.
ms.openlocfilehash: 97d602c40b247f9a6650cc4440b53bf23c18482e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461327"
---
# <a name="domainrequired-pox"></a>DomainRequired (POX)

El elemento **DomainRequired** indica si el dominio es necesario para la autenticación. 
  
- [Detección automática (POX)](autodiscover-pox.md)  
- [Respuesta (POX)](response-pox.md) 
- [Cuenta (POX)](account-pox.md)  
- [Protocolo (POX)](protocol-pox.md)  
- [DomainRequired (POX)](domainrequired-pox.md)
  
```xml
<DomainRequired>on or off</DomainRequired>
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

El valor de texto indica si el dominio es necesario para la autenticación. Los valores posibles son **activado** y **desactivado**. Si el valor es **on**, la siguiente solicitud debe contener el dominio de la cuenta del usuario.
  
## <a name="remarks"></a>Comentarios

Si no se especifica el dominio en el elemento [LoginName (POX)](loginname-pox.md) o no se especificó el elemento **LoginName** , el usuario debe especificar el dominio para que la autenticación se realice correctamente. 
  
## <a name="see-also"></a>Vea también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

