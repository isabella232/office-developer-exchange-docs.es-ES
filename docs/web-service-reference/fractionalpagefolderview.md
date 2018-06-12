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
description: El elemento FractionalPageFolderView describe donde se inicia la vista de página y devuelve el número máximo de carpetas en una solicitud FindFolder.
ms.openlocfilehash: 3cb5f8333634a0c484ae3ce6a6256631cff57cc5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764705"
---
# <a name="fractionalpagefolderview"></a>FractionalPageFolderView

El elemento **FractionalPageFolderView** describe donde se inicia la vista de página y devuelve el número máximo de carpetas en una solicitud [FindFolder](findfolder.md) . 
  
[FindFolder](findfolder.md)
  
[FractionalPageFolderView](fractionalpagefolderview.md)
  
```xml
<FractionalPageFolderView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 **FractionalPageViewType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Identifica el número máximo de resultados a devolver en la respuesta [FindFolder](findfolder.md) . Este atributo es opcional.  <br/> |
|**Numerador** <br/> |Representa el numerador de la fraccionario desplazamiento desde el comienzo del conjunto de resultados. Este atributo es necesario. El numerador debe ser igual o menor que el denominador. Este atributo debe representar un valor entero que es igual o mayor que cero. Para obtener más información, vea Comentarios más adelante en este tema.  <br/> |
|**Denominador** <br/> |Representa el denominador de la fraccionario desplazamiento desde el comienzo del número total de carpetas en el conjunto de resultados. Este atributo es necesario. Este atributo debe representar un valor entero que es mayor que uno. Para obtener más información, vea Comentarios más adelante en este tema.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Define una solicitud para identificar las carpetas de un buzón de correo.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a>Notas

Se describe el desplazamiento de la vista de página desde el comienzo del conjunto de carpetas que se encuentran por una fracción. La fracción, que se define mediante los atributos **numerador** y **denominador** , describe donde se inicia la página de información. Por ejemplo, si **numerador** es igual a cuatro y **denominador** es igual a cinco, la página de información devuelta que comienza en una entrada que encuentra cuatro quintos de la forma en el conjunto de resultados. 
  
Si el argumento de fracción se evalúa como cero, indica el inicio del conjunto de resultados. Si el argumento de fracción se evalúa como uno, indica el final del conjunto de resultados.
  
> [!NOTE]
> La fracción representa el punto inicial de la página, se devolverán resultados no cuántos en el conjunto de resultados. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindFolder](findfolder-operation.md)


[Buscar carpetas](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

