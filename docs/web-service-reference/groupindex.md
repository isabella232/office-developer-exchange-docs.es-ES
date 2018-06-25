---
title: GroupIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupIndex
api_type:
- schema
ms.assetid: 7a596ff7-6cc3-4626-a52c-538a92202337
description: El elemento GroupIndex representa el valor de la propiedad que se usa para agrupar los elementos para el grupo actual de elementos de una llamada a una operación FindItem.
ms.openlocfilehash: 8b23f5142a15c099c30209ea48cd04f4af4e8c6a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835762"
---
# <a name="groupindex"></a>GroupIndex

El elemento **GroupIndex** representa el valor de la propiedad que se usa para agrupar los elementos para el grupo actual de elementos de una llamada a una [operación FindItem](finditem-operation.md) . 
  
[FindItemResponse](finditemresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[FindItemResponseMessage](finditemresponsemessage.md)
  
[RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md)
  
[Grupos](groups.md)
  
[GroupedItems](groupeditems.md)
  
[GroupIndex](groupindex.md)
  
```xml
<GroupIndex/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GroupedItems](groupeditems.md) <br/> |Representa una colección de elementos que son el resultado de una [operación FindItem](finditem-operation.md) de agrupada de llamadas.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/FindItemResponse/ResponseMessages/FindItemResponseMessage/RootFolder/Groups/GroupedItems[i]` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Esta propiedad es de sólo lectura.
  
## <a name="remarks"></a>Comentarios

Este elemento sólo se produce en una respuesta de [la operación FindItem](finditem-operation.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación FindItem](finditem-operation.md)


[Buscar elementos](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

