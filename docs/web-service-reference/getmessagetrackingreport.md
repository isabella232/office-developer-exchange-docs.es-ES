---
title: GetMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMessageTrackingReport
api_type:
- schema
ms.assetid: b6ffa8ef-90f6-402d-afac-c3f5ee55cf49
description: El elemento GetMessageTrackingReport contiene la solicitud para la operación GetMessageTrackingReport recuperar el mensaje completo informe de seguimiento para el identificador especificado.
ms.openlocfilehash: cb16f6e9d322cefb0d59c962af8e2f60ebae0e90
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764912"
---
# <a name="getmessagetrackingreport"></a>GetMessageTrackingReport

El elemento **GetMessageTrackingReport** contiene la solicitud para la [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md) recuperar el mensaje completo informe de seguimiento para el identificador especificado. 
  
```XML
<GetMessageTrackingReport>
   <Scope/>
   <ReportTemplate/>
   <RecipientFilter/>
   <MessageTrackingReportId/>
   <ReturnQueueEvents/>
   <DiagnosticsLevel/>
   <Properties/>
</GetMessageTrackingReport>
```

 **GetMessageTrackingReportRequestType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Ámbito (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |Especifica dónde se debe realizar la búsqueda. Se requiere este elemento.  <br/> |
|[ReportTemplate](reporttemplate.md) <br/> |Especifica el tipo de informe para recuperar de seguimiento. Se requiere este elemento.  <br/> |
|[RecipientFilter](recipientfilter.md) <br/> |Especifica una dirección de destinatario para usar con el informe de seguimiento especificado. Este elemento es opcional.  <br/> |
|[MessageTrackingReportId](messagetrackingreportid.md) <br/> |Especifica una cadena de identidad que se ha obtenido de la operación de **FindMessageTrackingReport** . Se requiere este elemento.  <br/> |
|[ReturnQueueEvents](returnqueueevents.md) <br/> |Especifica que la persona que está ejecutando la tarea tiene una función que tiene privilegios. Este elemento es opcional.  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |Especifica información de rendimiento y control de tiempo que se utilizará para derivar el informe de seguimiento. Este elemento es opcional.  <br/> |
|[Propiedades (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Especifica una lista de una o varias propiedades de seguimiento. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

