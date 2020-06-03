---
title: MailStore (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af338f99-9e62-4124-9bff-8d7cc2008161
description: El elemento MailStore contiene las especificaciones para conectar un cliente al buzón de correo del usuario mediante el protocolo MAPI/HTTP.
ms.openlocfilehash: 635228fcfeb3ad791c845050b82666a6e060b229
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459794"
---
# <a name="mailstore-pox"></a>MailStore (POX)

El elemento **MailStore** contiene las especificaciones para conectar un cliente al buzón de correo del usuario mediante el protocolo MAPI/http. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[MailStore (POX)](mailstore-pox.md)
  
```XML
<MailStore>
   <ExternalUrl/>
   <InternalUrl/>
</MailStore>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ExternalUrl (POX)](externalurl-pox.md) <br/> |Contiene la dirección URL que se debe usar para obtener acceso al buzón de correo del usuario desde fuera de la red de la organización por medio del protocolo MAPI/HTTP.  <br/> |
|[InternalUrl (POX)](internalurl-pox.md) <br/> |Contiene la dirección URL que se debe usar para obtener acceso al buzón de correo del usuario desde dentro de la red de la organización por medio del protocolo MAPI/HTTP.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al servidor de acceso de cliente.  <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento **MailStore** está presente en una respuesta que tiene un elemento [Protocol (POX)](protocol-pox.md) con un valor de atributo de **tipo** de "mapiHttp". 
  
El elemento **MailStore** está disponible para los clientes que implementan el protocolo MAPI/http y tienen como objetivo Exchange Online, Exchange online como parte de Office 365 y las versiones locales de Exchange que comienzan con la compilación 15.00.0847.032 (exchange Server 2013 SP1). 
  
## <a name="see-also"></a>Vea también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

