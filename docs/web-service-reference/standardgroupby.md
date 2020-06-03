---
title: StandardGroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StandardGroupBy
api_type:
- schema
ms.assetid: 04a84f71-b7eb-44dc-ac2c-ed504b52c463
description: El elemento StandardGroupBy representa los mecanismos estándar de agrupación y agregación para una operación FindItem agrupada.
ms.openlocfilehash: 3e135feba322979de3d66d5a45d423654ccc9100
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467560"
---
# <a name="standardgroupby"></a>StandardGroupBy

El elemento **StandardGroupBy** representa los mecanismos estándar de agrupación y agregación para una operación FindItem agrupada. 
  
[FindItem](finditem.md)
  
[DistinguishedGroupBy](distinguishedgroupby.md)
  
[StandardGroupBy](standardgroupby.md)
  
```xml
<StandardGroupBy/>
```

 **StandardGroupByType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DistinguishedGroupBy](distinguishedgroupby.md) <br/> |Proporciona agrupaciones estándar para las consultas FindItem.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El único valor que se puede usar para este elemento es **ConversationTopic**. **ConversationTopic** grupos por mensaje: ConversationTopic y agregados en el elemento: DateTimeReceived (máximo). Para obtener más información acerca de la agregación, vea [AggregateOn](aggregateon.md).
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación FindItem](finditem-operation.md)
  
[FindItem](finditem.md)


[Buscar elementos](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

