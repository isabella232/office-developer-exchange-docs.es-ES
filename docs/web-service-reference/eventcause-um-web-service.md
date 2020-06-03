---
title: EventCause (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- EventCause
api_type:
- schema
ms.assetid: 7b3c1db8-cad4-4050-a50d-b06f065db530
description: El elemento EventCause contiene un valor que indica la causa de un evento de llamada en una respuesta a una solicitud GetCallInfo (servicio Web de mensajería unificada).
ms.openlocfilehash: 9d49fd4b16236d0dd87889fbbd039f2e271a5968
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458680"
---
# <a name="eventcause-um-web-service"></a>EventCause (servicio Web de mensajería unificada)

El elemento **EventCause** contiene un valor que indica la causa de un evento de llamada en una respuesta a una solicitud [GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md) . 
  
[GetCallInfoResponse (servicio Web de mensajería unificada)](getcallinforesponse-um-web-service.md)
  
[EventCause (servicio Web de mensajería unificada)](eventcause-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <EventCause/>
</GetCallInfoResponse>
```

 **UMEventCause**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetCallInfoResponse (servicio Web de mensajería unificada)](getcallinforesponse-um-web-service.md) <br/> |Define una respuesta a una solicitud de [operación de GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md) .  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Los valores posibles son los siguientes:
  
- Ninguno
    
- UserBusy
    
- Noanswer
    
- Otros
    
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse (servicio Web de mensajería unificada)](getcallinforesponse-um-web-service.md)

