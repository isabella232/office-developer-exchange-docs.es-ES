---
title: Desconectar (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Disconnect
api_type:
- schema
ms.assetid: 2f8c1e8c-3bd4-4988-96b9-735c347b29f7
description: El elemento Desconectar define una solicitud para desconectar la llamada.
ms.openlocfilehash: 764532bdadd69caaa68406c84277197def3160af
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764209"
---
# <a name="disconnect-um-web-service"></a>Desconectar (servicio web de mensajería unificada)

El elemento **Desconectar** define una solicitud para desconectar la llamada. 
  
- [Desconectar (servicio web de mensajería unificada)](disconnect-um-web-service.md)
  
```xml
<Disconnect>
  <CallId>   </CallId>
</Disconnect>
```

 **complexType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[CallId (servicio web de mensajería unificada)](callid-um-web-service.md) <br/> |El identificador de la llamada a desconectar.  <br/> |
   
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

- [(Servicio web de mensajería unificada) de la operación de desconexión](disconnect-operation-um-web-service.md)  
- [Operación PlayOnPhone (servicio web de mensajería unificada)](playonphone-operation-um-web-service.md) 
- [Operación PlayOnPhoneGreeting (servicio web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md)  
- [CallId (servicio web de mensajería unificada)](callid-um-web-service.md)

