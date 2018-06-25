---
title: PublicFolderServer (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 37ad46ab-7817-4fdd-ad2d-26cb525cd96b
description: El elemento PublicFolderServer contiene el nombre de dominio completo (FQDN) del servidor de carpetas públicas para el usuario.
ms.openlocfilehash: 6fb2f1a97279ee7f2e94c008474ddfed088faea1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836928"
---
# <a name="publicfolderserver-pox"></a>PublicFolderServer (POX)

El elemento **PublicFolderServer** contiene el nombre de dominio completo (FQDN) del servidor de carpetas públicas para el usuario. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[PublicFolderServer (POX)](publicfolderserver-pox.md)
  
```XML
<PublicFolderServer/>
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
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el FQDN del servidor de carpetas públicas para el usuario.
  
## <a name="remarks"></a>Comentarios

El elemento **PublicFolderServer** es un elemento secundario opcional del elemento **Protocol** . 
  
## <a name="see-also"></a>Vea también



[Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

