---
title: GetCallInfoResponse (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- GetCallInfoResponse
api_type:
- schema
ms.assetid: aa5196bf-f5f3-455c-94ea-304fb7920c79
description: El elemento GetCallInfoResponse define una respuesta a una solicitud de operación GetCallInfo (servicio web de mensajería unificada).
ms.openlocfilehash: 4b631bdee87e57c1612e906c725adabb9f9ce63e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526192"
---
# <a name="getcallinforesponse-um-web-service"></a>GetCallInfoResponse (servicio web de mensajería unificada)

El **elemento GetCallInfoResponse** define una respuesta a una solicitud de operación [GetCallInfo (servicio web de](getcallinfo-operation-um-web-service.md) mensajería unificada). 
  
[GetCallInfoResponse (servicio web de mensajería unificada)](getcallinforesponse-um-web-service.md)
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|CallState  <br/> |Contiene un valor que indica el estado de una llamada para la que la operación [GetCallInfo (servicio web](getcallinfo-operation-um-web-service.md) de mensajería unificada) solicitó información.  <br/> |
|EventCause  <br/> |Contiene un valor que indica la causa de un evento para una llamada para la que la operación [GetCallInfo (servicio web](getcallinfo-operation-um-web-service.md) de mensajería unificada) solicitó información.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md)
  
[CallState (servicio web de mensajería unificada)](callstate-um-web-service.md)
  
[EventCause (servicio web de mensajería unificada)](eventcause-um-web-service.md)

