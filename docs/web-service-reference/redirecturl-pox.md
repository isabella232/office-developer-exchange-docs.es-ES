---
title: RedirectUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: c54f310f-8c99-4c37-8e73-ac87722b6229
description: El elemento RedirectUrl contiene la dirección URL del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente que debe usarse para obtener la configuración de detección automática.
ms.openlocfilehash: d515f3f79f2370dc496614bab0a3f77300ad4e30
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513531"
---
# <a name="redirecturl-pox"></a>RedirectUrl (POX)

El **elemento RedirectUrl** contiene la dirección URL del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente que debe usarse para obtener la configuración de detección automática. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[RedirectUrl (POX)](redirecturl-pox.md)
  
```xml
<RedirectUrl/>
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

El valor de texto representa la dirección URL del servidor de acceso de cliente que se debe usar para obtener la configuración de detección automática.
  
## <a name="remarks"></a>Comentarios

La aplicación cliente debe dejar de redirigir después de 10 redireccionamientos.
  
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

