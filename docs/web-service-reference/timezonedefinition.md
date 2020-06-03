---
title: TimeZoneDefinition
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
description: El elemento TimeZoneDefinition especifica los períodos y las transiciones que definen una zona horaria.
ms.openlocfilehash: 58d34556686bfc77244b5829798eada51a1df843
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466069"
---
# <a name="timezonedefinition"></a>TimeZoneDefinition

El elemento **TimeZoneDefinition** especifica los períodos y las transiciones que definen una zona horaria. 
  
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
|[Períodos](periods.md) <br/> |Representa una matriz de elementos [period](period.md) que define el desplazamiento de tiempo en diferentes etapas de la zona horaria.  <br/> |
|[TransitionsGroups](transitionsgroups.md) <br/> |Representa una matriz de elementos [TransitionsGroup](transitionsgroup.md) que especifican las transiciones de la zona horaria.  <br/> |
|[Transiciones](transitions.md) <br/> |Representa una matriz de transiciones de zona horaria.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[TimeZoneDefinitions](timezonedefinitions.md) <br/> |Representa una matriz de definiciones de zona horaria.  <br/> |
|[TimeZoneContext](timezonecontext.md) <br/> |Representa la definición de zona horaria predeterminada que se va a usar para establecer el ámbito de las propiedades DateTime de los objetos que se crean, actualizan y recuperan mediante los servicios web Exchange (EWS).  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

