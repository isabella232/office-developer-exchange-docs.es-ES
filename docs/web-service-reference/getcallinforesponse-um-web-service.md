---
title: GetCallInfoResponse (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetCallInfoResponse
api_type:
- schema
ms.assetid: aa5196bf-f5f3-455c-94ea-304fb7920c79
description: El elemento GetCallInfoResponse define una respuesta a una solicitud de GetCallInfo (servicio Web de mensajería unificada).
ms.openlocfilehash: 6e54ec61a9a5ebecd96bbd39dad68f8cc011b8a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461208"
---
# <a name="getcallinforesponse-um-web-service"></a>GetCallInfoResponse (servicio Web de mensajería unificada)

El elemento **GetCallInfoResponse** define una respuesta a una solicitud de [GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md) . 
  
[GetCallInfoResponse (servicio Web de mensajería unificada)](getcallinforesponse-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <CallState/>
  <EventCause/>
</GetCallInfoResponse>
```

 **UMCallInfo**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|CallState  <br/> |Contiene un valor que indica el estado de una llamada para la que la [operación GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md) ha solicitado información.  <br/> |
|EventCause  <br/> |Contiene un valor que indica la causa de un evento para una llamada para la que la [operación GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md) solicita información.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguna.
  
## <a name="text-value"></a>Valor de texto

Ninguna.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md)
  
[CallState (servicio Web de mensajería unificada)](callstate-um-web-service.md)
  
[EventCause (servicio Web de mensajería unificada)](eventcause-um-web-service.md)

