---
title: PlayOnPhoneResponse (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhoneResponse
api_type:
- schema
ms.assetid: 42b16880-1271-4690-abd0-0072d95b04b7
description: El elemento PlayOnPhoneResponse define una respuesta a una solicitud de reproducir (servicio Web de mensajería unificada).
ms.openlocfilehash: ddb9cc9a8feaeb476e6502339fdc74d024797b9b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459619"
---
# <a name="playonphoneresponse-um-web-service"></a>PlayOnPhoneResponse (servicio Web de mensajería unificada)

El elemento **PlayOnPhoneResponse** define una respuesta a una solicitud de [reproducir (servicio Web de mensajería unificada)](playonphone-operation-um-web-service.md) . 
  
[PlayOnPhoneResponse (servicio Web de mensajería unificada)](playonphoneresponse-um-web-service.md)
  
```xml
<PlayOnPhoneResponse />
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

Ninguna.
  
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor de texto es el identificador de llamada que se va a usar para el valor de [CallId (servicio Web de mensajería unificada)](callid-um-web-service.md) en una solicitud de [GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md) o una solicitud de [desconexión (servicio Web de mensajería unificada)](disconnect-operation-um-web-service.md) . 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación reproducir (servicio Web de mensajería unificada)](playonphone-operation-um-web-service.md)

