---
title: TextBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bd0c0bce-3e7c-47c7-af7f-5ee5f5ad9820
description: El elemento TextBody especifica el cuerpo del texto.
ms.openlocfilehash: c0002785fb990a251267218f7a5f232e521db41a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459486"
---
# <a name="textbody"></a>TextBody

El elemento **TextBody** especifica el cuerpo del texto. 
  
```XML
<TextBody BodyTypeType=" HTML | Text" IsTruncated=" true | false"></TextBody>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|BodyTypeType  <br/> |Indica el tipo de cuerpo. El valor de **Text** para el atributo **BodyTypeType** indica que el cuerpo está en forma de texto sin formato. El valor de **HTML** para el atributo **BodyTypeType** indica que el cuerpo está en formato HTML. El atributo **BodyTypeType** es obligatorio.  <br/> |
|IsTruncated  <br/> |Indica que se ha truncado el contenido del cuerpo. Un valor de texto **falso** para el atributo **IsTruncated** indica que el contenido del cuerpo no se ha truncado. El cuerpo normalizado se truncará si la longitud del cuerpo del texto es mayor que el valor establecido en el elemento [MaximumBodySize](maximumbodysize.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[Elemento](item.md)  |  [Contacto](contact.md)  |  [Mensaje de error](message-ex15websvcsotherref.md)  |  [DistributionList](distributionlist.md)  |  [CalendarItem](calendaritem.md)  |  [PostItem](postitem.md)  |  [Tarea](task.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **TextBody** es el cuerpo del texto del elemento. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

