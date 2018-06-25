---
title: Para
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- To
api_type:
- schema
ms.assetid: d14e46da-14bd-4a33-a78e-8ee314d9c1d8
description: El elemento especifica el destino de la transición de la zona horaria. El destino es un período de zona horaria o un grupo de transiciones de zona horaria.
ms.openlocfilehash: dc7df8ed3ddd6a9b4222ffab4c2b47b00ee4ba0c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840682"
---
# <a name="to"></a>Para

El elemento **que** especifica el destino de la transición de la zona horaria. El destino es un período de zona horaria o un grupo de transiciones de zona horaria. 
  
```xml
<To Kind=""/>
```

 **TransitionTargetType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|Tipo  <br/> |Indica si el destino de la transición de zona horaria es un período de zona horaria o de un grupo de transiciones de zona horaria.  <br/> |
   
#### <a name="kind-attribute-values"></a>Valores de atributo Kind

|**Valor**|**Descripción**|
|:-----|:-----|
|Punto  <br/> |Especifica que el destino de la transición de zona horaria es un período de zona horaria.  <br/> |
|Group  <br/> |Especifica que el destino de la transición de zona horaria es un grupo de transiciones de zona horaria.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[AbsoluteDateTransition](absolutedatetransition.md) <br/> |Representa una transición de la zona horaria que se produce en una fecha específica y a una hora específica.  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Representa una transición de la zona horaria que se produce en el mismo día cada año.  <br/> |
|[RecurringDateTransition](recurringdatetransition.md) <br/> |Representa una transición de la zona horaria que se produce en un día del año especificado.  <br/> |
|[Transición](transition.md) <br/> |Representa una transición de la zona horaria.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es una cadena que especifica el identificador exclusivo del [período](period.md) o [TransitionsGroup](transitionsgroup.md) que es el destino de la transición de la zona horaria. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

