---
title: DeliveryStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeliveryStatus
api_type:
- schema
ms.assetid: eab55db3-affb-42be-a586-5caa04052433
description: El elemento DeliveryStatus especifica el estado de un mensaje.
ms.openlocfilehash: f11952f401e0d22d780725598bfb32cbd3a8d622
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543390"
---
# <a name="deliverystatus"></a>DeliveryStatus

El **elemento DeliveryStatus** especifica el estado de un mensaje. 
  
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
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |Contiene información para un único evento para un destinatario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la tabla siguiente se enumeran los posibles valores de texto para el **elemento DeliveryStatus.** 
  
**Valores del elemento DeliveryStatus**

|**Valor**|**Descripción**|
|:-----|:-----|
|Fallido  <br/> |Especifica que no se entregó un mensaje.  <br/> |
|Pendiente  <br/> |Especifica que el mensaje está esperando la aprobación de un moderador.  <br/> |
|Entregado  <br/> |Especifica que el mensaje se entregó a todos los destinatarios especificados.  <br/> |
|Transfer  <br/> |Especifica que el mensaje se transfirió a un servidor fuera del ámbito de búsqueda.  <br/> |
|Read  <br/> |Especifica que los destinatarios entregaron y leyeron el mensaje.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **elemento DeliveryStatus** era del tipo **MessageTrackingDeliveryStatusType** en Exchange Server 2010. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

