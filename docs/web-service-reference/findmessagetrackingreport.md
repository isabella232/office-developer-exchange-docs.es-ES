---
title: FindMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FindMessageTrackingReport
api_type:
- schema
ms.assetid: 7ca6e2f7-aae1-4920-b839-73513ba8d4d8
description: El elemento FindMessageTrackingReport especifica criterios para los tipos de mensajes que se deben buscar.
ms.openlocfilehash: ec2ab16c6649d85edd86b9438e00ea7cfb9841ef
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513692"
---
# <a name="findmessagetrackingreport"></a>FindMessageTrackingReport

El **elemento FindMessageTrackingReport** especifica criterios para los tipos de mensajes que se deben buscar. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Scope (NonEmptyStringType)](scope-nonemptystringtype.md) <br/> |Representa lo extenso que debe ser el informe de seguimiento de mensajes.  <br/> |
|[Domain (Message Tracking)](domain-message-tracking.md) <br/> |Contiene el nombre del dominio donde se ejecuta el seguimiento de mensajes.  <br/> |
|[Sender (EmailAddressType)](sender-emailaddresstype.md) <br/> |Contiene información de contacto del remitente del mensaje de correo electrónico.  <br/> |
|[PurportedSender](purportedsender.md) <br/> |Contiene información de contacto del supuesto remitente de un mensaje de correo electrónico.  <br/> |
|[Destinatario](recipient.md) <br/> |Contiene la dirección de correo electrónico del destinatario del mensaje.  <br/> |
|[Asunto](subject.md) <br/> |Contiene el asunto del mensaje de correo electrónico.  <br/> |
|[StartDateTime](startdatetime.md) <br/> |Contiene la fecha y hora de inicio de la búsqueda.  <br/> |
|[EndDateTime](enddatetime.md) <br/> |Contiene la fecha y hora de finalización de la búsqueda.  <br/> |
|[MessageId](messageid.md) <br/> |Contiene el identificador de mensaje de la búsqueda.  <br/> |
|[FederatedDeliveryMailbox](federateddeliverymailbox.md) <br/> |Contiene el nombre del buzón donde se envió el mensaje entre locales.  <br/> |
|[DiagnosticsLevel](diagnosticslevel.md) <br/> |Representa el nivel de detalle de los informes de diagnóstico.  <br/> |
|[ServerHint](serverhint.md) <br/> |Representa el punto de partida para realizar un seguimiento de un mensaje en un sitio o bosque remoto.  <br/> |
|[Properties (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Contiene una lista de una o más propiedades de seguimiento. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

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



[Operación FindMessageTrackingReport](findmessagetrackingreport-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

