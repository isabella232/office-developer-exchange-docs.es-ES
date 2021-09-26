---
title: 'Status (servicio web de mensajería unificada: SetOofStatus)'
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- Status
api_type:
- schema
ms.assetid: 893bcff1-ccdc-493f-b366-ce8a68c813bd
description: El elemento Status define el valor que se usará en una solicitud de operación SetOofStatus (servicio web de mensajería unificada).
ms.openlocfilehash: fc4806e4978ae51ec6113ff8fd45da7db223a071
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546941"
---
# <a name="status-um-web-service---setoofstatus"></a>Status (servicio web de mensajería unificada: SetOofStatus)

El **elemento Status** define el valor que se usará en una solicitud de operación [SetOofStatus (servicio web de](setoofstatus-operation-um-web-service.md) mensajería unificada). 
  
[SetOofStatus (servicio web de mensajería unificada)](setoofstatus-um-web-service.md)
  
[Status (servicio web de mensajería unificada: SetOofStatus)](status-um-web-servicesetoofstatus.md)
  
```xml
<SetOofStatus>
  <status/>
</SetOofStatus>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SetOofStatus (servicio web de mensajería unificada)](setoofstatus-um-web-service.md) <br/> |Define una solicitud para establecer el estado de mensajería unificada fuera de Office (OOF) para el usuario que realiza la solicitud.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor booleano. Los valores posibles son los siguientes:
  
- Verdadero
    
- Falso
    
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



[Operación SetOofStatus (servicio web de mensajería unificada)](setoofstatus-operation-um-web-service.md)

