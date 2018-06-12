---
title: ReminderGroup
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e23c2a1-05d8-4fec-897c-f684a5b97e4c
description: El elemento ReminderGroup especifica si el aviso es para un elemento de calendario o una tarea.
ms.openlocfilehash: d9d31cdab482d04149428021ad44cc742108053a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837060"
---
# <a name="remindergroup"></a>ReminderGroup

El elemento **ReminderGroup** especifica si el aviso es para un elemento de calendario o una tarea. 
  
```XML
<ReminderGroup> Calendar | Task </ReminderGroup>
```

 **ReminderGroupType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[Aviso](reminder.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **ReminderGroup** es el tipo de grupo del aviso. El valor de texto del **calendario** especifica que es un aviso de un elemento de calendario. El valor de texto de **tarea** especifica que es un aviso de un elemento de tarea. 
  
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Aviso](reminder.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

