---
title: CallId (servicio web de mensajería unificada)
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
description: El elemento CallId contiene el valor que representa el identificador de la llamada en una solicitud de GetCallInfo (servicio web de mensajería unificada) o la solicitud de desconexión (servicio web de mensajería unificada).
ms.openlocfilehash: 49690f41b9a002b05c7c9b1a1240073c7230ab92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763720"
---
# <a name="callid-um-web-service"></a>CallId (servicio web de mensajería unificada)

El elemento **CallId** contiene el valor que representa el identificador de la llamada en una solicitud de [GetCallInfo (servicio web de mensajería unificada)](getcallinfo-um-web-service.md) o una solicitud de [desconexión (servicio web de mensajería unificada)](disconnect-um-web-service.md) . 
  
[GetCallInfo (servicio web de mensajería unificada)](getcallinfo-um-web-service.md)
  
[CallId (servicio web de mensajería unificada)](callid-um-web-service.md)
  
[Desconectar (servicio web de mensajería unificada)](disconnect-um-web-service.md)
  
[CallId (servicio web de mensajería unificada)](callid-um-web-service.md)
  
```xml
<CallId/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetCallInfo (servicio web de mensajería unificada)](getcallinfo-um-web-service.md) <br/> |Define una solicitud para obtener información acerca de una llamada.  <br/> |
|[Desconectar (servicio web de mensajería unificada)](disconnect-um-web-service.md) <br/> |Define una solicitud para desconectar la llamada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor de texto representa el identificador para una llamada.
  
## <a name="remarks"></a>Notas

Para inicial de una llamada, use la [operación de PlayOnPhone (servicio web de mensajería unificada)](playonphone-operation-um-web-service.md) o [PlayOnPhoneGreeting (servicio web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md). Use el valor de texto que se devuelve en los elementos [PlayOnPhoneResponse (servicio web de mensajería unificada)](playonphoneresponse-um-web-service.md) o [PlayOnPhoneGreetingResponse (servicio web de mensajería unificada)](playonphonegreetingresponse-um-web-service.md) para el valor de texto del elemento **CallId** . 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md)
  
[(Servicio web de mensajería unificada) de la operación de desconexión](disconnect-operation-um-web-service.md)
  
[Operación PlayOnPhone (servicio web de mensajería unificada)](playonphone-operation-um-web-service.md)
  
[Operación PlayOnPhoneGreeting (servicio web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md)

