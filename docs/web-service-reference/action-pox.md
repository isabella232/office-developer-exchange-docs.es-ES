---
title: Action (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a3462c6b-453c-462a-830d-f29ee4a2babb
description: El elemento Action proporciona información que se usa para determinar si se necesita otra solicitud de detección automática para devolver la información de configuración del usuario.
ms.openlocfilehash: b1c07fefc6b8033b9b93bd044c04fb07ba289177
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513860"
---
# <a name="action-pox"></a>Action (POX)

El **elemento Action** proporciona información que se usa para determinar si se necesita otra solicitud de detección automática para devolver la información de configuración del usuario. 
  
- [AutoDiscover (POX)](autodiscover-pox.md)
  
- [Response (POX)](response-pox.md)
  
- [Account (POX)](account-pox.md)
  
- [Action (POX)](action-pox.md)
  
```xml
<Action>redirectUrl or redirectAddr or settings</Action>
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

El valor de texto representa si es necesaria otra solicitud de detección automática para recuperar la información de configuración del usuario. En la tabla siguiente se enumeran los valores posibles.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|redirectUrl  <br/> |Si se especifica este valor, el elemento [RedirectUrl (POX)](redirecturl-pox.md) especificará la dirección URL del servidor de acceso de cliente que se usará en la solicitud de detección automática posterior. La aplicación cliente debe dejar de redirigir después de 10 redireccionamientos.  <br/> |
|redirectAddr  <br/> |Si se especifica este valor, el elemento [RedirectAddr (POX)](redirectaddr-pox.md) especificará la dirección de correo electrónico que se debe usar para una solicitud de detección automática posterior.  <br/> |
|configuración  <br/> |Si se especifica este valor, la respuesta de detección automática contiene opciones que se usan para configurar la cuenta. La mayoría de la configuración se encuentra en el [elemento Protocol (POX).](protocol-pox.md)  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

