---
title: AggregationRestriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d05044f9-d2ff-4aca-956c-20c9cb2f7709
description: El elemento AggregationRestriction especifica un valor que se aplica a un conjunto de propiedades de Persona resultantes de una solicitud FindPeople y filtra el resultado según la restricción especificada.
ms.openlocfilehash: 6a00035f87e0f365f4551df1a6ff570e01761770
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546794"
---
# <a name="aggregationrestriction"></a>AggregationRestriction

El **elemento AggregationRestriction** especifica un valor que se aplica a un conjunto de propiedades de Persona resultantes de una solicitud FindPeople y filtra el resultado según la restricción especificada. 
  
```XML
<AggregationRestriction>
   <SearchExpression/>
</AggregationRestriction>
```

 **RestrictionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[SearchExpression](searchexpression.md)
  
### <a name="parent-elements"></a>Elementos principales

[FindPeople](findpeople.md)
  
## <a name="remarks"></a>Comentarios

El **elemento AggregationRestriction** puede contener cualquier elemento secundario que use el grupo de sustitución **SearchExpression.** Los elementos que forman parte del grupo de sustitución **SearchExpression** son: [Contains](contains.md), [Excludes](excludes.md), [Exists](exists.md), [Not](not.md), [Or](or.md), [And](and.md), [IsEqualTo](isequalto.md), [IsNotEqualTo](isnotequalto.md), [IsGreaterThan](isgreaterthan.md), [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md), [IsLessThan](islessthan.md)y [IsLessThanOrEqualTo](islessthanorequalto.md).
  
Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |messages.xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

