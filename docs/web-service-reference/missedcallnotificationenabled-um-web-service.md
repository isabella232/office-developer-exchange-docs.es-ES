---
title: MissedCallNotificationEnabled (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- MissedCallNotificationEnabled
api_type:
- schema
ms.assetid: 8e6bf0b1-ff76-474c-ac0f-621b6ab89212
description: El elemento MissedCallNotificationEnabled contiene un valor que indica si una notificación de llamada perdida está habilitada en una respuesta a una solicitud GetUMProperties (servicio Web de mensajería unificada).
ms.openlocfilehash: e2f18027c56be1408c27d5f687fe90f8ffd724db
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468659"
---
# <a name="missedcallnotificationenabled-um-web-service"></a>MissedCallNotificationEnabled (servicio Web de mensajería unificada)

El elemento **MissedCallNotificationEnabled** contiene un valor que indica si una notificación de llamada perdida está habilitada en una respuesta a una solicitud [GetUMProperties (servicio Web de mensajería unificada)](getumproperties-operation-um-web-service.md) . 
  
[GetUMPropertiesResponse (servicio Web de mensajería unificada)](getumpropertiesresponse-um-web-service.md)
  
[MissedCallNotificationEnabled (servicio Web de mensajería unificada)](missedcallnotificationenabled-um-web-service.md)
  
```xml
<MissedCallNotificationEnabled/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetUMPropertiesResponse (servicio Web de mensajería unificada)](getumpropertiesresponse-um-web-service.md) <br/> |Define una respuesta a una solicitud de [operación de GetUMProperties (servicio Web de mensajería unificada)](getumproperties-operation-um-web-service.md) .  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto booleano. Los valores posibles son los siguientes:
  
- Verdadero
    
- Falso
    
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUMProperties (servicio Web de mensajería unificada)](getumproperties-operation-um-web-service.md)
  
[Operación SetMissedCallNotificationEnabled (servicio Web de mensajería unificada)](setmissedcallnotificationenabled-operation-um-web-service.md)

