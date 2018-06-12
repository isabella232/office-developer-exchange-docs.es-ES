---
title: DateTimePrecision
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 822dc5a6-2d57-474b-8a7d-da150898e5b6
description: El elemento DateTimePrecision especifica la precisión para valores de fecha y hora devuelto.
ms.openlocfilehash: 4d11598628228b41adf021adbbaa77e6348534bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764034"
---
# <a name="datetimeprecision"></a>DateTimePrecision

El elemento **DateTimePrecision** especifica la precisión para valores de fecha y hora devuelto. 
  
```XML
<DateTimePrecision />
```

**DateTimePrecisionType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

El elemento **DateTimePrecision** se encuentra en el encabezado SOAP. 
  
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Los valores posibles son:
  
- Segundos
    
- Milisegundos
    
## <a name="remarks"></a>Notas

Fecha y hora cuando se usa un encabezado SOAP con el elemento **DateTimePrecision** establecido en "Segundos", se devuelven valores a los más cercanos segundos (00: 00:00). Fecha y hora cuando se usan "Milisegundos", se devuelven valores al milisegundo más próximo (00:00:00.0000). 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
Este elemento se introdujo en Exchange Server 2010 Service Pack 2 (SP2).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   

