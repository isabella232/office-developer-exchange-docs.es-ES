---
title: DeletedOccurrenceStateDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a9c01c64-e76c-4adc-8b04-88af97bd0cc8
description: El DeletedOccurrenceStateDefinition especifica el estado de una repetición eliminado de un elemento de calendario.
ms.openlocfilehash: ad0434d604ee78ebf1905b60857929e1af4d45f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764086"
---
# <a name="deletedoccurrencestatedefinition"></a>DeletedOccurrenceStateDefinition

El **DeletedOccurrenceStateDefinition** especifica el estado de una repetición eliminado de un elemento de calendario. 
  
```XML
<DeletedOccurrenceStateDefinition>
    <OccurrenceDate></OccurrenceDate>
    <IsOccurrencePresent></IsOccurrencePresent>
</DeletedOccurrenceStateDefinition>
```

 **DeletedOccurrenceStateDefinitionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Aparición (transición de la zona horaria)](occurrence-time-zone-transition.md) <br/> |Especifica la fecha de la aparición de un elemento de calendario.  <br/> |
|[IsOccurrencePresent](isoccurrencepresent.md) <br/> |Especifica un valor booleano que indica si está presente una ocurrencia en el elemento de calendario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[StateDefinition](statedefinition.md) <br/> |Especifica una definición de estado.  <br/> |
   
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

