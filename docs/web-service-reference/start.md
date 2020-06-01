---
title: Iniciar
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Start
api_type:
- schema
ms.assetid: 7cfe9979-c893-4f9b-b3a1-8f9e17515a4b
description: El elemento Start representa el inicio de una duración.
ms.openlocfilehash: 0daf9c1422f7ba3894f9785aacac58263c5e721e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457217"
---
# <a name="start"></a>Iniciar

El elemento **Start** representa el inicio de una duración. 
  
```xml
<Start/>
```

**DateTime**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[DeletedOccurrence](deletedoccurrence.md) <br/> |Representa una ocurrencia eliminada de un elemento de calendario periódico.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Representa la primera aparición de un elemento de calendario periódico.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Representa la última repetición de un elemento de calendario periódico.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[Suceda](occurrence.md) <br/> |Representa una ocurrencia única modificada de un elemento de calendario periódico.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el inicio de una duración.
  
## <a name="remarks"></a>Comentarios

La operación UpdateItem puede establecer la hora de [Inicio](start.md) y de [finalización](end-ex15websvcsotherref.md) de un elemento de almacén de Exchange. En una solicitud UpdateItem, se puede establecer la hora de **Inicio** sin establecer también la hora de **finalización** . Esto puede provocar un error si la hora de **Inicio** es posterior a la hora de **finalización** . Tenga en cuenta que las aplicaciones cliente deben realizar ajustes en la hora de **finalización** cuando se cambia la hora de **Inicio** a fin de preservar la duración. 
  
> [!NOTE]
> La información de desplazamiento de zona horaria se pierde si las fechas de [Inicio](start.md) y [finalización](end-ex15websvcsotherref.md) del elemento maestro periódico no tienen una fecha igual a la primera aparición de un patrón de periodicidad semanal. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [WeeklyRecurrence](weeklyrecurrence.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

