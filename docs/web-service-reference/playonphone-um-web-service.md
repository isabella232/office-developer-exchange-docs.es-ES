---
title: PlayOnPhone (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 206a2ad1-a01d-4e71-99a1-90c2530423da
description: El elemento PlayOnPhone define una solicitud para reproducir un elemento en un teléfono.
ms.openlocfilehash: 7e5c1e25512a59d1ac3295b476fcc2b6b0f5a2b1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836825"
---
# <a name="playonphone-um-web-service"></a>PlayOnPhone (servicio web de mensajería unificada)

El elemento **PlayOnPhone** define una solicitud para reproducir un elemento en un teléfono. 
  
[PlayOnPhone (servicio web de mensajería unificada)](playonphone-um-web-service.md)
  
```xml
<PlayOnPhone>
  <entryId>   </entryId>
  <DialString>   </DialString>
</PlayOnPhone>
```

 **complexType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[entryId (servicio web de mensajería unificada)](entryid-um-web-service.md) <br/> |Contiene el valor que representa el identificador del elemento que se va a reproducir en el teléfono en una solicitud de [operación PlayOnPhone (servicio web de mensajería unificada)](playonphone-operation-um-web-service.md) .  <br/> |
|[dialString (servicio web de mensajería unificada)](dialstring-um-web-service.md) <br/> |Contiene el valor para el número de teléfono a marcar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación PlayOnPhone (servicio web de mensajería unificada)](playonphone-operation-um-web-service.md)

