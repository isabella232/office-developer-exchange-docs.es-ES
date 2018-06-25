---
title: Usuario (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 7c42b516-77f6-4aee-99d8-b866d82d793a
description: El elemento de usuario proporciona información específica del usuario.
ms.openlocfilehash: 3f90ff0cc00170170c7304f2a19fe1d7abd9d1bc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840896"
---
# <a name="user-pox"></a>Usuario (POX)

El elemento de **usuario** proporciona información específica del usuario. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Usuario (POX)](user-pox.md)
  
```xml
<User>
   <DisplayName/>
   <LegacyDN/>
   <DeploymentId/>
   <AutoDiscoverSMTPAddress/>
</User>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[DisplayName (cadena)](displayname-string.md) <br/> |Representa el nombre para mostrar del usuario.  <br/> |
|[LegacyDN (POX)](legacydn-pox.md) <br/> |Identifica el buzón de un usuario por su nombre distintivo (DN) heredado.  <br/> |
|[DeploymentId (POX)](deploymentid-pox.md) <br/> |Identifica de forma exclusiva el bosque de Exchange.  <br/> |
|[AutoDiscoverSMTPAddress (POX)](autodiscoversmtpaddress-pox.md) <br/> |Contiene una dirección SMTP del usuario que se usa para el proceso de detección automática.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Respuesta (POX)](response-pox.md) <br/> |Contiene la respuesta del servicio Detección automática.  <br/> |
   
## <a name="remarks"></a>Comentarios

Las respuestas y solicitudes de detección automática deben ser con codificación UTF-8.
  
## <a name="see-also"></a>Vea también



[Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

