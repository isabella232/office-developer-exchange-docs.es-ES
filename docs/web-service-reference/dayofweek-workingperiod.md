---
title: DayOfWeek (WorkingPeriod)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DayOfWeek
api_type:
- schema
ms.assetid: 7a8a8cc1-392b-4db5-bb76-710477e31396
description: El elemento DayOfWeek contiene la lista de días laborables programados para el usuario del buzón.
ms.openlocfilehash: 97950d7f2d6db76ac76253979e9187bddc5c99e1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529009"
---
# <a name="dayofweek-workingperiod"></a>DayOfWeek (WorkingPeriod)

El **elemento DayOfWeek** contiene la lista de días laborables programados para el usuario del buzón. 
  
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)  
- [FreeBusyResponseArray](freebusyresponsearray.md)  
- [FreeBusyResponse](freebusyresponse.md)  
- [FreeBusyView](freebusyview.md)  
- [WorkingHours](workinghours-ex15websvcsotherref.md)  
- [WorkingPeriodArray](workingperiodarray.md) 
- [WorkingPeriod](workingperiod.md)  
- [DayOfWeek (WorkingPeriod)](dayofweek-workingperiod.md)
  
```xml
<DayOfWeek>Sunday Monday Tuesday Wednesday Thursday Friday Saturday</DayOfWeek>
```

**DaysOfWeek**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[WorkingPeriod](workingperiod.md) <br/> |Contiene los días y horas de la semana laboral del usuario del buzón.<br/><br/>A continuación se muestra la expresión XPath de este elemento:<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod[i[` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se devuelve un valor de texto si el usuario del buzón tiene días establecidos para representar la semana laboral. Estos son los valores posibles para este elemento:
  
- Domingo    
- lunes    
- martes    
- miércoles    
- jueves    
- viernes    
- Sábado 
    
Los valores de texto se devolverán en ese orden.
  
## <a name="remarks"></a>Comentarios

Es importante tener en cuenta que la diferencia entre este elemento y el elemento Availability [DayOfWeek (TimeZone)](dayofweek-timezone.md) es el tipo. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserAvailability](getuseravailability-operation.md)  
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

