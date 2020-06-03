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
description: El elemento RoutingType define el tipo de dirección para el buzón.
ms.openlocfilehash: d4229f2857a5c99cc9bb7ff9b9b103de099a0055
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465089"
---
# <a name="routingtype-emailaddresstype"></a>RoutingType (EmailAddressType)

El elemento **RoutingType** define el tipo de dirección para el buzón. 
  
```XML
<RoutingType/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Acciones](actingas.md) <br/> |Identifica quién envía el autor de la llamada.  <br/> |
|[Buzón](mailbox.md) <br/> |Identifica una dirección de correo electrónico completamente resuelta.  <br/> |
|[RoomList](roomlist.md) <br/> |Identifica una lista de salas de reuniones.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa un tipo de enrutamiento. SMTP es el valor de texto típico de este elemento.
  
## <a name="remarks"></a>Comentarios

Este elemento es opcional en el elemento [Mailbox](mailbox.md) . Se usa otro elemento [RoutingType (EmailAddress)](routingtype-emailaddress.md) para las operaciones de disponibilidad. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

