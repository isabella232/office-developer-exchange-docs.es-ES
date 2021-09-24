---
title: OofStatus (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- OofStatus
api_type:
- schema
ms.assetid: 0ba4225a-784e-4e6e-bd20-be45f0f7597c
description: El elemento OofStatus contiene un valor que indica el estado de mensajería unificada fuera de Office para el usuario que realiza una solicitud de operación GetUMProperties (servicio web de mensajería unificada).
ms.openlocfilehash: 4e899317defdb4ac4c27c3fdc17d7b7222dff6a7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539272"
---
# <a name="oofstatus-um-web-service"></a>OofStatus (servicio web de mensajería unificada)

El **elemento OofStatus** contiene un valor que indica el estado de mensajería unificada fuera de Office para el usuario que realiza una solicitud de operación [GetUMProperties (servicio web](getumproperties-operation-um-web-service.md) de mensajería unificada). 
  
[GetUMPropertiesResponse (servicio web de mensajería unificada)](getumpropertiesresponse-um-web-service.md)
  
[OofStatus (servicio web de mensajería unificada)](oofstatus-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
    <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
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
|[GetUMPropertiesResponse (servicio web de mensajería unificada)](getumpropertiesresponse-um-web-service.md) <br/> |Define una respuesta a una [solicitud de operación GetUMProperties (servicio web de](getumproperties-operation-um-web-service.md) mensajería unificada).  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto booleano. Los valores posibles son los siguientes:
  
- Verdadero
    
- Falso
    
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUMProperties (servicio web de mensajería unificada)](getumproperties-operation-um-web-service.md)
  
[GetUMPropertiesResponse (servicio web de mensajería unificada)](getumpropertiesresponse-um-web-service.md)

