---
title: Proponer una nueva hora de reunión mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: d5ac8e5b-3876-4f20-b4d3-44505e066042
description: Descubra cómo proponer nuevas horas de reunión desde su Exchange cliente mediante EWS en Exchange.
ms.openlocfilehash: a6406aaef2005e74165e647510af891d2a59503e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522232"
---
# <a name="propose-a-new-meeting-time-by-using-ews-in-exchange"></a>Proponer una nueva hora de reunión mediante EWS en Exchange

Descubra cómo proponer nuevas horas de reunión desde su Exchange cliente mediante EWS en Exchange.
  
La característica proponer nueva hora permite a los asistentes proponer nuevas horas de reunión al organizador de la reunión como parte del flujo de trabajo Exchange calendario. Cuando un asistente propone una nueva reunión, el organizador puede usar la nueva hora de reunión propuesta para actualizar la reunión y enviar actualizaciones a todos los asistentes. Antes de permitir que los asistentes propongan nuevas horas de reunión, debes determinar si el organizador permite nuevas propuestas de tiempo. En este artículo se describe cómo determinar si puede proponer una nueva hora y cómo usar EWS para proponer una nueva hora.
  
> [!NOTE]
> La API administrada de EWS no implementa esta funcionalidad. 
  
## <a name="determine-whether-you-can-propose-a-new-time-for-a-meeting-by-using-ews"></a>Determinar si puede proponer una nueva hora para una reunión mediante EWS
<a name="bk_Determine"> </a>

Antes de poder proponer una nueva hora para una reunión, debe encontrar una referencia a esa reunión y determinar si el organizador de la reunión configuró la reunión para admitir nuevas propuestas de tiempo. Para obtener una referencia a una reunión, haga lo siguiente: 
  
- Buscar la solicitud de reunión en la Bandeja de entrada
    
- Buscar la cita en el calendario
    
Siga estos pasos para buscar una referencia de reunión:
  
1. Use la [operación EWS FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) (o el método de API administrada EWS [Folder.FindItems)](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) para buscar la solicitud de reunión de destino o el elemento de calendario. Como alternativa, puede usar la [operación EWS SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) para obtener el identificador de la solicitud de reunión de destino o elemento de calendario. 
    
2. Analice los resultados de la **operación FindItem** (o **el método Folder.FindItems)** para obtener el identificador del elemento de reunión. 
    
3. Use la [operación EWS GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) para obtener los objetos de respuesta de la reunión. 
    
El siguiente XML muestra lo que se envía para solicitar los objetos de respuesta en un elemento.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:MailboxCulture>en-US</t:MailboxCulture>
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:ResponseObjects"/>
          <t:FieldURI FieldURI="item:Subject"/>
          <t:FieldURI FieldURI="calendar:Start"/>
          <t:FieldURI FieldURI="calendar:End"/>
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkADEzOTExYjJkL1AAA=" ChangeKey="CwAAAB/G6X"/>
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

La respuesta de la operación **GetItem** tendrá un aspecto similar al siguiente XML si solicita el identificador de elemento, la hora de inicio y finalización de la reunión, la colección de objetos de respuesta y si el organizador permite cambios propuestos en la hora de reunión. La colección de objetos response, que se representa mediante el [elemento ResponseObjects,](https://msdn.microsoft.com/library/ad29e064-3f3d-4b7b-aa4c-9ec27326381d%28Office.15%29.aspx) contiene el conjunto de respuestas que son válidas para el elemento de calendario. El **elemento ProposeNewTime** es un objeto de respuesta que indica que el usuario puede proponer una nueva hora para la reunión. Los [elementos AcceptItem](https://msdn.microsoft.com/library/05a15431-77e1-411a-a16b-5481d364d3cc%28Office.15%29.aspx), [TentativelyAcceptItem](https://msdn.microsoft.com/library/ce6f50ef-ad8a-47e4-915a-487b2ef7a2e0%28Office.15%29.aspx)y [DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) representan los objetos de respuesta que puede usar para proponer una nueva hora de reunión al organizador de la reunión. 
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:MeetingRequest>
              <t:ItemId Id="AAMkADEzOTExYjJkL1AAA=" ChangeKey="CwAAAB/G6X"/>
              <t:Subject>Competitive analysis: kick off meeting</t:Subject>
              <t:ResponseObjects>
                <t:AcceptItem/>
                <t:TentativelyAcceptItem/>
                <t:DeclineItem/>
                <t:ProposeNewTime/>
                <t:ReplyToItem/>
                <t:ReplyAllToItem/>
                <t:ForwardItem/>
              </t:ResponseObjects>
              <t:Start>2013-11-09T17:00:00Z</t:Start>
              <t:End>2013-11-09T17:30:00Z</t:End>
            </t:MeetingRequest>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="propose-a-new-meeting-time-by-using-ews"></a>Proponer una nueva hora de reunión mediante EWS
<a name="bk_Propose"> </a>

Si recibió un objeto de respuesta **ProposeNewTime** cuando usó la operación **GetItem** para obtener un elemento de calendario o una solicitud de reunión, puede responder con una nueva hora de reunión propuesta. Si no recibió un objeto de respuesta **ProposeNewTime,** no podrá proponer una nueva hora de reunión como parte del flujo de trabajo del calendario. Sin embargo, puede responder al organizador para solicitar una nueva hora de reunión. Si recibe un objeto de respuesta **ProposeNewTime,** puede responder a la reunión haciendo referencia a su identificador y proponer una nueva hora de reunión al organizador. Aquí es donde el objeto de respuesta **ProposeNewTime** es diferente del patrón de objeto de respuesta típico en que no responde con un objeto de respuesta **ProposeNewTime.** Use uno de los otros objetos de respuesta a la reunión, como **AcceptItem**, **TentativelyAcceptItem** o **DeclineItem**, para proponer una nueva reunión. En este ejemplo se usa el **objeto de respuesta AcceptItem.** 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013"/>
  </soap:Header>
  <soap:Body>
    <m:CreateItem>
      <m:Items>
        <t:AcceptItem>
          <t:Body BodyType="Text">This time works better for the HiPPO.</t:Body>
          <t:ReferenceItemId Id="AAMkADEzOTExYjJkL1AAA=" ChangeKey="CwAAAB/G6X"/>
          <t:ProposedStart>2013-11-28T04:00:00Z</t:ProposedStart>
          <t:ProposedEnd>2013-11-28T04:30:00Z</t:ProposedEnd>
        </t:AcceptItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

La respuesta a esta solicitud contiene el identificador del elemento de calendario que se agregó al calendario del asistente y una copia de la solicitud de reunión que se colocó en la carpeta Elementos eliminados del asistente. El mensaje de respuesta con la nueva propuesta de tiempo también se guardó en la carpeta Elementos enviados del asistente (tendrá que buscar el mensaje de respuesta de la reunión para obtener un controlador sobre ella).
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkAGRmOWE2OWAAA=" ChangeKey="DwAAJsmU"/>
            </t:CalendarItem>
            <t:MeetingRequest>
              <t:ItemId Id="AAMkAGRmOWE2AAABB=" ChangeKey="AAAGJu1A"/>
            </t:MeetingRequest>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

El organizador recibirá un mensaje [de MeetingResponse](https://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx) cuando el asistente responda con una nueva hora de reunión propuesta. El **mensaje MeetingResponse** contiene la nueva hora de inicio y finalización de la reunión propuesta, y el identificador del elemento de calendario asociado en el calendario del organizador. El organizador puede usar esa información para actualizar el elemento de calendario existente para la reunión. El siguiente es el flujo de trabajo para que el organizador responda a un mensaje **de MeetingResponse** que proponga una nueva hora de reunión: 
  
1. Determine si los **elementos ProposedStart** o **ProposedEnd** se han establecido en **MeetingResponse**. Si es así, vaya al paso 2. Si no es así, el **mensaje MeetingResponse** solo indica si el asistente ha aceptado, aceptado provisionalmente o rechazado la reunión. 
    
2. Obtener el elemento de calendario existente del organizador para la reunión mediante el identificador EWS devuelto en el **elemento AssociatedCalendarItemId.** 
    
3. Compare la hora de inicio y finalización original con la nueva hora de reunión propuesta. Si la nueva hora de reunión propuesta es aceptable para el organizador, vaya al paso 4. De lo contrario, el organizador de la reunión puede omitir la hora de reunión propuesta o enviar una respuesta de correo electrónico al asistente que propuso la nueva hora de reunión.
    
4. (Opcional) Realice una llamada a la operación EWS [GetUserAvailability](https://msdn.microsoft.com/library/8da17226-5d3a-4525-9ffa-d83730f47bb1%28Office.15%29.aspx) para averiguar si la hora propuesta funcionará para todos los asistentes, incluidos los buzones de sala y recursos. (También puede usar el método de LA API administrada de EWS [ExchangeService.GetUserAvailability](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getuseravailability%28v=exchg.80%29.aspx) para hacerlo). 
    
5. A continuación, el organizador puede actualizar su reunión con las nuevas horas de reunión propuestas y enviar las actualizaciones a todos los asistentes mediante la operación [EWS UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) (o el método de la API administrada ews [Appointment.Update).](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) 
    
En la siguiente figura se muestra el proceso que se produce entre el organizador de la reunión, el asistente y el servidor Exchange que controló las llamadas EWS.
  
**Figura 1. Proceso para proponer una nueva hora de reunión**

![La figura muestra el flujo de trabajo entre el organizador, Exchange y un asistente cuando se propone una nueva hora de reunión. Si el organizador permite nuevas propuestas para la reunión, un asistente puede proponer una nueva hora de reunión con un objeto Response.](media/Ex_ProposeNewMeetingTime.png)
  
## <a name="version-differences"></a>Diferencias de versión
<a name="bk_Behavior"> </a>

La nueva característica de tiempo de propuesta se introdujo Exchange versión de compilación 15.00.0800.007. En versiones anteriores de Exchange, los usuarios de la aplicación EWS tienen que enviar un correo electrónico independiente al organizador de la reunión para solicitar una hora de reunión diferente. 
  
## <a name="see-also"></a>Ver también


- [Calendarios y EWS en Exchange](calendars-and-ews-in-exchange.md)
    
- [Crear citas y reuniones mediante EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Obtener citas y reuniones mediante EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Actualice las citas y reuniones mediante EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Eliminar citas y cancelar reuniones mediante EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

