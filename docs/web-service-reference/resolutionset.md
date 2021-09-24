---
title: ResolutionSet
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResolutionSet
api_type:
- schema
ms.assetid: 43d5b876-0e87-4414-9b1d-bff1c1ec825c
description: El elemento ResolutionSet contiene una matriz de resoluciones para un nombre ambiguo.
ms.openlocfilehash: f77b8a94871aa7827c98a3bb15fdf4a3a35c7c55
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521749"
---
# <a name="resolutionset"></a>ResolutionSet

El **elemento ResolutionSet** contiene una matriz de resoluciones para un nombre ambiguo. 
  
[ResolveNamesResponse](resolvenamesresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
  
[ResolutionSet](resolutionset.md)
  
```xml
<ResolutionSet IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Resolution/>
</ResolutionSet>
```

 **ArrayOfResolutionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |Representa el siguiente índice que se debe usar para la siguiente solicitud cuando se usa una vista de página indizada.  <br/> |
|**NumeratorOffset** <br/> |Representa el nuevo valor de numerador que se usará para la siguiente solicitud cuando se usan vistas de página de fracción.  <br/> |
|**AbsoluteDenominator** <br/> |Representa el siguiente denominador que se usará para la siguiente solicitud cuando se usan vistas de página de fracción.  <br/> |
|**IncludesLastItemInRange** <br/> |Este atributo será true si los resultados actuales contienen el último elemento de la consulta, de modo que no se necesite paginación adicional.  <br/> |
|**TotalItemsInView** <br/> |Representa el número total de elementos de la vista.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Resolución](resolution.md) <br/> |Contiene una única entidad resuelta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud ResolveNames.  <br/> |
   
## <a name="remarks"></a>Comentarios

Un **elemento ResolutionSet** puede contener un máximo de 100 entidades resueltas. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[ResolveNames](resolvenames.md)
  
[ResolveNamesResponse](resolvenamesresponse.md)
  
[Operación ResolveNames](resolvenames-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

