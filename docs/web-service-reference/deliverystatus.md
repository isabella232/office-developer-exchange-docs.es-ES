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
ms.openlocfilehash: ae32202284d3dd272f693fbb7b76070cb6019d28
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461404"
---
# <a name="deliverystatus"></a>DeliveryStatus

El elemento **DeliveryStatus** especifica el estado de un mensaje. 
  
```XML
<DeliveryStatus>Unsuccessful | Pending | Delivered | Transferred | Read</DeliveryStatus>
```

 **MessageTrackingDeliveryStatusType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |Contiene información de un evento único para un destinatario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumeran los valores de texto posibles para el elemento **DeliveryStatus** . 
  
**Valores del elemento DeliveryStatus**

|**Valor**|**Descripción**|
|:-----|:-----|
|Correctamente  <br/> |Especifica que no se entregó un mensaje.  <br/> |
|Pending  <br/> |Especifica que el mensaje está esperando su aprobación de un moderador.  <br/> |
|Pronuncia  <br/> |Especifica que el mensaje se entregó a todos los destinatarios especificados.  <br/> |
|Transferido  <br/> |Especifica que el mensaje se transfirió a un servidor fuera del ámbito de búsqueda.  <br/> |
|Read  <br/> |Especifica que el mensaje fue entregado y leído por los destinatarios.  <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento **DeliveryStatus** era de tipo **MessageTrackingDeliveryStatusType** en Exchange Server 2010. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

