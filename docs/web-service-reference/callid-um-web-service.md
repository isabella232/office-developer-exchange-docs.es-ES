---
title: CallId (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- CallId
api_type:
- schema
ms.assetid: 2e044109-8bf3-488c-a654-459ac62fa1e7
description: El elemento CallId contiene el valor que representa el identificador de la llamada en una solicitud de desconexión (servicio Web de mensajería unificada) o solicitud de GetCallInfo (servicio Web de mensajería unificada).
ms.openlocfilehash: 5d5f596d4a98cbfb4b53be04278dae2305fc10c3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529458"
---
# <a name="callid-um-web-service"></a>CallId (servicio Web de mensajería unificada)

El elemento **CallId** contiene el valor que representa el identificador de la llamada en una solicitud de [desconexión (servicio Web de mensajería unificada](disconnect-um-web-service.md) ) o solicitud de [GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-um-web-service.md) . 
  
[GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-um-web-service.md)
  
[CallId (servicio Web de mensajería unificada)](callid-um-web-service.md)
  
[Disconnect (servicio Web de mensajería unificada)](disconnect-um-web-service.md)
  
[CallId (servicio Web de mensajería unificada)](callid-um-web-service.md)
  
```xml
<CallId/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-um-web-service.md) <br/> |Define una solicitud para obtener información sobre una llamada.  <br/> |
|[Disconnect (servicio Web de mensajería unificada)](disconnect-um-web-service.md) <br/> |Define una solicitud para desconectar una llamada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor de texto representa el identificador de una llamada.
  
## <a name="remarks"></a>Comentarios

Para iniciar una llamada, use la [operación reproducir (servicio Web de mensajería unificada)](playonphone-operation-um-web-service.md) o la [operación PlayOnPhoneGreeting (servicio Web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md). Use el valor de texto que se devuelve en los elementos [PlayOnPhoneResponse (servicio Web de mensajería unificada)](playonphoneresponse-um-web-service.md) o [PlayOnPhoneGreetingResponse (servicio Web de mensajería unificada)](playonphonegreetingresponse-um-web-service.md) para el valor de texto del elemento **CallId** . 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md)
  
[Operación Disconnect (servicio Web de mensajería unificada)](disconnect-operation-um-web-service.md)
  
[Operación reproducir (servicio Web de mensajería unificada)](playonphone-operation-um-web-service.md)
  
[Operación PlayOnPhoneGreeting (servicio Web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md)

