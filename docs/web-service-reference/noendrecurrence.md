---
title: NoEndRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- NoEndRecurrence
api_type:
- schema
ms.assetid: ab2ebd9c-388e-45f1-abf9-56e293ef123b
description: El elemento NoEndRecurrence describe la fecha de inicio de un patrón de periodicidad de elementos que no tiene una fecha de finalización definida.
ms.openlocfilehash: 862bd58c295aabe807768f93506b4002d83c4552
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529810"
---
# <a name="noendrecurrence"></a>NoEndRecurrence

El **elemento NoEndRecurrence** describe la fecha de inicio de un patrón de periodicidad de elementos que no tiene una fecha de finalización definida. 
  
```xml
<NoEndRecurrence>
   <StartDate/>
</NoEndRecurrence>
```

 **NoEndRecurrenceRangeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[StartDate (Recurrence)](startdate-recurrence.md) <br/> |Representa la fecha de inicio de una tarea periódica o un elemento de calendario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Recurrence (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Contiene el patrón de periodicidad de los elementos de calendario y las solicitudes de reunión.  <br/> |
|[Recurrence (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Contiene información de periodicidad para tareas periódicas.  <br/> |
   
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

