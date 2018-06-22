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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763482"
---
# <a name="applyconversationaction-operation"></a><span data-ttu-id="c9fdf-105">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="c9fdf-105">ApplyConversationAction operation</span></span>

<span data-ttu-id="c9fdf-106">La operación **ApplyConversationAction** establece una sola vez o realizar un seguimiento de la acción de todos los elementos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="c9fdf-106">The **ApplyConversationAction** operation sets a one-time or follow up action on all the items in a conversation.</span></span> <span data-ttu-id="c9fdf-107">La operación de **ApplyConversationAction** permite clasificar, mover, copiar, eliminar y establecer el estado de lectura en todos los elementos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="c9fdf-107">The **ApplyConversationAction** operation allows you to categorize, move, copy, delete, and set the read state on all items in a conversation.</span></span> <span data-ttu-id="c9fdf-108">También se pueden establecer acciones para mensajes nuevos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="c9fdf-108">Actions can also be set for new messages in a conversation.</span></span> 
  
## <a name="applyconversationaction-request-example"></a><span data-ttu-id="c9fdf-109">Ejemplo de solicitud de ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="c9fdf-109">ApplyConversationAction request example</span></span>

### <a name="description"></a><span data-ttu-id="c9fdf-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9fdf-110">Description</span></span>

<span data-ttu-id="c9fdf-111">El siguiente ejemplo de una solicitud de **ApplyConversationAction** muestra cómo mover los elementos de la conversación especificada a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="c9fdf-111">The following example of an **ApplyConversationAction** request shows how to move the items in the specified conversation to another folder.</span></span> <span data-ttu-id="c9fdf-112">Los elementos que se agregan a la conversación también se moverán a la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="c9fdf-112">Items that are added to the conversation will also be moved to the specified folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c9fdf-113">Código</span><span class="sxs-lookup"><span data-stu-id="c9fdf-113">Code</span></span>

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

### <a name="remarks"></a><span data-ttu-id="c9fdf-114">Notas</span><span class="sxs-lookup"><span data-stu-id="c9fdf-114">Remarks</span></span>

<span data-ttu-id="c9fdf-115">Los identificadores de conversación y carpeta se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c9fdf-115">The conversation and folder identifiers have been shortened to preserve readability.</span></span>
  
## <a name="applyconversationaction-response-example"></a><span data-ttu-id="c9fdf-116">Ejemplo de respuesta ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="c9fdf-116">ApplyConversationAction response example</span></span>

### <a name="description"></a><span data-ttu-id="c9fdf-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9fdf-117">Description</span></span>

<span data-ttu-id="c9fdf-118">En el ejemplo siguiente se muestra una respuesta a una solicitud **ApplyConversationAction** correcta.</span><span class="sxs-lookup"><span data-stu-id="c9fdf-118">The following example shows a successful response to an **ApplyConversationAction** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c9fdf-119">Código</span><span class="sxs-lookup"><span data-stu-id="c9fdf-119">Code</span></span>

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

## <a name="see-also"></a><span data-ttu-id="c9fdf-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="c9fdf-120">See also</span></span>

- [<span data-ttu-id="c9fdf-121">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="c9fdf-121">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="c9fdf-122">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c9fdf-122">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="c9fdf-123">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c9fdf-123">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="c9fdf-124">Conversaciones de EWS</span><span class="sxs-lookup"><span data-stu-id="c9fdf-124">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

