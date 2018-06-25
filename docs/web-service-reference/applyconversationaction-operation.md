---
title: Operación ApplyConversationAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ApplyConversationAction
api_type:
- schema
ms.assetid: 73d7943d-d361-4f8b-9948-d85f886efa1a
description: La operación ApplyConversationAction establece una sola vez o realizar un seguimiento de la acción de todos los elementos en una conversación. La operación de ApplyConversationAction permite clasificar, mover, copiar, eliminar y establecer el estado de lectura en todos los elementos en una conversación. También se pueden establecer acciones para mensajes nuevos en una conversación.
ms.openlocfilehash: 2a485b84ee87aec2ed807e3f4f0901b83432fa0a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763482"
---
# <a name="applyconversationaction-operation"></a>Operación ApplyConversationAction

La operación **ApplyConversationAction** establece una sola vez o realizar un seguimiento de la acción de todos los elementos en una conversación. La operación de **ApplyConversationAction** permite clasificar, mover, copiar, eliminar y establecer el estado de lectura en todos los elementos en una conversación. También se pueden establecer acciones para mensajes nuevos en una conversación. 
  
## <a name="applyconversationaction-request-example"></a>Ejemplo de solicitud de ApplyConversationAction

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de **ApplyConversationAction** muestra cómo mover los elementos de la conversación especificada a otra carpeta. Los elementos que se agregan a la conversación también se moverán a la carpeta especificada. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:ApplyConversationAction>
      <m:ConversationActions>
        <t:ConversationAction>
          <t:Action>AlwaysMove</t:Action>
          <t:ConversationId Id="AAQkADVkNjM1EH39AWcDUGrnrnJ32hHpdc="/>
          <t:DestinationFolderId>
            <t:FolderId Id="AAMkADVkNjM1ODI3LTEwYTAtNDUBTTT6tWal35iSoKAAAABZZWAAA="/>
          </t:DestinationFolderId>
        </t:ConversationAction>
      </m:ConversationActions>
    </m:ApplyConversationAction>
  </soap:Body>
</soap:Envelope>
```

### <a name="remarks"></a>Comentarios

Los identificadores de conversación y carpeta se han abreviado para conservar la legibilidad.
  
## <a name="applyconversationaction-response-example"></a>Ejemplo de respuesta ApplyConversationAction

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta a una solicitud **ApplyConversationAction** correcta. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="91" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ApplyConversationActionResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ApplyConversationActionResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:ApplyConversationActionResponseMessage>
      </m:ResponseMessages>
    </m:ApplyConversationActionResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>Vea también

- [Operación ApplyConversationAction](applyconversationaction-operation.md)
- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)
- [Conversaciones de EWS](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

