---
title: Comprobación de los resultados de una llamada de EWS o la API administrada de EWS
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78a1741c-1bbe-4cb4-9331-9d6d3171fc11
description: Obtenga información sobre cómo comprobar los resultados de las llamadas de EWS o la API administrada de EWS.
ms.openlocfilehash: 077dd923710a1a7f5cad4c822cbbd58ab3603661
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763309"
---
# <a name="verifying-the-results-of-an-ews-or-ews-managed-api-call"></a>Comprobación de los resultados de una llamada de EWS o la API administrada de EWS

Obtenga información sobre cómo comprobar los resultados de las llamadas de EWS o la API administrada de EWS.
  
Cuando las cosas no funcionan correctamente, es muy útil para ver lo que está ocurriendo mediante el examen de las solicitudes SOAP que su aplicación se envíe a través de la red y las respuestas que el servidor envía de vuelta. El artículo de [Herramientas y recursos para solucionar problemas de aplicaciones de EWS](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md) incluye vínculos a herramientas que ayudan a capturar y ver las solicitudes SOAP. ¿Una vez que dispone de las solicitudes y las respuestas, cómo comprobar que la solicitud que envía al servidor se procesó correctamente? Siga leyendo para averiguar. 
  
Si va a enviar solicitudes EWS, va a iniciar la comprobación comprobando el atributo **ResponseClass** para cada mensaje de respuesta en la respuesta. Que le indicará si la operación se completó correctamente en cada elemento. 
  
Dependiendo del objeto que el método está llamando a, si se usa la API administrada de EWS para enviar solicitudes, puede hacer algunos comprobación mediante los objetos de respuesta. Pero, debido a que la respuesta SOAP contiene un superconjunto de qué se incluye en los objetos de respuesta de la API administrada de EWS, es posible que desee estudiar así como la respuesta SOAP. Debido a que la respuesta SOAP a menudo puede contener más información que los objetos de respuesta de la API administrada de EWS, inicie la comprobación con la respuesta SOAP.
  
## <a name="verifying-the-results-of-a-soap-response"></a>Comprobación de los resultados de una respuesta SOAP
<a name="bk_verifysoap"> </a>

Cuando recibe una respuesta SOAP, lo primero que debe mirar es el atributo **ResponseClass** . Este atributo se incluye en cada instancia de **ResponseMessageType** en el elemento [ResponseMessages](http://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx) , tal como se muestra en el siguiente ejemplo. 
  
```XML
<s:Body>
      <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <m:ResponseMessages>
          <m:GetItemResponseMessage ResponseClass="Success">
          …
```

Debido a que una respuesta SOAP puede contener varios mensajes de respuesta en una sola respuesta SOAP, es importante comprobar individualmente cada mensaje de respuesta.
  
Si está trabajando con una operación que incluye un **ResponseClass** como parte de la respuesta de la operación, como la siguiente, es posible que vean tentados a comprobar sólo el **ResponseClass** de la operación. 
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  …

```

Sin embargo, el estado de la operación sólo refleja la forma de la respuesta de nivel superior y no refleja el estado de todas las respuestas de mensajes individuales. En el ejemplo siguiente, la operación de [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) tiene un **ResponseClass** de **éxito**, pero el elemento [DelegateUserResponseMessageType](http://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx) subyacente tiene un valor de **ResponseClass** de **Error**.
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

Por lo tanto para las respuestas SOAP EWS, no puede confiar en la **ResponseClass** de la operación: tiene que examine el **ResponseClass** de cada mensaje de respuesta para determinar si la operación ha encontrado los errores de procesamiento de los elementos. 
  
### <a name="verifying-success"></a>Comprobación de éxito

Si cada atributo **ResponseClass** para cada atributo **ResponseMessage** se establece en **correcto**, la operación ha finalizado correctamente en todos los elementos, y puede pasar a la siguiente tarea.
  
En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) para recuperar un único elemento. Tenga en cuenta que cuando se establece la **ResponseClass** para el **éxito**, el asociado [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) siempre se establece en **NoError**.
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
             xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

La siguiente es una respuesta correcta a una solicitud de operación **GetItem** para recuperar varios elementos. Cada uno de los elementos de [GetItemResponseMessage](http://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx) tiene un **ResponseClass** de **éxito**.
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
             xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                     xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="handling-errors-and-warnings"></a>Controlar errores y advertencias

Cuando recibe una respuesta y el atributo **ResponseClass** se establece en **Error**, la operación no se completó correctamente en uno o varios elementos. Corrija el problema y vuelva a intentar la solicitud o la parte de la solicitud que ha fallado. Un valor del atributo **ResponseClass** del valor de **Advertencia** sólo es devuelto por la operación [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) e indica que la entidad no se pudo resolver a una identidad única. Se puede omitir para todas las demás operaciones. 
  
En la siguiente respuesta, el atributo **ResponseClass** tiene un valor de **Error**.
  
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

En este ejemplo, EWS proporciona pistas para depurar el problema. Cuando el atributo **ResponseClass** tiene un valor de **Error**, se incluyen los siguientes elementos adicionales en la respuesta cuando sea aplicable:
  
- [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) : describe el error. 
    
- [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) — contiene el código de error, que se puede utilizar para buscar recursos de solución de problemas adicionales. 
    
- [MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) : identifica los elementos que causó el error. 
    
- [DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) — no usados. 
    
Puede usar la información proporcionada en estos elementos para investigar el problema. En el ejemplo anterior, la **MessageText** indica que la propiedad no es válida para el tipo de objeto. La solicitud era obtener un mensaje de correo electrónico, pero el conjunto de propiedades incluye la **AssociatedCalendarItemId**, que sólo es válido para elementos de cita.
  
En el ejemplo siguiente se muestra un error que se ha recibido como parte de una operación por lotes para obtener varios elementos de correo electrónico. El primer elemento se recuperó correctamente y se establece la **ResponseClass** para el **éxito**. No se pudo encontrar el segundo elemento, y el **ResponseClass** se establece en **Error**.
  
```XML
<m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Cuando no se puede procesar uno o varios elementos en una solicitud por lotes como se ha solicitado, se devuelve un error para cada elemento que no se pudo, y el resto de los elementos en el lote se procesan según lo previsto. Pueden producirse errores en el procesamiento por lotes si el elemento se ha eliminado y por lo tanto, no se envía, recuperar o actualizado, o si el elemento se mueve a una carpeta diferente y, por lo tanto, tiene un nuevo identificador de elemento. Debido a que la operación se complete para algunos de los elementos y no devuelve un error cuando no se puede procesar uno o varios elementos, es importante comprobar cada atributo **ResponseClass** antes de pasar a la siguiente operación. 
  
Si la información proporcionada por los elementos de respuesta no ayuda a corregir su solicitud o desbloquear en caso contrario,, vea los [pasos siguientes](#bk_nextsteps).
  
## <a name="verifying-the-results-of-an-ews-managed-api-method-call"></a>Comprobación de los resultados de una llamada de API administrada de EWS (método)
<a name="bk_successful"> </a>

Si está usando la API administrada de EWS y llamar a un método en un objeto [ExchangeService](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) , el método devolverá es probable que un objeto [ServiceResponseCollection](http://msdn.microsoft.com/EN-US/library/dd633715%28v=exchg.80%29.aspx) , que contiene una colección de objetos de [ServiceResponse](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) o una colección de objetos derivados de los objetos **ServiceResponse** . El **ServiceResponseCollection** y objetos **ServiceResponse** incluidos contienen información sobre el resultado de la llamada al método, que puede utilizar para comprobar los resultados. 
  
Si está usando la API administrada de EWS y llamar a un método en un objeto de [elemento](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) , o en uno de los objetos derivados, el método es probable que no devuelve un objeto de respuesta para comprobar el funcionamiento correcto, pero produce una [excepción](http://msdn.microsoft.com/EN-US/library/c18k6c59) si no se completa el método correctamente. 
  
### <a name="verifying-success"></a>Comprobación de éxito

Una ventaja de utilizar la API administrada de EWS es que proporciona un estado global cuando trabaja con varios elementos en una respuesta. Por lo tanto, si el método al que llamó devuelve una **ServiceResponseCollection**, puede comprobar que la propiedad [OverallResult](http://msdn.microsoft.com/en-us/library/dd634515%28v=exchg.80%29.aspx) de la **ServiceResponseCollection** es igual a [ServiceResult.Success](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx). Si es así, todos los elementos en el proceso por lotes se han completado correctamente; no es necesario que comprobar individualmente cada objeto **ServiceResponse** . Si no se establece la propiedad **OverallResult** para **ServiceResult.Success**, se debe [controlar el error o la advertencia](#bk_ewsmaerrors).
  
Si el método que se está llamando no devuelve un **ServiceResponseCollection**, pero devuelve un objeto **ServiceResponse** , se debe comprobar el valor de la propiedad **Result** . Si se establece el valor del **resultado** para el **éxito**, sabrá que el método que se realizó correctamente.
  
Si el método que se está llamando no tiene ningún valor devuelto, no es realmente ninguna forma de comprobar el funcionamiento correcto a través de la API administrada de EWS. Siempre y cuando no se produce una excepción, se puede suponer que el método que se realizó correctamente. Para una validación adicional, también puede [comprobar la respuesta SOAP para comprobar los resultados](#bk_verifysoap).
  
### <a name="handling-errors-warnings-and-exceptions"></a>Tratamiento de errores, advertencias y excepciones
<a name="bk_ewsmaerrors"> </a>

Si el código de la API administrada de EWS produce una **excepción**, puede usar el valor [Exception.Message](http://msdn.microsoft.com/EN-US/library/9btwf6wk) para determinar el origen del error. La propiedad **Message** contiene el contenido del elemento [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) en la respuesta SOAP subyacente. Además, si la excepción es del tipo de objeto [ServiceResponseException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) , una de las excepciones más comunes, también puede recuperar el [código de error](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx) incluido en el elemento SOAP [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) subyacente y la [respuesta](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx) propiedad que identifica el objeto [ServiceResponse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) asociado. El código siguiente muestra cómo detectar y mostrar el contenido de una **ServiceResponseException**. 
  
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

Si el método al que llamó devuelve una **ServiceResponseCollection**y el valor de la propiedad **OverallResult** es igual a **Advertencia** o **Error**, tendrá que establecer un bucle por cada objeto en la **ServiceResponseCollection** a Busque el error. La propiedad **OverallResult** se establece en **Advertencia** si al menos una respuesta tiene su valor de **resultado** que se establece como de **Advertencia** y todas las respuestas de otras tienen sus valores de **resultado** sea **correcto**. La propiedad **OverallResult** se establece en **Error** si al menos una respuesta tiene su valor de **resultado** que se establezca en **Error**. Cuando el **OverallResult** se establece en **Advertencia** o **Error**, se establecen las siguientes propiedades en los objetos **ServiceResponse** según corresponda: 
  
- [ErrorCode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) — contiene el código de error, que se puede utilizar para buscar recursos de solución de problemas adicionales. 
    
- [ErrorDetails](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) — contiene detalles sobre el error para algunos **ErrorCodes**. Por ejemplo, cuando el código de error es **ErrorRecurrenceHasNoOccurrence**, el **ErrorDetails** contendrá claves para **EffectiveStartDate** y **EffectiveEndDate**. 
    
- [ErrorMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) : describe el error. 
    
- [ErrorProperties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) : si está disponible, se identifican las propiedades que causó el error. Por ejemplo, cuando el código de error es **ErrorInvalidPropertyForOperation**, **ErrorProperties** contiene la definición de la propiedad que no es válida para la solicitud. 
    
- [Resultado](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx) : Contains **Error** o **Advertencia** cuando se detecta un problema. 
    
Si la información proporcionada por las propiedades **ServiceResponse** no proporciona suficiente información como para corregir la llamada al método o desbloquear, consulte los [pasos siguientes](#bk_nextsteps) para profundizar más información sobre los valores de **código de error** . 
  
## 
<a name="bk_nextsteps"> </a>

Puede buscar información de solución de problemas adicional en los temas siguientes:
  
- Elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) 
    
- [Depuracuión puede contener](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) (enumeración) 
    
- [Errores relacionados con la propiedad EWS](ews-property-related-errors.md)
    
Además, dependiendo de lo que está intentando llevar a cabo en la solicitud, es posible que encontrar información útil adicional sobre el código de error en los temas siguientes:
  
- [Administrar los mensajes de error de detección automática](handling-autodiscover-error-messages.md)
    
- [Tratamiento de errores relacionados con la notificación en EWS en Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Tratamiento de errores relacionados con la sincronización en EWS en Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Tratamiento de errores relacionados con la eliminación de EWS en Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>Ver también


- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Herramientas y recursos para solucionar problemas de aplicaciones de EWS para Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

