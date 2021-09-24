---
title: ExternalUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3b647d88-6feb-40d7-9299-b2ca47b707db
description: El elemento ExternalUrl contiene la dirección URL para conectar un cliente al servidor de libreta de direcciones o al buzón de un usuario desde fuera de la organización del usuario mediante el protocolo MAPI/HTTP.
ms.openlocfilehash: 90aaf9cabedba4ea89e0ed47da010245006407ba
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510080"
---
# <a name="externalurl-pox"></a>ExternalUrl (POX)

El **elemento ExternalUrl** contiene la dirección URL para conectar un cliente al servidor de libreta de direcciones o al buzón de un usuario desde fuera de la organización del usuario mediante el protocolo MAPI/HTTP. 
  
```XML
<ExternalUrl/>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AddressBook (POX)](addressbook-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al servidor de libreta de direcciones mediante el protocolo MAPI/HTTP.  <br/> |
|[MailStore (POX)](mailstore-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al buzón del usuario mediante el protocolo MAPI/HTTP.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa una dirección URL que se puede usar para obtener acceso a un servidor de libreta de direcciones o al buzón del usuario desde fuera de la organización del usuario.
  
## <a name="remarks"></a>Comentarios

El **elemento ExternalUrl** puede estar presente en una respuesta que tiene un elemento [Protocol (POX)](protocol-pox.md) con un valor de atributo **Type** de "mapiHttp". 
  
El **elemento ExternalUrl** está disponible para clientes que implementan el protocolo MAPI/HTTP y el Exchange Online de destino, Exchange Online como parte de Office 365 y versiones locales de Exchange a partir de la compilación 15.00.0847.032 (Exchange Server 2013 SP1). 
  
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

