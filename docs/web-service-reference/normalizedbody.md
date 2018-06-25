---
title: NormalizedBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfb813e4-642d-4f1b-9e91-1fee89dbd083
description: El elemento NormalizedBody especifica una representación HTML de la propiedad de cuerpo de un elemento como un fragmento que puede insertarse en otro cuerpo HTML.
ms.openlocfilehash: 07c2176d2c8a7473c06b7e42f8bcbbe6670581ef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836548"
---
# <a name="normalizedbody"></a>NormalizedBody

El elemento **NormalizedBody** especifica una representación HTML de la propiedad de **cuerpo** de un elemento como un fragmento que puede insertarse en otro cuerpo HTML. 
  
```XML
<NormalizedBody BodyType="Text | HTML" IsTruncated="true | false"></NormalizedBody>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|BodyType  <br/> |Indica el tipo de cuerpo. El valor de **texto** para el atributo **BodyType** indica que el cuerpo tiene formato de texto sin formato. El valor de **HTML** para el atributo **BodyType** indica que el cuerpo está en formato HTML. El atributo **BodyType** es necesario.  <br/> |
|IsTruncated  <br/> |Indica que el contenido del cuerpo se ha truncado. Un valor de texto de **false** para el atributo **IsTruncated** indica que no se ha truncado el contenido del cuerpo. Si la longitud del cuerpo normalizado es mayor que el valor establecido en el elemento [MaximumBodySize](maximumbodysize.md) , se truncará el cuerpo normalizado.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[Elemento](item.md) | [mensaje](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [tarea](task.md) | [PostItem ](postitem.md)  |  [CalendarItem](calendaritem.md) | [contacto](contact.md) | [DistributionList](distributionlist.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **NormalizedBody** es el cuerpo del elemento normalizado. 
  
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
   

