---
title: Interval
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Interval
api_type:
- schema
ms.assetid: d0c97a5f-96be-40c6-b7d4-abf4c3870adf
description: El elemento Interval define el intervalo entre dos elementos periódicos consecutivos.
ms.openlocfilehash: 6df46865d7a89a0bfde9afc5f84ffdb78d956a30
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541031"
---
# <a name="interval"></a>Interval

El **elemento Interval** define el intervalo entre dos elementos periódicos consecutivos. 
  
```xml
<Interval/>
```

 **int**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |Representa un patrón de periodicidad mensual.  <br/> |
|[DailyRegeneration](dailyregeneration.md) <br/> |Describe la frecuencia, en días, en la que se regenera una tarea.  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |Describe la frecuencia, en días, en la que se repite una tarea.  <br/> |
|[MonthlyRegeneration](monthlyregeneration.md) <br/> |Describe la frecuencia, en meses, en la que se regenera una tarea.  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |Describe un patrón mensual relativo para una tarea periódica.  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Describe la frecuencia, en semanas, en la que y los días en los que se repite una tarea.  <br/> |
|[WeeklyRegeneration](weeklyregeneration.md) <br/> |Describe la frecuencia, en semanas, en la que se regenera una tarea.  <br/> |
|[YearlyRegeneration](yearlyregeneration.md) <br/> |Describe la frecuencia, en años, en la que se regenera una tarea.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa un número entero.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

