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
description: El elemento GetMessageTrackingReport contiene la solicitud de la operación GetMessageTrackingReport para recuperar el informe completo de seguimiento de mensajes del identificador especificado.
ms.openlocfilehash: 30596acd209580147e0f03e12a7868502159b29c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/02/2020
ms.locfileid: "44466580"
---
# <a name="getmessagetrackingreport"></a>GetMessageTrackingReport

El elemento **GetMessageTrackingReport** contiene la solicitud de la [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md) para recuperar el informe completo de seguimiento de mensajes del identificador especificado. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Ámbito (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |Especifica dónde se va a realizar la búsqueda. Se requiere este elemento.  <br/> |
|[ReportTemplate](reporttemplate.md) <br/> |Especifica el tipo de informe de seguimiento que se va a recuperar. Se requiere este elemento.  <br/> |
|[RecipientFilter](recipientfilter.md) <br/> |Especifica la dirección del destinatario que se va a usar con el informe de seguimiento especificado. Este elemento es opcional.  <br/> |
|[MessageTrackingReportId](messagetrackingreportid.md) <br/> |Especifica una cadena de identidad obtenida de la operación **FindMessageTrackingReport** . Se requiere este elemento.  <br/> |
|[ReturnQueueEvents](returnqueueevents.md) <br/> |Especifica que la persona que ejecuta la tarea tiene un rol privilegiado. Este elemento es opcional.  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |Especifica la información de tiempo y rendimiento que se usará para derivar el informe de seguimiento. Este elemento es opcional.  <br/> |
|[Propiedades (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Especifica una lista de una o varias propiedades de seguimiento. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

