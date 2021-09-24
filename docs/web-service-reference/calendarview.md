---
title: CalendarView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CalendarView
api_type:
- schema
ms.assetid: a4a953b8-0710-416c-95ef-59e51eba9982
description: El elemento CalendarView define una operación FindItem como devolver elementos de calendario en un conjunto tal como aparecen en un calendario.
ms.openlocfilehash: 5e0180bb5e8a6d9fcbe42380abbe32820117ae29
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518830"
---
# <a name="calendarview"></a>CalendarView

El **elemento CalendarView** define una [operación FindItem](finditem-operation.md) como devolver elementos de calendario en un conjunto tal como aparecen en un calendario. 
  
[FindItem](finditem.md)
  
[CalendarView](calendarview.md)
  
```XML
<CalendarView MaxEntriesReturned="" StartDate="" EndDate="" />
```

**CalendarView**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Describe el número máximo de resultados que se devolverán en la respuesta FindItem.  <br/> |
|**StartDate** <br/> |Identifica el inicio de un intervalo de tiempo que se consulta para los elementos del calendario. No se devolverán todos los elementos del calendario que tengan una hora de finalización anterior **a StartDate.** El valor de **StartDate** se puede especificar en formato de hora universal coordinada (UTC), como en 2006-01-02T12:00:00Z, o en un formato donde se especifica el desplazamiento de hora y zona horaria local, como en 2006-01-02T04:00:00-08:00.  <br/><br/>Este atributo es obligatorio.  <br/> |
|**EndDate** <br/> |Identifica el final de un intervalo de tiempo que se consulta para los elementos del calendario. No se devolverán todos los elementos del calendario que tengan una hora de inicio que esté en o después de **EndDate.** El valor de **EndDate** se puede especificar en formato UTC, como en 2006-02-02T12:00:00Z, o en un formato donde se especifica el desplazamiento de hora y zona horaria local, como en 2006-02-02T04:00:00-08:00.  <br/><br/>**EndDate** debe ser mayor o igual que **StartDate**; de lo contrario, se devuelve un error. Este atributo es obligatorio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón.<br/><br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>Comentarios

Si el **elemento CalendarView** se especifica en una solicitud FindItem, el servicio web devuelve una lista de elementos de calendario único y repeticiones de elementos de calendario periódicos dentro del intervalo especificado por **StartDate** y **EndDate**.
  
Si el **elemento CalendarView** no se especifica en una solicitud FindItem, el servicio web devuelve una lista de elementos de calendario único y elementos de calendario maestro periódicos. Las repeticiones de calendario de un elemento de calendario periódico no se expanden. 
  
Las consultas CalendarView solo deben usar las siguientes propiedades, ya que admiten consultas de calendario más rápidas.
  
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
    
### <a name="calculated-from-the-primary-recurrence-blob-or-master"></a>Calculado a partir del blob o patrón de periodicidad principal
  
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
    
### <a name="master-calendar-item-properties"></a>Propiedades de elementos de calendario maestro
  
- EntryID
    
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
    
- Categories
    
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra una solicitud FindItem. Una solicitud correcta devuelve una respuesta que incluye elementos de calendario que se iniciaron en 2006-05-18T00:00:00-08:00 o después y finalizaron antes de 2006-05-19T00:00:00-08:00.
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación FindItem](finditem-operation.md)
- [Buscar elementos](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

