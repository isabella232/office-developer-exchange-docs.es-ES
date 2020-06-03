---
title: SetPlayOnPhoneDialString (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetPlayOnPhoneDialString
api_type:
- schema
ms.assetid: 513a5072-c3ac-405f-98c2-0ab982d0a360
description: El elemento SetPlayOnPhoneDialString define una solicitud para establecer la cadena de marcado predeterminada para las solicitudes de reproducir operación (servicio Web de mensajería unificada) y operación PlayOnPhoneGreeting (servicio Web de mensajería unificada).
ms.openlocfilehash: 40021e9dedafb5fafda91bf3612d8a6485dae8e7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458631"
---
# <a name="setplayonphonedialstring-um-web-service"></a>SetPlayOnPhoneDialString (servicio Web de mensajería unificada)

El elemento **SetPlayOnPhoneDialString** define una solicitud para establecer la cadena de marcado predeterminada para las solicitudes de [reproducir operación (servicio Web de mensajería unificada)](playonphone-operation-um-web-service.md) y [operación PlayOnPhoneGreeting (servicio Web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md) . 
  
[SetPlayOnPhoneDialString (servicio Web de mensajería unificada)](setplayonphonedialstring-um-web-service.md)
  
```xml
<SetPlayOnPhoneDialString>
  <dialString>   </dialString>
</SetPlayOnPhoneDialString>
```

 **complexType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[dialString (servicio Web de mensajería unificada)](dialstring-um-web-service.md) <br/> |El número de teléfono que se establece como la cadena de marcado predeterminada.  <br/> |
   
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



[Operación SetPlayOnPhoneDialString (servicio Web de mensajería unificada)](setplayonphonedialstring-operation-um-web-service.md)

