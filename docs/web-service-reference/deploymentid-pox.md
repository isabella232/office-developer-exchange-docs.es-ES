---
title: DeploymentId (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: b879c134-307e-4645-bb53-55d8ba4fad9c
description: El elemento DeploymentId identifica de forma única el bosque de Microsoft Exchange Server 2007.
ms.openlocfilehash: 4f2548709753d8407d02218acecd9233f0ba764f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764127"
---
# <a name="deploymentid-pox"></a>DeploymentId (POX)

El elemento **DeploymentId** identifica de forma única el bosque de Microsoft Exchange Server 2007. 
  
- [Detección automática (POX)](autodiscover-pox.md)  
- [Respuesta (POX)](response-pox.md) 
- [Usuario (POX)](user-pox.md)  
- [DeploymentId (POX)](deploymentid-pox.md)
  
```xml
<DeploymentId/>
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
|[Usuario (POX)](user-pox.md) <br/> |Proporciona información específica del usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto identifica de forma única el bosque de Exchange 2007 en formato GUID.
  
## <a name="remarks"></a>Comentarios

Si desinstala y, a continuación, vuelva a instalar Exchange 2007 y usar el mismo nombre de servidor, se cambia el valor de **DeploymentId** . 
  
## <a name="see-also"></a>Vea también

- [Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

