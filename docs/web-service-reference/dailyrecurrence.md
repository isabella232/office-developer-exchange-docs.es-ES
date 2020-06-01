---
title: DailyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DailyRecurrence
api_type:
- schema
ms.assetid: 0aaf265d-b723-49c6-8e9c-9ba60141e9ab
description: El elemento DailyRecurrence describe la frecuencia, en días, en que se repite un elemento de calendario o una tarea.
ms.openlocfilehash: d18a04ced19c87996c3a092f6668ab00c5a3f006
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462174"
---
# <a name="dailyrecurrence"></a>DailyRecurrence

El elemento **DailyRecurrence** describe la frecuencia, en días, en que se repite un elemento de calendario o una tarea. 
  
```xml
<DailyRecurrence>
   <Interval/>
</DailyRecurrence>
```

**DailyRecurrencePatternType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Intervalo de](interval.md) <br/> |Define el intervalo, en días, entre dos elementos periódicos consecutivos. El valor debe estar comprendido entre 1 y 999.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Periodicidad (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Contiene información de periodicidad para tareas periódicas.  <br/> |
|[Recurrence (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Contiene el patrón de periodicidad para los elementos de calendario y las convocatorias de reunión.  <br/> |
   
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

