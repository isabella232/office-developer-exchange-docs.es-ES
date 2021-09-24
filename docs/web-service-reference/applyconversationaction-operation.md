---
title: Operación ApplyConversationAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ApplyConversationAction
api_type:
- schema
ms.assetid: 73d7943d-d361-4f8b-9948-d85f886efa1a
description: La operación ApplyConversationAction establece una acción única o de seguimiento en todos los elementos de una conversación. La operación ApplyConversationAction permite clasificar, mover, copiar, eliminar y establecer el estado de lectura en todos los elementos de una conversación. También se pueden establecer acciones para nuevos mensajes en una conversación.
ms.openlocfilehash: ed3ed02dc045a095bcc86124b8d3e1c5a65dae84
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520104"
---
# <a name="applyconversationaction-operation"></a>Operación ApplyConversationAction

La **operación ApplyConversationAction** establece una acción única o de seguimiento en todos los elementos de una conversación. La **operación ApplyConversationAction** permite clasificar, mover, copiar, eliminar y establecer el estado de lectura en todos los elementos de una conversación. También se pueden establecer acciones para nuevos mensajes en una conversación. 
  
## <a name="applyconversationaction-request-example"></a>Ejemplo de solicitud ApplyConversationAction

### <a name="description"></a>Description

En el siguiente ejemplo de una **solicitud ApplyConversationAction** se muestra cómo mover los elementos de la conversación especificada a otra carpeta. Los elementos que se agregan a la conversación también se mueven a la carpeta especificada. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

Los identificadores de conversación y carpeta se han acortado para conservar la legibilidad.
  
## <a name="applyconversationaction-response-example"></a>Ejemplo de respuesta ApplyConversationAction

### <a name="description"></a>Description

En el ejemplo siguiente se muestra una respuesta correcta a una **solicitud ApplyConversationAction.** 
  
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
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ApplyConversationActionResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ApplyConversationActionResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:ApplyConversationActionResponseMessage>
      </m:ResponseMessages>
    </m:ApplyConversationActionResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>Ver también

- [Operación ApplyConversationAction](applyconversationaction-operation.md)
- [Operaciones ews en Exchange](ews-operations-in-exchange.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)
- [Conversaciones en EWS](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

