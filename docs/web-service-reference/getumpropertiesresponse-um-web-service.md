---
title: GetUMPropertiesResponse (servicio Web de mensajería unificada)
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
description: El elemento GetUMPropertiesResponse define una respuesta a una solicitud de GetUMProperties (servicio Web de mensajería unificada).
ms.openlocfilehash: 3247489a305c694c10764d7a0c6f02b1fad51ebf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459128"
---
# <a name="getumpropertiesresponse-um-web-service"></a>GetUMPropertiesResponse (servicio Web de mensajería unificada)

El elemento **GetUMPropertiesResponse** define una respuesta a una solicitud de [GetUMProperties (servicio Web de mensajería unificada)](getumproperties-operation-um-web-service.md) . 
  
[GetUMPropertiesResponse (servicio Web de mensajería unificada)](getumpropertiesresponse-um-web-service.md)
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MissedCallNotificationEnabled (servicio Web de mensajería unificada)](missedcallnotificationenabled-um-web-service.md) <br/> |Indica si las notificaciones de llamadas perdidas están habilitadas.  <br/> |
|[PlayOnPhoneDialString (servicio Web de mensajería unificada)](playonphonedialstring-um-web-service.md) <br/> |Contiene la cadena de marcado predeterminada que se debe usar para la [operación reproducir (servicio Web de mensajería unificada)](playonphone-operation-um-web-service.md) y la [operación PlayOnPhoneGreeting (servicio Web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md).  <br/> |
|[TelephoneAccessNumbers (servicio Web de mensajería unificada)](telephoneaccessnumbers-um-web-service.md) <br/> |Contiene la lista de números de teléfono que el usuario puede usar para tener acceso a la mensajería unificada a través de un teléfono.  <br/> |
|[TelephoneAccessFolderEmail (servicio Web de mensajería unificada)](telephoneaccessfolderemail-um-web-service.md) <br/> |Contiene el identificador de la carpeta de correo electrónico desde la que la mensajería unificada leerá los mensajes a través del teléfono.  <br/> |
   
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



[Operación GetUMProperties (servicio Web de mensajería unificada)](getumproperties-operation-um-web-service.md)

