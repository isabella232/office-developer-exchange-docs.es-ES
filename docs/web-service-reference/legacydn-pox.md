---
title: LegacyDN (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 9fb9529f-52c5-4907-a84b-935b78de16c3
description: El elemento LegacyDN identifica el buzón de un usuario mediante el nombre distintivo heredado.
ms.openlocfilehash: b9af4278a5421dc932573396c3563a64a78de41e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526385"
---
# <a name="legacydn-pox"></a>LegacyDN (POX)

El elemento **LegacyDN** identifica el buzón de un usuario mediante el nombre distintivo heredado. 
  
```xml
<LegacyDN/>
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
|[Solicitud (POX)](request-pox.md) <br/> |Contiene la solicitud al servicio Detección automática.  <br/> |
|[Usuario (POX)](user-pox.md) <br/> |Proporciona información específica del usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa una dirección de correo electrónico heredada de un usuario.
  
## <a name="remarks"></a>Comentarios

El elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) es un elemento alternativo para una solicitud de detección automática. Se usa cuando existe un buzón de correo en un equipo que ejecuta Microsoft Exchange Server 2007. 
  
## <a name="see-also"></a>Vea también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

