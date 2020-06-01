---
title: InternalUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4649baa9-eec9-426d-952b-361818c25fe0
description: El elemento InternalUrl contiene la dirección URL para conectar un cliente al servidor de la libreta de direcciones o al buzón de un usuario desde dentro de la organización del usuario mediante el protocolo MAPI/HTTP.
ms.openlocfilehash: 9c6ba621a681ec54d88089de6b7ae1eefdebc679
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465579"
---
# <a name="internalurl-pox"></a>InternalUrl (POX)

El elemento **InternalUrl** contiene la dirección URL para conectar un cliente al servidor de la libreta de direcciones o al buzón de un usuario desde dentro de la organización del usuario mediante el protocolo MAPI/http. 
  
```XML
<InternalUrl/>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AddressBook (POX)](addressbook-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al servidor de libreta de direcciones mediante el protocolo MAPI/HTTP.  <br/> |
|[MailStore (POX)](mailstore-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al buzón de correo del usuario mediante el protocolo MAPI/HTTP.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa una dirección URL que se puede usar para obtener acceso a un servidor de libreta de direcciones o a un buzón de correo de un usuario desde dentro de la organización del usuario.
  
## <a name="remarks"></a>Comentarios

El elemento **InternalUrl** puede estar presente en una respuesta que tiene un elemento [Protocol (POX)](protocol-pox.md) con un valor de atributo de **tipo** de "mapiHttp". 
  
El elemento **InternalUrl** está disponible para clientes que implementan el protocolo MAPI/http y tienen como objetivo Exchange Online, Exchange online como parte de Office 365 y versiones locales de Exchange que comienzan con la compilación 15.00.0847.032 (Exchange Server 2013 SP1). 
  
## <a name="see-also"></a>Vea también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

