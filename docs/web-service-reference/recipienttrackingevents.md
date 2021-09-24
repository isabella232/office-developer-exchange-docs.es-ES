---
title: RecipientTrackingEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RecipientTrackingEvents
api_type:
- schema
ms.assetid: c4f729aa-674e-43b2-97f2-bf49740b0a34
description: El elemento RecipientTrackingEvents representa una colección de uno o más eventos para un mensaje.
ms.openlocfilehash: 47a327e7715a46d8d40621310a5fb1a338dbcce8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525641"
---
# <a name="recipienttrackingevents"></a>RecipientTrackingEvents

El **elemento RecipientTrackingEvents** representa una colección de uno o más eventos para un mensaje. 
  
```XML
<RecipientTrackingEvents>
   <RecipientTrackingEvent/>
</RecipientTrackingEvents>
```

 **ArrayOfRecipientTrackingEventType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |Contiene detalles de un evento específico en el informe de seguimiento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MessageTrackingReport](messagetrackingreport.md) <br/> |Contiene un único mensaje que se devuelve en una [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md).  <br/> |
   
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

