---
title: PublicFolderServer (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 37ad46ab-7817-4fdd-ad2d-26cb525cd96b
description: El elemento PublicFolderServer contiene el nombre de dominio completo (FQDN) del servidor de carpetas públicas del usuario.
ms.openlocfilehash: 868eab83d05387f570bc033522121f25f09817c4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44433689"
---
# <a name="publicfolderserver-pox"></a>PublicFolderServer (POX)

El elemento **PublicFolderServer** contiene el nombre de dominio completo (FQDN) del servidor de carpetas públicas del usuario. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[PublicFolderServer (POX)](publicfolderserver-pox.md)
  
```XML
<PublicFolderServer/>
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
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el FQDN del servidor de carpetas públicas del usuario.
  
## <a name="remarks"></a>Comentarios

El elemento **PublicFolderServer** es un elemento secundario opcional del elemento **Protocol** . 
  
## <a name="see-also"></a>Vea también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

