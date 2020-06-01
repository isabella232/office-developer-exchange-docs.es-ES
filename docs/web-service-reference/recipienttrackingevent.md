---
title: RecipientTrackingEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientTrackingEvent
api_type:
- schema
ms.assetid: 2bffdac7-c2f5-4805-ae7e-bd865301acb6
description: El elemento RecipientTrackingEvent contiene información de un evento único para un destinatario.
ms.openlocfilehash: e9a014cdfac122f112205cfa5032535a770f9d82
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465488"
---
# <a name="recipienttrackingevent"></a>RecipientTrackingEvent

El elemento **RecipientTrackingEvent** contiene información de un evento único para un destinatario. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Fecha (MessageTracking)](date-messagetracking.md) <br/> |Se requiere este elemento.  <br/> |
|[Destinatario](recipient.md) <br/> |Se requiere este elemento.  <br/> |
|[DeliveryStatus](deliverystatus.md) <br/> |Se requiere este elemento.  <br/> |
|[EventDescription](eventdescription.md) <br/> |Se requiere este elemento.  <br/> |
|[EventData](eventdata.md) <br/> |Este elemento es opcional.  <br/> |
|[Servidor (MessageTracking)](server-messagetracking.md) <br/> |Se requiere este elemento.  <br/> |
|[InternalId](internalid.md) <br/> |Se requiere este elemento.  <br/> |
|[BccRecipient](bccrecipient.md) <br/> |Este elemento es opcional.  <br/> |
|[HiddenRecipient](hiddenrecipient.md) <br/> |Este elemento es opcional.  <br/> |
|[UniquePathId](uniquepathid.md) <br/> |Este elemento es opcional.  <br/> |
|[RootAddress](rootaddress.md) <br/> |Este elemento es opcional.  <br/> |
|[Propiedades (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RecipientTrackingEvents](recipienttrackingevents.md) <br/> |Contiene una lista de uno o más eventos de seguimiento de un destinatario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

