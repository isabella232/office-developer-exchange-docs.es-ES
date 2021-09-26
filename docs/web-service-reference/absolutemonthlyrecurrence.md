---
title: AbsoluteMonthlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AbsoluteMonthlyRecurrence
api_type:
- schema
ms.assetid: 178fa0ae-9dfc-417f-933c-d657d31c2161
description: El elemento AbsoluteMonthlyRecurrence representa un patrón de periodicidad mensual.
ms.openlocfilehash: 7fcc1811a7c42fc653344fb3c052adac820d6a5d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546920"
---
# <a name="absolutemonthlyrecurrence"></a>AbsoluteMonthlyRecurrence

El **elemento AbsoluteMonthlyRecurrence** representa un patrón de periodicidad mensual. 
  
```xml
<AbsoluteMonthlyRecurrence>
   <Interval/>
   <DayOfMonth/>
</AbsoluteMonthlyRecurrence>
```

 **AbsoluteMonthlyRecurrencePatternType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DayOfMonth](dayofmonth.md) <br/> |Describe el día de un mes en el que se produce un elemento periódico. El intervalo de valores de esta propiedad es de 1 a 31. Si para un mes determinado este valor es mayor que el número de días del mes, se asume el último día del mes para esta propiedad.  <br/> |
|[Intervalo de](interval.md) <br/> |Define el intervalo entre dos elementos periódicos consecutivos. Por ejemplo, si el **elemento Interval** tiene un valor de 5, el elemento periódico se produce cada 5 meses. El intervalo de valores válidos va de 1 a 99.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Recurrence (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Contiene información de periodicidad para tareas periódicas.  <br/> |
|[Recurrence (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Contiene el patrón de periodicidad de los elementos de calendario y las solicitudes de reunión.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

