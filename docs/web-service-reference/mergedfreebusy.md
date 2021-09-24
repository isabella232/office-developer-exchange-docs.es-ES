---
title: MergedFreeBusy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MergedFreeBusy
api_type:
- schema
ms.assetid: ea45590d-476e-4b68-9fe8-ae392feadfea
description: El elemento MergedFreeBusy contiene la secuencia de datos de disponibilidad combinada.
ms.openlocfilehash: db451d6b2e67313836771604fae57b14b6b3db10
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511033"
---
# <a name="mergedfreebusy"></a>MergedFreeBusy

El **elemento MergedFreeBusy** contiene la secuencia de datos de disponibilidad combinada. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[MergedFreeBusy](mergedfreebusy.md)
  
```xml
<MergedFreeBusy>...</MergedFreeBusy>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FreeBusyView](freebusyview.md) <br/> |Contiene información de disponibilidad para un usuario específico.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a>Valor de texto

El servidor proporciona un valor de texto si el valor del [elemento FreeBusyViewType](freebusyviewtype.md) es uno de los siguientes: 
  
- DetailedMerged
    
- FreeBusyMerged
    
- MergedOnly
    
El valor de texto es una secuencia de información de disponibilidad. 
  
## <a name="remarks"></a>Comentarios

La secuencia de datos proporcionada por este elemento se define mediante los [elementos MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) y [TimeWindow.](timewindow.md) El [elemento TimeWindow](timewindow.md) define el intervalo de tiempo que se consulta para la disponibilidad. El [elemento MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) define cómo se divide la hora del elemento [TimeWindow](timewindow.md) en intervalos devueltos en el **elemento MergedFreeBusy.** Cada número de la **secuencia MergedFreeBusy** representa un intervalo único definido por el [elemento MergedFreeBusyIntervalInMinutes.](mergedfreebusyintervalinminutes.md) En la tabla siguiente se enumeran los valores posibles de un intervalo individual. 
  
|**Dígito**|**Disponibilidad**|
|:-----|:-----|
|0  <br/> |Libre  <br/> |
|1  <br/> |Provisional  <br/> |
|2  <br/> |Ocupado  <br/> |
|3  <br/> |Fuera de la oficina  <br/> |
|4   <br/> |Sin datos  <br/> |
   
Por ejemplo, una solicitud de datos de disponibilidad incluye un elemento [TimeWindow](timewindow.md) que representa cuatro horas y un elemento [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) que representa 60 minutos. Si el calendario del usuario solicitado es OOF durante los primeros 60 minutos, ocupado durante los 90 minutos siguientes y no programado para los últimos 90 minutos en la ventana de tiempo, la secuencia **MergedFreeBusy** será 3220. Si un intervalo contiene más de una clasificación de disponibilidad, se usa el número más alto para clasificar ese intervalo. 
  
El nivel de detalle proporcionado por este elemento depende de los permisos concedidos al solicitante.
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUserAvailability](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

