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
description: El elemento de acción proporciona información que se utiliza para determinar si se requiere otra solicitud de detección automática para devolver la información de configuración de usuario.
ms.openlocfilehash: 118bb59f2c929e3c74683dbf3f073da34d67a3e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764557"
---
# <a name="action-pox"></a>Acción (POX)

El elemento de **acción** proporciona información que se utiliza para determinar si se requiere otra solicitud de detección automática para devolver la información de configuración de usuario. 
  
- [Detección automática (POX)](autodiscover-pox.md)
  
- [Respuesta (POX)](response-pox.md)
  
- [Cuenta (POX)](account-pox.md)
  
- [Acción (POX)](action-pox.md)
  
```xml
<Action>redirectUrl or redirectAddr or settings</Action>
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

El valor de texto representa si otra solicitud de detección automática es necesario para recuperar información de configuración del usuario. En la siguiente tabla se enumera los valores posibles.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|redirectUrl  <br/> |Si se especifica este valor, el elemento [RedirectUrl (POX)](redirecturl-pox.md) especifique la dirección URL del servidor acceso de cliente que se utilizará en la siguiente solicitud de detección automática. La aplicación cliente debe dejar de redirigir después de 10 redirecciones.  <br/> |
|redirectAddr  <br/> |Si se especifica este valor, el elemento [RedirectAddr (POX)](redirectaddr-pox.md) especifique la dirección de correo electrónico que se debe usar para una solicitud de detección automática subsiguiente.  <br/> |
|settings  <br/> |Si se especifica este valor, la respuesta de detección automática contiene la configuración que se usa para configurar la cuenta. La mayoría de las opciones se encuentran en el elemento de [Protocolo (POX)](protocol-pox.md) .  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

