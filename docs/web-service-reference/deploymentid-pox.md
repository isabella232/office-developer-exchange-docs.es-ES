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
description: El elemento DeploymentId identifica de forma exclusiva el bosque de Microsoft Exchange Server 2007.
ms.openlocfilehash: 4986a3404763e88fb3e84d52a5d30d54c810f93a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467924"
---
# <a name="deploymentid-pox"></a>DeploymentId (POX)

El elemento **DeploymentId** identifica de forma exclusiva el bosque de Microsoft Exchange Server 2007. 
  
- [Detección automática (POX)](autodiscover-pox.md)  
- [Respuesta (POX)](response-pox.md) 
- [Usuario (POX)](user-pox.md)  
- [DeploymentId (POX)](deploymentid-pox.md)
  
```xml
<DeploymentId/>
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
|[Usuario (POX)](user-pox.md) <br/> |Proporciona información específica del usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto identifica de forma exclusiva el bosque de Exchange 2007 en formato GUID.
  
## <a name="remarks"></a>Comentarios

Si desinstala y, a continuación, reinstala Exchange 2007 y usa el mismo nombre de servidor, cambia el valor **DeploymentId** . 
  
## <a name="see-also"></a>Vea también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

