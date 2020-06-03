---
title: ResolutionSet
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolutionSet
api_type:
- schema
ms.assetid: 43d5b876-0e87-4414-9b1d-bff1c1ec825c
description: El elemento ResolutionSet contiene una matriz de resoluciones para un nombre ambiguo.
ms.openlocfilehash: 483a096a7fcedbabe25758ebcaa31c83405a0ad4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467175"
---
# <a name="resolutionset"></a>ResolutionSet

El elemento **ResolutionSet** contiene una matriz de resoluciones para un nombre ambiguo. 
  
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
|**NumeratorOffset** <br/> |Representa el nuevo valor del numerador que se va a usar para la siguiente solicitud cuando se usan vistas de página de fracción.  <br/> |
|**AbsoluteDenominator** <br/> |Representa el siguiente denominador que se va a usar para la siguiente solicitud cuando se usan vistas de página de fracción.  <br/> |
|**IncludesLastItemInRange** <br/> |Este atributo será true si los resultados actuales contienen el último elemento de la consulta, por lo que no se necesita ninguna paginación adicional.  <br/> |
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

Un elemento **ResolutionSet** puede contener un máximo de 100 entidades resueltas. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[ResolveNames](resolvenames.md)
  
[ResolveNamesResponse](resolvenamesresponse.md)
  
[Operación ResolveNames](resolvenames-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

