---
title: Libreta de direcciones (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b2d62fd0-741c-4a41-9762-cc7d0ff01c9c
description: El elemento de la libreta de direcciones contiene las especificaciones para conectar a un cliente con el servidor de la libreta de direcciones mediante el protocolo HTTP/MAPI.
ms.openlocfilehash: c30f0ee7c36de7e63157d07d003a11187d661fd7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763411"
---
# <a name="addressbook-pox"></a>Libreta de direcciones (POX)

El elemento de la **Libreta de direcciones** contiene las especificaciones para conectar a un cliente con el servidor de la libreta de direcciones mediante el protocolo HTTP/MAPI. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[Libreta de direcciones (POX)](addressbook-pox.md)
  
```XML
<AddressBook>
   <ExternalUrl/>
   <InternalUrl/>
</AddressBook>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ExternalUrl (POX)](externalurl-pox.md) <br/> |Contiene la dirección URL que se debe utilizar para tener acceso a la libreta de direcciones desde fuera de la red de la organización mediante el protocolo HTTP/MAPI.  <br/> |
|[InternalUrl (POX)](internalurl-pox.md) <br/> |Contiene la dirección URL que se debe utilizar para tener acceso a la libreta de direcciones desde dentro de la red de la organización mediante el protocolo HTTP/MAPI.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente con el servidor de acceso de cliente.  <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento de la **Libreta de direcciones** está presente en una respuesta que tiene un elemento de [Protocolo (POX)](protocol-pox.md) con un valor de atributo de **tipo** de "mapiHttp". 
  
El elemento de la **Libreta de direcciones** está disponible para los clientes que implementan el protocolo HTTP/MAPI y destino Exchange Online, Exchange Online como parte de Office 365, y las versiones locales de Exchange a partir creación 15.00.0847.032 (Exchange Server 2013 SP1) . 
  
## <a name="see-also"></a>Vea también

- [Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

