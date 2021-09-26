---
title: DeploymentId (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: b879c134-307e-4645-bb53-55d8ba4fad9c
description: El elemento DeploymentId identifica de forma única Microsoft Exchange Server bosque de 2007.
ms.openlocfilehash: 37d66eadb38f02e75a35d0516b36aff07dfdafa6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545359"
---
# <a name="deploymentid-pox"></a>DeploymentId (POX)

El **elemento DeploymentId** identifica de forma única Microsoft Exchange Server bosque de 2007. 
  
- [AutoDiscover (POX)](autodiscover-pox.md)  
- [Response (POX)](response-pox.md) 
- [User (POX)](user-pox.md)  
- [DeploymentId (POX)](deploymentid-pox.md)
  
```xml
<DeploymentId/>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[User (POX)](user-pox.md) <br/> |Proporciona información específica del usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto identifica de forma única Exchange bosque de 2007 en formato GUID.
  
## <a name="remarks"></a>Comentarios

Si desinstala y vuelve a instalar Exchange 2007 y usa el mismo nombre de servidor, cambia **el valor DeploymentId.** 
  
## <a name="see-also"></a>Consulte también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

