---
title: AggregationRestriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d05044f9-d2ff-4aca-956c-20c9cb2f7709
description: El elemento AggregationRestriction especifica un valor que se aplica a un conjunto de propiedades de rol resultante de una solicitud de FindPeople y filtra el resultado de acuerdo con la restricción especificada.
ms.openlocfilehash: 8b4d5952dedb4de0201d2ecf2219c69f65f7dc09
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763425"
---
# <a name="aggregationrestriction"></a>AggregationRestriction

El elemento **AggregationRestriction** especifica un valor que se aplica a un conjunto de propiedades de rol resultante de una solicitud de FindPeople y filtra el resultado de acuerdo con la restricción especificada. 
  
```XML
<AggregationRestriction>
   <SearchExpression/>
</AggregationRestriction>
```

 **RestrictionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[SearchExpression](searchexpression.md)
  
### <a name="parent-elements"></a>Elementos principales

[FindPeople](findpeople.md)
  
## <a name="remarks"></a>Notas

El elemento **AggregationRestriction** puede contener cualquier elemento secundario que usa el grupo de sustitución **SearchExpression** . Los elementos que forman parte del grupo de sustitución **SearchExpression** son: [Contains](contains.md), [excluye](excludes.md), [Exists](exists.md), [no](not.md), [o](or.md) [y](and.md), [IsEqualTo](isequalto.md), [IsNotEqualTo](isnotequalto.md), [IsGreaterThan ](isgreaterthan.md), [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md), [IsLessThan](islessthan.md)y [IsLessThanOrEqualTo](islessthanorequalto.md).
  
Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |falso  <br/> |
   

