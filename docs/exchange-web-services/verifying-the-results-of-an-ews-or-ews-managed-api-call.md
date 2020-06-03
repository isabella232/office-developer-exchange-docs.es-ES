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
# <a name="verifying-the-results-of-an-ews-or-ews-managed-api-call"></a><span data-ttu-id="564c9-103">Comprobación de los resultados de una llamada de API administrada de EWS o EWS</span><span class="sxs-lookup"><span data-stu-id="564c9-103">Verifying the results of an EWS or EWS Managed API call</span></span>

<span data-ttu-id="564c9-104">Obtenga información sobre cómo comprobar los resultados de las llamadas de la API administrada de EWS o EWS.</span><span class="sxs-lookup"><span data-stu-id="564c9-104">Learn how to verify the results of your EWS or EWS Managed API calls.</span></span>
  
<span data-ttu-id="564c9-105">Cuando las cosas no funcionan correctamente, le ayudarán a ver lo que está ocurriendo examinando las solicitudes SOAP que la aplicación envía a través de la red y las respuestas que el servidor envía de vuelta.</span><span class="sxs-lookup"><span data-stu-id="564c9-105">When things aren't working correctly, it helps to see what's going on by examining the SOAP requests that your application is sending over the network and the responses that the server is sending back.</span></span> <span data-ttu-id="564c9-106">El artículo [herramientas y recursos para solucionar problemas de las aplicaciones de EWS](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md) incluye vínculos a herramientas para ayudar a capturar y ver esas solicitudes SOAP.</span><span class="sxs-lookup"><span data-stu-id="564c9-106">The [tools and resources for troubleshooting EWS applications](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md) article includes links to tools to help capture and view those SOAP requests.</span></span> <span data-ttu-id="564c9-107">Una vez que haya recibido las solicitudes y las respuestas, ¿cómo comprobar que la solicitud que envió al servidor se ha procesado correctamente?</span><span class="sxs-lookup"><span data-stu-id="564c9-107">After you've got the requests and the responses, how do you verify that the request you sent to the server was processed correctly?</span></span> <span data-ttu-id="564c9-108">Siga leyendo para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="564c9-108">Read on to find out.</span></span> 
  
<span data-ttu-id="564c9-109">Si va a enviar solicitudes EWS, empezará la comprobación comprobando el atributo **ResponseClass** de cada mensaje de respuesta en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="564c9-109">If you're sending EWS requests, you're going to start your verification by checking the **ResponseClass** attribute for each response message in the response.</span></span> <span data-ttu-id="564c9-110">Esto le indicará si la operación se completó correctamente en cada elemento.</span><span class="sxs-lookup"><span data-stu-id="564c9-110">That will tell you whether the operation completed successfully on each item.</span></span> 
  
<span data-ttu-id="564c9-111">Según el objeto al que llame el método, si está usando la API administrada de EWS para enviar solicitudes, puede realizar alguna comprobación con los objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="564c9-111">Depending on the object that your method is calling, if you're using the EWS Managed API to send requests, you can do some verification using the response objects.</span></span> <span data-ttu-id="564c9-112">Pero debido a que la respuesta SOAP contiene un superconjunto de lo que se incluye en los objetos de respuesta de la API administrada de EWS, es posible que también desee mirar la respuesta SOAP.</span><span class="sxs-lookup"><span data-stu-id="564c9-112">But because the SOAP response contains a superset of what's included in the EWS Managed API response objects, you might want to look at the SOAP response as well.</span></span> <span data-ttu-id="564c9-113">Dado que la respuesta SOAP puede contener a menudo más información que los objetos de respuesta de la API administrada de EWS, inicie la comprobación con la respuesta SOAP.</span><span class="sxs-lookup"><span data-stu-id="564c9-113">Because the SOAP response can often contain more information than the EWS Managed API response objects, start your verification with the SOAP response.</span></span>
  
## <a name="verifying-the-results-of-a-soap-response"></a><span data-ttu-id="564c9-114">Comprobación de los resultados de una respuesta SOAP</span><span class="sxs-lookup"><span data-stu-id="564c9-114">Verifying the results of a SOAP response</span></span>
<span data-ttu-id="564c9-115"><a name="bk_verifysoap"> </a></span><span class="sxs-lookup"><span data-stu-id="564c9-115"><a name="bk_verifysoap"> </a></span></span>

<span data-ttu-id="564c9-116">Cuando recibe una respuesta SOAP, lo primero que debe considerar es el atributo **ResponseClass** .</span><span class="sxs-lookup"><span data-stu-id="564c9-116">When you receive a SOAP response, the first thing to look at is the **ResponseClass** attribute.</span></span> <span data-ttu-id="564c9-117">Este atributo se incluye en cada instancia de **ResponseMessageType** en el elemento [ResponseMessages](https://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx) , como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="564c9-117">This attribute is included in each **ResponseMessageType** instance in the [ResponseMessages](https://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx) element, as shown in the following example.</span></span> 
  
```XML
<s:Body>
      <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
        <m:ResponseMessages>
          <m:GetItemResponseMessage ResponseClass="Success">
          …
```

<span data-ttu-id="564c9-118">Como una respuesta SOAP puede contener varios mensajes de respuesta en una sola respuesta SOAP, es importante comprobar cada mensaje de respuesta de forma individual.</span><span class="sxs-lookup"><span data-stu-id="564c9-118">Because a SOAP response might contain multiple response messages in a single SOAP response, it's important to check each response message individually.</span></span>
  
<span data-ttu-id="564c9-119">Si está trabajando con una operación que incluye un **ResponseClass** como parte de la respuesta de la operación, como la siguiente, es posible que se vea tentado a comprobar solo la **ResponseClass** de la operación.</span><span class="sxs-lookup"><span data-stu-id="564c9-119">If you're working with an operation that includes a **ResponseClass** as part of the operation response, like the following, you might be tempted to only check the **ResponseClass** of the operation.</span></span> 
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  …

```

<span data-ttu-id="564c9-120">Sin embargo, el estado de la operación sólo refleja la forma de la respuesta de nivel superior y no refleja el estado de todas las respuestas de mensaje individuales.</span><span class="sxs-lookup"><span data-stu-id="564c9-120">However, the operation status only reflects the shape of the top-level response and does not reflect the status of all the individual message responses.</span></span> <span data-ttu-id="564c9-121">En el siguiente ejemplo, la operación [AddDelegateResponse](https://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) tiene un **ResponseClass** de **correcto**, pero el elemento [DelegateUserResponseMessageType](https://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx) subyacente tiene un valor **ResponseClass** de **error**.</span><span class="sxs-lookup"><span data-stu-id="564c9-121">In the following example, the [AddDelegateResponse](https://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) operation has a **ResponseClass** of **Success**, but the underlying [DelegateUserResponseMessageType](https://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx) element has a **ResponseClass** value of **Error**.</span></span>
  
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

<span data-ttu-id="564c9-122">Por lo tanto, para las respuestas de EWS SOAP, no puede confiar en la **ResponseClass** de la operación, tiene que mirar el **ResponseClass** de cada mensaje de respuesta para determinar si la operación encontró algún error al procesar los elementos.</span><span class="sxs-lookup"><span data-stu-id="564c9-122">So for SOAP EWS responses, you can't rely on the **ResponseClass** of the operation - you have to look at the **ResponseClass** of each response message to determine whether the operation encountered any errors processing the items.</span></span> 
  
### <a name="verifying-success"></a><span data-ttu-id="564c9-123">Comprobar el éxito</span><span class="sxs-lookup"><span data-stu-id="564c9-123">Verifying success</span></span>

<span data-ttu-id="564c9-124">Si cada atributo **ResponseClass** de cada atributo **ResponseMessage** se establece en **correcto**, la operación se completó correctamente en todos los elementos y puede pasar a la siguiente tarea.</span><span class="sxs-lookup"><span data-stu-id="564c9-124">If each **ResponseClass** attribute for each **ResponseMessage** attribute is set to **Success**, the operation completed successfully on all the items, and you can move on to your next task.</span></span>
  
<span data-ttu-id="564c9-125">En el siguiente ejemplo se muestra una respuesta correcta a una solicitud de [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) Operation para recuperar un único elemento.</span><span class="sxs-lookup"><span data-stu-id="564c9-125">The following example shows a successful response to a [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) operation request to retrieve a single item.</span></span> <span data-ttu-id="564c9-126">Tenga en cuenta que cuando **ResponseClass** se establece en **Success**, el [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) asociado siempre se establece en **NoError**.</span><span class="sxs-lookup"><span data-stu-id="564c9-126">Note that when the **ResponseClass** is set to **Success**, the associated [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) is always set to **NoError**.</span></span>
  
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

<span data-ttu-id="564c9-127">La siguiente es una respuesta correcta a una solicitud de operación de **GetItem** para recuperar varios elementos.</span><span class="sxs-lookup"><span data-stu-id="564c9-127">The following is a successful response to a **GetItem** operation request to retrieve multiple items.</span></span> <span data-ttu-id="564c9-128">Cada uno de los elementos [GetItemResponseMessage](https://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx) tiene un **ResponseClass** de **operación correcta**.</span><span class="sxs-lookup"><span data-stu-id="564c9-128">Each of the [GetItemResponseMessage](https://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx) elements has a **ResponseClass** of **Success**.</span></span>
  
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

### <a name="handling-errors-and-warnings"></a><span data-ttu-id="564c9-129">Control de errores y advertencias</span><span class="sxs-lookup"><span data-stu-id="564c9-129">Handling errors and warnings</span></span>

<span data-ttu-id="564c9-130">Cuando recibe una respuesta y el atributo **ResponseClass** se establece en **error**, la operación no se completó correctamente en uno o varios elementos.</span><span class="sxs-lookup"><span data-stu-id="564c9-130">When you receive a response and the **ResponseClass** attribute is set to **Error**, the operation did not complete successfully on one or more items.</span></span> <span data-ttu-id="564c9-131">Corrija el problema y vuelva a intentar la solicitud, o la parte de su solicitud que ha fallado.</span><span class="sxs-lookup"><span data-stu-id="564c9-131">Correct the issue and retry your request, or the part of your request that failed.</span></span> <span data-ttu-id="564c9-132">Un valor de atributo **ResponseClass** de valor de **ADVERTENCIA** solo lo devuelve la operación [ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) e indica que la entidad no se pudo resolver como una identidad única.</span><span class="sxs-lookup"><span data-stu-id="564c9-132">A **ResponseClass** attribute value of **Warning** value is only returned by the [ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) operation, and indicates that the entity could not be resolved to a unique identity.</span></span> <span data-ttu-id="564c9-133">Puede ignorarlo para todas las demás operaciones.</span><span class="sxs-lookup"><span data-stu-id="564c9-133">You can ignore it for all other operations.</span></span> 
  
<span data-ttu-id="564c9-134">En la siguiente respuesta, el atributo **ResponseClass** tiene un valor de **error**.</span><span class="sxs-lookup"><span data-stu-id="564c9-134">In the following response, the **ResponseClass** attribute has a value of **Error**.</span></span>
  
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

<span data-ttu-id="564c9-135">En este ejemplo, EWS proporciona pistas para depurar el problema.</span><span class="sxs-lookup"><span data-stu-id="564c9-135">In this example, EWS provides clues to debug the issue.</span></span> <span data-ttu-id="564c9-136">Cuando el atributo **ResponseClass** tiene un valor de **error**, se incluyen los siguientes elementos adicionales en la respuesta cuando corresponda:</span><span class="sxs-lookup"><span data-stu-id="564c9-136">When the **ResponseClass** attribute has a value of **Error**, the following additional elements are included in the response when applicable:</span></span>
  
- <span data-ttu-id="564c9-137">[MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) : describe el error.</span><span class="sxs-lookup"><span data-stu-id="564c9-137">[MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) — Describes the error.</span></span> 
    
- <span data-ttu-id="564c9-138">[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) : contiene el código de error, que se puede usar para buscar recursos de solución de problemas adicionales.</span><span class="sxs-lookup"><span data-stu-id="564c9-138">[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) — Contains the error code, which can be used to find additional troubleshooting resources.</span></span> 
    
- <span data-ttu-id="564c9-139">[MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) : identifica los elementos que causaron el error.</span><span class="sxs-lookup"><span data-stu-id="564c9-139">[MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) — Identifies the elements that caused the error.</span></span> 
    
- <span data-ttu-id="564c9-140">[DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) : no se usa.</span><span class="sxs-lookup"><span data-stu-id="564c9-140">[DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) — Unused.</span></span> 
    
<span data-ttu-id="564c9-141">Puede usar la información proporcionada en estos elementos para investigar el problema.</span><span class="sxs-lookup"><span data-stu-id="564c9-141">You can use the information provided in these elements to investigate your issue.</span></span> <span data-ttu-id="564c9-142">En el ejemplo anterior, el **MessageText** indica que la propiedad no es válida para el tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="564c9-142">In the previous example, the **MessageText** indicates that the property isn't valid for the object type.</span></span> <span data-ttu-id="564c9-143">La solicitud era obtener un mensaje de correo electrónico, pero el conjunto de propiedades incluyó la **AssociatedCalendarItemId**, que solo es válida para los elementos de cita.</span><span class="sxs-lookup"><span data-stu-id="564c9-143">The request was to get an email message, but the property set included the **AssociatedCalendarItemId**, which is only valid for appointment items.</span></span>
  
<span data-ttu-id="564c9-144">En el ejemplo siguiente se muestra un error que se recibió como parte de una operación por lotes para obtener varios elementos de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="564c9-144">The following example shows an error that was received as part of a batched operation to get multiple email items.</span></span> <span data-ttu-id="564c9-145">El primer elemento se recuperó correctamente y **ResponseClass** se establece en **Success**.</span><span class="sxs-lookup"><span data-stu-id="564c9-145">The first item was retrieved successfully and the **ResponseClass** is set to **Success**.</span></span> <span data-ttu-id="564c9-146">No se encontró el segundo elemento y **ResponseClass** se ha establecido en **error**.</span><span class="sxs-lookup"><span data-stu-id="564c9-146">The second item could not be found, and the **ResponseClass** is set to **Error**.</span></span>
  
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

<span data-ttu-id="564c9-147">Cuando uno o varios elementos de una solicitud por lotes no se pueden procesar como se solicitan, se devuelve un error para cada elemento que ha fallado y el resto de los elementos del lote se procesan como se esperaba.</span><span class="sxs-lookup"><span data-stu-id="564c9-147">When one or more items in a batched request can't be processed as requested, an error is returned for each item that failed, and the rest of the items in the batch are processed as expected.</span></span> <span data-ttu-id="564c9-148">Los errores en el procesamiento por lotes pueden producirse si el elemento se eliminó y, por lo tanto, no se puede enviar, recuperar o actualizar, o si el elemento se movió a una carpeta diferente y, por lo tanto, tiene un identificador de elemento nuevo.</span><span class="sxs-lookup"><span data-stu-id="564c9-148">Failures in batch processing can occur if the item was deleted, and therefore can't be sent, retrieved, or updated, or if the item moved to a different folder, and therefore has a new item ID.</span></span> <span data-ttu-id="564c9-149">Como la operación se completará para algunos elementos y no devolverá un error cuando no se puedan procesar uno o varios elementos, es importante comprobar cada atributo **ResponseClass** antes de pasar a la siguiente operación.</span><span class="sxs-lookup"><span data-stu-id="564c9-149">Because the operation will complete for some items and not return an error when one or more items can't be processed, it's important to check each **ResponseClass** attribute before you move on to your next operation.</span></span> 
  
<span data-ttu-id="564c9-150">Si la información proporcionada por los elementos Response no le ayuda a corregir la solicitud o desbloquearlo de algún otro modo, vea [los siguientes pasos](#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="564c9-150">If the information provided by the response elements doesn't help you correct your request or otherwise unblock you, see [Next steps](#bk_nextsteps).</span></span>
  
## <a name="verifying-the-results-of-an-ews-managed-api-method-call"></a><span data-ttu-id="564c9-151">Comprobación de los resultados de una llamada de método de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="564c9-151">Verifying the results of an EWS Managed API method call</span></span>
<span data-ttu-id="564c9-152"><a name="bk_successful"> </a></span><span class="sxs-lookup"><span data-stu-id="564c9-152"><a name="bk_successful"> </a></span></span>

<span data-ttu-id="564c9-153">Si usa la API administrada de EWS y llama a un método en un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) , es probable que el método devuelva un objeto [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) , que contiene una colección de objetos [ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) o una colección de objetos derivados de los objetos **ServiceResponse** .</span><span class="sxs-lookup"><span data-stu-id="564c9-153">If you're using the EWS Managed API and calling a method on an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, your method will likely return a [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) object, which contains a collection of [ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) objects, or a collection of objects derived from the **ServiceResponse** objects.</span></span> <span data-ttu-id="564c9-154">Los objetos **ServiceResponseCollection** e incluidos **ServiceResponse** contienen información sobre el resultado de la llamada al método, que puede usar para comprobar los resultados.</span><span class="sxs-lookup"><span data-stu-id="564c9-154">The **ServiceResponseCollection** and included **ServiceResponse** objects contain information about the result of the method call, which you can use to verify your results.</span></span> 
  
<span data-ttu-id="564c9-155">Si está usando la API administrada de EWS y llama a un método en un objeto de [elemento](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) o uno de los objetos derivados, es probable que el método no devuelva un objeto de respuesta para comprobar si el resultado es correcto, pero produce una [excepción](https://msdn.microsoft.com/library/c18k6c59) si el método no se completa correctamente.</span><span class="sxs-lookup"><span data-stu-id="564c9-155">If you're using the EWS Managed API and calling a method on an [Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) object, or one of the derived objects, the method likely does not return a response object to check for success, but does throw an [Exception](https://msdn.microsoft.com/library/c18k6c59) if the method does not complete successfully.</span></span> 
  
### <a name="verifying-success"></a><span data-ttu-id="564c9-156">Comprobar el éxito</span><span class="sxs-lookup"><span data-stu-id="564c9-156">Verifying success</span></span>

<span data-ttu-id="564c9-157">Una de las ventajas de usar la API administrada de EWS es que proporciona un estado general al tratar con varios elementos en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="564c9-157">One benefit of using the EWS Managed API is that it provides an overall status when dealing with multiple items in one response.</span></span> <span data-ttu-id="564c9-158">Por lo tanto, si el método al que llama devuelve **ServiceResponseCollection**, puede comprobar que la propiedad [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) de **ServiceResponseCollection** es igual a [ServiceResult. Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="564c9-158">So if the method you called returns a **ServiceResponseCollection**, you can check that the [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) property of the **ServiceResponseCollection** is equal to [ServiceResult.Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="564c9-159">Si es así, todos los elementos del proceso por lotes se completaron correctamente; no es necesario comprobar cada objeto **ServiceResponse** de forma individual.</span><span class="sxs-lookup"><span data-stu-id="564c9-159">If so, all the items in the batched process were completed successfully; you don't have to check each **ServiceResponse** object individually.</span></span> <span data-ttu-id="564c9-160">Si la propiedad **OverallResult** no está establecida en **ServiceResult. Success**, debe [controlar el error o la advertencia](#bk_ewsmaerrors).</span><span class="sxs-lookup"><span data-stu-id="564c9-160">If the **OverallResult** property is not set to **ServiceResult.Success**, you have to [handle the error or warning](#bk_ewsmaerrors).</span></span>
  
<span data-ttu-id="564c9-161">Si el método que está llamando no devuelve una **ServiceResponseCollection**, pero devuelve un objeto **ServiceResponse** , tiene que comprobar el valor de la propiedad **result** .</span><span class="sxs-lookup"><span data-stu-id="564c9-161">If the method you're calling does not return a **ServiceResponseCollection**, but does return a **ServiceResponse** object, you have to check the value of the **Result** property.</span></span> <span data-ttu-id="564c9-162">Si el valor del **resultado** se establece en **correcto**, sabrá que el método se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="564c9-162">If the **Result** value is set to **Success**, you know the method completed successfully.</span></span>
  
<span data-ttu-id="564c9-163">Si el método al que llama no tiene ningún valor devuelto, no hay ninguna forma de comprobar el éxito mediante la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="564c9-163">If the method you're calling has no return value, there's really no way to check for success via the EWS Managed API.</span></span> <span data-ttu-id="564c9-164">Siempre que no se produzca una excepción, puede suponer que el método se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="564c9-164">As long as an exception is not thrown, you can assume the method completed successfully.</span></span> <span data-ttu-id="564c9-165">Para obtener más validación, también puede [comprobar la respuesta SOAP para comprobar los resultados](#bk_verifysoap).</span><span class="sxs-lookup"><span data-stu-id="564c9-165">For additional validation, you can also [check the SOAP response to verify the results](#bk_verifysoap).</span></span>
  
### <a name="handling-errors-warnings-and-exceptions"></a><span data-ttu-id="564c9-166">Control de errores, advertencias y excepciones</span><span class="sxs-lookup"><span data-stu-id="564c9-166">Handling errors, warnings, and exceptions</span></span>
<span data-ttu-id="564c9-167"><a name="bk_ewsmaerrors"> </a></span><span class="sxs-lookup"><span data-stu-id="564c9-167"><a name="bk_ewsmaerrors"> </a></span></span>

<span data-ttu-id="564c9-168">Si el código de la API administrada de EWS produce una **excepción**, puede usar el valor [Exception. Message](https://msdn.microsoft.com/library/9btwf6wk) para determinar el origen del error.</span><span class="sxs-lookup"><span data-stu-id="564c9-168">If your EWS Managed API code throws an **Exception**, you can use the [Exception.Message](https://msdn.microsoft.com/library/9btwf6wk) value to determine the source of the error.</span></span> <span data-ttu-id="564c9-169">La propiedad **Message** contiene el contenido del elemento [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) en la respuesta SOAP subyacente.</span><span class="sxs-lookup"><span data-stu-id="564c9-169">The **Message** property contains the contents of the [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) element in the underlying SOAP response.</span></span> <span data-ttu-id="564c9-170">Además, si la excepción es del tipo [ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) Object, una de las excepciones más comunes, también puede recuperar el [ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx) que se incluye en el elemento de [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) SOAP subyacente, y la propiedad [Response](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx) que identifica el objeto [ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) asociado.</span><span class="sxs-lookup"><span data-stu-id="564c9-170">In addition, if the exception is of type [ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) object, one of the most common exceptions, you can also retrieve the [ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx) contained in the underlying SOAP [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element, and the [Response](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx) property that identifies the associated [ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) object.</span></span> <span data-ttu-id="564c9-171">El siguiente código muestra cómo detectar y mostrar el contenido de un **ServiceResponseException**.</span><span class="sxs-lookup"><span data-stu-id="564c9-171">The following code shows how to catch and display the contents of a **ServiceResponseException**.</span></span> 
  
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

<span data-ttu-id="564c9-172">Si el método al que ha llamado devuelve una **ServiceResponseCollection**y el valor de la propiedad **OverallResult** es igual a **Warning** o **error**, tendrá que recorrer todos los objetos de la **ServiceResponseCollection** para encontrar el error.</span><span class="sxs-lookup"><span data-stu-id="564c9-172">If the method you called returns a **ServiceResponseCollection**, and the value of the **OverallResult** property is equal to **Warning** or **Error**, you'll have to loop through each object in the **ServiceResponseCollection** to find the error.</span></span> <span data-ttu-id="564c9-173">La propiedad **OverallResult** se establece en **Warning** si al menos una respuesta tiene el valor de **resultado** establecido en **Warning** y el resto de las respuestas tienen los valores de **resultado** establecidos en **correcto**.</span><span class="sxs-lookup"><span data-stu-id="564c9-173">The **OverallResult** property is set to **Warning** if at least one response has its **Result** value set to **Warning** and all other responses have their **Result** values set to **Success**.</span></span> <span data-ttu-id="564c9-174">La propiedad **OverallResult** se establece en **error** si al menos una respuesta tiene el valor de **resultado** establecido en **error**.</span><span class="sxs-lookup"><span data-stu-id="564c9-174">The **OverallResult** property is set to **Error** if at least one response has its **Result** value set to **Error**.</span></span> <span data-ttu-id="564c9-175">Cuando **OverallResult** se establece en **Warning** o **error**, se establecen las siguientes propiedades en los objetos **ServiceResponse** según corresponda:</span><span class="sxs-lookup"><span data-stu-id="564c9-175">When the **OverallResult** is set to **Warning** or **Error**, the following properties are set on the **ServiceResponse** objects as appropriate:</span></span> 
  
- <span data-ttu-id="564c9-176">[ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) : contiene el código de error, que se puede usar para buscar recursos de solución de problemas adicionales.</span><span class="sxs-lookup"><span data-stu-id="564c9-176">[ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) — Contains the error code, which can be used to find additional troubleshooting resources.</span></span> 
    
- <span data-ttu-id="564c9-177">[ErrorDetails](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) : contiene detalles sobre el error de algunos **ErrorCodes**.</span><span class="sxs-lookup"><span data-stu-id="564c9-177">[ErrorDetails](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) — Contains details about the error for some **ErrorCodes**.</span></span> <span data-ttu-id="564c9-178">Por ejemplo, cuando el código de error es **ErrorRecurrenceHasNoOccurrence**, **ErrorDetails** contendrá claves para **EffectiveStartDate** y **EffectiveEndDate**.</span><span class="sxs-lookup"><span data-stu-id="564c9-178">For example, when the error code is **ErrorRecurrenceHasNoOccurrence**, the **ErrorDetails** will contain keys for **EffectiveStartDate** and **EffectiveEndDate**.</span></span> 
    
- <span data-ttu-id="564c9-179">[ErrorMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) : describe el error.</span><span class="sxs-lookup"><span data-stu-id="564c9-179">[ErrorMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) — Describes the error.</span></span> 
    
- <span data-ttu-id="564c9-180">[ErrorProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) : Si está disponible, identifica las propiedades que causaron el error.</span><span class="sxs-lookup"><span data-stu-id="564c9-180">[ErrorProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) — If available, identifies the properties that caused the error.</span></span> <span data-ttu-id="564c9-181">Por ejemplo, cuando el código de error es **ErrorInvalidPropertyForOperation**, **ErrorProperties** contiene la definición de la propiedad que no era válida para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="564c9-181">For example, when the error code is **ErrorInvalidPropertyForOperation**, **ErrorProperties** contains the definition of the property that was invalid for the request.</span></span> 
    
- <span data-ttu-id="564c9-182">[Result](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx) : contiene un **error** o una **ADVERTENCIA** cuando se encuentra un problema.</span><span class="sxs-lookup"><span data-stu-id="564c9-182">[Result](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx) — Contains **Error** or **Warning** when an issue is encountered.</span></span> 
    
<span data-ttu-id="564c9-183">Si la información proporcionada por las propiedades **ServiceResponse** no proporciona suficiente información para corregir la llamada al método o desbloquear por usted, consulte [los pasos siguientes](#bk_nextsteps) para obtener más información sobre los valores de **ErrorCode** .</span><span class="sxs-lookup"><span data-stu-id="564c9-183">If the information provided by the **ServiceResponse** properties doesn't provide enough information to correct your method call or unblock you, see [Next steps](#bk_nextsteps) to dig up more information on **ErrorCode** values.</span></span> 
  
## 
<span data-ttu-id="564c9-184"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="564c9-184"><a name="bk_nextsteps"> </a></span></span>

<span data-ttu-id="564c9-185">Puede buscar información adicional de solución de problemas en los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="564c9-185">You can look up additional troubleshooting information in the following topics:</span></span>
  
- <span data-ttu-id="564c9-186">Elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="564c9-186">[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element</span></span> 
    
- <span data-ttu-id="564c9-187">Enumeración [ServiceError](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="564c9-187">[ServiceError](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) enumeration</span></span> 
    
- [<span data-ttu-id="564c9-188">Errores relacionados con la propiedad EWS</span><span class="sxs-lookup"><span data-stu-id="564c9-188">EWS property-related errors</span></span>](ews-property-related-errors.md)
    
<span data-ttu-id="564c9-189">Además, en función de lo que intente realizar en su solicitud, puede encontrar información adicional sobre el código de error en los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="564c9-189">In addition, depending on what you're trying to accomplish in your request, you might find additional helpful information about the error code in the following topics:</span></span>
  
- [<span data-ttu-id="564c9-190">Administrar los mensajes de error de detección automática</span><span class="sxs-lookup"><span data-stu-id="564c9-190">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    
- [<span data-ttu-id="564c9-191">Control de errores relacionados con la notificación en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="564c9-191">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="564c9-192">Controlar errores relacionados con la sincronización en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="564c9-192">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="564c9-193">Administración de errores relacionados con la eliminación en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="564c9-193">Handling deletion-related errors in EWS in Exchange</span></span>](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="564c9-194">Vea también</span><span class="sxs-lookup"><span data-stu-id="564c9-194">See also</span></span>


- [<span data-ttu-id="564c9-195">Desarrollar clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="564c9-195">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="564c9-196">Herramientas y recursos para solucionar problemas de las aplicaciones de EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="564c9-196">Tools and resources for troubleshooting EWS applications for Exchange</span></span>](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

