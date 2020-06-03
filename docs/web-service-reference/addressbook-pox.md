---
title: AddressBook (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b2d62fd0-741c-4a41-9762-cc7d0ff01c9c
description: El elemento AddressBook contiene las especificaciones para conectar un cliente al servidor de libreta de direcciones mediante el protocolo MAPI/HTTP.
ms.openlocfilehash: 0967ac123cd3bb0086fd004ea0d0d37c08d2e037
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463639"
---
# <a name="addressbook-pox"></a>AddressBook (POX)

El elemento **AddressBook** contiene las especificaciones para conectar un cliente al servidor de libreta de direcciones mediante el protocolo MAPI/http. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[AddressBook (POX)](addressbook-pox.md)
  
```XML
<AddressBook>
   <ExternalUrl/>
   <InternalUrl/>
</AddressBook>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ExternalUrl (POX)](externalurl-pox.md) <br/> |Contiene la dirección URL que se debe usar para obtener acceso a la libreta de direcciones desde fuera de la red de la organización mediante el protocolo MAPI/HTTP.  <br/> |
|[InternalUrl (POX)](internalurl-pox.md) <br/> |Contiene la dirección URL que se debe usar para obtener acceso a la libreta de direcciones desde el interior de la red de la organización mediante el protocolo MAPI/HTTP.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al servidor de acceso de cliente.  <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento **AddressBook** está presente en una respuesta que tiene un elemento [Protocol (POX)](protocol-pox.md) con un valor de atributo de **tipo** de "mapiHttp". 
  
El elemento **AddressBook** está disponible para clientes que implementan el protocolo MAPI/http y tienen como objetivo Exchange Online, Exchange online como parte de Office 365 y versiones locales de Exchange que comienzan con la compilación 15.00.0847.032 (Exchange Server 2013 SP1). 
  
## <a name="see-also"></a>Vea también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

