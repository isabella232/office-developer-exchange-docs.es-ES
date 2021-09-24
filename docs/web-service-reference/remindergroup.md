---
title: ReminderGroup
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3e23c2a1-05d8-4fec-897c-f684a5b97e4c
description: El elemento ReminderGroup especifica si el aviso es para un elemento de calendario o una tarea.
ms.openlocfilehash: 7ec19505e9237680aee1b3a31332db7fdc4c0dd4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512474"
---
# <a name="remindergroup"></a>ReminderGroup

El **elemento ReminderGroup** especifica si el aviso es para un elemento de calendario o una tarea. 
  
```XML
<ReminderGroup> Calendar | Task </ReminderGroup>
```

 **ReminderGroupType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[Aviso](reminder.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento ReminderGroup** es el tipo de grupo del aviso. El valor de texto **de Calendar** especifica que el aviso es para un elemento de calendario. El valor de texto **de Task** especifica que el aviso es para un elemento de tarea. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Aviso](reminder.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

