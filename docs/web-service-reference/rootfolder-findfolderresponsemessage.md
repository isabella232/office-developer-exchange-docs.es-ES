---
title: RootFolder (FindFolderResponseMessage)
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
ms.assetid: 5089c815-663f-46be-bc59-aed9ee20f94a
description: El elemento RootFolder contiene los resultados de una búsqueda de una sola carpeta raíz durante una operación FindFolder.
ms.openlocfilehash: b5601d6abec67196c9991908e272a2122a201d69
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457140"
---
# <a name="rootfolder-findfolderresponsemessage"></a>RootFolder (FindFolderResponseMessage)

El elemento **RootFolder** contiene los resultados de una búsqueda de una sola carpeta raíz durante una [operación FindFolder](findfolder-operation.md).
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Folders/>
</RootFolder>
```

 **FindFolderParentType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|IndexedPagingOffset  <br/> |Representa el siguiente índice que se debe usar para la siguiente solicitud al usar una vista de paginación indizada.  <br/> |
|NumeratorOffset  <br/> |Representa el nuevo valor del numerador que se va a usar para la siguiente solicitud cuando se usan vistas de página fraccionarias.  <br/> |
|AbsoluteDenominator  <br/> |Representa el siguiente denominador que se va a usar para la siguiente solicitud cuando se realiza una paginación fraccionada.  <br/> |
|IncludesLastItemInRange  <br/> |Indica si los resultados actuales contienen la última carpeta de la consulta, de modo que no es necesario realizar más paginación.  <br/> |
|TotalItemsInView  <br/> |Representa el número total de carpetas que superan la restricción.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Folders](folders-ex15websvcsotherref.md) <br/> |Contiene una matriz de carpetas que se han encontrado mediante la [operación FindFolder](findfolder-operation.md).  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación FindFolder](findfolder-operation.md) .  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación FindFolder](findfolder-operation.md)


[Buscar carpetas](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

