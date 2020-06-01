---
title: FractionalPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FractionalPageFolderView
api_type:
- schema
ms.assetid: ef681f8a-136a-4c0e-ade6-ddcdbf2d85ad
description: El elemento FractionalPageFolderView describe dónde se inicia la vista paginada y el número máximo de carpetas que se devuelven en una solicitud FindFolder.
ms.openlocfilehash: a8627c6277b49655d3933679128b844118633cda
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463072"
---
# <a name="fractionalpagefolderview"></a>FractionalPageFolderView

El elemento **FractionalPageFolderView** describe dónde se inicia la vista paginada y el número máximo de carpetas que se devuelven en una solicitud [FindFolder](findfolder.md) . 
  
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
|**MaxEntriesReturned** <br/> |Identifica el número máximo de resultados que se devolverá en la respuesta [FindFolder](findfolder.md) . Este atributo es opcional.  <br/> |
|**Numera** <br/> |Representa el numerador del desplazamiento fraccionario desde el inicio del conjunto de resultados. Este atributo es obligatorio. El numerador debe ser igual o menor que el denominador. Este atributo debe representar un valor integral que sea igual o mayor que cero. Para obtener más información, vea las notas más adelante en este tema.  <br/> |
|**Denominador** <br/> |Representa el denominador del desplazamiento fraccionario desde el principio del número total de carpetas del conjunto de resultados. Este atributo es obligatorio. Este atributo debe representar un valor integral que sea mayor que uno. Para obtener más información, vea las notas más adelante en este tema.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Define una solicitud para identificar las carpetas en un buzón.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>Comentarios

El desplazamiento de vista paginada desde el principio del conjunto de carpetas encontradas se describe mediante una fracción. La fracción, definida por los atributos **numerador** y **denominador** , describe dónde comienza la página de información. Por ejemplo, si el **numerador** es igual a cuatro y el **denominador** es cinco, la página de la información devuelta comienza en una entrada que se encuentra cuatro-quintos de la forma en el conjunto de resultados. 
  
Si la fracción da como resultado cero, indica el inicio del conjunto de resultados. Si la fracción da como resultado una, que indica el final del conjunto de resultados.
  
> [!NOTE]
> La fracción representa el punto de inicio de la página, no el número de resultados que se devolverán en el conjunto de resultados. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
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

