---
title: MailStore (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: af338f99-9e62-4124-9bff-8d7cc2008161
description: El elemento MailStore contiene las especificaciones para conectar un cliente al buzón del usuario mediante el protocolo MAPI/HTTP.
ms.openlocfilehash: 543bcb8df84904f2b70d6feeabf16d1cc021f3e5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511128"
---
# <a name="mailstore-pox"></a>MailStore (POX)

El **elemento MailStore** contiene las especificaciones para conectar un cliente al buzón del usuario mediante el protocolo MAPI/HTTP. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ExternalUrl (POX)](externalurl-pox.md) <br/> |Contiene la dirección URL que se debe usar para tener acceso al buzón del usuario desde fuera de la red de la organización mediante el protocolo MAPI/HTTP.  <br/> |
|[InternalUrl (POX)](internalurl-pox.md) <br/> |Contiene la dirección URL que se debe usar para tener acceso al buzón del usuario desde dentro de la red de la organización mediante el protocolo MAPI/HTTP.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al servidor de acceso de cliente.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **elemento MailStore** está presente en una respuesta que tiene un elemento [Protocol (POX)](protocol-pox.md) con un valor de atributo **Type** de "mapiHttp". 
  
El **elemento MailStore** está disponible para clientes que implementan el protocolo MAPI/HTTP y el Exchange Online de destino, Exchange Online como parte de Office 365 y versiones locales de Exchange a partir de la compilación 15.00.0847.032 (Exchange Server 2013 SP1). 
  
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

