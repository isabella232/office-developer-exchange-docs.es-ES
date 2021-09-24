---
title: LegacyDN (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 9fb9529f-52c5-4907-a84b-935b78de16c3
description: El elemento LegacyDN identifica el buzón de un usuario por nombre distintivo heredado.
ms.openlocfilehash: bd65e18daf1b05f66ebd767635cbe6a3135f1abf
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540835"
---
# <a name="legacydn-pox"></a>LegacyDN (POX)

El **elemento LegacyDN** identifica el buzón de un usuario por nombre distintivo heredado. 
  
```xml
<LegacyDN/>
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
|[Request (POX)](request-pox.md) <br/> |Contiene la solicitud al servicio de detección automática.  <br/> |
|[User (POX)](user-pox.md) <br/> |Proporciona información específica del usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa la dirección de correo electrónico heredada de un usuario.
  
## <a name="remarks"></a>Comentarios

El [elemento EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) es un elemento alternativo para una solicitud de detección automática. Se usa cuando existe un buzón en un equipo que se ejecuta Microsoft Exchange Server 2007. 
  
## <a name="see-also"></a>Ver también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

