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
# <a name="verifying-the-results-of-an-ews-or-ews-managed-api-call"></a><span data-ttu-id="1a9cf-103">Comprobación de los resultados de una llamada de EWS o la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="1a9cf-103">Verifying the results of an EWS or EWS Managed API call</span></span>

<span data-ttu-id="1a9cf-104">Obtenga información sobre cómo comprobar los resultados de las llamadas de EWS o la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-104">Learn how to verify the results of your EWS or EWS Managed API calls.</span></span>
  
<span data-ttu-id="1a9cf-105">Cuando las cosas no funcionan correctamente, es muy útil para ver lo que está ocurriendo mediante el examen de las solicitudes SOAP que su aplicación se envíe a través de la red y las respuestas que el servidor envía de vuelta.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-105">When things aren't working correctly, it helps to see what's going on by examining the SOAP requests that your application is sending over the network and the responses that the server is sending back.</span></span> <span data-ttu-id="1a9cf-106">El artículo de [Herramientas y recursos para solucionar problemas de aplicaciones de EWS](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md) incluye vínculos a herramientas que ayudan a capturar y ver las solicitudes SOAP.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-106">The [tools and resources for troubleshooting EWS applications](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md) article includes links to tools to help capture and view those SOAP requests.</span></span> <span data-ttu-id="1a9cf-107">¿Una vez que dispone de las solicitudes y las respuestas, cómo comprobar que la solicitud que envía al servidor se procesó correctamente?</span><span class="sxs-lookup"><span data-stu-id="1a9cf-107">After you've got the requests and the responses, how do you verify that the request you sent to the server was processed correctly?</span></span> <span data-ttu-id="1a9cf-108">Siga leyendo para averiguar.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-108">Read on to find out.</span></span> 
  
<span data-ttu-id="1a9cf-109">Si va a enviar solicitudes EWS, va a iniciar la comprobación comprobando el atributo **ResponseClass** para cada mensaje de respuesta en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-109">If you're sending EWS requests, you're going to start your verification by checking the **ResponseClass** attribute for each response message in the response.</span></span> <span data-ttu-id="1a9cf-110">Que le indicará si la operación se completó correctamente en cada elemento.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-110">That will tell you whether the operation completed successfully on each item.</span></span> 
  
<span data-ttu-id="1a9cf-111">Dependiendo del objeto que el método está llamando a, si se usa la API administrada de EWS para enviar solicitudes, puede hacer algunos comprobación mediante los objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-111">Depending on the object that your method is calling, if you're using the EWS Managed API to send requests, you can do some verification using the response objects.</span></span> <span data-ttu-id="1a9cf-112">Pero, debido a que la respuesta SOAP contiene un superconjunto de qué se incluye en los objetos de respuesta de la API administrada de EWS, es posible que desee estudiar así como la respuesta SOAP.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-112">But because the SOAP response contains a superset of what's included in the EWS Managed API response objects, you might want to look at the SOAP response as well.</span></span> <span data-ttu-id="1a9cf-113">Debido a que la respuesta SOAP a menudo puede contener más información que los objetos de respuesta de la API administrada de EWS, inicie la comprobación con la respuesta SOAP.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-113">Because the SOAP response can often contain more information than the EWS Managed API response objects, start your verification with the SOAP response.</span></span>
  
## <a name="verifying-the-results-of-a-soap-response"></a><span data-ttu-id="1a9cf-114">Comprobación de los resultados de una respuesta SOAP</span><span class="sxs-lookup"><span data-stu-id="1a9cf-114">Verifying the results of a SOAP response</span></span>
<span data-ttu-id="1a9cf-115"><a name="bk_verifysoap"> </a></span><span class="sxs-lookup"><span data-stu-id="1a9cf-115"></span></span>

<span data-ttu-id="1a9cf-116">Cuando recibe una respuesta SOAP, lo primero que debe mirar es el atributo **ResponseClass** .</span><span class="sxs-lookup"><span data-stu-id="1a9cf-116">When you receive a SOAP response, the first thing to look at is the **ResponseClass** attribute.</span></span> <span data-ttu-id="1a9cf-117">Este atributo se incluye en cada instancia de **ResponseMessageType** en el elemento [ResponseMessages](http://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx) , tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-117">This attribute is included in each **ResponseMessageType** instance in the [ResponseMessages](http://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx) element, as shown in the following example.</span></span> 
  
```XML
<s:Body>
      <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <m:ResponseMessages>
          <m:GetItemResponseMessage ResponseClass="Success">
          …
```

<span data-ttu-id="1a9cf-118">Debido a que una respuesta SOAP puede contener varios mensajes de respuesta en una sola respuesta SOAP, es importante comprobar individualmente cada mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-118">Because a SOAP response might contain multiple response messages in a single SOAP response, it's important to check each response message individually.</span></span>
  
<span data-ttu-id="1a9cf-119">Si está trabajando con una operación que incluye un **ResponseClass** como parte de la respuesta de la operación, como la siguiente, es posible que vean tentados a comprobar sólo el **ResponseClass** de la operación.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-119">If you're working with an operation that includes a **ResponseClass** as part of the operation response, like the following, you might be tempted to only check the **ResponseClass** of the operation.</span></span> 
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  …

```

<span data-ttu-id="1a9cf-120">Sin embargo, el estado de la operación sólo refleja la forma de la respuesta de nivel superior y no refleja el estado de todas las respuestas de mensajes individuales.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-120">However, the operation status only reflects the shape of the top-level response and does not reflect the status of all the individual message responses.</span></span> <span data-ttu-id="1a9cf-121">En el ejemplo siguiente, la operación de [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) tiene un **ResponseClass** de **éxito**, pero el elemento [DelegateUserResponseMessageType](http://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx) subyacente tiene un valor de **ResponseClass** de **Error**.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-121">In the following example, the [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) operation has a **ResponseClass** of **Success**, but the underlying [DelegateUserResponseMessageType](http://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx) element has a **ResponseClass** value of **Error**.</span></span>
  
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

<span data-ttu-id="1a9cf-122">Por lo tanto para las respuestas SOAP EWS, no puede confiar en la **ResponseClass** de la operación: tiene que examine el **ResponseClass** de cada mensaje de respuesta para determinar si la operación ha encontrado los errores de procesamiento de los elementos.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-122">So for SOAP EWS responses, you can't rely on the **ResponseClass** of the operation - you have to look at the **ResponseClass** of each response message to determine whether the operation encountered any errors processing the items.</span></span> 
  
### <a name="verifying-success"></a><span data-ttu-id="1a9cf-123">Comprobación de éxito</span><span class="sxs-lookup"><span data-stu-id="1a9cf-123">Verifying success</span></span>

<span data-ttu-id="1a9cf-124">Si cada atributo **ResponseClass** para cada atributo **ResponseMessage** se establece en **correcto**, la operación ha finalizado correctamente en todos los elementos, y puede pasar a la siguiente tarea.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-124">If each **ResponseClass** attribute for each **ResponseMessage** attribute is set to **Success**, the operation completed successfully on all the items, and you can move on to your next task.</span></span>
  
<span data-ttu-id="1a9cf-125">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) para recuperar un único elemento.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-125">The following example shows a successful response to a [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) operation request to retrieve a single item.</span></span> <span data-ttu-id="1a9cf-126">Tenga en cuenta que cuando se establece la **ResponseClass** para el **éxito**, el asociado [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) siempre se establece en **NoError**.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-126">Note that when the **ResponseClass** is set to **Success**, the associated [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) is always set to **NoError**.</span></span>
  
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

<span data-ttu-id="1a9cf-127">La siguiente es una respuesta correcta a una solicitud de operación **GetItem** para recuperar varios elementos.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-127">The following is a successful response to a **GetItem** operation request to retrieve multiple items.</span></span> <span data-ttu-id="1a9cf-128">Cada uno de los elementos de [GetItemResponseMessage](http://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx) tiene un **ResponseClass** de **éxito**.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-128">Each of the [GetItemResponseMessage](http://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx) elements has a **ResponseClass** of **Success**.</span></span>
  
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

### <a name="handling-errors-and-warnings"></a><span data-ttu-id="1a9cf-129">Controlar errores y advertencias</span><span class="sxs-lookup"><span data-stu-id="1a9cf-129">Handling errors and warnings</span></span>

<span data-ttu-id="1a9cf-130">Cuando recibe una respuesta y el atributo **ResponseClass** se establece en **Error**, la operación no se completó correctamente en uno o varios elementos.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-130">When you receive a response and the **ResponseClass** attribute is set to **Error**, the operation did not complete successfully on one or more items.</span></span> <span data-ttu-id="1a9cf-131">Corrija el problema y vuelva a intentar la solicitud o la parte de la solicitud que ha fallado.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-131">Correct the issue and retry your request, or the part of your request that failed.</span></span> <span data-ttu-id="1a9cf-132">Un valor del atributo **ResponseClass** del valor de **Advertencia** sólo es devuelto por la operación [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) e indica que la entidad no se pudo resolver a una identidad única.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-132">A **ResponseClass** attribute value of **Warning** value is only returned by the [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) operation, and indicates that the entity could not be resolved to a unique identity.</span></span> <span data-ttu-id="1a9cf-133">Se puede omitir para todas las demás operaciones.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-133">You can ignore it for all other operations.</span></span> 
  
<span data-ttu-id="1a9cf-134">En la siguiente respuesta, el atributo **ResponseClass** tiene un valor de **Error**.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-134">In the following response, the **ResponseClass** attribute has a value of **Error**.</span></span>
  
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

<span data-ttu-id="1a9cf-135">En este ejemplo, EWS proporciona pistas para depurar el problema.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-135">In this example, EWS provides clues to debug the issue.</span></span> <span data-ttu-id="1a9cf-136">Cuando el atributo **ResponseClass** tiene un valor de **Error**, se incluyen los siguientes elementos adicionales en la respuesta cuando sea aplicable:</span><span class="sxs-lookup"><span data-stu-id="1a9cf-136">When the **ResponseClass** attribute has a value of **Error**, the following additional elements are included in the response when applicable:</span></span>
  
- <span data-ttu-id="1a9cf-137">[MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) : describe el error.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-137">[MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) — Describes the error.</span></span> 
    
- <span data-ttu-id="1a9cf-138">[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) — contiene el código de error, que se puede utilizar para buscar recursos de solución de problemas adicionales.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-138">[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) — Contains the error code, which can be used to find additional troubleshooting resources.</span></span> 
    
- <span data-ttu-id="1a9cf-139">[MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) : identifica los elementos que causó el error.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-139">[MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) — Identifies the elements that caused the error.</span></span> 
    
- <span data-ttu-id="1a9cf-140">[DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) — no usados.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-140">[DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) — Unused.</span></span> 
    
<span data-ttu-id="1a9cf-141">Puede usar la información proporcionada en estos elementos para investigar el problema.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-141">You can use the information provided in these elements to investigate your issue.</span></span> <span data-ttu-id="1a9cf-142">En el ejemplo anterior, la **MessageText** indica que la propiedad no es válida para el tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-142">In the previous example, the **MessageText** indicates that the property isn't valid for the object type.</span></span> <span data-ttu-id="1a9cf-143">La solicitud era obtener un mensaje de correo electrónico, pero el conjunto de propiedades incluye la **AssociatedCalendarItemId**, que sólo es válido para elementos de cita.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-143">The request was to get an email message, but the property set included the **AssociatedCalendarItemId**, which is only valid for appointment items.</span></span>
  
<span data-ttu-id="1a9cf-144">En el ejemplo siguiente se muestra un error que se ha recibido como parte de una operación por lotes para obtener varios elementos de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-144">The following example shows an error that was received as part of a batched operation to get multiple email items.</span></span> <span data-ttu-id="1a9cf-145">El primer elemento se recuperó correctamente y se establece la **ResponseClass** para el **éxito**.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-145">The first item was retrieved successfully and the **ResponseClass** is set to **Success**.</span></span> <span data-ttu-id="1a9cf-146">No se pudo encontrar el segundo elemento, y el **ResponseClass** se establece en **Error**.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-146">The second item could not be found, and the **ResponseClass** is set to **Error**.</span></span>
  
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

<span data-ttu-id="1a9cf-147">Cuando no se puede procesar uno o varios elementos en una solicitud por lotes como se ha solicitado, se devuelve un error para cada elemento que no se pudo, y el resto de los elementos en el lote se procesan según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-147">When one or more items in a batched request can't be processed as requested, an error is returned for each item that failed, and the rest of the items in the batch are processed as expected.</span></span> <span data-ttu-id="1a9cf-148">Pueden producirse errores en el procesamiento por lotes si el elemento se ha eliminado y por lo tanto, no se envía, recuperar o actualizado, o si el elemento se mueve a una carpeta diferente y, por lo tanto, tiene un nuevo identificador de elemento.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-148">Failures in batch processing can occur if the item was deleted, and therefore can't be sent, retrieved, or updated, or if the item moved to a different folder, and therefore has a new item ID.</span></span> <span data-ttu-id="1a9cf-149">Debido a que la operación se complete para algunos de los elementos y no devuelve un error cuando no se puede procesar uno o varios elementos, es importante comprobar cada atributo **ResponseClass** antes de pasar a la siguiente operación.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-149">Because the operation will complete for some items and not return an error when one or more items can't be processed, it's important to check each **ResponseClass** attribute before you move on to your next operation.</span></span> 
  
<span data-ttu-id="1a9cf-150">Si la información proporcionada por los elementos de respuesta no ayuda a corregir su solicitud o desbloquear en caso contrario,, vea los [pasos siguientes](#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="1a9cf-150">If the information provided by the response elements doesn't help you correct your request or otherwise unblock you, see [Next steps](#bk_nextsteps).</span></span>
  
## <a name="verifying-the-results-of-an-ews-managed-api-method-call"></a><span data-ttu-id="1a9cf-151">Comprobación de los resultados de una llamada de API administrada de EWS (método)</span><span class="sxs-lookup"><span data-stu-id="1a9cf-151">Verifying the results of an EWS Managed API method call</span></span>
<span data-ttu-id="1a9cf-152"><a name="bk_successful"> </a></span><span class="sxs-lookup"><span data-stu-id="1a9cf-152"></span></span>

<span data-ttu-id="1a9cf-153">Si está usando la API administrada de EWS y llamar a un método en un objeto [ExchangeService](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) , el método devolverá es probable que un objeto [ServiceResponseCollection](http://msdn.microsoft.com/EN-US/library/dd633715%28v=exchg.80%29.aspx) , que contiene una colección de objetos de [ServiceResponse](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) o una colección de objetos derivados de los objetos **ServiceResponse** .</span><span class="sxs-lookup"><span data-stu-id="1a9cf-153">If you're using the EWS Managed API and calling a method on an [ExchangeService](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, your method will likely return a [ServiceResponseCollection](http://msdn.microsoft.com/EN-US/library/dd633715%28v=exchg.80%29.aspx) object, which contains a collection of [ServiceResponse](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) objects, or a collection of objects derived from the **ServiceResponse** objects.</span></span> <span data-ttu-id="1a9cf-154">El **ServiceResponseCollection** y objetos **ServiceResponse** incluidos contienen información sobre el resultado de la llamada al método, que puede utilizar para comprobar los resultados.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-154">The **ServiceResponseCollection** and included **ServiceResponse** objects contain information about the result of the method call, which you can use to verify your results.</span></span> 
  
<span data-ttu-id="1a9cf-155">Si está usando la API administrada de EWS y llamar a un método en un objeto de [elemento](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) , o en uno de los objetos derivados, el método es probable que no devuelve un objeto de respuesta para comprobar el funcionamiento correcto, pero produce una [excepción](http://msdn.microsoft.com/EN-US/library/c18k6c59) si no se completa el método correctamente.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-155">If you're using the EWS Managed API and calling a method on an [Item](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) object, or one of the derived objects, the method likely does not return a response object to check for success, but does throw an [Exception](http://msdn.microsoft.com/EN-US/library/c18k6c59) if the method does not complete successfully.</span></span> 
  
### <a name="verifying-success"></a><span data-ttu-id="1a9cf-156">Comprobación de éxito</span><span class="sxs-lookup"><span data-stu-id="1a9cf-156">Verifying success</span></span>

<span data-ttu-id="1a9cf-157">Una ventaja de utilizar la API administrada de EWS es que proporciona un estado global cuando trabaja con varios elementos en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-157">One benefit of using the EWS Managed API is that it provides an overall status when dealing with multiple items in one response.</span></span> <span data-ttu-id="1a9cf-158">Por lo tanto, si el método al que llamó devuelve una **ServiceResponseCollection**, puede comprobar que la propiedad [OverallResult](http://msdn.microsoft.com/en-us/library/dd634515%28v=exchg.80%29.aspx) de la **ServiceResponseCollection** es igual a [ServiceResult.Success](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1a9cf-158">So if the method you called returns a **ServiceResponseCollection**, you can check that the [OverallResult](http://msdn.microsoft.com/en-us/library/dd634515%28v=exchg.80%29.aspx) property of the **ServiceResponseCollection** is equal to [ServiceResult.Success](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="1a9cf-159">Si es así, todos los elementos en el proceso por lotes se han completado correctamente; no es necesario que comprobar individualmente cada objeto **ServiceResponse** .</span><span class="sxs-lookup"><span data-stu-id="1a9cf-159">If so, all the items in the batched process were completed successfully; you don't have to check each **ServiceResponse** object individually.</span></span> <span data-ttu-id="1a9cf-160">Si no se establece la propiedad **OverallResult** para **ServiceResult.Success**, se debe [controlar el error o la advertencia](#bk_ewsmaerrors).</span><span class="sxs-lookup"><span data-stu-id="1a9cf-160">If the **OverallResult** property is not set to **ServiceResult.Success**, you have to [handle the error or warning](#bk_ewsmaerrors).</span></span>
  
<span data-ttu-id="1a9cf-161">Si el método que se está llamando no devuelve un **ServiceResponseCollection**, pero devuelve un objeto **ServiceResponse** , se debe comprobar el valor de la propiedad **Result** .</span><span class="sxs-lookup"><span data-stu-id="1a9cf-161">If the method you're calling does not return a **ServiceResponseCollection**, but does return a **ServiceResponse** object, you have to check the value of the **Result** property.</span></span> <span data-ttu-id="1a9cf-162">Si se establece el valor del **resultado** para el **éxito**, sabrá que el método que se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-162">If the **Result** value is set to **Success**, you know the method completed successfully.</span></span>
  
<span data-ttu-id="1a9cf-163">Si el método que se está llamando no tiene ningún valor devuelto, no es realmente ninguna forma de comprobar el funcionamiento correcto a través de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-163">If the method you're calling has no return value, there's really no way to check for success via the EWS Managed API.</span></span> <span data-ttu-id="1a9cf-164">Siempre y cuando no se produce una excepción, se puede suponer que el método que se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-164">As long as an exception is not thrown, you can assume the method completed successfully.</span></span> <span data-ttu-id="1a9cf-165">Para una validación adicional, también puede [comprobar la respuesta SOAP para comprobar los resultados](#bk_verifysoap).</span><span class="sxs-lookup"><span data-stu-id="1a9cf-165">For additional validation, you can also [check the SOAP response to verify the results](#bk_verifysoap).</span></span>
  
### <a name="handling-errors-warnings-and-exceptions"></a><span data-ttu-id="1a9cf-166">Tratamiento de errores, advertencias y excepciones</span><span class="sxs-lookup"><span data-stu-id="1a9cf-166">Handling errors, warnings, and exceptions</span></span>
<span data-ttu-id="1a9cf-167"><a name="bk_ewsmaerrors"> </a></span><span class="sxs-lookup"><span data-stu-id="1a9cf-167"></span></span>

<span data-ttu-id="1a9cf-168">Si el código de la API administrada de EWS produce una **excepción**, puede usar el valor [Exception.Message](http://msdn.microsoft.com/EN-US/library/9btwf6wk) para determinar el origen del error.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-168">If your EWS Managed API code throws an **Exception**, you can use the [Exception.Message](http://msdn.microsoft.com/EN-US/library/9btwf6wk) value to determine the source of the error.</span></span> <span data-ttu-id="1a9cf-169">La propiedad **Message** contiene el contenido del elemento [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) en la respuesta SOAP subyacente.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-169">The **Message** property contains the contents of the [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) element in the underlying SOAP response.</span></span> <span data-ttu-id="1a9cf-170">Además, si la excepción es del tipo de objeto [ServiceResponseException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) , una de las excepciones más comunes, también puede recuperar el [código de error](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx) incluido en el elemento SOAP [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) subyacente y la [respuesta](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx) propiedad que identifica el objeto [ServiceResponse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) asociado.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-170">In addition, if the exception is of type [ServiceResponseException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) object, one of the most common exceptions, you can also retrieve the [ErrorCode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx) contained in the underlying SOAP [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element, and the [Response](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx) property that identifies the associated [ServiceResponse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) object.</span></span> <span data-ttu-id="1a9cf-171">El código siguiente muestra cómo detectar y mostrar el contenido de una **ServiceResponseException**.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-171">The following code shows how to catch and display the contents of a **ServiceResponseException**.</span></span> 
  
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

<span data-ttu-id="1a9cf-172">Si el método al que llamó devuelve una **ServiceResponseCollection**y el valor de la propiedad **OverallResult** es igual a **Advertencia** o **Error**, tendrá que establecer un bucle por cada objeto en la **ServiceResponseCollection** a Busque el error.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-172">If the method you called returns a **ServiceResponseCollection**, and the value of the **OverallResult** property is equal to **Warning** or **Error**, you'll have to loop through each object in the **ServiceResponseCollection** to find the error.</span></span> <span data-ttu-id="1a9cf-173">La propiedad **OverallResult** se establece en **Advertencia** si al menos una respuesta tiene su valor de **resultado** que se establece como de **Advertencia** y todas las respuestas de otras tienen sus valores de **resultado** sea **correcto**.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-173">The **OverallResult** property is set to **Warning** if at least one response has its **Result** value set to **Warning** and all other responses have their **Result** values set to **Success**.</span></span> <span data-ttu-id="1a9cf-174">La propiedad **OverallResult** se establece en **Error** si al menos una respuesta tiene su valor de **resultado** que se establezca en **Error**.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-174">The **OverallResult** property is set to **Error** if at least one response has its **Result** value set to **Error**.</span></span> <span data-ttu-id="1a9cf-175">Cuando el **OverallResult** se establece en **Advertencia** o **Error**, se establecen las siguientes propiedades en los objetos **ServiceResponse** según corresponda:</span><span class="sxs-lookup"><span data-stu-id="1a9cf-175">When the **OverallResult** is set to **Warning** or **Error**, the following properties are set on the **ServiceResponse** objects as appropriate:</span></span> 
  
- <span data-ttu-id="1a9cf-176">[ErrorCode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) — contiene el código de error, que se puede utilizar para buscar recursos de solución de problemas adicionales.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-176">[ErrorCode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) — Contains the error code, which can be used to find additional troubleshooting resources.</span></span> 
    
- <span data-ttu-id="1a9cf-177">[ErrorDetails](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) — contiene detalles sobre el error para algunos **ErrorCodes**.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-177">[ErrorDetails](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) — Contains details about the error for some **ErrorCodes**.</span></span> <span data-ttu-id="1a9cf-178">Por ejemplo, cuando el código de error es **ErrorRecurrenceHasNoOccurrence**, el **ErrorDetails** contendrá claves para **EffectiveStartDate** y **EffectiveEndDate**.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-178">For example, when the error code is **ErrorRecurrenceHasNoOccurrence**, the **ErrorDetails** will contain keys for **EffectiveStartDate** and **EffectiveEndDate**.</span></span> 
    
- <span data-ttu-id="1a9cf-179">[ErrorMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) : describe el error.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-179">[ErrorMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) — Describes the error.</span></span> 
    
- <span data-ttu-id="1a9cf-180">[ErrorProperties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) : si está disponible, se identifican las propiedades que causó el error.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-180">[ErrorProperties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) — If available, identifies the properties that caused the error.</span></span> <span data-ttu-id="1a9cf-181">Por ejemplo, cuando el código de error es **ErrorInvalidPropertyForOperation**, **ErrorProperties** contiene la definición de la propiedad que no es válida para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-181">For example, when the error code is **ErrorInvalidPropertyForOperation**, **ErrorProperties** contains the definition of the property that was invalid for the request.</span></span> 
    
- <span data-ttu-id="1a9cf-182">[Resultado](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx) : Contains **Error** o **Advertencia** cuando se detecta un problema.</span><span class="sxs-lookup"><span data-stu-id="1a9cf-182">[Result](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx) — Contains **Error** or **Warning** when an issue is encountered.</span></span> 
    
<span data-ttu-id="1a9cf-183">Si la información proporcionada por las propiedades **ServiceResponse** no proporciona suficiente información como para corregir la llamada al método o desbloquear, consulte los [pasos siguientes](#bk_nextsteps) para profundizar más información sobre los valores de **código de error** .</span><span class="sxs-lookup"><span data-stu-id="1a9cf-183">If the information provided by the **ServiceResponse** properties doesn't provide enough information to correct your method call or unblock you, see [Next steps](#bk_nextsteps) to dig up more information on **ErrorCode** values.</span></span> 
  
## 
<span data-ttu-id="1a9cf-184"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="1a9cf-184"></span></span>

<span data-ttu-id="1a9cf-185">Puede buscar información de solución de problemas adicional en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="1a9cf-185">You can look up additional troubleshooting information in the following topics:</span></span>
  
- <span data-ttu-id="1a9cf-186">Elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a9cf-186">[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element</span></span> 
    
- <span data-ttu-id="1a9cf-187">[Depuracuión puede contener](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) (enumeración)</span><span class="sxs-lookup"><span data-stu-id="1a9cf-187">[ServiceError](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) enumeration</span></span> 
    
- [<span data-ttu-id="1a9cf-188">Errores relacionados con la propiedad EWS</span><span class="sxs-lookup"><span data-stu-id="1a9cf-188">EWS property-related errors</span></span>](ews-property-related-errors.md)
    
<span data-ttu-id="1a9cf-189">Además, dependiendo de lo que está intentando llevar a cabo en la solicitud, es posible que encontrar información útil adicional sobre el código de error en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="1a9cf-189">In addition, depending on what you're trying to accomplish in your request, you might find additional helpful information about the error code in the following topics:</span></span>
  
- [<span data-ttu-id="1a9cf-190">Administrar los mensajes de error de detección automática</span><span class="sxs-lookup"><span data-stu-id="1a9cf-190">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    
- [<span data-ttu-id="1a9cf-191">Tratamiento de errores relacionados con la notificación en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1a9cf-191">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="1a9cf-192">Tratamiento de errores relacionados con la sincronización en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1a9cf-192">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="1a9cf-193">Tratamiento de errores relacionados con la eliminación de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1a9cf-193">Handling deletion-related errors in EWS in Exchange</span></span>](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="1a9cf-194">Ver también</span><span class="sxs-lookup"><span data-stu-id="1a9cf-194">See also</span></span>


- [<span data-ttu-id="1a9cf-195">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="1a9cf-195">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="1a9cf-196">Herramientas y recursos para solucionar problemas de aplicaciones de EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="1a9cf-196">Tools and resources for troubleshooting EWS applications for Exchange</span></span>](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

