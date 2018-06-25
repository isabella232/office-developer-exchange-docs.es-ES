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
description: El elemento IndexedPageFolderView describe cómo paginada elemento de información se devuelve en una respuesta FindFolder.
ms.openlocfilehash: f32f778daa6fa3fea93ab2bc1951f2407dcf7f80
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835910"
---
# <a name="indexedpagefolderview"></a>IndexedPageFolderView

El elemento **IndexedPageFolderView** describe cómo paginada elemento de información se devuelve en una respuesta [FindFolder](findfolder.md) . 
  
[FindFolder](findfolder.md)
  
[IndexedPageFolderView](indexedpagefolderview.md)
  
```xml
<IndexedPageFolderView MaxEntriesReturned="" Offset="" BasePoint="" />
```

 **IndexedPageViewType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Describe el número máximo de carpetas para devolver en la respuesta. Este atributo es opcional.  <br/> |
|**Offset** <br/> |Describe el desplazamiento desde el **punto base**. Desplazamiento debe ser mayor o igual que cero. Si el **punto base** es igual al principio, el desplazamiento es positivo. Si el **punto base** es igual a End, el desplazamiento se administra como si fuese negativo.  <br/> Esto identifica qué carpeta será la primera carpeta de entrega en la respuesta. Este atributo es necesario.  <br/> |
|**Punto base** <br/> |Describe si la página de las carpetas se iniciará desde el principio o el final del conjunto de carpetas que se encuentran con los criterios de búsqueda. Buscar desde el final siempre busca hacia atrás. Este atributo es necesario.  <br/> |
   
#### <a name="basepoint-attribute"></a>Atributo de punto base

|**Valor**|**Descripción**|
|:-----|:-----|
|Principio  <br/> |La vista de página comienza al principio del conjunto de carpetas que se encuentran.  <br/> |
|End  <br/> |Se inicia la vista de página al final del conjunto de carpetas que se encuentran.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Define una solicitud para buscar las carpetas en un buzón de correo.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>Comentarios

Solicitando a end implica mover para el origen identificado por el desplazamiento. Además, el puntero se mueve de nuevo el número de registros solicitados. Por ejemplo, si hay 100 registros y el desplazamiento es 25 desde el final, la búsqueda comienza desde 75. Si se devuelven 10 registros, el puntero se mueve hacia atrás un 10 adicionales a 65 de registros y devuelve los registros 65 a través de 75. El siguiente índice es 64. El desplazamiento desde el final de una página siguiente es 100 menos 64 que es igual a 36. El valor para el desvío siguiente desde el final para obtener la siguiente página indizada es 36.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   

