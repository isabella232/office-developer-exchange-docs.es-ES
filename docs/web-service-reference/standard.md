---
title: Estándar
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Standard
api_type:
- schema
ms.assetid: d598f0a6-e296-423f-8ce5-3da57cfd8189
description: El elemento Standard representa la fecha y hora en que la hora cambia del horario de verano al horario estándar.
ms.openlocfilehash: 8e44bc458f109975acd3d48c80726654b70373e8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544671"
---
# <a name="standard"></a>Estándar

El **elemento Standard** representa la fecha y hora en que la hora cambia del horario de verano al horario estándar. 
  
```xml
<Standard TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Standard>
```

```xml
<Standard TimeZoneName="">
   <Offset/>
   <AbsoluteDate/>
   <Time/>
</Standard>
```

**TimeChangeType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**TimeZoneName** <br/> |Describe el nombre de la zona horaria.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Offset](offset.md) <br/> |Describe el desplazamiento de [BaseOffset](baseoffset.md). Junto con el **elemento BaseOffset,** el **elemento Offset** identifica si la hora es la hora estándar o el horario de verano.  <br/> |
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Describe un patrón de periodicidad anual relativo para una fecha de transición de zona horaria.  <br/> |
|[AbsoluteDate](absolutedate.md) <br/> |Representa la fecha en la que la hora cambia desde la hora estándar o el horario de verano.  <br/> |
|[Time (TimeChangeType)](time-timechangetype.md) <br/> |Describe la hora en la que cambia la hora entre la hora estándar y el horario de verano.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MeetingTimeZone](meetingtimezone.md) <br/> |Representa la zona horaria de la ubicación donde se hospeda la reunión.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

