---
title: SetPlayOnPhoneDialString (servicio web de mensajería unificada)
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
description: El elemento SetPlayOnPhoneDialString define una solicitud para establecer la cadena de marcado predeterminado para la operación de PlayOnPhone (servicio web de mensajería unificada) y las solicitudes de PlayOnPhoneGreeting operación (servicio web de mensajería unificada).
ms.openlocfilehash: fd82dc6ef0dd90a2318da93191f657005b7a5c87
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837450"
---
# <a name="setplayonphonedialstring-um-web-service"></a>SetPlayOnPhoneDialString (servicio web de mensajería unificada)

El elemento **SetPlayOnPhoneDialString** define una solicitud para establecer la cadena de marcado de forma predeterminada para las solicitudes de [la operación de PlayOnPhone (servicio web de mensajería unificada)](playonphone-operation-um-web-service.md) y [PlayOnPhoneGreeting (servicio web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md) . 
  
[SetPlayOnPhoneDialString (servicio web de mensajería unificada)](setplayonphonedialstring-um-web-service.md)
  
```xml
<SetPlayOnPhoneDialString>
  <dialString>   </dialString>
</SetPlayOnPhoneDialString>
```

 **complexType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[dialString (servicio web de mensajería unificada)](dialstring-um-web-service.md) <br/> |El número de teléfono para establecer como la cadena de marcado de forma predeterminada.  <br/> |
   
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
   
## <a name="see-also"></a>Vea también



[Operación SetPlayOnPhoneDialString (servicio web de mensajería unificada)](setplayonphonedialstring-operation-um-web-service.md)

