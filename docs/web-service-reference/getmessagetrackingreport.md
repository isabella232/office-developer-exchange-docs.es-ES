---
title: GetMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetMessageTrackingReport
api_type:
- schema
ms.assetid: b6ffa8ef-90f6-402d-afac-c3f5ee55cf49
description: El elemento GetMessageTrackingReport contiene la solicitud de la operación GetMessageTrackingReport para recuperar el informe de seguimiento de mensajes completo del identificador especificado.
ms.openlocfilehash: cdf4e2c0f17c7d723dc56f30c445bfd527f891a3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516982"
---
# <a name="getmessagetrackingreport"></a>GetMessageTrackingReport

El **elemento GetMessageTrackingReport** contiene la solicitud de la operación [GetMessageTrackingReport](getmessagetrackingreport-operation.md) para recuperar el informe de seguimiento de mensajes completo del identificador especificado. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Scope (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |Especifica dónde realizar la búsqueda. Se requiere este elemento.  <br/> |
|[ReportTemplate](reporttemplate.md) <br/> |Especifica el tipo de informe de seguimiento que se debe recuperar. Se requiere este elemento.  <br/> |
|[RecipientFilter](recipientfilter.md) <br/> |Especifica una dirección de destinatario que se usará con el informe de seguimiento especificado. Este elemento es opcional.  <br/> |
|[MessageTrackingReportId](messagetrackingreportid.md) <br/> |Especifica una cadena de identidad que se obtuvo de la **operación FindMessageTrackingReport.** Se requiere este elemento.  <br/> |
|[ReturnQueueEvents](returnqueueevents.md) <br/> |Especifica que la persona que ejecuta la tarea tiene un rol con privilegios. Este elemento es opcional.  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |Especifica la información de tiempo y rendimiento que se usará para derivar el informe de seguimiento. Este elemento es opcional.  <br/> |
|[Properties (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Especifica una lista de una o más propiedades de seguimiento. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

