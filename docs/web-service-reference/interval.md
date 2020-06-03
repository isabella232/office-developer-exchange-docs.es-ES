---
title: Intervalo de
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Interval
api_type:
- schema
ms.assetid: d0c97a5f-96be-40c6-b7d4-abf4c3870adf
description: El elemento Interval define el intervalo entre dos elementos periódicos consecutivos.
ms.openlocfilehash: 70a41cfc438f057cbe11d792f0004d46d0abcc85
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526567"
---
# <a name="interval"></a>Intervalo de

El elemento **Interval** define el intervalo entre dos elementos periódicos consecutivos. 
  
```xml
<Interval/>
```

 **int**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |Representa un patrón de periodicidad mensual.  <br/> |
|[DailyRegeneration](dailyregeneration.md) <br/> |Describe la frecuencia, en días, en la que se regenera una tarea.  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |Describe la frecuencia, en días, en la que una tarea se repite.  <br/> |
|[MonthlyRegeneration](monthlyregeneration.md) <br/> |Describe la frecuencia, en meses, en la que se regenera una tarea.  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |Describe un patrón mensual relativo para una tarea repetitiva.  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Describe la frecuencia, en semanas, y los días en los que una tarea se repite.  <br/> |
|[WeeklyRegeneration](weeklyregeneration.md) <br/> |Describe la frecuencia, en semanas, en la que se regenera una tarea.  <br/> |
|[YearlyRegeneration](yearlyregeneration.md) <br/> |Describe la frecuencia, en años, con la que se regenera una tarea.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Es necesario un valor de texto que representa un entero.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

