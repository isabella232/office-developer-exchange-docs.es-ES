---
title: IndexedPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IndexedPageFolderView
api_type:
- schema
ms.assetid: c6dac232-244b-4db0-9a15-5e01b8aa7a7d
description: El elemento IndexedPageFolderView describe cómo se devuelve la información del elemento paginado en una respuesta FindFolder.
ms.openlocfilehash: 0a5d0f7e63549b7a851862d957ff32dff4333ce3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542242"
---
# <a name="indexedpagefolderview"></a>IndexedPageFolderView

El **elemento IndexedPageFolderView** describe cómo se devuelve la información del elemento paginado en una [respuesta FindFolder.](findfolder.md) 
  
[FindFolder](findfolder.md)
  
[IndexedPageFolderView](indexedpagefolderview.md)
  
```xml
<IndexedPageFolderView MaxEntriesReturned="" Offset="" BasePoint="" />
```

 **IndexedPageViewType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Describe el número máximo de carpetas que se devolverán en la respuesta. Este atributo es opcional.  <br/> |
|**Offset** <br/> |Describe el desplazamiento desde **BasePoint**. El desplazamiento debe ser mayor o igual que cero. Si **BasePoint** es igual a Beginning, el desplazamiento es positivo. Si **BasePoint** es igual a End, el desplazamiento se controla como si fuera negativo.  <br/> Esto identifica qué carpeta será la primera carpeta entregada en la respuesta. Este atributo es obligatorio.  <br/> |
|**BasePoint** <br/> |Describe si la página de carpetas se iniciará desde el inicio o el final del conjunto de carpetas que se encuentran con los criterios de búsqueda. Buscar desde el final siempre busca hacia atrás. Este atributo es obligatorio.  <br/> |
   
#### <a name="basepoint-attribute"></a>Atributo BasePoint

|**Valor**|**Descripción**|
|:-----|:-----|
|Principio  <br/> |La vista paginada comienza al principio del conjunto de carpetas encontrado.  <br/> |
|End  <br/> |La vista paginada comienza al final del conjunto de carpetas encontrado.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Define una solicitud para buscar carpetas en un buzón.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>Comentarios

Buscar desde el final implica pasar al origen identificado por el desplazamiento. Además, el número de registros solicitados mueve el puntero hacia atrás. Por ejemplo, si hay 100 registros y el desplazamiento es 25 desde el final, la búsqueda comienza a partir de 75. Si se devuelven 10 registros, el puntero se mueve hacia atrás 10 registros adicionales a 65 y devuelve los registros del 65 al 75. El siguiente índice es 64. El siguiente desplazamiento desde el final de una página es 100 menos 64 que es igual a 36. El valor del siguiente desplazamiento desde el final para obtener la siguiente página indizada es 36.
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   

