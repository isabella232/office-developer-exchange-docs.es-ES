---
title: Operación PerformReminderAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c597bb0e-13b0-422e-9c23-970463e2a5c3
description: Busque información sobre la EWS PerformReminderAction operación.
ms.openlocfilehash: 778fbb508413721f58cfcf9143a5296874e6cd1c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836722"
---
# <a name="performreminderaction-operation"></a>Operación PerformReminderAction

Obtenga información acerca de la operación de EWS **PerformReminderAction** . 
  
La operación de Exchange Web Services (EWS) **PerformReminderAction** inicia una acción descartar o posponer en un aviso. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-performreminderaction-operation"></a>Mediante la operación PerformReminderAction

Puede usar la operación **PerformReminderAction** para descartar o posponer avisos (retraso) devueltos por la operación [GetReminders](getreminders-operation.md) . Para posponer un aviso, establezca el [ActionType](actiontype-reminderactiontype.md) para **Posponer**y establezca el valor de [NewReminderTime](newremindertime.md) en un momento posterior a la actual [ReminderTime](remindertime.md), en caso contrario, el **NewReminderTime** se omite el servidor. Si el aviso es para una aparición de una reunión periódica, y se realiza la acción **Posponer** en el aviso con un **NewReminderTime** que está más allá del aviso de la siguiente aparición, eficazmente se omite el aviso. 
  
Para descartar un aviso, establezca el **ActionType** en **Descartar**. Cuando el servidor procesa la solicitud, el servidor cambia el valor de [IsReminderSet](isreminderset.md) para el elemento de **True** a **False**.
  
### <a name="performreminderaction-operation-soap-headers"></a>Encabezados SOAP de operación de PerformReminderAction

La operación de **PerformReminderAction** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla. 
  
|**Nombre de encabezado**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario que está realizando la suplantación de la aplicación cliente. Este encabezado es aplicable a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón. Este encabezado es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="performreminderaction-operation-request-example"></a>Ejemplo de solicitud de operación de PerformReminderAction

El siguiente ejemplo de una solicitud de operación **PerformReminderAction** muestra cómo aplazar un aviso actual y establecer una hora de aviso de nuevo. Tenga en cuenta que debe incluir el **ChangeKey** para el [ItemId](itemid.md) y la **NewReminderTime** se debe establecer en una hora posterior a la **ReminderTime** devuelto por la operación [GetReminders](getreminders-operation.md) . 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:PerformReminderAction>
      <m:ReminderItemActions>
        <t:ReminderItemAction>
          <t:ActionType>Snooze</t:ActionType>
          <t:ItemId Id="vwAAAA=="
           ChangeKey="DwAAABQAAACOs0HEMq1WTKpI7sNu5qXNAAAUDA=="/>
          <t:NewReminderTime>2014-04-16T17:00:00Z</t:NewReminderTime>
        </t:ReminderItemAction>
      </m:ReminderItemActions>
    </m:PerformReminderAction>
  </soap:Body>
</soap:Envelope>
```

> [!NOTE]
> Se ha reducido el valor **ItemId** para conservar la legibilidad. 
  
La solicitud SOAP body contiene los siguientes elementos:
  
- [PerformReminderAction](performreminderaction.md)
    
- [ReminderItemActions](reminderitemactions.md)
    
- [ReminderItemAction](reminderitemaction.md)
    
- [ActionType](actiontype-reminderactiontype.md)
    
- [ItemId](itemid.md)
    
- [NewReminderTime](newremindertime.md)
    
## <a name="successful-performreminderaction-operation-response"></a>Respuesta es correcta de operación PerformReminderAction

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **PerformReminderAction** . El elemento **UpdatedItemIds** contiene el **ItemID** del elemento de calendario actualizados. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="921"
                       MinorBuildNumber="20"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds>
        <ItemId Id="vwAAAA=="
                ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAAJKP+S"/>
      </UpdatedItemIds>
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

La respuesta SOAP body contiene los siguientes elementos:
  
- [PerformReminderActionResponse](performreminderactionresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [UpdatedItemIds](updateditemids.md)
    
- [ItemId](itemid.md)
    
## <a name="performreminderaction-operation-error-response-example"></a>Ejemplo de respuesta de error de operación de PerformReminderAction

En el ejemplo siguiente se muestra una respuesta a una solicitud de operación **PerformReminderAction** cuando se realizó ningún cambio en el servidor. Esta es una respuesta en el que se envió una solicitud, pero se han devuelto no **UpdatedItemIds** , lo que significa que no hay avisos se han cambiado. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds />
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

La respuesta de error SOAP body contiene los siguientes elementos:
  
- [PerformReminderActionResponse](performreminderactionresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [UpdatedItemIds](updateditemids.md)
    
Para códigos de error adicionales que son genéricos de EWS, consulte [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Vea también


- [Operación GetReminders](getreminders-operation.md)
    

