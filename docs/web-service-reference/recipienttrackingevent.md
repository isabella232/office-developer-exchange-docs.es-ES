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
description: El elemento RecipientTrackingEvent contiene información de un solo evento de un destinatario.
ms.openlocfilehash: c5488ba105f9a853a490d6f0f4ff9ff15b537e23
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836989"
---
# <a name="recipienttrackingevent"></a>RecipientTrackingEvent

El elemento **RecipientTrackingEvent** contiene información de un solo evento de un destinatario. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Fecha (MessageTracking)](date-messagetracking.md) <br/> |Se requiere este elemento.  <br/> |
|[Recipient](recipient.md) <br/> |Se requiere este elemento.  <br/> |
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

|**Element**|**Descripción**|
|:-----|:-----|
|[RecipientTrackingEvents](recipienttrackingevents.md) <br/> |Contiene una lista de uno o más eventos de seguimiento para un destinatario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

