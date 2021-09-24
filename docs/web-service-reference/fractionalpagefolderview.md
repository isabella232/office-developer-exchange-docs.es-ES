---
title: FractionalPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FractionalPageFolderView
api_type:
- schema
ms.assetid: ef681f8a-136a-4c0e-ade6-ddcdbf2d85ad
description: El elemento FractionalPageFolderView describe dónde se inicia la vista paginada y el número máximo de carpetas devueltas en una solicitud FindFolder.
ms.openlocfilehash: b3d4bd63f94c2db7761dabfad1e32558ceb30be5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530256"
---
# <a name="fractionalpagefolderview"></a>FractionalPageFolderView

El **elemento FractionalPageFolderView** describe dónde se inicia la vista paginada y el número máximo de carpetas devueltas en una [solicitud FindFolder.](findfolder.md) 
  
[FindFolder](findfolder.md)
  
[FractionalPageFolderView](fractionalpagefolderview.md)
  
```xml
<FractionalPageFolderView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 **FractionalPageViewType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Identifica el número máximo de resultados que se devolverán en la [respuesta FindFolder.](findfolder.md) Este atributo es opcional.  <br/> |
|**Numerador** <br/> |Representa el numerador del desplazamiento fraccional desde el inicio del conjunto de resultados. Este atributo es obligatorio. El numerador debe ser igual o menor que el denominador. Este atributo debe representar un valor integral igual o mayor que cero. Para obtener más información, vea Comentarios más adelante en este tema.  <br/> |
|**Denominador** <br/> |Representa el denominador del desplazamiento fraccionado desde el inicio del número total de carpetas del conjunto de resultados. Este atributo es obligatorio. Este atributo debe representar un valor integral mayor que uno. Para obtener más información, vea Comentarios más adelante en este tema.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Define una solicitud para identificar carpetas de un buzón.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>Comentarios

El desplazamiento de vista paginada desde el inicio del conjunto de carpetas encontradas se describe mediante una fracción. La fracción, definida por los atributos **Numerador** y **Denominador,** describe dónde comienza la página de información. Por ejemplo, si **Numerador** es igual a cuatro y **Denominador** es igual a cinco, la página de información devuelta comienza en una entrada ubicada cuatro quintas partes del camino en el conjunto de resultados. 
  
Si la fracción se evalúa en cero, esto indica el inicio del conjunto de resultados. Si la fracción se evalúa en uno, esto indica el final del conjunto de resultados.
  
> [!NOTE]
> La fracción representa el punto inicial de la página, no cuántos resultados se devolverán en el conjunto de resultados. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindFolder](findfolder-operation.md)


[Buscar carpetas](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

