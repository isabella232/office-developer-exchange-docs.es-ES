---
title: TextBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bd0c0bce-3e7c-47c7-af7f-5ee5f5ad9820
description: El elemento TextBody especifica el cuerpo de texto.
ms.openlocfilehash: 78b18b27891d571605d2eeeeffb5c252cc790c11
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840640"
---
# <a name="textbody"></a>TextBody

El elemento **TextBody** especifica el cuerpo de texto. 
  
```XML
<TextBody BodyTypeType=" HTML | Text" IsTruncated=" true | false"></TextBody>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|BodyTypeType  <br/> |Indica el tipo de cuerpo. El valor de **texto** para el atributo **BodyTypeType** indica que el cuerpo tiene formato de texto sin formato. El valor de **HTML** para el atributo **BodyTypeType** indica que el cuerpo está en formato HTML. Se requiere el atributo **BodyTypeType** .  <br/> |
|IsTruncated  <br/> |Indica que el contenido del cuerpo se ha truncado. Un valor de texto de **false** para el atributo **IsTruncated** indica que no se ha truncado el contenido del cuerpo. Si la longitud del texto del cuerpo es mayor que el valor establecido en el elemento [MaximumBodySize](maximumbodysize.md) , se truncará el cuerpo normalizado.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[Elemento](item.md) | [contacto](contact.md) | [mensaje](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [tarea](task.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **TextBody** es el cuerpo de texto del elemento. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

