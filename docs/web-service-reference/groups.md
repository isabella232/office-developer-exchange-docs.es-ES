---
title: Grupos
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Groups
api_type:
- schema
ms.assetid: 6b6b2d67-219d-4dfb-a4ed-d627b1cfb33f
description: El elemento Groups contiene una colección de grupos que se encuentran con los criterios de búsqueda y agregación que se identifican en la solicitud de operación FindItem.
ms.openlocfilehash: f47ab4111137d2e5d98fcc6dcf40fadc073b7af9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539685"
---
# <a name="groups"></a>Grupos

El **elemento Groups** contiene una colección de grupos que se encuentran con los criterios de búsqueda y agregación que se identifican en la solicitud de operación [FindItem.](finditem-operation.md) 
  
```xml
<Groups>
   <GroupedItems/>
</Groups>
```

 **ArrayOfGroupedItemsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GroupedItems](groupeditems.md) <br/> |Representa una colección de elementos que son el resultado de una llamada de operación [FindItem](finditem-operation.md) agrupada.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md) <br/> |Contiene los resultados de una búsqueda de una sola carpeta raíz durante una [operación FindItem.](finditem-operation.md)  <br/> |
   
## <a name="remarks"></a>Comentarios

Se [producirá una instancia GroupedItems](groupeditems.md) para cada grupo distinto dentro del resultado. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindItem](finditem-operation.md)


[Buscar elementos](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

