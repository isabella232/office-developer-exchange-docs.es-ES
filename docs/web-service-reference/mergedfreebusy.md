---
title: MergedFreeBusy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MergedFreeBusy
api_type:
- schema
ms.assetid: ea45590d-476e-4b68-9fe8-ae392feadfea
description: El elemento MergedFreeBusy contiene la secuencia de datos de disponibilidad combinada.
ms.openlocfilehash: a1483449534f0d886e3c97a23d28c5d78f865042
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468729"
---
# <a name="mergedfreebusy"></a>MergedFreeBusy

El elemento **MergedFreeBusy** contiene la secuencia de datos de disponibilidad combinada. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FreeBusyView](freebusyview.md) <br/> |Contiene la información de disponibilidad de un usuario específico.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a>Valor de texto

El servidor proporciona un valor de texto si el valor del elemento [FreeBusyViewType](freebusyviewtype.md) es uno de los siguientes: 
  
- DetailedMerged
    
- FreeBusyMerged
    
- MergedOnly
    
El valor de texto es una secuencia de información de disponibilidad. 
  
## <a name="remarks"></a>Comentarios

La secuencia de datos proporcionada por este elemento se define mediante los elementos [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) y [TimeWindow](timewindow.md) . El elemento [TimeWindow](timewindow.md) define el intervalo de tiempo consultado para la disponibilidad. El elemento [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) define cómo se divide la hora del elemento [TimeWindow](timewindow.md) en intervalos devueltos en el elemento **MergedFreeBusy** . Cada número de la secuencia **MergedFreeBusy** representa un intervalo único definido por el elemento [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) . En la siguiente tabla se enumeran los valores posibles para un intervalo individual. 
  
|**Digitaliza**|**Disponibilidad**|
|:-----|:-----|
|comprendi  <br/> |Libre  <br/> |
|1   <br/> |Provisional  <br/> |
|segundo  <br/> |Ocupado  <br/> |
|3  <br/> |Fuera de la oficina  <br/> |
|4   <br/> |No hay datos  <br/> |
   
Por ejemplo, una solicitud de datos de disponibilidad incluye un elemento [TimeWindow](timewindow.md) que representa cuatro horas y un elemento [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) que representa 60 minutos. Si el calendario del usuario solicitado es OOF para los primeros 60 minutos, ocupado durante los siguientes 90 minutos y no programado para los 90 minutos finales en el intervalo de tiempo, la secuencia **MergedFreeBusy** será 3220. Si un intervalo contiene más de una clasificación de disponibilidad, el número más alto se usa para clasificar ese intervalo. 
  
El nivel de detalle proporcionado por este elemento depende de los permisos concedidos al solicitante.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserAvailability](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

