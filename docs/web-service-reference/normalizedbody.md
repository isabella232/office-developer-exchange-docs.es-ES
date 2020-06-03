---
title: NormalizedBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfb813e4-642d-4f1b-9e91-1fee89dbd083
description: El elemento NormalizedBody especifica una representación HTML de la propiedad Body de un elemento como un fragmento que se puede insertar en otro cuerpo HTML.
ms.openlocfilehash: fb249794bccfeed198e7a3230ab53c66893dcf96
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462671"
---
# <a name="normalizedbody"></a>NormalizedBody

El elemento **NormalizedBody** especifica una representación HTML de la propiedad **Body** de un elemento como un fragmento que se puede insertar en otro cuerpo HTML. 
  
```XML
<NormalizedBody BodyType="Text | HTML" IsTruncated="true | false"></NormalizedBody>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|BodyType  <br/> |Indica el tipo de cuerpo. El valor de **Text** para el atributo **BodyType** indica que el cuerpo está en forma de texto sin formato. El valor de **HTML** para el atributo **BodyType** indica que el cuerpo está en formato HTML. El atributo **BodyType** es obligatorio.  <br/> |
|IsTruncated  <br/> |Indica que se ha truncado el contenido del cuerpo. Un valor de texto **falso** para el atributo **IsTruncated** indica que el contenido del cuerpo no se ha truncado. El cuerpo normalizado se truncará si la longitud del cuerpo normalizado es mayor que el valor establecido en el elemento [MaximumBodySize](maximumbodysize.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[Elemento](item.md)  |  [Mensaje de error](message-ex15websvcsotherref.md)  |  [MeetingMessage](meetingmessage.md)  |  Propiedad [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [Tarea](task.md)  |  [PostItem](postitem.md)  |  [CalendarItem](calendaritem.md)  |  [Contacto](contact.md)  |  [DistributionList](distributionlist.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **NormalizedBody** es el cuerpo normalizado del elemento. 
  
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
   

