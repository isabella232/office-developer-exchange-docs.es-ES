---
title: PlayOnPhoneGreeting (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- PlayOnPhoneGreeting
api_type:
- schema
ms.assetid: 43eda596-3609-4e1b-8502-1db2636535cf
description: El elemento PlayOnPhoneGreeting define una solicitud para reproducir un saludo de mensajería unificada en un teléfono.
ms.openlocfilehash: e3b6a7720be6d046a379af460adbcc88725c0ea3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543124"
---
# <a name="playonphonegreeting-um-web-service"></a>PlayOnPhoneGreeting (servicio web de mensajería unificada)

El **elemento PlayOnPhoneGreeting** define una solicitud para reproducir un saludo de mensajería unificada en un teléfono. 
  
[PlayOnPhoneGreeting (servicio web de mensajería unificada)](playonphonegreeting-um-web-service.md)
  
```xml
<PlayOnPhoneGreeting>
  <GreetingType/>
  <DialString/>
</PlayOnPhoneGreeting>
```

 **complexType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GreetingType (servicio web de mensajería unificada)](greetingtype-um-web-service.md) <br/> |Define el tipo de saludo que se usará en una [solicitud de operación PlayOnPhoneGreeting (servicio web de](playonphonegreeting-operation-um-web-service.md) mensajería unificada).  <br/> |
|[dialString (servicio web de mensajería unificada)](dialstring-um-web-service.md) <br/> |Contiene el valor del número de teléfono que se debe marcar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

Ninguna.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



[Operación PlayOnPhoneGreeting (servicio web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md)

