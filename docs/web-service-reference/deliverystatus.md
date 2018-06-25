---
title: DeliveryStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeliveryStatus
api_type:
- schema
ms.assetid: eab55db3-affb-42be-a586-5caa04052433
description: El elemento DeliveryStatus especifica el estado de un mensaje.
ms.openlocfilehash: 4e6f31e8ef4f98d8e838ba91167c7dd5d6ab2590
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764122"
---
# <a name="deliverystatus"></a>DeliveryStatus

El elemento **DeliveryStatus** especifica el estado de un mensaje. 
  
```XML
<DeliveryStatus>Unsuccessful | Pending | Delivered | Transferred | Read</DeliveryStatus>
```

 **MessageTrackingDeliveryStatusType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |Contiene información de un solo evento de un destinatario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumera los posibles valores de texto para el elemento **DeliveryStatus** . 
  
**Valores de elemento DeliveryStatus**

|**Valor**|**Descripción**|
|:-----|:-----|
|Realizado correctamente  <br/> |Especifica que un mensaje no se entregó.  <br/> |
|Pendiente  <br/> |Especifica que el mensaje está esperando la aprobación de un moderador.  <br/> |
|Entregado  <br/> |Especifica que el mensaje se entregó a todos los destinatarios especificados.  <br/> |
|Transfiere  <br/> |Especifica que el mensaje se ha transferido a un servidor fuera del ámbito de búsqueda.  <br/> |
|Leído  <br/> |Especifica que el mensaje se entrega y leer los destinatarios.  <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento **DeliveryStatus** era de tipo **MessageTrackingDeliveryStatusType** en Exchange Server 2010. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

