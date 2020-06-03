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
ms.openlocfilehash: 195ab229380f4386b39e5c3fd48208cf66e224f0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530947"
---
# <a name="subscriptionstatus"></a>SubscriptionStatus

El elemento **SubscriptionStatus** describe el estado de una suscripción de inserción. 
  
```xml
<SubscriptionStatus>OK or Unsubscribe</SubscriptionStatus>
```

 **SubscriptionStatusType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SendNotificationResult](sendnotificationresult.md) <br/> |Contiene la respuesta de la aplicación cliente ' a una notificación de inserción.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. A continuación se muestran los valores de texto posibles para este elemento:
  
- Aceptar
    
- Cancelar suscripción
    
## <a name="remarks"></a>Comentarios

Este elemento describe el estado de la suscripción. La aplicación cliente de suscripción de inserción devuelve el estado al equipo que ejecuta Exchange 2007 y que tiene instalado el rol de servidor acceso de clientes después de cada notificación de inserción. Si el valor **SubscriptionStatus** es igual a **unsubscribe**, el servidor de acceso de cliente dejará de enviar notificaciones y finalizará la suscripción. Si el valor de **SubscriptionStatus** es **correcto**, el servidor de acceso de cliente seguirá enviando notificaciones.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

