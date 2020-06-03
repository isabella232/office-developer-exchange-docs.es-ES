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
description: El elemento FindMessageTrackingReport especifica criterios para los tipos de mensajes que se van a buscar.
ms.openlocfilehash: d30e5391bb4305cae0004a9788df971a57297cae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462939"
---
# <a name="findmessagetrackingreport"></a>FindMessageTrackingReport

El elemento **FindMessageTrackingReport** especifica criterios para los tipos de mensajes que se van a buscar. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Ámbito (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |Representa la extensión que debe tener el informe de seguimiento de mensajes.  <br/> |
|[Dominio (seguimiento de mensajes)](domain-message-tracking.md) <br/> |Contiene el nombre del dominio donde se ejecuta el seguimiento de mensajes.  <br/> |
|[Remitente (EmailAddressType)](sender-emailaddresstype.md) <br/> |Contiene la información de contacto del remitente del mensaje de correo electrónico.  <br/> |
|[PurportedSender](purportedsender.md) <br/> |Contiene la información de contacto del remitente de un mensaje de correo electrónico.  <br/> |
|[Destinatario](recipient.md) <br/> |Contiene la dirección de correo electrónico del destinatario del mensaje.  <br/> |
|[Asunto](subject.md) <br/> |Contiene el asunto del mensaje de correo electrónico.  <br/> |
|[StartDateTime](startdatetime.md) <br/> |Contiene la fecha y hora de inicio de la búsqueda.  <br/> |
|[EndDateTime](enddatetime.md) <br/> |Contiene la fecha y hora de finalización de la búsqueda.  <br/> |
|[MessageId](messageid.md) <br/> |Contiene el identificador de mensaje para la búsqueda.  <br/> |
|[FederatedDeliveryMailbox](federateddeliverymailbox.md) <br/> |Contiene el nombre del buzón en el que se envió el mensaje entre locales.  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |Representa el nivel de detalle de los informes de diagnóstico.  <br/> |
|[ServerHint](serverhint.md) <br/> |Representa el punto de inicio para el seguimiento de un mensaje en un sitio o bosque remoto.  <br/> |
|[Propiedades (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Contiene una lista de una o varias propiedades de seguimiento. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguna.
  
## <a name="text-value"></a>Valor de texto

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



[Operación FindMessageTrackingReport](findmessagetrackingreport-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

