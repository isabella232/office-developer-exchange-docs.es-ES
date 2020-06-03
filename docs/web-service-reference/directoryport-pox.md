---
title: DirectoryPort (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ab436b54-ceba-4cd9-aeb4-134f9b93986d
description: El elemento DirectoryPort especifica el puerto que se usa para conectarse al directorio cuando se usa el protocolo de interfaz del proveedor de servicio de nombres (NSPI).
ms.openlocfilehash: 2ba0a15cea0b4eb9b6069fab384edb3d9747a360
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462090"
---
# <a name="directoryport-pox"></a>DirectoryPort (POX)

El elemento **DirectoryPort** especifica el puerto que se usa para conectarse al directorio cuando se usa el protocolo de interfaz del proveedor de servicio de nombres (NSPI). 
  
- [Detección automática (POX)](autodiscover-pox.md) 
- [Respuesta (POX)](response-pox.md)  
- [Cuenta (POX)](account-pox.md)  
- [Protocolo (POX)](protocol-pox.md)  
- [DirectoryPort (POX)](directoryport-pox.md)
  
```xml
<DirectoryPort/>
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

El valor de texto representa el puerto que se usa para obtener acceso al servidor de Exchange.
  
## <a name="remarks"></a>Comentarios

El elemento **DirectoryPort** solo se usa cuando el elemento [Type (POX)](type-pox.md) es igual a EXCH o a expr. 
  
## <a name="see-also"></a>Vea también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

