---
title: MeetingRequestType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingRequestType
api_type:
- schema
ms.assetid: bcd5c97c-19aa-4b1d-a8e8-e8c4bd473dd9
description: El elemento MeetingRequestType describe el tipo de la convocatoria de reunión.
ms.openlocfilehash: 7269587e2fa72aeb9070a7b53ee9215829729329
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836432"
---
# <a name="meetingrequesttype"></a>MeetingRequestType

El elemento **MeetingRequestType** describe el tipo de la convocatoria de reunión. 
  
```xml
<MeetingRequestType/>
```

 **MeetingRequestTypeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. En la siguiente tabla se enumera los posibles valores de texto para este elemento.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|FullUpdate  <br/> |Identifica la convocatoria de reunión como una actualización completa a una solicitud de existente. Se actualizó una actualización completa tiempo y contenido informativo.  <br/> |
|InformationalUpdate  <br/> |Identifica la convocatoria de reunión como sólo que contiene el contenido informativo actualizado.  <br/> |
|NewMeetingRequest  <br/> |Identifica la convocatoria de reunión como una nueva convocatoria de reunión.  <br/> |
|None  <br/> |Indica que el tipo de solicitud de la reunión no se ha definido.  <br/> |
|Obsoleto  <br/> |Identifica la convocatoria de reunión como obsoleto.  <br/> |
|PrincipalWantsCopy  <br/> |Indica que la convocatoria de reunión pertenece a una entidad de seguridad que se reenvió los mensajes de reunión a un delegado y tiene sus copias marcados como informativos.  <br/> |
|SilentUpdate  <br/> |Identifica la convocatoria de reunión como una actualización silenciosa a una reunión existente.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

