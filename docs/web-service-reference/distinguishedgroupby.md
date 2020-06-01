---
title: DistinguishedGroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistinguishedGroupBy
api_type:
- schema
ms.assetid: 6ff3ac48-02ba-40ec-a71b-c401bb2b127c
description: El elemento DistinguishedGroupBy proporciona agrupaciones estándar para las consultas FindItem.
ms.openlocfilehash: 004613d55419a19f69e960203ae13d8d906b74c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463142"
---
# <a name="distinguishedgroupby"></a>DistinguishedGroupBy

El elemento **DistinguishedGroupBy** proporciona agrupaciones estándar para las consultas FindItem. 
  
- [FindItem](finditem.md) 
- [DistinguishedGroupBy](distinguishedgroupby.md)
  
```xml
<DistinguishedGroupBy>
   <StandardGroupBy/>
</DistinguishedGroupBy>
```

 **DistinguishedGroupByType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[StandardGroupBy](standardgroupby.md) <br/> |Representa los mecanismos estándar de agrupación y agregación para una operación FindItem agrupada.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón.<br/><br/>La siguiente es la expresión XPath a este elemento:`/FindItem` <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento **DistinguishedGroupBy** se puede Agregar a una operación FindItem cuando los resultados deben ir agrupados y cuando uno de los grupos estándar cumple los requisitos de agrupación. Si no se especifica el elemento **DistinguishedGroupBy** ni el elemento [GroupBy](groupby.md) , los resultados de FindItem se desagruparán de nuevo. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación FindItem](finditem-operation.md)
- [Buscar elementos](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

