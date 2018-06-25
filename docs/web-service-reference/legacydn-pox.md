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
description: El elemento LegacyDN identifica el buzón de un usuario por su nombre distintivo (DN) heredado.
ms.openlocfilehash: f7ec1dea29a7d3ad6d470ef7812390d179fe1d2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836243"
---
# <a name="legacydn-pox"></a>LegacyDN (POX)

El elemento **LegacyDN** identifica el buzón de un usuario por su nombre distintivo (DN) heredado. 
  
```xml
<LegacyDN/>
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
|[Solicitud (POX)](request-pox.md) <br/> |Contiene la solicitud para el servicio Detección automática.  <br/> |
|[Usuario (POX)](user-pox.md) <br/> |Proporciona información específica del usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa la dirección de correo electrónico heredado de un usuario.
  
## <a name="remarks"></a>Comentarios

El elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) es un elemento alternativo para una solicitud de detección automática. Se utiliza cuando existe un buzón de correo en un equipo que ejecuta Microsoft Exchange Server 2007. 
  
## <a name="see-also"></a>Vea también

- [Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

