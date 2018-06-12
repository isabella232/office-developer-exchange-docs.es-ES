---
title: NoEndRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NoEndRecurrence
api_type:
- schema
ms.assetid: ab2ebd9c-388e-45f1-abf9-56e293ef123b
description: El elemento NoEndRecurrence describe la fecha de inicio de un patrón de periodicidad de elemento que no tiene una fecha de finalización definidas.
ms.openlocfilehash: fc3eae170f5c07e31d7a80b45836efd07d74e543
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836537"
---
# <a name="noendrecurrence"></a>NoEndRecurrence

El elemento **NoEndRecurrence** describe la fecha de inicio de un patrón de periodicidad de elemento que no tiene una fecha de finalización definidas. 
  
```xml
<NoEndRecurrence>
   <StartDate/>
</NoEndRecurrence>
```

 **NoEndRecurrenceRangeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[StartDate (periodicidad)](startdate-recurrence.md) <br/> |Representa la fecha de comienzo de una tarea periódica o elemento de calendario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Periodicidad (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.  <br/> |
|[Periodicidad (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Contiene información sobre la periodicidad para las tareas repetitivas.  <br/> |
   
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

