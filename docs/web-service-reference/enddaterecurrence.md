---
title: EndDateRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndDateRecurrence
api_type:
- schema
ms.assetid: a5ee2504-db84-49ee-870c-cca9269f2e26
description: El elemento EndDateRecurrence describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de elemento.
ms.openlocfilehash: 73450bf69c6b122e806d85011975159e348ad740
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764408"
---
# <a name="enddaterecurrence"></a>EndDateRecurrence

El elemento **EndDateRecurrence** describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de elemento. 
  
```xml
<EndDateRecurrence>
   <StartDate/>
   <EndDate/>
</EndDateRecurrence>
```

 **EndDateRecurrenceRangeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[StartDate (periodicidad)](startdate-recurrence.md) <br/> |Representa la fecha de comienzo de una tarea periódica o elemento de calendario.  <br/> |
|[EndDate (periodicidad)](enddate-recurrence.md) <br/> |Representa la fecha de finalización de una tarea periódica o elemento de calendario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Periodicidad (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.  <br/> |
|[Periodicidad (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Contiene el patrón de periodicidad para las tareas repetitivas.  <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

