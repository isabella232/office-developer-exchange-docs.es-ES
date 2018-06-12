---
title: IsRecurring
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsRecurring
api_type:
- schema
ms.assetid: f4df6997-8d5b-4893-a4a5-fc7047e0a9c3
description: El elemento IsRecurring indica si un elemento de calendario, una convocatoria de reunión o una tarea forma parte de un elemento periódico. Este elemento es de sólo lectura.
ms.openlocfilehash: dfb0c28fe225792c7128409a8cf010627c624fe0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836104"
---
# <a name="isrecurring"></a>IsRecurring

El elemento **IsRecurring** indica si un elemento de calendario, una convocatoria de reunión o una tarea forma parte de un elemento periódico. Este elemento es de sólo lectura. 
  
```xml
<IsRecurring/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa un valor de tipo Boolean.
  
## <a name="remarks"></a>Notas

En la tabla siguiente se muestra cómo se establece la propiedad **IsRecurring** para tipos de elemento de calendario diferente para los organizadores y los asistentes y para las convocatorias de reunión y actualizaciones. 
  
|**Tipo de CalendarItem**|**Organizador de <br/> (IsRecurring)**|**ATTENDEE <br/> (IsRecurring)**|**Solicitud y actualización de la reunión <br/> (IsRecurring)**|
|:-----|:-----|:-----|:-----|
|Ocurrencia  <br/> |**FALSE** <br/> |**FALSE** <br/> |**FALSE** <br/> |
|Maestro periódico  <br/> |**FALSE** <br/> |**ES TRUE** <br/> |**ES TRUE** <br/> |
|Excepción periódica  <br/> |**ES TRUE** <br/> |**ES TRUE** <br/> |**ES TRUE** <br/> |
   
El valor de propiedad **IsRecurring** que se establece para los elementos periódicos de calendario principal para el organizador no es correcto; Este valor debe establecerse en **TRUE**. 
  
> [!NOTE]
> La operación GetUserAvailability también tiene un elemento [IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[TaskType.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurring.aspx)
  
[CalendarEventDetails.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarEventDetails.IsRecurring.aspx)
  
[CalendarItemType.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurring.aspx)
  
[MeetingRequestMessageType.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurring.aspx)
  
[CalendarItemType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurringSpecified.aspx)
  
[MeetingRequestMessageType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurringSpecified.aspx)
  
[TaskType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurringSpecified.aspx)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

