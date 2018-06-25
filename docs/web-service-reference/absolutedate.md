---
title: AbsoluteDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AbsoluteDate
api_type:
- schema
ms.assetid: 8bc59a26-6fe1-42e9-968c-69a94a3fb0ae
description: El elemento AbsoluteDate representa la fecha cuando se cambia la hora del estándar o de horario de verano.
ms.openlocfilehash: d14cafb08297e5be3c8620c441f8b84b46ffe53e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763476"
---
# <a name="absolutedate"></a>AbsoluteDate

El elemento **AbsoluteDate** representa la fecha cuando se cambia la hora del estándar o de horario de verano. 
  
```xml
<AbsoluteDate/>
```

**fecha**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Standard](standard.md) <br/> |Representa la fecha y hora cuando se cambia la hora del horario de verano a la hora estándar.  <br/> |
|[Horario de verano](daylight.md) <br/> |Representa la fecha y hora en que cambia el tiempo de la hora estándar al horario de verano.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa la fecha de cuando se produce el desplazamiento entre standard o del horario de verano.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)




