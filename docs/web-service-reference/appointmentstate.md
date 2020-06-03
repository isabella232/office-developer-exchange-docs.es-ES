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
ms.openlocfilehash: 8b0e827d02e9051f31d43199503dc286c50e2125
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463478"
---
# <a name="appointmentstate"></a>AppointmentState

El elemento **AppointmentState** especifica el estado de la cita. 
  
```XML
<AppointmentState/>
```

 **int**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Este elemento contiene un valor de texto que representa los bits establecidos. Se encuentra en un formato entero. Este elemento es de sólo lectura. Solo se devolverá en una respuesta.
  
## <a name="remarks"></a>Comentarios

El valor entero que se devuelve representa la máscara de la máscara de estado de cita. En la tabla siguiente se describe cada bit.
  
|**Nombre**|**Bit**|**Descripción**|
|:-----|:-----|:-----|
|Ninguno  <br/> |0x0000  <br/> |No se ha establecido ningún marcador. Solo se usa para una cita que no incluye a los asistentes.  <br/> |
|Misma  <br/> |0x0001  <br/> |Esta cita es una reunión.  <br/> |
|Cantidad.Recibida  <br/> |0x0002  <br/> |Esta cita se ha recibido.  <br/> |
|Cancelado  <br/> |0x0004  <br/> |Esta cita se ha cancelado.  <br/> |
   
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

