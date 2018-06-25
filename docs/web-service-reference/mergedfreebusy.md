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
description: El elemento MergedFreeBusy contiene la secuencia de libre/ocupado combinada de datos.
ms.openlocfilehash: 542b9fae0c36b0236bd806e8a9117753968e812c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836449"
---
# <a name="mergedfreebusy"></a>MergedFreeBusy

El elemento **MergedFreeBusy** contiene la secuencia de libre/ocupado combinada de datos. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FreeBusyView](freebusyview.md) <br/> |Contiene la información de disponibilidad para un usuario específico.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto es proporcionado por el servidor si el valor para el elemento [FreeBusyViewType](freebusyviewtype.md) es una de las siguientes: 
  
- DetailedMerged
    
- FreeBusyMerged
    
- MergedOnly
    
El valor de texto es una secuencia de información de disponibilidad. 
  
## <a name="remarks"></a>Comentarios

La secuencia de datos proporcionados por este elemento se define por los elementos [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) y [ventana de tiempo](timewindow.md) . El elemento de la [ventana de tiempo](timewindow.md) define el intervalo de tiempo de consulta de la disponibilidad. El elemento [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) define cómo se divide el tiempo desde el elemento de la [ventana de tiempo](timewindow.md) en intervalos devueltos en el elemento **MergedFreeBusy** . Cada número en la secuencia de **MergedFreeBusy** representa un intervalo único definido por el elemento [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) . En la siguiente tabla se enumera los valores posibles para un intervalo individual. 
  
|**Estilo de dígitos**|**Disponibilidad**|
|:-----|:-----|
|0  <br/> |Gratuito  <br/> |
|1  <br/> |Provisional  <br/> |
|2  <br/> |Ocupado  <br/> |
|3  <br/> |Fuera de la oficina (OOF)  <br/> |
|4  <br/> |No hay datos  <br/> |
   
Por ejemplo, una solicitud de datos de disponibilidad incluye un elemento de la [ventana de tiempo](timewindow.md) que representa cuatro horas y un elemento [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) que representa 60 minutos. Si el calendario del usuario solicitado es OOF durante los primeros 60 minutos, ocupado para el siguientes 90 minutos y no programada para el final de 90 minutos en la ventana de tiempo, la secuencia de **MergedFreeBusy** será 3220. Si un intervalo contiene más de una clasificación de disponibilidad, el número más alto se utiliza para clasificar de ese intervalo. 
  
El nivel de detalle proporcionado por este elemento depende de los permisos concedidos para el solicitante.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserAvailability](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Obtención de disponibilidad del usuario](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

