---
title: RedirectAddr (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4
description: El elemento RedirectAddr especifica la dirección de correo electrónico que se debe usar para una solicitud de detección automática posterior.
ms.openlocfilehash: 75db62a84ccce743e73c812082ab9dbbc4fdb1cd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540597"
---
# <a name="redirectaddr-pox"></a>RedirectAddr (POX)

El **elemento RedirectAddr** especifica la dirección de correo electrónico que se debe usar para una solicitud de detección automática posterior. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[RedirectAddr (POX)](redirectaddr-pox.md)
  
```xml
<RedirectAddr/>
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
|[Account (POX)](account-pox.md) <br/> |Especifica la configuración de la cuenta para el usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa la dirección de correo electrónico que se debe usar para una solicitud de detección automática posterior.
  
## <a name="remarks"></a>Comentarios

Si este elemento está presente en la respuesta Detección automática, realice otra solicitud mediante el valor de texto del **elemento RedirectAddr.** 
  
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

