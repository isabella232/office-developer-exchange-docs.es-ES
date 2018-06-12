---
title: InternalUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4649baa9-eec9-426d-952b-361818c25fe0
description: El elemento InternalUrl contiene la dirección URL para conectar a un cliente con el servidor de la libreta de direcciones o buzón de un usuario desde dentro de la organización del usuario mediante el protocolo HTTP/MAPI.
ms.openlocfilehash: 3823236081961128b31bb2c0f563062897c55814
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835950"
---
# <a name="internalurl-pox"></a>InternalUrl (POX)

El elemento **InternalUrl** contiene la dirección URL para conectar a un cliente con el servidor de la libreta de direcciones o buzón de un usuario desde dentro de la organización del usuario mediante el protocolo HTTP/MAPI. 
  
```XML
<InternalUrl/>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Libreta de direcciones (POX)](addressbook-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente con el servidor de la libreta de direcciones mediante el protocolo HTTP/MAPI.  <br/> |
|[Almacenamiento de correo (POX)](mailstore-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente con el buzón del usuario mediante el protocolo HTTP/MAPI.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa una dirección URL que se puede usar para tener acceso al buzón del usuario desde dentro de la organización del usuario o un servidor de la libreta de direcciones.
  
## <a name="remarks"></a>Notas

El elemento **InternalUrl** puede estar presente en una respuesta que tiene un elemento de [Protocolo (POX)](protocol-pox.md) con un valor de atributo de **tipo** de "mapiHttp". 
  
El elemento **InternalUrl** está disponible para los clientes que implementan el protocolo HTTP/MAPI y destino Exchange Online, Exchange Online como parte de Office 365, y las versiones locales de Exchange a partir creación 15.00.0847.032 (Exchange Server 2013 SP1) . 
  
## <a name="see-also"></a>Ver también



[Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

