---
title: Disconnect (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- Disconnect
api_type:
- schema
ms.assetid: 2f8c1e8c-3bd4-4988-96b9-735c347b29f7
description: El elemento Disconnect define una solicitud para desconectar una llamada.
ms.openlocfilehash: 6aaff910d85a963a926e7c2a74a91963b120392c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538376"
---
# <a name="disconnect-um-web-service"></a>Disconnect (servicio web de mensajería unificada)

El **elemento Disconnect** define una solicitud para desconectar una llamada. 
  
- [Disconnect (servicio web de mensajería unificada)](disconnect-um-web-service.md)
  
```xml
<Disconnect>
  <CallId>   </CallId>
</Disconnect>
```

 **complexType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CallId (servicio web de mensajería unificada)](callid-um-web-service.md) <br/> |Identificador de la llamada a desconectar.  <br/> |
   
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

- [Operación Disconnect (servicio web de mensajería unificada)](disconnect-operation-um-web-service.md)  
- [Operación PlayOnPhone (servicio web de mensajería unificada)](playonphone-operation-um-web-service.md) 
- [Operación PlayOnPhoneGreeting (servicio web de mensajería unificada)](playonphonegreeting-operation-um-web-service.md)  
- [CallId (servicio web de mensajería unificada)](callid-um-web-service.md)

