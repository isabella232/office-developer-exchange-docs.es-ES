---
title: OofStatus (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- OofStatus
api_type:
- schema
ms.assetid: 0ba4225a-784e-4e6e-bd20-be45f0f7597c
description: El elemento OofStatus contiene un valor que indicaties el estado fuera de la oficina de mensajería unificada para el usuario que realiza una solicitud de GetUMProperties (servicio Web de mensajería unificada).
ms.openlocfilehash: 80b1d5aa508579eec14637ed10c322b5fbb670da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460578"
---
# <a name="oofstatus-um-web-service"></a>OofStatus (servicio Web de mensajería unificada)

El elemento **OofStatus** contiene un valor que indicaties el estado fuera de la oficina de mensajería unificada para el usuario que realiza una solicitud de [GetUMProperties (servicio Web de mensajería unificada)](getumproperties-operation-um-web-service.md) . 
  
[GetUMPropertiesResponse (servicio Web de mensajería unificada)](getumpropertiesresponse-um-web-service.md)
  
[OofStatus (servicio Web de mensajería unificada)](oofstatus-um-web-service.md)
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetUMPropertiesResponse (servicio Web de mensajería unificada)](getumpropertiesresponse-um-web-service.md) <br/> |Define una respuesta a una solicitud de [operación de GetUMProperties (servicio Web de mensajería unificada)](getumproperties-operation-um-web-service.md) .  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto booleano. Los valores posibles son los siguientes:
  
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



[Operación GetUMProperties (servicio Web de mensajería unificada)](getumproperties-operation-um-web-service.md)
  
[GetUMPropertiesResponse (servicio Web de mensajería unificada)](getumpropertiesresponse-um-web-service.md)

