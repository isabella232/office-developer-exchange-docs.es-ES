---
title: ExternalUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b647d88-6feb-40d7-9299-b2ca47b707db
description: El elemento ExternalUrl contiene la dirección URL para conectar a un cliente con el servidor de la libreta de direcciones o buzón de un usuario desde fuera de la organización del usuario mediante el protocolo HTTP/MAPI.
ms.openlocfilehash: 603e2109e7b3c98acdd4cbc13df81ed9717630ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764570"
---
# <a name="externalurl-pox"></a>ExternalUrl (POX)

El elemento **ExternalUrl** contiene la dirección URL para conectar a un cliente con el servidor de la libreta de direcciones o buzón de un usuario desde fuera de la organización del usuario mediante el protocolo HTTP/MAPI. 
  
```XML
<ExternalUrl/>
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

El valor de texto representa una dirección URL que se puede usar para tener acceso al buzón del usuario desde fuera de la organización del usuario o un servidor de la libreta de direcciones.
  
## <a name="remarks"></a>Notas

El elemento **ExternalUrl** puede estar presente en una respuesta que tiene un elemento de [Protocolo (POX)](protocol-pox.md) con un valor de atributo de **tipo** de "mapiHttp". 
  
El elemento **ExternalUrl** está disponible para los clientes que implementan el protocolo HTTP/MAPI y destino Exchange Online, Exchange Online como parte de Office 365, y las versiones locales de Exchange a partir creación 15.00.0847.032 (Exchange Server 2013 SP1) . 
  
## <a name="see-also"></a>Ver también



[Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

