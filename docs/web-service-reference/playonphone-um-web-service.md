---
title: PlayOnPhone (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 206a2ad1-a01d-4e71-99a1-90c2530423da
description: El elemento PlayOnPhone define una solicitud para reproducir un elemento en un teléfono.
ms.openlocfilehash: 240c8f474c87e0c123a6d8239eb691079385e348
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527992"
---
# <a name="playonphone-um-web-service"></a>PlayOnPhone (servicio web de mensajería unificada)

El **elemento PlayOnPhone** define una solicitud para reproducir un elemento en un teléfono. 
  
[PlayOnPhone (servicio web de mensajería unificada)](playonphone-um-web-service.md)
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[entryId (servicio web de mensajería unificada)](entryid-um-web-service.md) <br/> |Contiene el valor que representa el identificador del elemento que se reproducirá en el teléfono en una solicitud de [operación PlayOnPhone (servicio web](playonphone-operation-um-web-service.md) de mensajería unificada).  <br/> |
|[dialString (servicio web de mensajería unificada)](dialstring-um-web-service.md) <br/> |Contiene el valor del número de teléfono que se debe marcar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación PlayOnPhone (servicio web de mensajería unificada)](playonphone-operation-um-web-service.md)

