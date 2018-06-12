---
title: Estado (servicio web de mensajería unificada - SetOofStatus)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Status
api_type:
- schema
ms.assetid: 893bcff1-ccdc-493f-b366-ce8a68c813bd
description: El elemento Status define el valor que se utilizará en una solicitud de SetOofStatus operación (servicio web de mensajería unificada).
ms.openlocfilehash: 57b4f8fe1a64341b1c2ae0a06bc98f1c9cfd28c4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837583"
---
# <a name="status-um-web-service---setoofstatus"></a>Estado (servicio web de mensajería unificada - SetOofStatus)

El elemento **Status** define el valor que se utilizará en una solicitud de [operación SetOofStatus (servicio web de mensajería unificada)](setoofstatus-operation-um-web-service.md) . 
  
[SetOofStatus (servicio web de mensajería unificada)](setoofstatus-um-web-service.md)
  
[Estado (servicio web de mensajería unificada - SetOofStatus)](status-um-web-servicesetoofstatus.md)
  
```xml
<SetOofStatus>
  <status/>
</SetOofStatus>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[SetOofStatus (servicio web de mensajería unificada)](setoofstatus-um-web-service.md) <br/> |Define una solicitud para establecer el estado de Unified Messaging fuera de oficina (OOF) del usuario que realiza la solicitud.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Es necesario un valor Boolean. Los valores posibles son:
  
- Verdadero
    
- False
    
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación SetOofStatus (servicio web de mensajería unificada)](setoofstatus-operation-um-web-service.md)

