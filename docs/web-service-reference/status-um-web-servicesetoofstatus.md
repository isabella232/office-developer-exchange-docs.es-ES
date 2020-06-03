---
title: Estado (servicio Web de mensajería unificada-SetOofStatus)
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
description: El elemento status define el valor que se debe usar en una solicitud de operación SetOofStatus (servicio Web de mensajería unificada).
ms.openlocfilehash: 865152baf28c22578664e16db2dcd5f82a04af98
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459983"
---
# <a name="status-um-web-service---setoofstatus"></a>Estado (servicio Web de mensajería unificada-SetOofStatus)

El elemento **status** define el valor que se debe usar en una solicitud de [operación SetOofStatus (servicio Web de mensajería unificada)](setoofstatus-operation-um-web-service.md) . 
  
[SetOofStatus (servicio Web de mensajería unificada)](setoofstatus-um-web-service.md)
  
[Estado (servicio Web de mensajería unificada-SetOofStatus)](status-um-web-servicesetoofstatus.md)
  
```xml
<SetOofStatus>
  <status/>
</SetOofStatus>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SetOofStatus (servicio Web de mensajería unificada)](setoofstatus-um-web-service.md) <br/> |Define una solicitud para establecer el estado fuera de la oficina de la mensajería unificada (OOF) del usuario que realiza la solicitud.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor booleano. Los valores posibles son los siguientes:
  
- Verdadero
    
- Falso
    
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación SetOofStatus (servicio Web de mensajería unificada)](setoofstatus-operation-um-web-service.md)

