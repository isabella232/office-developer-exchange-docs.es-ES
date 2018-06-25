---
title: AppointmentState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AppointmentState
api_type:
- schema
ms.assetid: ab3f5d04-ace1-4a15-9107-cefa6c41abc7
description: El elemento AppointmentState especifica el estado de la cita.
ms.openlocfilehash: 05e92a3fea10a84518b0680c425011a91bc43d93
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763538"
---
# <a name="appointmentstate"></a>AppointmentState

El elemento **AppointmentState** especifica el estado de la cita. 
  
```XML
<AppointmentState/>
```

 **int**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Este elemento contiene un valor de texto que representa el conjunto de bits. Esto está en formato de número entero. Este elemento es de sólo lectura. Sólo se devolverán en una respuesta.
  
## <a name="remarks"></a>Comentarios

El valor de número entero que se devuelve representa la máscara de bits de estado de una cita. En la siguiente tabla se describe cada bit.
  
|**Name**|**Bit**|**Descripción**|
|:-----|:-----|:-----|
|None  <br/> |0x0000  <br/> |Se han establecido ningún indicador. Sólo se utiliza para una cita que no incluye a los asistentes.  <br/> |
|Reunión  <br/> |0 x 0001  <br/> |Esta cita es una reunión.  <br/> |
|Cantidad.Recibida  <br/> |0x0002  <br/> |Se ha recibido esta cita.  <br/> |
|Cancelado  <br/> |0x0004  <br/> |Se ha cancelado esta cita.  <br/> |
   
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

