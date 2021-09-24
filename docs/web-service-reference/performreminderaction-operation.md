---
title: Operación PerformReminderAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c597bb0e-13b0-422e-9c23-970463e2a5c3
description: Busque información sobre la operación EWS PerformReminderAction.
ms.openlocfilehash: ca547c401100afdfd9d846ca3bfddf710efd2797
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515309"
---
# <a name="performreminderaction-operation"></a>Operación PerformReminderAction

Busque información sobre la **operación EWS PerformReminderAction.** 
  
La **operación PerformReminderAction** Exchange Web Services (EWS) inicia una acción de descarte o de snooze en un aviso. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-performreminderaction-operation"></a>Uso de la operación PerformReminderAction

Puede usar la **operación PerformReminderAction** para descartar o snooze (retraso) los avisos devueltos por la [operación GetReminders.](getreminders-operation.md) Para snooze un aviso, establezca [ActionType](actiontype-reminderactiontype.md) en **Snooze** y establezca el valor [NewReminderTime](newremindertime.md) en un momento posterior al [reminderTime](remindertime.md)actual , de lo contrario el servidor omite **el valor NewReminderTime.** Si el aviso es para una repetición de una reunión periódica y la acción **Snooze** se toma en el aviso con un **NewReminderTime** que ha pasado el aviso de la siguiente repetición, el aviso se descarta de forma eficaz. 
  
Para descartar un aviso, establezca **ActionType** en **Descartar**. Cuando el servidor procesa la solicitud, el servidor cambia el valor [IsReminderSet](isreminderset.md) para el elemento de **True** a **False**.
  
### <a name="performreminderaction-operation-soap-headers"></a>Encabezados SOAP de la operación PerformReminderAction

La **operación PerformReminderAction** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Nombre de encabezado**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario al que la aplicación cliente está suplantando. Este encabezado es aplicable a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, tal como se define en RFC 3066, "Etiquetas para la identificación de idiomas", que se usará para tener acceso al buzón. Este encabezado es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="performreminderaction-operation-request-example"></a>Ejemplo de solicitud de operación PerformReminderAction

En el siguiente ejemplo de una solicitud de operación **PerformReminderAction** se muestra cómo snooze un aviso actual y establecer una nueva hora de aviso. Tenga en cuenta que debe incluir **changekey** para [ItemId](itemid.md) y **NewReminderTime** debe establecerse en una hora posterior a la **remindertime** devuelta por la operación [GetReminders.](getreminders-operation.md) 
  
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
> El **valor ItemId** se ha acortado para conservar la legibilidad. 
  
El cuerpo SOAP de la solicitud contiene los siguientes elementos:
  
- [PerformReminderAction](performreminderaction.md)
    
- [ReminderItemActions](reminderitemactions.md)
    
- [ReminderItemAction](reminderitemaction.md)
    
- [ActionType](actiontype-reminderactiontype.md)
    
- [ItemId](itemid.md)
    
- [NewReminderTime](newremindertime.md)
    
## <a name="successful-performreminderaction-operation-response"></a>Respuesta de operación PerformReminderAction correcta

En el ejemplo siguiente se muestra una respuesta correcta a una **solicitud de operación PerformReminderAction.** El **elemento UpdatedItemIds** contiene **los ItemIds** del elemento de calendario actualizado. 
  
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

El cuerpo SOAP de la respuesta contiene los siguientes elementos:
  
- [PerformReminderActionResponse](performreminderactionresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [UpdatedItemIds](updateditemids.md)
    
- [ItemId](itemid.md)
    
## <a name="performreminderaction-operation-error-response-example"></a>Ejemplo de respuesta de error de operación PerformReminderAction

En el ejemplo siguiente se muestra una respuesta a una solicitud de operación **PerformReminderAction** cuando no se realizó ningún cambio en el servidor. Se trata de una respuesta en la que se envió una solicitud, pero no se devolvió **UpdatedItemIds,** lo que significa que no se cambiaron los avisos. 
  
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

El cuerpo SOAP de la respuesta de error contiene los siguientes elementos:
  
- [PerformReminderActionResponse](performreminderactionresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [UpdatedItemIds](updateditemids.md)
    
Para obtener códigos de error adicionales genéricos para EWS, vea [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Ver también


- [Operación GetReminders](getreminders-operation.md)
    

