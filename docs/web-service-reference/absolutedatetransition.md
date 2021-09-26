---
title: AbsoluteDateTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AbsoluteDateTransition
api_type:
- schema
ms.assetid: 8f5731eb-bed0-45bf-ba89-4aaf20c34a39
description: El elemento AbsoluteDateTransition representa una transición de zona horaria que se produce en una fecha específica y en una hora específica.
ms.openlocfilehash: c0d4e28d8ecefaaa72ded50ab3022666d74ce479
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542550"
---
# <a name="absolutedatetransition"></a>AbsoluteDateTransition

El **elemento AbsoluteDateTransition** representa una transición de zona horaria que se produce en una fecha específica y en una hora específica. 
  
```xml
<AbsoluteDateTransition>
   <To/>
   <DateTime/>
</AbsoluteDateTransition>
```

**AbsoluteDateTransitionType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[To](to.md) <br/> |Especifica el [Period](period.md) o [TransitionsGroup](transitionsgroup.md) que es el destino de la transición de zona horaria.  <br/> |
|[DateTime](datetime.md) <br/> |Representa la fecha y hora en que se produce la transición de zona horaria.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Transitions](transitions.md) <br/> |Representa una colección de transiciones de zona horaria.  <br/> |
|[TransitionsGroup](transitionsgroup.md) <br/> |Representa una colección de transiciones de zona horaria.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

