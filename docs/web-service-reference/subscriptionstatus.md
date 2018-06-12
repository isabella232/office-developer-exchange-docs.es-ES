---
title: SubscriptionStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubscriptionStatus
api_type:
- schema
ms.assetid: 2d64ebb7-f26a-4d02-b7ef-d9d7da75f0c3
description: El elemento SubscriptionStatus describe el estado de una suscripción de inserción.
ms.openlocfilehash: 1f6de15f7a3b07714899aef2ff74a8d556f8ca1d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840595"
---
# <a name="subscriptionstatus"></a>SubscriptionStatus

El elemento **SubscriptionStatus** describe el estado de una suscripción de inserción. 
  
```xml
<SubscriptionStatus>OK or Unsubscribe</SubscriptionStatus>
```

 **SubscriptionStatusType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[SendNotificationResult](sendnotificationresult.md) <br/> |Contiene la respuesta de la aplicación cliente ' a una notificación de inserción.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Los siguientes son los posibles valores de texto para este elemento:
  
- Aceptar
    
- Cancelar suscripción
    
## <a name="remarks"></a>Notas

Este elemento describe el estado de la suscripción. La aplicación de cliente de suscripción de inserción envía el estado al equipo que ejecuta Exchange 2007 que tiene el rol de servidor de acceso de cliente instalado después de cada notificación de inserción. Si el valor de **SubscriptionStatus** es igual a **Cancelar la suscripción**, el servidor de acceso de cliente detendrá enviar notificaciones y finalizar la suscripción. Si el valor de **SubscriptionStatus** es igual a **Aceptar**, el servidor de acceso de cliente continuará enviar notificaciones.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

