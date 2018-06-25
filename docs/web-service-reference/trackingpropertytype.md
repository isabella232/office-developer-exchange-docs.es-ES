---
title: TrackingPropertyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TrackingPropertyType
api_type:
- schema
ms.assetid: 1d0f219b-1063-4eaa-9d3b-da384a544f89
description: El elemento TrackingPropertyType representa un par de cadenas nombre y valor que se usa para crear las propiedades de los informes de seguimiento de mensajes.
ms.openlocfilehash: 762c7d364382c3087277651cc01329e3c85df4e4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840717"
---
# <a name="trackingpropertytype"></a>TrackingPropertyType

El elemento **TrackingPropertyType** representa un par de cadenas nombre y valor que se usa para crear las propiedades de los informes de seguimiento de mensajes. 
  
[Propiedades (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md)
  
[TrackingPropertyType](trackingpropertytype.md)
  
```xml
<TrackingPropertyType>
   <Name/>
   <Value/>
</TrackingPropertyType>
```

 **TrackingPropertyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Nombre (el seguimiento de mensajes)](name-message-tracking.md) <br/> |Define un nombre para la propiedad de informe de seguimiento de mensajes.  <br/> |
|[Valor (el seguimiento de mensajes)](value-message-tracking.md) <br/> |Define un valor para la propiedad de informe de seguimiento de mensajes. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Propiedades (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Contiene una lista de una o varias propiedades de seguimiento.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

