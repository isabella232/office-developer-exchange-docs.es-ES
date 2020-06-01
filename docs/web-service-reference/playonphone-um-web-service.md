---
title: Reproducir (servicio Web de mensajería unificada)
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
description: El elemento reproducir define una solicitud para reproducir un elemento en un teléfono.
ms.openlocfilehash: 9acbf9edbf4a889506558b24f5736a44d5015d3f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44434081"
---
# <a name="playonphone-um-web-service"></a>Reproducir (servicio Web de mensajería unificada)

El elemento **reproducir** define una solicitud para reproducir un elemento en un teléfono. 
  
[Reproducir (servicio Web de mensajería unificada)](playonphone-um-web-service.md)
  
```xml
<PlayOnPhone>
  <entryId>   </entryId>
  <DialString>   </DialString>
</PlayOnPhone>
```

 **complexType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[entryId (servicio Web de mensajería unificada)](entryid-um-web-service.md) <br/> |Contiene el valor que representa el identificador del elemento que se va a reproducir en el teléfono en una solicitud de [operación de reproducir (servicio Web de mensajería unificada)](playonphone-operation-um-web-service.md) .  <br/> |
|[dialString (servicio Web de mensajería unificada)](dialstring-um-web-service.md) <br/> |Contiene el valor del número de teléfono que se marca.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguna.
  
## <a name="text-value"></a>Valor de texto

Ninguna.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación reproducir (servicio Web de mensajería unificada)](playonphone-operation-um-web-service.md)

