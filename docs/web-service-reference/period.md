---
title: Punto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Period
api_type:
- schema
ms.assetid: 2f9cf6af-c531-4d7d-90c9-1a1db504d890
description: El elemento Period define el nombre, el desplazamiento de tiempo y el identificador único para una región específica de la zona horaria.
ms.openlocfilehash: 3b5d5877e6d9baffdfe536a0feec3b25b6d2883f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836726"
---
# <a name="period"></a>Punto

El elemento de **período** define el nombre, el desplazamiento de tiempo y el identificador único para una región específica de la zona horaria. 
  
```xml
<Period Bias="" Name="" Id=""/>
```

 **PeriodType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|Bias  <br/> |Un valor de Duration que representa el desplazamiento de tiempo de la hora Universal coordinada (UTC) para el período.  <br/> |
|Nombre  <br/> |Un valor de tipo string que representa el nombre descriptivo del período.  <br/> |
|Id  <br/> |Un valor de tipo string que representa el identificador para el período.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Períodos](periods.md) <br/> |Representa una matriz de los períodos que definen el desplazamiento de tiempo en diferentes fases de la zona horaria.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

