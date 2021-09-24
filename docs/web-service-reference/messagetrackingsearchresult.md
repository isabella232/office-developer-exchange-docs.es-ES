---
title: MessageTrackingSearchResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MessageTrackingSearchResult
api_type:
- schema
ms.assetid: 8ea77aa8-b93f-4287-be36-0a9da06e0946
description: El elemento MessageTrackingSearchResult contiene un único resultado de mensaje para un elemento FindMessageTrackingReportResponse.
ms.openlocfilehash: 2bd70461b2896d0204b163365d525f76d42bb213
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523884"
---
# <a name="messagetrackingsearchresult"></a>MessageTrackingSearchResult

El **elemento MessageTrackingSearchResult** contiene un único resultado de mensaje para un [elemento FindMessageTrackingReportResponse.](findmessagetrackingreportresponse.md) 
  
```xml
<MessageTrackingSearchResult>
   <Subject/>
   <Sender/>
   <PurportedSender/>
   <Recipients/>
   <SubmittedTime/>
   <MessageTrackingReportId/>
   <PreviousHopServer/>
   <FirstHopServer/>
   <Properties/>
</MessageTrackingSearchResult>
```

 **FindMessageTrackingSearchResultType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Asunto](subject.md) <br/> |Contiene el asunto del mensaje de correo electrónico.  <br/> |
|[Sender (EmailAddressType)](sender-emailaddresstype.md) <br/> |Contiene la dirección del remitente del mensaje de correo electrónico.  <br/> |
|[PurportedSender](purportedsender.md) <br/> |Contiene información de contacto del supuesto remitente de un mensaje de correo electrónico.  <br/> |
|[Recipients (ArrayOfRecipientsType)](recipients-arrayofrecipientstype.md) <br/> |Contiene una lista de direcciones de correo electrónico que recibieron este mensaje.  <br/> |
|[SubmittedTime](submittedtime.md) <br/> |Contiene la hora en que se envió el mensaje.  <br/> |
|[MessageTrackingReportId](messagetrackingreportid.md) <br/> |Contiene un identificador interno que identifica el mensaje en la base de datos de transporte.  <br/> |
|[PreviousHopServer](previoushopserver.md) <br/> |Contiene el nombre del servidor del bosque que aceptó previamente el mensaje.  <br/> |
|[FirstHopServer](firsthopserver.md) <br/> |Contiene el nombre del servidor del bosque que aceptó por primera vez el mensaje.  <br/> |
|[Properties (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Contiene una lista de una o más propiedades de seguimiento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MessageTrackingSearchResults](messagetrackingsearchresults.md) <br/> |Contiene una lista de mensajes que coinciden con los criterios de búsqueda.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Web Services.Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindMessageTrackingReport](findmessagetrackingreport-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

