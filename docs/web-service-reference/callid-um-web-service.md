---
title: CallId (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- CallId
api_type:
- schema
ms.assetid: 2e044109-8bf3-488c-a654-459ac62fa1e7
description: El elemento CallId contiene el valor que representa el identificador de la llamada en una solicitud GetCallInfo (servicio web de mensajería unificada) o una solicitud Disconnect (servicio web de mensajería unificada).
ms.openlocfilehash: c19f1061d81bf7683fd2c84fb1c6968826046be6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522036"
---
# <a name="callid-um-web-service"></a>CallId (servicio web de mensajería unificada)

El **elemento CallId** contiene el valor que representa el identificador de la llamada en una solicitud [GetCallInfo (servicio web](getcallinfo-um-web-service.md) de mensajería unificada) o una solicitud Disconnect [(servicio web de](disconnect-um-web-service.md) mensajería unificada). 
  
[GetCallInfo (servicio web de mensajería unificada)](getcallinfo-um-web-service.md)
  
[CallId (servicio web de mensajería unificada)](callid-um-web-service.md)
  
[Disconnect (servicio web de mensajería unificada)](disconnect-um-web-service.md)
  
[CallId (servicio web de mensajería unificada)](callid-um-web-service.md)
  
```xml
<CallId/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetCallInfo (servicio web de mensajería unificada)](getcallinfo-um-web-service.md) <br/> |Define una solicitud para obtener información sobre una llamada.  <br/> |
|[Disconnect (servicio web de mensajería unificada)](disconnect-um-web-service.md) <br/> |Define una solicitud para desconectar una llamada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor de texto representa el identificador de una llamada.
  
## <a name="remarks"></a>Comentarios

Para inicializar una llamada, use la operación [PlayOnPhone (servicio web](playonphone-operation-um-web-service.md) de mensajería unificada) o [la operación PlayOnPhoneGreeting (servicio web de](playonphonegreeting-operation-um-web-service.md)mensajería unificada). Use el valor de texto que se devuelve en los [elementos PlayOnPhoneResponse (servicio web](playonphoneresponse-um-web-service.md) de mensajería unificada) o [PlayOnPhoneGreetingResponse (servicio web](playonphonegreetingresponse-um-web-service.md) de mensajería unificada) para el valor de texto del elemento **CallId.** 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetCallInfo (servicio web de mensajería unificada)](getcallinfo-operation-um-web-service.md)
  
[Operación Disconnect (servicio web de mensajería unificada)](disconnect-operation-um-web-service.md)
  
[Operación PlayOnPhone (servicio web de mensajería unificada)](playonphone-operation-um-web-service.md)
  
[Operación PlayOnPhoneGreeting (servicio web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md)

