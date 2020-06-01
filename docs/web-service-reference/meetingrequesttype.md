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
description: El elemento MeetingRequestType describe el tipo de convocatoria de reunión.
ms.openlocfilehash: e90c44dd4124d698ca5ef7655f6429a7167673e6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44465789"
---
# <a name="meetingrequesttype"></a>MeetingRequestType

El elemento **MeetingRequestType** describe el tipo de convocatoria de reunión. 
  
```xml
<MeetingRequestType/>
```

 **MeetingRequestTypeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. En la siguiente tabla se enumeran los valores de texto posibles para este elemento.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|FullUpdate  <br/> |Identifica la convocatoria de reunión como una actualización completa de una solicitud existente. Una actualización completa ha actualizado el tiempo y el contenido informativo.  <br/> |
|InformationalUpdate  <br/> |Identifica la convocatoria de reunión como que solo contiene contenido informativo actualizado.  <br/> |
|NewMeetingRequest  <br/> |Identifica la convocatoria de reunión como una convocatoria de reunión nueva.  <br/> |
|Ninguno  <br/> |Indica que no se ha definido el tipo de convocatoria de reunión.  <br/> |
|Obsoleta  <br/> |Identifica la convocatoria de reunión como no actualizada.  <br/> |
|PrincipalWantsCopy  <br/> |Indica que la convocatoria de reunión pertenece a una entidad de identidad que ha reenviado mensajes de reunión a un delegado y tiene sus copias marcadas como informativas.  <br/> |
|SilentUpdate  <br/> |Identifica la convocatoria de reunión como una actualización silenciosa de una reunión existente.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

