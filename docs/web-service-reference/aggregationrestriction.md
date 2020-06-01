---
title: AggregationRestriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d05044f9-d2ff-4aca-956c-20c9cb2f7709
description: El elemento AggregationRestriction especifica un valor que se aplica a un conjunto de propiedades de rol como resultado de una solicitud FindPeople y filtra el resultado de acuerdo con la restricción especificada.
ms.openlocfilehash: f07e54235cf13b43da26ed1c56596d3c7c357bf2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463527"
---
# <a name="aggregationrestriction"></a>AggregationRestriction

El elemento **AggregationRestriction** especifica un valor que se aplica a un conjunto de propiedades de rol como resultado de una solicitud FindPeople y filtra el resultado de acuerdo con la restricción especificada. 
  
```XML
<AggregationRestriction>
   <SearchExpression/>
</AggregationRestriction>
```

 **RestrictionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

[SearchExpression](searchexpression.md)
  
### <a name="parent-elements"></a>Elementos principales

[FindPeople](findpeople.md)
  
## <a name="remarks"></a>Comentarios

El elemento **AggregationRestriction** puede contener cualquier elemento secundario que use el grupo de sustitución **SearchExpression** . Los elementos que forman parte del grupo de sustitución de **SearchExpression** son: [Contains](contains.md), [Excludes](excludes.md), [EXISTS](exists.md), [Not](not.md), [or](or.md), [and](and.md), [IsEqualTo](isequalto.md), [IsNotEqualTo](isnotequalto.md), [IsGreaterThan](isgreaterthan.md), [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md), [IsLessThan](islessthan.md)y [IsLessThanOrEqualTo](islessthanorequalto.md).
  
Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |messages. xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

