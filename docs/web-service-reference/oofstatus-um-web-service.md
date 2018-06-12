---
title: OofStatus (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- OofStatus
api_type:
- schema
ms.assetid: 0ba4225a-784e-4e6e-bd20-be45f0f7597c
description: El elemento OofStatus contiene un valor que indicaties el estado de Unified Messaging fuera de la oficina del usuario que está realizando una solicitud de GetUMProperties operación (servicio web de mensajería unificada).
ms.openlocfilehash: 1fe358a8bfea3c509220d6705a238ae832de37e8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836650"
---
# <a name="oofstatus-um-web-service"></a>OofStatus (servicio web de mensajería unificada)

El elemento **OofStatus** contiene un valor que indicaties el estado de Unified Messaging fuera de la oficina del usuario que está realizando una solicitud de [operación GetUMProperties (servicio web de mensajería unificada)](getumproperties-operation-um-web-service.md) . 
  
[GetUMPropertiesResponse (servicio web de mensajería unificada)](getumpropertiesresponse-um-web-service.md)
  
[OofStatus (servicio web de mensajería unificada)](oofstatus-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
    <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetUMPropertiesResponse (servicio web de mensajería unificada)](getumpropertiesresponse-um-web-service.md) <br/> |Define una respuesta a una solicitud de [operación GetUMProperties (servicio web de mensajería unificada)](getumproperties-operation-um-web-service.md) .  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de tipo Boolean de texto. Los valores posibles son:
  
- Verdadero
    
- False
    
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUMProperties (servicio web de mensajería unificada)](getumproperties-operation-um-web-service.md)
  
[GetUMPropertiesResponse (servicio web de mensajería unificada)](getumpropertiesresponse-um-web-service.md)

