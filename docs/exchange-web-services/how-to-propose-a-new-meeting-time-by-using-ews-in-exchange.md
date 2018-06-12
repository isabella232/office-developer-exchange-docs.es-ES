---
title: Proponer una nueva hora de reunión mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d5ac8e5b-3876-4f20-b4d3-44505e066042
description: Descubra cómo proponer nuevas horas de reunión desde la aplicación de cliente de Exchange mediante el uso de EWS en Exchange.
ms.openlocfilehash: f9edd8511332474a728635a6aa369a772da24786
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763155"
---
# <a name="propose-a-new-meeting-time-by-using-ews-in-exchange"></a>Proponer una nueva hora de reunión mediante el uso de EWS en Exchange

Descubra cómo proponer nuevas horas de reunión desde la aplicación de cliente de Exchange mediante el uso de EWS en Exchange.
  
La nueva característica de tiempo proponer permite a los asistentes proponer nuevas horas de reunión al organizador de la reunión como parte del flujo de trabajo de calendario de Exchange. Cuando un asistente propone una nueva reunión, el organizador puede usar la nueva hora de reunión propuesta para actualizar la reunión y enviar actualizaciones a todos los asistentes. Antes de poder habilitar a los asistentes proponer nuevas horas de reunión, debe determinar si se permite el Organizador para nuevas propuestas de plazos. En este artículo se describe cómo determinar si puede proponer una nueva hora y cómo usar EWS para proponer una nueva hora.
  
> [!NOTE]
> La API administrada de EWS no implementa esta funcionalidad. 
  
## <a name="determine-whether-you-can-propose-a-new-time-for-a-meeting-by-using-ews"></a>Determinar si puede proponer una nueva hora para una reunión mediante el uso de EWS
<a name="bk_Determine"> </a>

Antes de proponer una nueva hora para una reunión, debe buscar una referencia a dicha reunión y determinar si el organizador de la reunión configurado la reunión para admitir nuevas propuestas de plazos. Puede obtener una referencia a una reunión mediante una de las siguientes opciones: 
  
- Búsqueda de la convocatoria de reunión en la Bandeja de entrada
    
- Búsqueda de la cita en el calendario
    
Use los pasos siguientes para buscar una referencia de la reunión:
  
1. Use la operación de EWS [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) (o el método de la API administrada de EWS [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) ) para encontrar el destino solicitud o elemento de calendario de la reunión. Como alternativa, puede usar la operación de EWS [SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) para obtener el identificador del elemento de calendario o solicitud de reunión de destino. 
    
2. Analizar los resultados de la operación de **FindItem** (o el método **Folder.FindItems** ) para obtener el identificador de elemento del elemento de reunión. 
    
3. Use la operación de EWS [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) para obtener los objetos de respuesta para la reunión. 
    
El siguiente código XML muestra lo que se envía a los objetos de respuesta en un elemento de solicitud.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

La respuesta de la operación **GetItem** tendrá un aspecto similar al código XML siguiente si solicita el identificador del elemento, el inicio de la reunión y hora de finalización, la colección de objetos de respuesta, y si el organizador permite cambios propuestos para el tiempo de la reunión. La colección de objetos de respuesta, que está representada por el elemento [ResponseObjects](http://msdn.microsoft.com/library/ad29e064-3f3d-4b7b-aa4c-9ec27326381d%28Office.15%29.aspx) , contiene el conjunto de las respuestas que son válidos para el elemento de calendario. El elemento **ProposeNewTime** es un objeto de respuesta que indica que el usuario puede proponer una nueva hora para la reunión. Los elementos de [AcceptItem](http://msdn.microsoft.com/library/05a15431-77e1-411a-a16b-5481d364d3cc%28Office.15%29.aspx), [TentativelyAcceptItem](http://msdn.microsoft.com/library/ce6f50ef-ad8a-47e4-915a-487b2ef7a2e0%28Office.15%29.aspx)y [DeclineItem](http://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) representan los objetos de respuesta que puede usar para proponer una nueva hora de reunión al organizador de la reunión. 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="propose-a-new-meeting-time-by-using-ews"></a>Proponer una nueva hora de reunión mediante el uso de EWS
<a name="bk_Propose"> </a>

Si ha recibido un objeto de respuesta **ProposeNewTime** cuando se usa la operación **GetItem** para obtener un elemento de calendario o convocatoria de reunión, puede responder con una nueva hora de reunión propuesta. Si no ha recibido un objeto de respuesta **ProposeNewTime** , no podrá proponer una nueva hora de reunión como parte del flujo de trabajo de calendario. Sin embargo, puede responder al organizador para solicitar una nueva hora de reunión. Si recibe un objeto de respuesta **ProposeNewTime** , puede responder a la reunión mediante una referencia a su identificador y proponer una nueva hora de reunión del organizador. Esto es donde el objeto de respuesta **ProposeNewTime** es diferente del modelo de objeto de respuesta típica en que no responde con un objeto de respuesta **ProposeNewTime** . Use uno de los otros objetos de respuesta, como **AcceptItem**, **TentativelyAcceptItem**o **DeclineItem**, para proponer una nueva reunión de la reunión. En este ejemplo se utiliza el objeto de respuesta de **AcceptItem** . 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

La respuesta a esta solicitud contiene el identificador del elemento de calendario que se ha agregado para el calendario del asistente y una copia de la convocatoria de reunión que se ha puesto en la carpeta de elementos eliminados del asistente. El mensaje de respuesta con la nueva propuesta de hora también se guardó en la carpeta de elementos enviados del asistente (necesita encontrar la reunión mensaje de respuesta para obtener un identificador en él).
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

El organizador recibirá un mensaje de [MeetingResponse](http://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx) cuando el Asistente responde con una nueva hora de reunión propuesta. El mensaje de **MeetingResponse** contiene la reunión propuesta de nueva hora de inicio y hora de finalización y el identificador del elemento de calendario asociado en el calendario del organizer. El organizador puede utilizar esa información para actualizar su elemento de calendario existente para la reunión. El siguiente es el flujo de trabajo para el organizador responder a un mensaje de **MeetingResponse** que propone una nueva hora de reunión: 
  
1. Determinar si se han establecido los elementos **ProposedStart** o **///ProposedEnd** en el **MeetingResponse**. Si es así, vaya al paso 2. Si no es así, el mensaje de **MeetingResponse** sólo indica si el asistente ha aceptado, aceptado provisionalmente o rechazado la reunión. 
    
2. Obtener elemento de calendario existente del organizador de la reunión utilizando el identificador EWS devuelto en el elemento **AssociatedCalendarItemId** . 
    
3. Compare el inicio original y la hora de finalización con la nueva hora de reunión propuesta. Si la nueva hora de reunión propuesta es aceptable para el organizador, vaya al paso 4. De lo contrario, el organizador de la reunión puede omitir la hora de reunión propuesta o enviar una respuesta de correo electrónico a los asistentes que proponen la nueva hora de reunión.
    
4. (Opcional) Realizar una llamada de operación de EWS [GetUserAvailability](http://msdn.microsoft.com/library/8da17226-5d3a-4525-9ffa-d83730f47bb1%28Office.15%29.aspx) para averiguar si la hora propuesta funcionará para todos los asistentes, incluidos los buzones de sala y recursos. (Se puede utilizar el método de la API administrada de EWS [ExchangeService.GetUserAvailability](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getuseravailability%28v=exchg.80%29.aspx) hacerlo.) 
    
5. El organizador, a continuación, puede actualizar sus reuniones con los nuevos tiempos de reunión propuesta y enviar las actualizaciones a todos los asistentes mediante el uso de la operación de EWS [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) (o el método de la API administrada de EWS [Appointment.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) ). 
    
La siguiente ilustración muestra el proceso que se produce entre el organizador de la reunión, el asistente y el servidor de Exchange que administra las llamadas EWS.
  
**En la figura 1. Proceso para proponer una nueva hora de reunión**

![La figura muestra el flujo de trabajo entre el organizador, Exchange y un asistente cuando se propone una nueva hora de reunión. Si el organizador permite nuevas propuestas para la reunión, un asistente puede proponer una nueva hora de reunión con un objeto Response.](media/Ex_ProposeNewMeetingTime.png)
  
## <a name="version-differences"></a>Diferencias de versión
<a name="bk_Behavior"> </a>

La nueva característica de tiempo proponer se introdujo en la versión de compilación de Exchange 15.00.0800.007. En versiones anteriores de Exchange, usuarios de la aplicación de EWS tienen que enviar un correo electrónico independiente al organizador de la reunión para solicitar una hora de reunión diferente. 
  
## <a name="see-also"></a>Ver también


- [Calendarios y EWS en Exchange](calendars-and-ews-in-exchange.md)
    
- [Crear citas y reuniones mediante el uso de EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [Obtener las citas y reuniones con EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Actualizar las citas y reuniones con EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [Eliminar las citas y cancelar reuniones mediante el uso de EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

