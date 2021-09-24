---
title: Cuerpo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 7851ea9b-9f87-4adc-a26f-7a27df4a9bca
description: El elemento Body especifica el cuerpo de un elemento.
ms.openlocfilehash: 47f0726c6ef329fbbefc99be3b1e2d605f852afa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526851"
---
# <a name="body"></a>Cuerpo

El **elemento Body** especifica el cuerpo de un elemento. 
  
```XML
<Body> BodyType="" IsTruncated="" </Body>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|BodyType  <br/> |Especifica el tipo del cuerpo.  <br/> |
|IsTruncated  <br/> |Valor booleano que indica si el cuerpo está truncado.  <br/> |
   
#### <a name="bodytype"></a>BodyType

|**Valor**|**Descripción**|
|:-----|:-----|
|HTML  <br/> |Indica que el cuerpo está en HTML.  <br/> |
|Texto  <br/> |Indica que el cuerpo está en texto.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
|[Contact](contact.md) <br/> |Representa un elemento de contacto en el Exchange almacén.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento genérico en el Exchange almacén.  <br/> |
|[Mensaje](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo Exchange microsoft.  <br/> |
|[PostItem](postitem.md) <br/> |Representa un elemento de publicación en el Exchange almacén.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el Exchange almacén.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento Body** es el contenido del cuerpo del elemento. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

