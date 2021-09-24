---
title: SetPlayOnPhoneDialString (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- SetPlayOnPhoneDialString
api_type:
- schema
ms.assetid: 513a5072-c3ac-405f-98c2-0ab982d0a360
description: El elemento SetPlayOnPhoneDialString define una solicitud para establecer la cadena de marcado predeterminada para las solicitudes de operación playOnPhone (servicio web de mensajería unificada) y operación PlayOnPhoneGreeting (servicio web de mensajería unificada).
ms.openlocfilehash: e485fd092da29a3f54b1acc2b7e50167084e13fa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540506"
---
# <a name="setplayonphonedialstring-um-web-service"></a>SetPlayOnPhoneDialString (servicio web de mensajería unificada)

El **elemento SetPlayOnPhoneDialString** define una solicitud para establecer la cadena de marcado predeterminada para las solicitudes de operación [playOnPhone (servicio web](playonphone-operation-um-web-service.md) de mensajería unificada) y operación [PlayOnPhoneGreeting (servicio web](playonphonegreeting-operation-um-web-service.md) de mensajería unificada). 
  
[SetPlayOnPhoneDialString (servicio web de mensajería unificada)](setplayonphonedialstring-um-web-service.md)
  
```xml
<SetPlayOnPhoneDialString>
  <dialString>   </dialString>
</SetPlayOnPhoneDialString>
```

 **complexType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[dialString (servicio web de mensajería unificada)](dialstring-um-web-service.md) <br/> |Número de teléfono que se establecerá como cadena de marcado predeterminada.  <br/> |
   
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



[Operación SetPlayOnPhoneDialString (servicio web de mensajería unificada)](setplayonphonedialstring-operation-um-web-service.md)

