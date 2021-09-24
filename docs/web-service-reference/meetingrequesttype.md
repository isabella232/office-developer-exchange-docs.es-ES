---
title: MeetingRequestType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MeetingRequestType
api_type:
- schema
ms.assetid: bcd5c97c-19aa-4b1d-a8e8-e8c4bd473dd9
description: El elemento MeetingRequestType describe el tipo de la solicitud de reunión.
ms.openlocfilehash: 1a8371331691bb9dee5595b0130ec0c3c75c47c5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539377"
---
# <a name="meetingrequesttype"></a>MeetingRequestType

El **elemento MeetingRequestType** describe el tipo de la solicitud de reunión. 
  
```xml
<MeetingRequestType/>
```

 **MeetingRequestTypeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. En la tabla siguiente se enumeran los posibles valores de texto para este elemento.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|FullUpdate  <br/> |Identifica la solicitud de reunión como una actualización completa de una solicitud existente. Una actualización completa tiene el tiempo actualizado y el contenido informativo.  <br/> |
|InformationalUpdate  <br/> |Identifica la solicitud de reunión como solo que contiene contenido informativo actualizado.  <br/> |
|NewMeetingRequest  <br/> |Identifica la solicitud de reunión como una nueva solicitud de reunión.  <br/> |
|Ninguno  <br/> |Indica que el tipo de solicitud de reunión no está definido.  <br/> |
|Obsoleto  <br/> |Identifica la solicitud de reunión como obsoleta.  <br/> |
|PrincipalWantsCopy  <br/> |Indica que la solicitud de reunión pertenece a una entidad de seguridad que reenvía mensajes de reunión a un delegado y tiene sus copias marcadas como informativos.  <br/> |
|SilentUpdate  <br/> |Identifica la solicitud de reunión como una actualización silenciosa de una reunión existente.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

