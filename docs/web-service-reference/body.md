---
title: Cuerpo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7851ea9b-9f87-4adc-a26f-7a27df4a9bca
description: El elemento Body especifica el cuerpo de un elemento.
ms.openlocfilehash: a4803c0e5ac3b027396983a5524241590eac35f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763641"
---
# <a name="body"></a>Cuerpo

El elemento **Body** especifica el cuerpo de un elemento. 
  
```XML
<Body> BodyType="" IsTruncated="" </Body>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|BodyType  <br/> |Especifica el tipo del cuerpo.  <br/> |
|IsTruncated  <br/> |Valor booleano que indica si el cuerpo se trunca.  <br/> |
   
#### <a name="bodytype"></a>BodyType

|**Valor**|**Descripción**|
|:-----|:-----|
|HTML  <br/> |Indica que el cuerpo en HTML.  <br/> |
|Texto  <br/> |Indica que es el cuerpo de texto.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[Contact](contact.md) <br/> |Representa un elemento de contacto en el almacén de Exchange.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Item](item.md) <br/> |Representa un elemento genérico en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Microsoft Exchange.  <br/> |
|[Objeto postItem](postitem.md) <br/> |Representa un elemento para exponer en el almacén de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **Body** es el contenido del cuerpo del elemento. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

