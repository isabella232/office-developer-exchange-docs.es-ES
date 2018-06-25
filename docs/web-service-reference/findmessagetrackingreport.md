---
title: FindMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindMessageTrackingReport
api_type:
- schema
ms.assetid: 7ca6e2f7-aae1-4920-b839-73513ba8d4d8
description: El elemento FindMessageTrackingReport especifica los criterios para los tipos de mensajes para buscar.
ms.openlocfilehash: 77545121aa056992248c045af3f3d36566678b94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764642"
---
# <a name="findmessagetrackingreport"></a>FindMessageTrackingReport

El elemento **FindMessageTrackingReport** especifica los criterios para los tipos de mensajes para buscar. 
  
```xml
<FindMessageTrackingReport>
   <Scope/>
   <Domain/>
   <Sender/>
   <PurportedSender/>
   <Recipient/>
   <Subject/>
   <StartDateTime/>
   <EndDateTime/>
   <MessageId/>
   <FederatedDeliveryMailbox/>
   <DiagnosticsLevel/>
   <ServerHint/>
   <Properties/>
</FindMessageTrackingReport>
```

 **FindMessageTrackingReportRequestType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Ámbito (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |Representa la extensión deben ser el informe de seguimiento de mensajes.  <br/> |
|[Dominio (el seguimiento de mensajes)](domain-message-tracking.md) <br/> |Contiene el nombre del dominio donde se ejecutan el seguimiento de mensajes.  <br/> |
|[Remitente (EmailAddressType)](sender-emailaddresstype.md) <br/> |Contiene información de contacto para el remitente del mensaje de correo electrónico.  <br/> |
|[PurportedSender](purportedsender.md) <br/> |Contiene información de contacto para el remitente presunta de un mensaje de correo electrónico.  <br/> |
|[Recipient](recipient.md) <br/> |Contiene la dirección de correo electrónico para el destinatario del mensaje.  <br/> |
|[Subject](subject.md) <br/> |Contiene al asunto del mensaje de correo electrónico.  <br/> |
|[StartDateTime](startdatetime.md) <br/> |Contiene la fecha y la hora para la búsqueda inicial.  <br/> |
|[EndDateTime](enddatetime.md) <br/> |Contiene la fecha final y la hora para la búsqueda.  <br/> |
|[MessageId](messageid.md) <br/> |Contiene el identificador de mensaje para la búsqueda.  <br/> |
|[FederatedDeliveryMailbox](federateddeliverymailbox.md) <br/> |Contiene el nombre del buzón donde se envió el mensaje entre locales.  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |Representa el nivel de detalle de los informes de diagnóstico.  <br/> |
|[ServerHint](serverhint.md) <br/> |Representa el punto de partida para el seguimiento de un mensaje en un sitio remoto o un bosque.  <br/> |
|[Propiedades (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Contiene una lista de una o varias propiedades de seguimiento. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación FindMessageTrackingReport](findmessagetrackingreport-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

