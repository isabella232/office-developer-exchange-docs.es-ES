---
title: RootFolder (FindItemResponseMessage)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RootFolder
api_type:
- schema
ms.assetid: 187e009f-efaa-42a8-8962-329a645213ab
description: El elemento RootFolder contiene los resultados de una búsqueda de una sola carpeta raíz durante una operación FindItem.
ms.openlocfilehash: 96fa9e162dde34394e7c34543dd25a6f018ae7de
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527540"
---
# <a name="rootfolder-finditemresponsemessage"></a>RootFolder (FindItemResponseMessage)

El **elemento RootFolder** contiene los resultados de una búsqueda de una sola carpeta raíz durante una [operación FindItem](finditem-operation.md).
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Items/>
   <Groups/>
</RootFolder>
```

 **FindItemParentType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |Representa el siguiente índice que se debe usar para la siguiente solicitud al usar una vista de paginación indizada.  <br/> |
|**NumeratorOffset** <br/> |Representa el nuevo valor de numerador que se usará para la siguiente solicitud al usar vistas de página de fracción.  <br/> |
|**AbsoluteDenominator** <br/> |Representa el siguiente denominador que se usará para la siguiente solicitud al realizar la paginación fraccional.  <br/> |
|**IncludesLastItemInRange** <br/> |Indica si los resultados actuales contienen el último elemento de la consulta, de manera que no se necesite una paginación adicional.  <br/> |
|**TotalItemsInView** <br/> |Representa el número total de elementos que pasan la restricción. En una operación [FindItem agrupada,](finditem-operation.md)el atributo **TotalItemsInView** devuelve el número total de elementos de la vista más el número total de grupos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Items](items.md) <br/> |Contiene una matriz de elementos encontrados que tienen los criterios de búsqueda identificados en la [solicitud de operación FindItem.](finditem-operation.md)  <br/> |
|[Grupos](groups.md) <br/> |Contiene una colección de grupos encontrados que tienen los criterios de búsqueda y agregación identificados en la [solicitud de operación FindItem.](finditem-operation.md)  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindItemResponseMessage](finditemresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación FindItem.](finditem-operation.md)  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que se ejecuta Exchange Server con el rol de servidor acceso de cliente instalado.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindItem](finditem-operation.md)
  
[IndexedPagingOffset](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IndexedPagingOffset.aspx)
  
[NumeratorOffset](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.NumeratorOffset.aspx)
  
[AbsoluteDenominator](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.AbsoluteDenominator.aspx)
  
[IncludesLastItemInRange](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IncludesLastItemInRange.aspx)
  
[TotalItemsInView](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.TotalItemsInView.aspx)


[Buscar elementos](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

