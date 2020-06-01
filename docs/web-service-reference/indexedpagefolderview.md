---
title: IndexedPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedPageFolderView
api_type:
- schema
ms.assetid: c6dac232-244b-4db0-9a15-5e01b8aa7a7d
description: El elemento IndexedPageFolderView describe cómo se devuelve la información del elemento paginado en una respuesta FindFolder.
ms.openlocfilehash: 6e9e2796c0bdcd9a15487f0e1bc7cbdf09d0a492
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457203"
---
# <a name="indexedpagefolderview"></a>IndexedPageFolderView

El elemento **IndexedPageFolderView** describe cómo se devuelve la información del elemento paginado en una respuesta [FindFolder](findfolder.md) . 
  
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
|**MaxEntriesReturned** <br/> |Describe el número máximo de carpetas que se devolverá en la respuesta. Este atributo es opcional.  <br/> |
|**Offset** <br/> |Describe el desplazamiento desde **BasePoint**. El desplazamiento debe ser mayor o igual que cero. Si **BasePoint** es igual al principio, el desplazamiento es positivo. Si **BasePoint** es igual a end, el desplazamiento se trata como si fuera negativo.  <br/> Esto identifica la carpeta que será la primera carpeta entregada en la respuesta. Este atributo es obligatorio.  <br/> |
|**BasePoint** <br/> |Describe si la página de carpetas se iniciará desde el principio o el final del conjunto de carpetas que se encuentren con los criterios de búsqueda. Buscar desde el final siempre busca hacia atrás. Este atributo es obligatorio.  <br/> |
   
#### <a name="basepoint-attribute"></a>Atributo BasePoint

|**Valor**|**Descripción**|
|:-----|:-----|
|Empezar  <br/> |La vista paginada comienza al principio del conjunto de carpetas encontradas.  <br/> |
|End  <br/> |La vista paginada se inicia al final del conjunto de carpetas encontradas.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Define una solicitud para buscar carpetas en un buzón.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>Comentarios

La búsqueda en el final implica moverse al origen identificado por el desplazamiento. Además, el puntero se mueve hacia atrás el número de registros solicitados. Por ejemplo, si hay 100 registros y el desplazamiento es 25 desde el final, la búsqueda se inicia desde 75. Si se devuelven 10 registros, el puntero se mueve hacia atrás unos 10 registros adicionales a 65 y devuelve los registros 65 a 75. El siguiente índice es 64. El siguiente desplazamiento desde el final de una página es 100 menos 64, que es igual a 36. El valor del siguiente desplazamiento desde el final para obtener la siguiente página indizada es 36.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   

