---
title: Estándar
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Standard
api_type:
- schema
ms.assetid: d598f0a6-e296-423f-8ce5-3da57cfd8189
description: El elemento estándar representa la fecha y hora cuando se cambia la hora del horario de verano a la hora estándar.
ms.openlocfilehash: 1c9be4cf35773583078bc8e16ddf44433d3ad98c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837536"
---
# <a name="standard"></a>Estándar

El elemento **estándar** representa la fecha y hora cuando se cambia la hora del horario de verano a la hora estándar. 
  
```xml
<Standard TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Standard>
```

 **TimeChangeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**TimeZoneName** <br/> |Describe el nombre de la zona horaria.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Offset](offset.md) <br/> |Describe el desplazamiento desde el [BaseOffset](baseoffset.md). Junto con el elemento **BaseOffset** , el elemento de **desplazamiento** identifica si el tiempo es la hora estándar o el horario de verano.  <br/> |
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Describe un patrón de periodicidad anual relativa para una fecha de transición de la zona horaria.  <br/> |
|[AbsoluteDate](absolutedate.md) <br/> |Representa la fecha cuando se cambia el tiempo de hora estándar o el horario de verano.  <br/> |
|[Tiempo (TimeChangeType)](time-timechangetype.md) <br/> |Describe la hora cuando se cambia el tiempo entre la hora estándar y el horario de verano.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[MeetingTimeZone](meetingtimezone.md) <br/> |Representa la zona horaria de la ubicación donde se hospeda la reunión.  <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

