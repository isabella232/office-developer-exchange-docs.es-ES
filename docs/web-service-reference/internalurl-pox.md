---
title: InternalUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4649baa9-eec9-426d-952b-361818c25fe0
description: El elemento InternalUrl contiene la dirección URL para conectar un cliente al servidor de libreta de direcciones o al buzón de un usuario desde dentro de la organización del usuario mediante el protocolo MAPI/HTTP.
ms.openlocfilehash: 4ce04743c7d0f260439849a02f8f6d389f6c83fa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542200"
---
# <a name="internalurl-pox"></a>InternalUrl (POX)

El **elemento InternalUrl** contiene la dirección URL para conectar un cliente al servidor de libreta de direcciones o al buzón de un usuario desde dentro de la organización del usuario mediante el protocolo MAPI/HTTP. 
  
```XML
<InternalUrl/>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AddressBook (POX)](addressbook-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al servidor de libreta de direcciones mediante el protocolo MAPI/HTTP.  <br/> |
|[MailStore (POX)](mailstore-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al buzón del usuario mediante el protocolo MAPI/HTTP.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa una dirección URL que se puede usar para obtener acceso a un servidor de libreta de direcciones o al buzón del usuario desde dentro de la organización del usuario.
  
## <a name="remarks"></a>Comentarios

El **elemento InternalUrl** puede estar presente en una respuesta que tiene un elemento [Protocol (POX)](protocol-pox.md) con un valor de atributo **Type** de "mapiHttp". 
  
El **elemento InternalUrl** está disponible para clientes que implementan el protocolo MAPI/HTTP y el Exchange Online de destino, Exchange Online como parte de Office 365 y versiones locales de Exchange a partir de la compilación 15.00.0847.032 (Exchange Server 2013 SP1). 
  
## <a name="see-also"></a>Consulte también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

