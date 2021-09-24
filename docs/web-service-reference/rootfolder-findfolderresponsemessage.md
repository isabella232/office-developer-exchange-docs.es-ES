---
title: RootFolder (FindFolderResponseMessage)
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
ms.assetid: 5089c815-663f-46be-bc59-aed9ee20f94a
description: El elemento RootFolder contiene los resultados de una búsqueda de una sola carpeta raíz durante una operación FindFolder.
ms.openlocfilehash: 582d4642bb4ecd2816beba6df863eb274762f804
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512278"
---
# <a name="rootfolder-findfolderresponsemessage"></a>RootFolder (FindFolderResponseMessage)

El **elemento RootFolder** contiene los resultados de una búsqueda de una sola carpeta raíz durante una [operación FindFolder](findfolder-operation.md).
  
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
|NumeratorOffset  <br/> |Representa el nuevo valor de numerador que se usará para la siguiente solicitud al usar vistas de página fraccionales.  <br/> |
|AbsoluteDenominator  <br/> |Representa el siguiente denominador que se usará para la siguiente solicitud al realizar la paginación fraccional.  <br/> |
|IncludesLastItemInRange  <br/> |Indica si los resultados actuales contienen la última carpeta de la consulta, de manera que no se necesite más paginación.  <br/> |
|TotalItemsInView  <br/> |Representa el número total de carpetas que pasan la restricción.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Folders](folders-ex15websvcsotherref.md) <br/> |Contiene una matriz de carpetas encontradas mediante la [operación FindFolder](findfolder-operation.md).  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindFolderResponseMessage](findfolderresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación FindFolder.](findfolder-operation.md)  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindFolder](findfolder-operation.md)


[Buscar carpetas](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

