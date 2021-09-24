---
title: TimeZoneDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- TimeZoneDefinition
api_type:
- schema
ms.assetid: b005a80c-addb-4409-beff-e5162076752c
description: El elemento TimeZoneDefinition especifica los períodos y transiciones que definen una zona horaria.
ms.openlocfilehash: 6f2b580d2c3e31826ca74034cfda938cff71ee53
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538817"
---
# <a name="timezonedefinition"></a>TimeZoneDefinition

El **elemento TimeZoneDefinition** especifica los períodos y transiciones que definen una zona horaria. 
  
```XML
<TimeZoneDefinition Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</TimeZoneDefinition>

```

 **TimeZoneDefinitionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Representa el identificador único de la zona horaria.  <br/> |
|Nombre  <br/> |Representa el nombre descriptivo de la zona horaria.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Periods](periods.md) <br/> |Representa una matriz de [elementos Period](period.md) que definen el desplazamiento de hora en distintas fases de la zona horaria.  <br/> |
|[TransitionsGroups](transitionsgroups.md) <br/> |Representa una matriz de [elementos TransitionsGroup](transitionsgroup.md) que especifican transiciones de zona horaria.  <br/> |
|[Transitions](transitions.md) <br/> |Representa una matriz de transiciones de zona horaria.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[TimeZoneDefinitions](timezonedefinitions.md) <br/> |Representa una matriz de definiciones de zona horaria.  <br/> |
|[TimeZoneContext](timezonecontext.md) <br/> |Representa la definición de zona horaria predeterminada que se va a usar para el ámbito de las propiedades DateTime de los objetos que se crean, actualizan y recuperan mediante Exchange Web Services (EWS).  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

