---
title: ResponseType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResponseType
api_type:
- schema
ms.assetid: cdc09dda-ce20-4504-880d-9da6025ca812
description: El elemento ResponseType representa el tipo de respuesta de destinatario que se recibe para una reunión.
ms.openlocfilehash: d986eff544dc55d257903a2114e87af16eefea97
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518970"
---
# <a name="responsetype"></a>ResponseType

El **elemento ResponseType** representa el tipo de respuesta de destinatario que se recibe para una reunión. 
  
```xml
<ResponseType/>
```

 **ResponseTypeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Attendee](attendee.md) <br/> |Representa los asistentes y los recursos de una reunión.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el Exchange de reuniones  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa un mensaje de reunión en el Exchange almacén.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta de reunión en Exchange almacén.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Los siguientes son los valores de texto posibles para este elemento:
  
- Unknown
    
- Organizador
    
- Provisional
    
- Aceptar
    
- Declinar
    
- NoResponseReceived
    
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

