---
title: RecipientTrackingEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RecipientTrackingEvent
api_type:
- schema
ms.assetid: 2bffdac7-c2f5-4805-ae7e-bd865301acb6
description: El elemento RecipientTrackingEvent contiene información para un único evento para un destinatario.
ms.openlocfilehash: 30d9cd4ca075fda9607b191f576cac1b7a529988
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525766"
---
# <a name="recipienttrackingevent"></a>RecipientTrackingEvent

El **elemento RecipientTrackingEvent** contiene información para un único evento para un destinatario. 
  
```XML
<RecipientTrackingEvent>
   <Date/>
   <Recipient/>
   <DeliveryStatus/>
   <EventDescription/>
   <EventData/>
   <Server/>
   <InternalId/>
   <BccRecipient/>
   <HiddenRecipient/>
   <UniquePathId/>
   <RootAddress/>
   <Properties/>
</RecipientTrackingEvent>
```

 **RecipientTrackingEventType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Date (MessageTracking)](date-messagetracking.md) <br/> |Se requiere este elemento.  <br/> |
|[Destinatario](recipient.md) <br/> |Se requiere este elemento.  <br/> |
|[DeliveryStatus](deliverystatus.md) <br/> |Se requiere este elemento.  <br/> |
|[EventDescription](eventdescription.md) <br/> |Se requiere este elemento.  <br/> |
|[EventData](eventdata.md) <br/> |Este elemento es opcional.  <br/> |
|[Server (MessageTracking)](server-messagetracking.md) <br/> |Se requiere este elemento.  <br/> |
|[InternalId](internalid.md) <br/> |Se requiere este elemento.  <br/> |
|[BccRecipient](bccrecipient.md) <br/> |Este elemento es opcional.  <br/> |
|[HiddenRecipient](hiddenrecipient.md) <br/> |Este elemento es opcional.  <br/> |
|[UniquePathId](uniquepathid.md) <br/> |Este elemento es opcional.  <br/> |
|[RootAddress](rootaddress.md) <br/> |Este elemento es opcional.  <br/> |
|[Properties (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RecipientTrackingEvents](recipienttrackingevents.md) <br/> |Contiene una lista de uno o varios eventos de seguimiento para un destinatario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

