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
description: El elemento IsRecurring indica si un elemento de calendario, una convocatoria de reunión o una tarea forman parte de un elemento periódico. Este elemento es de sólo lectura.
ms.openlocfilehash: 72c71c1955b69f1c0df855ce4bd0ed02d4c89122
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526490"
---
# <a name="isrecurring"></a>IsRecurring

El elemento **IsRecurring** indica si un elemento de calendario, una convocatoria de reunión o una tarea forman parte de un elemento periódico. Este elemento es de sólo lectura. 
  
```xml
<IsRecurring/>
```

 **Boolean**
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
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea del almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa un valor booleano.
  
## <a name="remarks"></a>Comentarios

La siguiente tabla muestra cómo se establece la propiedad **IsRecurring** para distintos tipos de elemento de calendario para organizadores y asistentes, y para las convocatorias de reunión y las actualizaciones. 
  
|**Tipo CalendarItem**|**Organizador <br/> (IsRecurring)**|**Asistente <br/> (IsRecurring)**|**Convocatoria de reunión/actualización <br/> (IsRecurring)**|
|:-----|:-----|:-----|:-----|
|Ocurrencia única  <br/> |**FALSE** <br/> |**FALSE** <br/> |**FALSE** <br/> |
|Maestro recurrente  <br/> |**FALSE** <br/> |**CASO** <br/> |**CASO** <br/> |
|Excepción periódica  <br/> |**CASO** <br/> |**CASO** <br/> |**CASO** <br/> |
   
El valor de la propiedad **IsRecurring** que se establece para los elementos de calendario maestro periódicos para el organizador es incorrecto; Este valor debe establecerse en **true**. 
  
> [!NOTE]
> La operación GetUserAvailability también tiene un elemento [IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[TaskType. IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurring.aspx)
  
[CalendarEventDetails. IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarEventDetails.IsRecurring.aspx)
  
[CalendarItemType. IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurring.aspx)
  
[MeetingRequestMessageType. IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurring.aspx)
  
[CalendarItemType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurringSpecified.aspx)
  
[MeetingRequestMessageType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurringSpecified.aspx)
  
[TaskType. IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurringSpecified.aspx)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

