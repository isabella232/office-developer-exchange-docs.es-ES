---
title: Operación PerformReminderAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c597bb0e-13b0-422e-9c23-970463e2a5c3
description: Buscar información sobre la operación de EWS de PerformReminderAction.
ms.openlocfilehash: 4c069d541e9a42167c447a50c405399958d3608d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462293"
---
# <a name="performreminderaction-operation"></a>Operación PerformReminderAction

Buscar información sobre la operación de EWS de **PerformReminderAction** . 
  
La operación de los servicios web Exchange (EWS) de **PerformReminderAction** inicia una acción de descartar o posponer en un aviso. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-performreminderaction-operation"></a>Uso de la operación PerformReminderAction

Puede usar la operación **PerformReminderAction** para descartar o posponer (retrasar) los avisos devueltos por la operación [GetReminders](getreminders-operation.md) . Para posponer un aviso, establezca [ActionType](actiontype-reminderactiontype.md) en **SNOOZE**y establezca el valor de [NewReminderTime](newremindertime.md) en una hora posterior a la [ReminderTime](remindertime.md)actual, de lo contrario el servidor omite el **NewReminderTime** . Si el aviso es para una ocurrencia de una reunión periódica y se lleva a cabo la acción de **posponer** en el aviso con un **NewReminderTime** que supera el aviso de la siguiente repetición, el aviso se descarta de manera efectiva. 
  
Para descartar un aviso, establezca **ActionType** en **Dismiss**. Cuando el servidor procesa la solicitud, el servidor cambia el valor [IsReminderSet](isreminderset.md) para el elemento de **true** a **false**.
  
### <a name="performreminderaction-operation-soap-headers"></a>Encabezados SOAP de operación PerformReminderAction

La operación **PerformReminderAction** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Nombre de encabezado**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica al usuario que está suplantando la aplicación cliente. Este encabezado se aplica a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón. Este encabezado se aplica a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Este encabezado se aplica a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Este encabezado se aplica a una respuesta.  <br/> |
   
## <a name="performreminderaction-operation-request-example"></a>Ejemplo de solicitud de operación PerformReminderAction

El siguiente ejemplo de una solicitud de operación de **PerformReminderAction** muestra cómo posponer un aviso actual y establecer una nueva hora de aviso. Tenga en cuenta que debe incluir **changekey** para [Itemid](itemid.md) y **NewReminderTime** debe estar establecido en una hora posterior a la **ReminderTime** devuelta por la operación [GetReminders](getreminders-operation.md) . 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
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
> El valor de **Itemid** se ha abreviado para preservar la legibilidad. 
  
El cuerpo SOAP de la solicitud contiene los siguientes elementos:
  
- [PerformReminderAction](performreminderaction.md)
    
- [ReminderItemActions](reminderitemactions.md)
    
- [ReminderItemAction](reminderitemaction.md)
    
- [ActionType](actiontype-reminderactiontype.md)
    
- [ItemId](itemid.md)
    
- [NewReminderTime](newremindertime.md)
    
## <a name="successful-performreminderaction-operation-response"></a>Respuesta de operación PerformReminderAction correcta

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **PerformReminderAction** . El elemento **UpdatedItemIds** contiene la **ItemIds** del elemento de calendario actualizado. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="921"
                       MinorBuildNumber="20"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds>
        <ItemId Id="vwAAAA=="
                ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAAJKP+S"/>
      </UpdatedItemIds>
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

El cuerpo SOAP de respuesta contiene los siguientes elementos:
  
- [PerformReminderActionResponse](performreminderactionresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [UpdatedItemIds](updateditemids.md)
    
- [ItemId](itemid.md)
    
## <a name="performreminderaction-operation-error-response-example"></a>Ejemplo de respuesta de error de operación PerformReminderAction

En el ejemplo siguiente se muestra una respuesta a una solicitud de operación de **PerformReminderAction** cuando no se ha realizado ningún cambio en el servidor. Se trata de una respuesta en la que se ha enviado una solicitud, pero no se ha devuelto ningún **UpdatedItemIds** , lo que significa que no se ha cambiado ningún aviso. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds />
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

El cuerpo SOAP de respuesta de error contiene los siguientes elementos:
  
- [PerformReminderActionResponse](performreminderactionresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [UpdatedItemIds](updateditemids.md)
    
Para obtener los códigos de error adicionales que son genéricos para EWS, consulte [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Vea también


- [Operación GetReminders](getreminders-operation.md)
    

