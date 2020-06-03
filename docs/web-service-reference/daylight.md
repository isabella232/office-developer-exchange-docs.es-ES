---
title: Horario
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Daylight
api_type:
- schema
ms.assetid: ea400839-fba8-4a5e-a5d1-9b677afc0ff9
description: El elemento diurna representa la fecha y hora cuando cambia la hora estándar al horario de verano.
ms.openlocfilehash: bf2041cb4677f837ddb5b399041f1c19a7b5f577
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457462"
---
# <a name="daylight"></a>Horario

El elemento **diurna** representa la fecha y hora cuando cambia la hora estándar al horario de verano. 
  
```xml
<Daylight TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Daylight>
```

```xml
<Daylight TimeZoneName="">
   <Offset/>
   <AbsoluteDate/>
   <Time/>
</Daylight>
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
|[Offset](offset.md) <br/> |Describe el desplazamiento desde [BaseOffset](baseoffset.md). El desplazamiento base, además de este desplazamiento, identifica el tiempo según si es estándar o el horario de verano.  <br/> |
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Describe un patrón de periodicidad anual relativo para un patrón de fecha de transición de zona horaria.  <br/> |
|[AbsoluteDate](absolutedate.md) <br/> |Representa la fecha en que cambia el horario estándar o el horario de verano.  <br/> |
|[Hora (TimeChangeType)](time-timechangetype.md) <br/> |Describe el momento en que cambia el tiempo entre el horario estándar y el horario de verano.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MeetingTimeZone](meetingtimezone.md) <br/> |Representa la zona horaria de la ubicación donde se hospeda la reunión.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

