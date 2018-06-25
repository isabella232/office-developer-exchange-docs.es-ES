---
title: Definición de zona horaria
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZoneDefinition
api_type:
- schema
ms.assetid: b005a80c-addb-4409-beff-e5162076752c
description: El elemento de la definición de zona horaria especifica los períodos y las transiciones que definen una zona horaria.
ms.openlocfilehash: ffd5ed0c862af794e4aff2387f508849b1d5fd5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840688"
---
# <a name="timezonedefinition"></a>Definición de zona horaria

El elemento de la **definición de zona horaria** especifica los períodos y las transiciones que definen una zona horaria. 
  
```XML
<TimeZoneDefinition Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</TimeZoneDefinition>

```

 **TimeZoneDefinitionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Representa el identificador único de la zona horaria.  <br/> |
|Nombre  <br/> |Representa el nombre descriptivo de la zona horaria.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Períodos](periods.md) <br/> |Representa una matriz de elementos de [período](period.md) que definen el desplazamiento de tiempo en diferentes fases de la zona horaria.  <br/> |
|[TransitionsGroups](transitionsgroups.md) <br/> |Representa una matriz de elementos de [TransitionsGroup](transitionsgroup.md) que especifican las transiciones de zona horaria.  <br/> |
|[Transiciones](transitions.md) <br/> |Representa una matriz de las transiciones de zona horaria.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[TimeZoneDefinitions](timezonedefinitions.md) <br/> |Representa una matriz de definiciones de zona horaria.  <br/> |
|[TimeZoneContext](timezonecontext.md) <br/> |Representa la definición de zona horaria predeterminada que se utiliza para definir el ámbito de las propiedades de fecha y hora de objetos que se crean, actualizan y recuperados mediante servicios Web de Exchange (EWS).  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

