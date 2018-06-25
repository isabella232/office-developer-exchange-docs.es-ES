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
description: El elemento ResolutionSet contiene una matriz de soluciones para un nombre ambiguo.
ms.openlocfilehash: ad7bd31c85051e8c80aea25aa9e6f2914cf0ad01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837160"
---
# <a name="resolutionset"></a>ResolutionSet

El elemento **ResolutionSet** contiene una matriz de soluciones para un nombre ambiguo. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |Representa el siguiente índice que se debe usar para la solicitud siguiente cuando se usa una vista de página indizados.  <br/> |
|**NumeratorOffset** <br/> |Representa el nuevo valor: número que se usará para la solicitud siguiente cuando se utilizan vistas de página de fracción.  <br/> |
|**AbsoluteDenominator** <br/> |Representa el denominador siguiente para usar para la solicitud siguiente cuando se utilizan vistas de página de fracción.  <br/> |
|**IncludesLastItemInRange** <br/> |Este atributo será true si los resultados actuales contienen el último elemento de la consulta, por lo que no es necesaria la paginación adicional.  <br/> |
|**TotalItemsInView** <br/> |Representa el número total de elementos en la vista.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Resoluci?n](resolution.md) <br/> |Contiene una única entidad resuelta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de ResolveNames.  <br/> |
   
## <a name="remarks"></a>Comentarios

Un elemento **ResolutionSet** puede contener un máximo de 100 entidades resueltos. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[ResolveNames](resolvenames.md)
  
[ResolveNamesResponse](resolvenamesresponse.md)
  
[Operación ResolveNames](resolvenames-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

