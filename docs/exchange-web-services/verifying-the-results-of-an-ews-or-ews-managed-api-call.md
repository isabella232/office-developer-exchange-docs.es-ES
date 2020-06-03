---
title: Comprobación de los resultados de una llamada de API administrada de EWS o EWS
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: 78a1741c-1bbe-4cb4-9331-9d6d3171fc11
description: Obtenga información sobre cómo comprobar los resultados de las llamadas de la API administrada de EWS o EWS.
localization_priority: Priority
ms.openlocfilehash: be8e76898dd111a6dec33d4a57d9d50a2a935390
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457399"
---
# <a name="verifying-the-results-of-an-ews-or-ews-managed-api-call"></a>Comprobación de los resultados de una llamada de API administrada de EWS o EWS

Obtenga información sobre cómo comprobar los resultados de las llamadas de la API administrada de EWS o EWS.
  
Cuando las cosas no funcionan correctamente, le ayudarán a ver lo que está ocurriendo examinando las solicitudes SOAP que la aplicación envía a través de la red y las respuestas que el servidor envía de vuelta. El artículo [herramientas y recursos para solucionar problemas de las aplicaciones de EWS](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md) incluye vínculos a herramientas para ayudar a capturar y ver esas solicitudes SOAP. Una vez que haya recibido las solicitudes y las respuestas, ¿cómo comprobar que la solicitud que envió al servidor se ha procesado correctamente? Siga leyendo para obtener más información. 
  
Si va a enviar solicitudes EWS, empezará la comprobación comprobando el atributo **ResponseClass** de cada mensaje de respuesta en la respuesta. Esto le indicará si la operación se completó correctamente en cada elemento. 
  
Según el objeto al que llame el método, si está usando la API administrada de EWS para enviar solicitudes, puede realizar alguna comprobación con los objetos de respuesta. Pero debido a que la respuesta SOAP contiene un superconjunto de lo que se incluye en los objetos de respuesta de la API administrada de EWS, es posible que también desee mirar la respuesta SOAP. Dado que la respuesta SOAP puede contener a menudo más información que los objetos de respuesta de la API administrada de EWS, inicie la comprobación con la respuesta SOAP.
  
## <a name="verifying-the-results-of-a-soap-response"></a>Comprobación de los resultados de una respuesta SOAP
<a name="bk_verifysoap"> </a>

Cuando recibe una respuesta SOAP, lo primero que debe considerar es el atributo **ResponseClass** . Este atributo se incluye en cada instancia de **ResponseMessageType** en el elemento [ResponseMessages](https://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx) , como se muestra en el ejemplo siguiente. 
  
```XML
<s:Body>
      <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
        <m:ResponseMessages>
          <m:GetItemResponseMessage ResponseClass="Success">
          …
```

Como una respuesta SOAP puede contener varios mensajes de respuesta en una sola respuesta SOAP, es importante comprobar cada mensaje de respuesta de forma individual.
  
Si está trabajando con una operación que incluye un **ResponseClass** como parte de la respuesta de la operación, como la siguiente, es posible que se vea tentado a comprobar solo la **ResponseClass** de la operación. 
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  …

```

Sin embargo, el estado de la operación sólo refleja la forma de la respuesta de nivel superior y no refleja el estado de todas las respuestas de mensaje individuales. En el siguiente ejemplo, la operación [AddDelegateResponse](https://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) tiene un **ResponseClass** de **correcto**, pero el elemento [DelegateUserResponseMessageType](https://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx) subyacente tiene un valor **ResponseClass** de **error**.
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
    <m:ResponseCode>NoError</m:ResponseCode>
    <m:ResponseMessages>
      <m:DelegateUserResponseMessageType ResponseClass="Error">
        <m:MessageText>The user is already a delegate for the mailbox.</m:MessageText>
        <m:ResponseCode>ErrorDelegateAlreadyExists</m:ResponseCode>
        <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
      </m:DelegateUserResponseMessageType>
    </m:ResponseMessages>
  </m:AddDelegateResponse>
</soap:Body>
```

Por lo tanto, para las respuestas de EWS SOAP, no puede confiar en la **ResponseClass** de la operación, tiene que mirar el **ResponseClass** de cada mensaje de respuesta para determinar si la operación encontró algún error al procesar los elementos. 
  
### <a name="verifying-success"></a>Comprobar el éxito

Si cada atributo **ResponseClass** de cada atributo **ResponseMessage** se establece en **correcto**, la operación se completó correctamente en todos los elementos y puede pasar a la siguiente tarea.
  
En el siguiente ejemplo se muestra una respuesta correcta a una solicitud de [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) Operation para recuperar un único elemento. Tenga en cuenta que cuando **ResponseClass** se establece en **Success**, el [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) asociado siempre se establece en **NoError**.
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
             xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
        <m:ResponseMessages>
          <m:GetItemResponseMessage ResponseClass="Success">
            <m:ResponseCode>NoError</m:ResponseCode>
            <m:Items>
              <t:Message>
                <t:ItemId Id="Er5bAAA=" 
                          ChangeKey="CQAAABYAAAD32nSTjepyT63rYH17n9THAAAhE0/M" />
                <t:Subject>Dinner Party</t:Subject>
              </t:Message>
            </m:Items>
          </m:GetItemResponseMessage>
        </m:ResponseMessages>
      </m:GetItemResponse>
    </s:Body>
```

La siguiente es una respuesta correcta a una solicitud de operación de **GetItem** para recuperar varios elementos. Cada uno de los elementos [GetItemResponseMessage](https://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx) tiene un **ResponseClass** de **operación correcta**.
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
             xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
    <m:ResponseMessages>
      <m:GetItemResponseMessage ResponseClass="Success">
        <m:ResponseCode>NoError</m:ResponseCode>
        <m:Items>
          <t:Message>
            <t:ItemId Id="Er5bAAA=" 
                      ChangeKey="CQAAABYAAAD32nSTjepyT63rYH17n9THAAAhE0/M" /
            <t:Subject>Dinner Party</t:Subject>
          </t:Message>
        </m:Items>
      </m:GetItemResponseMessage>
      <m:GetItemResponseMessage ResponseClass="Success">
        <m:ResponseCode>NoError</m:ResponseCode>
        <m:Items>
          <t:Message>
            <t:ItemId Id="3c66AAA="
                      ChangeKey="CQAAABYAAAD32nSTjepyT63rYH17n9THAAAc3kqm" />
            <t:Subject>Company Soccer Team</t:Subject>
          </t:Message>
        </m:Items>
      </m:GetItemResponseMessage>
    </m:ResponseMessages>
  </m:GetItemResponse>
</s:Body>
```

### <a name="handling-errors-and-warnings"></a>Control de errores y advertencias

Cuando recibe una respuesta y el atributo **ResponseClass** se establece en **error**, la operación no se completó correctamente en uno o varios elementos. Corrija el problema y vuelva a intentar la solicitud, o la parte de su solicitud que ha fallado. Un valor de atributo **ResponseClass** de valor de **ADVERTENCIA** solo lo devuelve la operación [ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) e indica que la entidad no se pudo resolver como una identidad única. Puede ignorarlo para todas las demás operaciones. 
  
En la siguiente respuesta, el atributo **ResponseClass** tiene un valor de **error**.
  
```XML
<m:GetItemResponseMessage ResponseClass="Error">
  <m:MessageText>Property is not valid for this object type.</m:MessageText>
  <m:ResponseCode>ErrorInvalidPropertyRequest</m:ResponseCode>
  <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
  <m:MessageXml>
    <t:FieldURI FieldURI="meeting:AssociatedCalendarItemId" />
  </m:MessageXml>
  <m:Items />
</m:GetItemResponseMessage>
```

En este ejemplo, EWS proporciona pistas para depurar el problema. Cuando el atributo **ResponseClass** tiene un valor de **error**, se incluyen los siguientes elementos adicionales en la respuesta cuando corresponda:
  
- [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) : describe el error. 
    
- [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) : contiene el código de error, que se puede usar para buscar recursos de solución de problemas adicionales. 
    
- [MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) : identifica los elementos que causaron el error. 
    
- [DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) : no se usa. 
    
Puede usar la información proporcionada en estos elementos para investigar el problema. En el ejemplo anterior, el **MessageText** indica que la propiedad no es válida para el tipo de objeto. La solicitud era obtener un mensaje de correo electrónico, pero el conjunto de propiedades incluyó la **AssociatedCalendarItemId**, que solo es válida para los elementos de cita.
  
En el ejemplo siguiente se muestra un error que se recibió como parte de una operación por lotes para obtener varios elementos de correo electrónico. El primer elemento se recuperó correctamente y **ResponseClass** se establece en **Success**. No se encontró el segundo elemento y **ResponseClass** se ha establecido en **error**.
  
```XML
<m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <m:ResponseMessages>
    <m:GetItemResponseMessage ResponseClass="Success">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:Items>
        <t:Message>
          <t:ItemId Id="Er5cAAA="
                    ChangeKey="CQAAABYAAAD32nSTjepyT63rYH17n9THAAAhE0/O" />
          <t:Subject>Business plans</t:Subject>
        </t:Message>
      </m:Items>
    </m:GetItemResponseMessage>
    <m:GetItemResponseMessage ResponseClass="Error">
      <m:MessageText>The specified object was not found in the store.</m:MessageText>
      <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
      <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
      <m:Items />
    </m:GetItemResponseMessage>
  </m:ResponseMessages>
</m:GetItemResponse>
```

Cuando uno o varios elementos de una solicitud por lotes no se pueden procesar como se solicitan, se devuelve un error para cada elemento que ha fallado y el resto de los elementos del lote se procesan como se esperaba. Los errores en el procesamiento por lotes pueden producirse si el elemento se eliminó y, por lo tanto, no se puede enviar, recuperar o actualizar, o si el elemento se movió a una carpeta diferente y, por lo tanto, tiene un identificador de elemento nuevo. Como la operación se completará para algunos elementos y no devolverá un error cuando no se puedan procesar uno o varios elementos, es importante comprobar cada atributo **ResponseClass** antes de pasar a la siguiente operación. 
  
Si la información proporcionada por los elementos Response no le ayuda a corregir la solicitud o desbloquearlo de algún otro modo, vea [los siguientes pasos](#bk_nextsteps).
  
## <a name="verifying-the-results-of-an-ews-managed-api-method-call"></a>Comprobación de los resultados de una llamada de método de la API administrada de EWS
<a name="bk_successful"> </a>

Si usa la API administrada de EWS y llama a un método en un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) , es probable que el método devuelva un objeto [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) , que contiene una colección de objetos [ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) o una colección de objetos derivados de los objetos **ServiceResponse** . Los objetos **ServiceResponseCollection** e incluidos **ServiceResponse** contienen información sobre el resultado de la llamada al método, que puede usar para comprobar los resultados. 
  
Si está usando la API administrada de EWS y llama a un método en un objeto de [elemento](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) o uno de los objetos derivados, es probable que el método no devuelva un objeto de respuesta para comprobar si el resultado es correcto, pero produce una [excepción](https://msdn.microsoft.com/library/c18k6c59) si el método no se completa correctamente. 
  
### <a name="verifying-success"></a>Comprobar el éxito

Una de las ventajas de usar la API administrada de EWS es que proporciona un estado general al tratar con varios elementos en una respuesta. Por lo tanto, si el método al que llama devuelve **ServiceResponseCollection**, puede comprobar que la propiedad [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) de **ServiceResponseCollection** es igual a [ServiceResult. Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx). Si es así, todos los elementos del proceso por lotes se completaron correctamente; no es necesario comprobar cada objeto **ServiceResponse** de forma individual. Si la propiedad **OverallResult** no está establecida en **ServiceResult. Success**, debe [controlar el error o la advertencia](#bk_ewsmaerrors).
  
Si el método que está llamando no devuelve una **ServiceResponseCollection**, pero devuelve un objeto **ServiceResponse** , tiene que comprobar el valor de la propiedad **result** . Si el valor del **resultado** se establece en **correcto**, sabrá que el método se ha completado correctamente.
  
Si el método al que llama no tiene ningún valor devuelto, no hay ninguna forma de comprobar el éxito mediante la API administrada de EWS. Siempre que no se produzca una excepción, puede suponer que el método se ha completado correctamente. Para obtener más validación, también puede [comprobar la respuesta SOAP para comprobar los resultados](#bk_verifysoap).
  
### <a name="handling-errors-warnings-and-exceptions"></a>Control de errores, advertencias y excepciones
<a name="bk_ewsmaerrors"> </a>

Si el código de la API administrada de EWS produce una **excepción**, puede usar el valor [Exception. Message](https://msdn.microsoft.com/library/9btwf6wk) para determinar el origen del error. La propiedad **Message** contiene el contenido del elemento [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) en la respuesta SOAP subyacente. Además, si la excepción es del tipo [ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) Object, una de las excepciones más comunes, también puede recuperar el [ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx) que se incluye en el elemento de [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) SOAP subyacente, y la propiedad [Response](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx) que identifica el objeto [ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) asociado. El siguiente código muestra cómo detectar y mostrar el contenido de un **ServiceResponseException**. 
  
```cs
try
    {
         …
    }
    catch (ServiceResponseException ex)
    {
        Console.WriteLine("Error code: " + ex.ErrorCode);
        Console.WriteLine("Error message: " + ex.Message);
        Console.WriteLine("Response: " + ex.Response);
    }
```

Si el método al que ha llamado devuelve una **ServiceResponseCollection**y el valor de la propiedad **OverallResult** es igual a **Warning** o **error**, tendrá que recorrer todos los objetos de la **ServiceResponseCollection** para encontrar el error. La propiedad **OverallResult** se establece en **Warning** si al menos una respuesta tiene el valor de **resultado** establecido en **Warning** y el resto de las respuestas tienen los valores de **resultado** establecidos en **correcto**. La propiedad **OverallResult** se establece en **error** si al menos una respuesta tiene el valor de **resultado** establecido en **error**. Cuando **OverallResult** se establece en **Warning** o **error**, se establecen las siguientes propiedades en los objetos **ServiceResponse** según corresponda: 
  
- [ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) : contiene el código de error, que se puede usar para buscar recursos de solución de problemas adicionales. 
    
- [ErrorDetails](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) : contiene detalles sobre el error de algunos **ErrorCodes**. Por ejemplo, cuando el código de error es **ErrorRecurrenceHasNoOccurrence**, **ErrorDetails** contendrá claves para **EffectiveStartDate** y **EffectiveEndDate**. 
    
- [ErrorMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) : describe el error. 
    
- [ErrorProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) : Si está disponible, identifica las propiedades que causaron el error. Por ejemplo, cuando el código de error es **ErrorInvalidPropertyForOperation**, **ErrorProperties** contiene la definición de la propiedad que no era válida para la solicitud. 
    
- [Result](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx) : contiene un **error** o una **ADVERTENCIA** cuando se encuentra un problema. 
    
Si la información proporcionada por las propiedades **ServiceResponse** no proporciona suficiente información para corregir la llamada al método o desbloquear por usted, consulte [los pasos siguientes](#bk_nextsteps) para obtener más información sobre los valores de **ErrorCode** . 
  
## 
<a name="bk_nextsteps"> </a>

Puede buscar información adicional de solución de problemas en los siguientes temas:
  
- Elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) 
    
- Enumeración [ServiceError](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) 
    
- [Errores relacionados con la propiedad EWS](ews-property-related-errors.md)
    
Además, en función de lo que intente realizar en su solicitud, puede encontrar información adicional sobre el código de error en los siguientes temas:
  
- [Administrar los mensajes de error de detección automática](handling-autodiscover-error-messages.md)
    
- [Control de errores relacionados con la notificación en EWS en Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Controlar errores relacionados con la sincronización en EWS en Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Administración de errores relacionados con la eliminación en EWS en Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también


- [Desarrollar clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Herramientas y recursos para solucionar problemas de las aplicaciones de EWS para Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

