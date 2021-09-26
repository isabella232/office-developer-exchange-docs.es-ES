---
title: AppointmentState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AppointmentState
api_type:
- schema
ms.assetid: ab3f5d04-ace1-4a15-9107-cefa6c41abc7
description: El elemento AppointmentState especifica el estado de la cita.
ms.openlocfilehash: f984bbd5a1319a6051a3394ed04d56deabbb2c5a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544286"
---
# <a name="appointmentstate"></a>AppointmentState

El **elemento AppointmentState** especifica el estado de la cita. 
  
```XML
<AppointmentState/>
```

 **int**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una reunión en el Exchange almacén.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Este elemento contiene un valor de texto que representa los bits establecidos. Se trata de un número entero. Este elemento es de solo lectura. Solo se devolverá en una respuesta.
  
## <a name="remarks"></a>Comentarios

El valor entero que se devuelve representa la máscara de bits de estado de cita. En la tabla siguiente se describe cada bit.
  
|**Nombre**|**Bit**|**Descripción**|
|:-----|:-----|:-----|
|Ninguno  <br/> |0x0000  <br/> |No se han establecido marcas. Esto solo se usa para una cita que no incluye asistentes.  <br/> |
|Reunión  <br/> |0x0001  <br/> |Esta cita es una reunión.  <br/> |
|Cantidad.Recibida  <br/> |0x0002  <br/> |Esta cita se ha recibido.  <br/> |
|Cancelado  <br/> |0x0004  <br/> |Esta cita se ha cancelado.  <br/> |
   
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

