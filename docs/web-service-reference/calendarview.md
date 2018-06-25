---
title: CalendarView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarView
api_type:
- schema
ms.assetid: a4a953b8-0710-416c-95ef-59e51eba9982
description: El elemento CalendarView define una operación FindItem como devolver elementos de calendario en un conjunto, tal como aparecen en un calendario.
ms.openlocfilehash: 79b5ad268a8013092c1122c99bdcd10d876abf2c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763717"
---
# <a name="calendarview"></a>CalendarView

El elemento **CalendarView** define una [operación FindItem](finditem-operation.md) como devolver elementos de calendario en un conjunto, tal como aparecen en un calendario. 
  
[FindItem](finditem.md)
  
[CalendarView](calendarview.md)
  
```XML
<CalendarView MaxEntriesReturned="" StartDate="" EndDate="" />
```

**CalendarView**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Describe el número máximo de resultados a devolver en la respuesta FindItem.  <br/> |
|**StartDate** <br/> |Identifica el inicio de un intervalo de tiempo de consulta para los elementos del calendario. Todos los elementos de calendario que tienen una hora de finalización que no antes se devolverán **StartDate** . Se puede especificar el valor de **StartDate** en formato de hora universal coordinada (UTC), al igual que en 2006-01-02T12:00:00Z, o en un formato donde se especifica el desplazamiento de hora local y la zona horaria, al igual que en 2006-01-02T04:00:00-08:00.  <br/><br/>Este atributo es necesario.  <br/> |
|**EndDate** <br/> |Identifica el final de un intervalo de tiempo de consulta para los elementos del calendario. No se devolverán todos los elementos de calendario que tienen una hora de inicio que se encuentra en o después de la **fecha de finalización** . Se puede especificar el valor de **fecha de finalización** en formato UTC, como se muestra en 2006-02-02T12:00:00Z, o en un formato donde se especifica el desplazamiento de hora local y la zona horaria, al igual que en 2006-02-02T04:00:00-08:00.  <br/><br/>**Fecha de finalización** debe ser mayor o igual a **StartDate**; en caso contrario, se devuelve un error. Este atributo es necesario.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón de correo.<br/><br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>Comentarios

Si el elemento **CalendarView** está especificado en una solicitud FindItem, el servicio Web devuelve una lista de elementos de calendario único y las apariciones de los elementos de calendario periódicos dentro del intervalo especificado por **StartDate** y **EndDate**.
  
Si no se especifica el elemento **CalendarView** en una solicitud FindItem, el servicio Web devuelve una lista de elementos de calendario único y elementos periódicos del calendario principal. Repeticiones de calendario de un elemento periódico de calendario no se expanden. 
  
Solo deben realizar consultas CalendarView utilizar de las siguientes propiedades, ya que estos admiten las consultas de calendario más rápidas.
  
### <a name="recurrence-blob-properties"></a>Propiedades de blob de periodicidad
  
- MapiStartTime
    
- MapiEndTime
    
- SubjectPrefixInternal
    
- NormalizedSubjectInternal
    
- MapiSubject
    
- Ubicación
    
- AppointmentColor
    
- MapiIsAllDayEvent
    
- MapiHasAttachment
    
- FreeBusyStatus
    
- ReminderIsSetInternal
    
- ReminderMinutesBeforeStartInternal
    
- AppointmentState
    
- AllAttachmentsHidden
    
- ChangeHighlight
    
### <a name="calculated-from-the-primary-recurrence-blob-or-master"></a>Calcular a partir la blob de periodicidad principal o del patrón
  
- ItemId
    
- IsRecurring
    
- IsException
    
- AppointmentRecurring
    
- MapiStartTime
    
- MapiPRStartDate
    
- MapiEndTime
    
- MapiPREndDate
    
- CalendarItemType
    
- GlobalObjectId
    
- TimeZoneDefinitionStart
    
- TimeZoneDefinitionEnd
    
### <a name="master-calendar-item-properties"></a>Propiedades de elementos de calendario principal
  
- Propiedad EntryId
    
- ChangeKey
    
- ItemClass
    
- SentRepresentingEmailAddress
    
- SentRepresentingDisplayName
    
- SentRepresentingEntryId
    
- AppointmentRecurrenceBlob
    
- TimeZone
    
- TimeZoneBlob
    
- TimeZoneDefinitionRecurring
    
- CleanGlobalObjectId
    
- AppointmentRecurring
    
- IsException
    
- IsRecurring
    
- MapiSensitivity
    
- ContainerClass
    
- MapiPRStartDate
    
- MapiPREndDate
    
- Categorías
    
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra una solicitud FindItem. Una solicitud correcta devuelve una respuesta que incluye los elementos de calendario que se iniciaron a 2006-05-18T00:00:00-08:00 o posterior y terminado antes de 2006-05-19T00:00:00-08:00.
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="calendar:Start"/>
          <t:FieldURI FieldURI="calendar:End"/>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <CalendarView MaxEntriesReturned="2" StartDate="2006-05-18T00:00:00-08:00" EndDate="2006-05-19T00:00:00-08:00"/>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación FindItem](finditem-operation.md)
- [Buscar elementos](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

