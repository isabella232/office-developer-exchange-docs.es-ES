---
title: RedirectAddr (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4
description: El elemento RedirectAddr especifica la dirección de correo electrónico que se debe usar para una solicitud de detección automática subsiguiente.
ms.openlocfilehash: fe15054b9962fc2decf52ac3c42536e36358948a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837020"
---
# <a name="redirectaddr-pox"></a>RedirectAddr (POX)

El elemento **RedirectAddr** especifica la dirección de correo electrónico que se debe usar para una solicitud de detección automática subsiguiente. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[RedirectAddr (POX)](redirectaddr-pox.md)
  
```xml
<RedirectAddr/>
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

El valor de texto representa la dirección de correo electrónico que se debe usar para una solicitud de detección automática subsiguiente.
  
## <a name="remarks"></a>Comentarios

Si este elemento está presente en la respuesta de detección automática, realizar otra solicitud usando el valor de texto del elemento **RedirectAddr** . 
  
## <a name="see-also"></a>Vea también



[Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

