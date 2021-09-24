---
title: CalendarItemType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CalendarItemType
api_type:
- schema
ms.assetid: 1feb0788-adf7-4a7c-830c-005214ad930f
description: El elemento CalendarItemType representa el tipo de un elemento de calendario.
ms.openlocfilehash: fcb661bb219944e03479abc6bf1d579db58f29fb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526776"
---
# <a name="calendaritemtype"></a>CalendarItemType

El **elemento CalendarItemType** representa el tipo de un elemento de calendario. 
  
```xml
<CalendarItemType/>
```

 **CalendarItemTypeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Representa una reunión en el Exchange almacén.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, se requiere un valor de texto. Estos son los valores posibles para este elemento:
  
- **Single** El elemento no está asociado a un elemento de calendario periódico. 
    
- **Ocurrencia** El elemento es una repetición de un elemento de calendario periódico. 
    
- **Excepción** El elemento es una excepción a un elemento de calendario periódico. 
    
- **RecurringMaster** El elemento es el patrón de un conjunto de elementos de calendario periódicos. 
    
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

