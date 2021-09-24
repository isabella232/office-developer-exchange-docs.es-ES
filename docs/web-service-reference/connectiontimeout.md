---
title: ConnectionTimeout
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConnectionTimeout
api_type:
- schema
ms.assetid: 14da68a0-bcca-4281-a774-47644baa4ee9
description: El elemento ConnectionTimeout especifica el número de minutos que se debe mantener abierta una conexión.
ms.openlocfilehash: 7ca7a0b0b71d40a4f7888b63663b7d1e0f81b449
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536830"
---
# <a name="connectiontimeout"></a>ConnectionTimeout

El **elemento ConnectionTimeout** especifica el número de minutos que se debe mantener abierta una conexión. 
  
[Operación GetStreamingEvents](getstreamingevents-operation.md)
  
[ConnectionTimeout](connectiontimeout.md)
  
```xml
<ConnectionTimeout/>
```

 **int**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetStreamingEvents](getstreamingevents.md) <br/> |Define una solicitud para obtener notificaciones de eventos desde una conexión de streaming.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa un entero que describe el número máximo de minutos para mantener abierta una conexión de streaming. El valor debe estar entre 1 y 30, ambos incluidos.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Web Services.Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetStreamingEvents](getstreamingevents-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

