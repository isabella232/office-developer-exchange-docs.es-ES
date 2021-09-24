---
title: User (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 7c42b516-77f6-4aee-99d8-b866d82d793a
description: El elemento User proporciona información específica del usuario.
ms.openlocfilehash: 832e0a63e75a08406b3aa397ac29ad5aa300cfe0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522413"
---
# <a name="user-pox"></a>User (POX)

El **elemento User** proporciona información específica del usuario. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[User (POX)](user-pox.md)
  
```xml
<User>
   <DisplayName/>
   <LegacyDN/>
   <DeploymentId/>
   <AutoDiscoverSMTPAddress/>
</User>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DisplayName (cadena)](displayname-string.md) <br/> |Representa el nombre para mostrar del usuario.  <br/> |
|[LegacyDN (POX)](legacydn-pox.md) <br/> |Identifica el buzón de un usuario por nombre distintivo heredado.  <br/> |
|[DeploymentId (POX)](deploymentid-pox.md) <br/> |Identifica de forma única el Exchange bosque.  <br/> |
|[AutoDiscoverSMTPAddress (POX)](autodiscoversmtpaddress-pox.md) <br/> |Contiene la dirección SMTP del usuario que se usa para el proceso de detección automática.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Response (POX)](response-pox.md) <br/> |Contiene la respuesta del servicio de detección automática.  <br/> |
   
## <a name="remarks"></a>Comentarios

Las solicitudes y respuestas de detección automática deben estar codificadas en UTF-8.
  
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

