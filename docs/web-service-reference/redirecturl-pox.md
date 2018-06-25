---
title: RedirectUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c54f310f-8c99-4c37-8e73-ac87722b6229
description: El elemento RedirectUrl contiene la dirección URL del equipo que ejecuta Microsoft Exchange Server 2007 que tiene el rol de servidor de acceso de cliente instalado que se debe usar para obtener la configuración de detección automática.
ms.openlocfilehash: 3b634f1a3a3d44b6aae1a826a005149200641dcb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837027"
---
# <a name="redirecturl-pox"></a>RedirectUrl (POX)

El elemento **RedirectUrl** contiene la dirección URL del equipo que ejecuta Microsoft Exchange Server 2007 que tiene el rol de servidor de acceso de cliente instalado que se debe usar para obtener la configuración de detección automática. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[RedirectUrl (POX)](redirecturl-pox.md)
  
```xml
<RedirectUrl/>
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
|[Cuenta (POX)](account-pox.md) <br/> |Especifica la configuración de cuenta para el usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa la dirección URL del servidor de acceso de cliente que se debe usar para obtener la configuración de detección automática.
  
## <a name="remarks"></a>Comentarios

La aplicación cliente debe dejar de redirigir después de 10 redirecciones.
  
## <a name="see-also"></a>Vea también



[Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

