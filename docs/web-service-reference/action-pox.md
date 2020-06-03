---
title: Acción (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a3462c6b-453c-462a-830d-f29ee4a2babb
description: El elemento Action proporciona información que se usa para determinar si se requiere otra solicitud de detección automática para devolver la información de configuración del usuario.
ms.openlocfilehash: f6d542b908948d09020b850b60ca1bdb025dd342
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529696"
---
# <a name="action-pox"></a>Acción (POX)

El elemento **Action** proporciona información que se usa para determinar si se requiere otra solicitud de detección automática para devolver la información de configuración del usuario. 
  
- [Detección automática (POX)](autodiscover-pox.md)
  
- [Respuesta (POX)](response-pox.md)
  
- [Cuenta (POX)](account-pox.md)
  
- [Acción (POX)](action-pox.md)
  
```xml
<Action>redirectUrl or redirectAddr or settings</Action>
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
|[Cuenta (POX)](account-pox.md) <br/> |Especifica la configuración de la cuenta del usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa si es necesaria otra solicitud de detección automática para recuperar la información de configuración del usuario. En la siguiente tabla se enumeran los valores posibles.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|redirectUrl  <br/> |Si se especifica este valor, el elemento [RedirectURL (POX)](redirecturl-pox.md) especificará la dirección URL del servidor de acceso de cliente que se usará en la siguiente solicitud de detección automática. La aplicación cliente debe dejar de redirigir después de 10 redirecciones.  <br/> |
|redirectAddr  <br/> |Si se especifica este valor, el elemento [RedirectAddr (POX)](redirectaddr-pox.md) especificará la dirección de correo electrónico que se debe usar para una solicitud de detección automática subsiguiente.  <br/> |
|settings  <br/> |Si se especifica este valor, la respuesta de detección automática contiene la configuración que se usa para configurar la cuenta. La mayoría de las opciones de configuración se encuentran en el elemento [Protocolo (POX)](protocol-pox.md) .  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

