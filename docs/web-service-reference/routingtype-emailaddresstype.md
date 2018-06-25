---
title: RoutingType (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoutingType
api_type:
- schema
ms.assetid: 683216be-9972-4f48-a148-c34bfe7f53e5
description: El elemento RoutingType define el tipo de dirección para el buzón de correo.
ms.openlocfilehash: a02c3b5711a657311428d67cccabd9c8c231db67
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837256"
---
# <a name="routingtype-emailaddresstype"></a>RoutingType (EmailAddressType)

El elemento **RoutingType** define el tipo de dirección para el buzón de correo. 
  
```XML
<RoutingType/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ActingAs](actingas.md) <br/> |Identifique quién envía como el autor de la llamada.  <br/> |
|[Buzón de correo](mailbox.md) <br/> |Identifica una dirección de correo electrónico completa resuelta.  <br/> |
|[RoomList](roomlist.md) <br/> |Identifica una lista de las salas de reuniones.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa un tipo de distribución. SMTP es el valor de texto típico para este elemento.
  
## <a name="remarks"></a>Comentarios

Este elemento es opcional en el elemento de [buzón de correo](mailbox.md) . Otro elemento de [RoutingType (EmailAddress)](routingtype-emailaddress.md) se usa para operaciones de disponibilidad. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

