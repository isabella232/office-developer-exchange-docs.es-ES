---
title: IsRecurring
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IsRecurring
api_type:
- schema
ms.assetid: f4df6997-8d5b-4893-a4a5-fc7047e0a9c3
description: El elemento IsRecurring indica si un elemento de calendario, una solicitud de reunión o una tarea forma parte de un elemento periódico. Este elemento es de solo lectura.
ms.openlocfilehash: ea910b78e962906285a73c869e394147c324372c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59532730"
---
# <a name="isrecurring"></a>IsRecurring

El **elemento IsRecurring** indica si un elemento de calendario, una solicitud de reunión o una tarea forma parte de un elemento periódico. Este elemento es de solo lectura. 
  
```xml
<IsRecurring/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el Exchange almacén.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa un valor booleano.
  
## <a name="remarks"></a>Comentarios

En la tabla siguiente se muestra cómo se establece la propiedad **IsRecurring** para diferentes tipos de elementos de calendario para organizadores y asistentes, así como para solicitudes y actualizaciones de reuniones. 
  
|**Tipo CalendarItem**|**Organizador  <br/> (IsRecurring)**|**Attendee  <br/> (IsRecurring)**|**Solicitud/actualización de  <br/> reunión (IsRecurring)**|
|:-----|:-----|:-----|:-----|
|Repetición única  <br/> |**FALSE** <br/> |**FALSE** <br/> |**FALSE** <br/> |
|Patrón periódico  <br/> |**FALSE** <br/> |**TRUE** <br/> |**TRUE** <br/> |
|Excepción periódica  <br/> |**TRUE** <br/> |**TRUE** <br/> |**TRUE** <br/> |
   
El **valor de la propiedad IsRecurring** que se establece para los elementos de calendario maestro periódicos para el organizador es incorrecto; este valor debe establecerse en **TRUE**. 
  
> [!NOTE]
> La operación GetUserAvailability también tiene un [elemento IsRecurring (CalendarEventDetails).](isrecurring-calendareventdetails.md) 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[TaskType.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurring.aspx)
  
[CalendarEventDetails.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarEventDetails.IsRecurring.aspx)
  
[CalendarItemType.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurring.aspx)
  
[MeetingRequestMessageType.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurring.aspx)
  
[CalendarItemType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurringSpecified.aspx)
  
[MeetingRequestMessageType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurringSpecified.aspx)
  
[TaskType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurringSpecified.aspx)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

