---
title: GetUMPropertiesResponse (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetUMPropertiesResponse
api_type:
- schema
ms.assetid: fcd93ce5-7403-46a9-b46e-56d2ebdd2f79
description: El elemento GetUMPropertiesResponse define una respuesta a una solicitud de GetUMProperties operación (servicio web de mensajería unificada).
ms.openlocfilehash: c0df872ad6b8e6541fa750ab87f4c1e5f0118b00
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835685"
---
# <a name="getumpropertiesresponse-um-web-service"></a>GetUMPropertiesResponse (servicio web de mensajería unificada)

El elemento **GetUMPropertiesResponse** define una respuesta a una solicitud de [operación GetUMProperties (servicio web de mensajería unificada)](getumproperties-operation-um-web-service.md) . 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[MissedCallNotificationEnabled (servicio web de mensajería unificada)](missedcallnotificationenabled-um-web-service.md) <br/> |Indica si están habilitadas las notificaciones de llamadas perdidas.  <br/> |
|[PlayOnPhoneDialString (servicio web de mensajería unificada)](playonphonedialstring-um-web-service.md) <br/> |Contiene la cadena de marcado predeterminado que se usará para la [operación de PlayOnPhone (servicio web de mensajería unificada)](playonphone-operation-um-web-service.md) y el [funcionamiento de PlayOnPhoneGreeting (servicio web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md).  <br/> |
|[TelephoneAccessNumbers (servicio web de mensajería unificada)](telephoneaccessnumbers-um-web-service.md) <br/> |Contiene la lista de números de teléfono que el usuario puede utilizar para tener acceso a mensajería unificada a través de un teléfono.  <br/> |
|[TelephoneAccessFolderEmail (servicio web de mensajería unificada)](telephoneaccessfolderemail-um-web-service.md) <br/> |Contiene el identificador de la carpeta de correo electrónico desde la que mensajería unificada va a leer los mensajes a través del teléfono.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUMProperties (servicio web de mensajería unificada)](getumproperties-operation-um-web-service.md)

