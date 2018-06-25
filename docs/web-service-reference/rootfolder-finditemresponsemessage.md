---
title: RootFolder (FindItemResponseMessage)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootFolder
api_type:
- schema
ms.assetid: 187e009f-efaa-42a8-8962-329a645213ab
description: El elemento RootFolder contiene los resultados de una búsqueda de una sola carpeta raíz durante una operación de FindItem.
ms.openlocfilehash: ea17369ef4efc4112a738b430c8f0dbab3886341
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837254"
---
# <a name="rootfolder-finditemresponsemessage"></a>RootFolder (FindItemResponseMessage)

El elemento **RootFolder** contiene los resultados de una búsqueda de una sola carpeta raíz durante una [operación de FindItem](finditem-operation.md).
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Items/>
   <Groups/>
</RootFolder>
```

 **FindItemParentType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |Representa el siguiente índice que se debe usar para la solicitud siguiente cuando se usa una vista indizada de paginación.  <br/> |
|**NumeratorOffset** <br/> |Representa el nuevo valor numerador debe usar para la solicitud siguiente con vistas de página de fracción.  <br/> |
|**AbsoluteDenominator** <br/> |Representa el denominador siguiente para usar para la solicitud siguiente al realizar la paginación fraccionaria.  <br/> |
|**IncludesLastItemInRange** <br/> |Indica si los resultados actuales contienen el último elemento de la consulta, por ejemplo, que no es necesaria la paginación aún más.  <br/> |
|**TotalItemsInView** <br/> |Representa el número total de elementos que pase la restricción. En una [operación FindItem](finditem-operation.md)agrupada, el atributo **TotalItemsInView** devuelve el número total de elementos en la vista más el número total de grupos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Items](items.md) <br/> |Contiene una matriz de elementos que tienen los criterios de búsqueda identificados en la solicitud de [operación FindItem](finditem-operation.md) .  <br/> |
|[Grupos](groups.md) <br/> |Contiene una colección de grupos encontrados que cumplen los criterios de búsqueda y agregación identificados en la solicitud de [operación FindItem](finditem-operation.md) .  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación FindItem](finditem-operation.md) .  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación FindItem](finditem-operation.md)
  
[IndexedPagingOffset](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IndexedPagingOffset.aspx)
  
[NumeratorOffset](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.NumeratorOffset.aspx)
  
[AbsoluteDenominator](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.AbsoluteDenominator.aspx)
  
[IncludesLastItemInRange](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IncludesLastItemInRange.aspx)
  
[TotalItemsInView](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.TotalItemsInView.aspx)


[Buscar elementos](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

