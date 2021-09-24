---
title: End
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- End
api_type:
- schema
ms.assetid: 72329821-32ff-495d-b6e5-fdc011003c2e
description: El elemento End representa el final de una duración.
ms.openlocfilehash: 8f7fd448a873f82a82c6bd129fc16af9241d7f3c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540106"
---
# <a name="end"></a>End

El **elemento End** representa el final de una duración. 
  
```xml
<End/>
```

 **DateTime**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Representa la primera aparición de un elemento de calendario periódico.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Representa la última aparición de un elemento de calendario periódico.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
|[Occurrence](occurrence.md) <br/> |Representa una única aparición modificada de un elemento de calendario periódico.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el final de una duración.
  
## <a name="remarks"></a>Comentarios

La operación UpdateItem puede establecer [la](start.md) hora **de** inicio y finalización de un elemento Exchange almacén. En una solicitud UpdateItem, puede establecer la [hora de](start.md) inicio sin establecer también la **hora de** finalización. Esto puede provocar un error si la [hora de](start.md) inicio es posterior a la **hora de** finalización. Tenga en cuenta que las aplicaciones  cliente deben [](start.md) realizar ajustes en la hora de finalización cuando se cambia la hora de inicio para conservar la duración. 
  
 **Nota** La información de desplazamiento de [](start.md) zona  horaria se pierde si las fechas Inicio y Fin del elemento maestro periódico no tienen una fecha igual a la primera aparición de un patrón de periodicidad semanal. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[WeeklyRecurrence](weeklyrecurrence.md)
  
 **End**


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

