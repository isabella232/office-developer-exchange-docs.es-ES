---
title: IsOrganizer
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a31ac268-5061-4272-a433-ffaea2fbcfa9
description: El elemento IsOrganizer especifica un valor booleano que indica si esta persona es el organizador de la reunión.
ms.openlocfilehash: a60485146e333e69391dc1771b2c72ef25043a8b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518270"
---
# <a name="isorganizer"></a>IsOrganizer

El **elemento IsOrganizer** especifica un valor booleano que indica si esta persona es el organizador de la reunión. 
  
```XML
<IsOrganizer>true | false</IsOrganizer>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa un mensaje de reunión.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento IsOrganizer** indica que el usuario creó el elemento de calendario o el mensaje de reunión. Un valor de **false** indica que el elemento de calendario o el mensaje de reunión no se creó bv el usuario. 
  
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

