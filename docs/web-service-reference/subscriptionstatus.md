---
title: SubscriptionStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SubscriptionStatus
api_type:
- schema
ms.assetid: 2d64ebb7-f26a-4d02-b7ef-d9d7da75f0c3
description: El elemento SubscriptionStatus describe el estado de una suscripción de inserción.
ms.openlocfilehash: 6918a4965da2c075341c99581c3bd06c93da35fa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546934"
---
# <a name="subscriptionstatus"></a>SubscriptionStatus

El **elemento SubscriptionStatus** describe el estado de una suscripción de inserción. 
  
```xml
<SubscriptionStatus>OK or Unsubscribe</SubscriptionStatus>
```

 **SubscriptionStatusType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SendNotificationResult](sendnotificationresult.md) <br/> |Contiene la respuesta de la aplicación cliente' a una notificación de inserción.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Los siguientes son los valores de texto posibles para este elemento:
  
- Aceptar
    
- Unsubscribe
    
## <a name="remarks"></a>Comentarios

Este elemento describe el estado de la suscripción. La aplicación cliente de suscripción de inserción devuelve el estado al equipo que ejecuta Exchange 2007 que tiene instalada la función de servidor Acceso de cliente después de cada notificación de inserción. Si el **valor SubscriptionStatus** es igual a **Unsubscribe,** el servidor de acceso de cliente dejará de enviar notificaciones y finalizará la suscripción. Si el **valor SubscriptionStatus** es igual a **Aceptar,** el servidor de acceso de cliente seguirá mandando notificaciones.
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

