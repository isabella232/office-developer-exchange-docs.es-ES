---
title: GetUMPropertiesResponse (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- GetUMPropertiesResponse
api_type:
- schema
ms.assetid: fcd93ce5-7403-46a9-b46e-56d2ebdd2f79
description: El elemento GetUMPropertiesResponse define una respuesta a una solicitud de operación GetUMProperties (servicio web de mensajería unificada).
ms.openlocfilehash: 97c3850d46369d4ab533629a8b24e199db3dd44a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522967"
---
# <a name="getumpropertiesresponse-um-web-service"></a>GetUMPropertiesResponse (servicio web de mensajería unificada)

El **elemento GetUMPropertiesResponse** define una respuesta a una solicitud [de operación GetUMProperties (servicio web de](getumproperties-operation-um-web-service.md) mensajería unificada). 
  
[GetUMPropertiesResponse (servicio web de mensajería unificada)](getumpropertiesresponse-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
  <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 **UMProperties**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MissedCallNotificationEnabled (servicio web de mensajería unificada)](missedcallnotificationenabled-um-web-service.md) <br/> |Indica si las notificaciones de llamadas perdidas están habilitadas.  <br/> |
|[PlayOnPhoneDialString (servicio web de mensajería unificada)](playonphonedialstring-um-web-service.md) <br/> |Contiene la cadena de marcado predeterminada que se usará para la operación [PlayOnPhone (servicio web](playonphone-operation-um-web-service.md) de mensajería unificada) y [la operación PlayOnPhoneGreeting (servicio web de](playonphonegreeting-operation-um-web-service.md)mensajería unificada).  <br/> |
|[TelephoneAccessNumbers (servicio web de mensajería unificada)](telephoneaccessnumbers-um-web-service.md) <br/> |Contiene la lista de números de teléfono que el usuario puede usar para acceder a la mensajería unificada a través de un teléfono.  <br/> |
|[TelephoneAccessFolderEmail (servicio web de mensajería unificada)](telephoneaccessfolderemail-um-web-service.md) <br/> |Contiene el identificador de la carpeta de correo electrónico desde la que la mensajería unificada leerá los mensajes por teléfono.  <br/> |
   
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



[Operación GetUMProperties (servicio web de mensajería unificada)](getumproperties-operation-um-web-service.md)

