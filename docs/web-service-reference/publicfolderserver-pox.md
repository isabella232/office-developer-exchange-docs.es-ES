---
title: PublicFolderServer (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 37ad46ab-7817-4fdd-ad2d-26cb525cd96b
description: El elemento PublicFolderServer contiene el nombre de dominio completo (FQDN) del servidor de carpetas públicas para el usuario.
ms.openlocfilehash: d81d7cdc10cdf0c5f06e9c4bf9e1c8a089de293d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542956"
---
# <a name="publicfolderserver-pox"></a>PublicFolderServer (POX)

El **elemento PublicFolderServer** contiene el nombre de dominio completo (FQDN) del servidor de carpetas públicas para el usuario. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[PublicFolderServer (POX)](publicfolderserver-pox.md)
  
```XML
<PublicFolderServer/>
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
|[Protocol (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor Acceso de cliente.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el FQDN del servidor de carpetas públicas para el usuario.
  
## <a name="remarks"></a>Comentarios

El **elemento PublicFolderServer** es un elemento secundario opcional del **elemento Protocol.** 
  
## <a name="see-also"></a>Consulte también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

