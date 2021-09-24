---
title: To
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- To
api_type:
- schema
ms.assetid: d14e46da-14bd-4a33-a78e-8ee314d9c1d8
description: El elemento To especifica el destino de la transición de zona horaria. El destino es un período de zona horaria o un grupo de transiciones de zona horaria.
ms.openlocfilehash: 64f3f3258fd7c2bad051eabb1b33617bb056ab39
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522554"
---
# <a name="to"></a>To

El **elemento To** especifica el destino de la transición de zona horaria. El destino es un período de zona horaria o un grupo de transiciones de zona horaria. 
  
```xml
<To Kind=""/>
```

 **TransitionTargetType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|Tipo  <br/> |Indica si el destino de transición de zona horaria es un período de zona horaria o de un grupo de transiciones de zona horaria.  <br/> |
   
#### <a name="kind-attribute-values"></a>Valores de atributo Kind

|**Valor**|**Descripción**|
|:-----|:-----|
|Period  <br/> |Especifica que el destino de transición de zona horaria es un período de zona horaria.  <br/> |
|Group  <br/> |Especifica que el destino de transición de zona horaria es un grupo de transiciones de zona horaria.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AbsoluteDateTransition](absolutedatetransition.md) <br/> |Representa una transición de zona horaria que se produce en una fecha específica y en una hora específica.  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Representa una transición de zona horaria que se produce el mismo día de cada año.  <br/> |
|[RecurringDateTransition](recurringdatetransition.md) <br/> |Representa una transición de zona horaria que se produce en un día especificado del año.  <br/> |
|[Transition](transition.md) <br/> |Representa una transición de zona horaria.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es una cadena que especifica el identificador único de [Period](period.md) o [TransitionsGroup](transitionsgroup.md) que es el destino de la transición de zona horaria. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

