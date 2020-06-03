---
title: FindPeople
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 12c70441-77b9-4619-8e66-1b7e3a63ba48
description: 'El elemento FindPeople especifica un conjunto de datos que se usa en una solicitud de FindPeople. Los datos incluyen cero o más de los siguientes elementos: una forma persona (opcional), una vista de elemento de página indizada, una restricción (opcional), una restricción de agregación (opcional), un criterio de ordenación (opcional), un identificador de carpeta principal y una cadena de consulta (opcional).'
ms.openlocfilehash: 4777601b7146ec857b5c79fa9d4ced59a7247889
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462904"
---
# <a name="findpeople"></a>FindPeople

El elemento **FindPeople** especifica un conjunto de datos que se usa en una solicitud de FindPeople. Los datos incluyen cero o más de los siguientes elementos: una forma persona (opcional), una vista de elemento de página indizada, una restricción (opcional), una restricción de agregación (opcional), un criterio de ordenación (opcional), un identificador de carpeta principal y una cadena de consulta (opcional). 
  
```XML
<FindPeople>
   <PersonaShape/>
   <IndexedPageItemView/>
   <Restriction/>
   <AggregationRestriction/>
   <SortOrder/>
   <ParentFolderId/>
   <QueryString/>
</FindPeople>
```

 **FindPeopleType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

[PersonaShape](personashape.md)  |  [IndexedPageItemView](indexedpageitemview.md)  |  [Restricción](restriction.md)  |  [AggregationRestriction](aggregationrestriction.md)  |  [SortOrder](sortorder.md)  |  [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)  |  [QueryString (QueryStringType)](querystring-querystringtype.md)
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |messages. xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

