---
title: Operación RemoveImGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5e788016-68e0-4a3f-9243-03f6b6c6b389
description: Buscar información sobre la operación de EWS de RemoveImGroup.
ms.openlocfilehash: b5e38404cbb1907a1118ab3ae8e56abb5a8d5e41
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456768"
---
# <a name="removeimgroup-operation"></a><span data-ttu-id="c39b3-103">Operación RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="c39b3-103">RemoveImGroup operation</span></span>

<span data-ttu-id="c39b3-104">Buscar información sobre la operación de EWS de **RemoveImGroup** .</span><span class="sxs-lookup"><span data-stu-id="c39b3-104">Find information about the **RemoveImGroup** EWS operation.</span></span> 
  
<span data-ttu-id="c39b3-105">La operación **RemoveImGroup** quita un solo grupo de mensajería instantánea (mi) de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c39b3-105">The **RemoveImGroup** operation removes a single instant messaging (IM) group from a mailbox.</span></span> 
  
<span data-ttu-id="c39b3-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c39b3-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-removeimgroup-operation"></a><span data-ttu-id="c39b3-107">Uso de la operación RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="c39b3-107">Using the RemoveImGroup operation</span></span>

<span data-ttu-id="c39b3-108">La operación **RemoveImGroup** sólo toma un único argumento de identificador de grupo.</span><span class="sxs-lookup"><span data-stu-id="c39b3-108">The **RemoveImGroup** operation only takes a single group identifier argument.</span></span> 
  
### <a name="removeimgroup-operation-soap-headers"></a><span data-ttu-id="c39b3-109">Encabezados SOAP de operación RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="c39b3-109">RemoveImGroup operation SOAP headers</span></span>

<span data-ttu-id="c39b3-110">La operación **RemoveImGroup** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c39b3-110">The **RemoveImGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="c39b3-111">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="c39b3-111">**Header name**</span></span>|<span data-ttu-id="c39b3-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c39b3-112">**Element**</span></span>|<span data-ttu-id="c39b3-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c39b3-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c39b3-114">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="c39b3-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="c39b3-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="c39b3-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="c39b3-116">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="c39b3-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="c39b3-117">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="c39b3-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c39b3-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="c39b3-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="c39b3-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="c39b3-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="c39b3-120">Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="c39b3-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="c39b3-121">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="c39b3-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c39b3-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="c39b3-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="c39b3-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="c39b3-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="c39b3-124">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="c39b3-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="c39b3-125">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="c39b3-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c39b3-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="c39b3-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="c39b3-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c39b3-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="c39b3-128">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c39b3-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="c39b3-129">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="c39b3-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="removeimgroup-operation-request-example"></a><span data-ttu-id="c39b3-130">Ejemplo de solicitud de operación RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="c39b3-130">RemoveImGroup operation request example</span></span>

<span data-ttu-id="c39b3-131">El siguiente ejemplo de una solicitud de operación de **RemoveImGroup** muestra cómo quitar un grupo de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="c39b3-131">The following example of a **RemoveImGroup** operation request shows how to remove an IM group.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c39b3-132">El identificador de grupo se ha reducido para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c39b3-132">The group ID has been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:RemoveImGroup>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDA5hQoTbWAAAAAAQRAAA="
                    ChangeKey="EgAAAA=="/>
      </m:RemoveImGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c39b3-133">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="c39b3-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c39b3-134">RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="c39b3-134">RemoveImGroup</span></span>](removeimgroup.md)
    
- [<span data-ttu-id="c39b3-135">GroupId</span><span class="sxs-lookup"><span data-stu-id="c39b3-135">GroupId</span></span>](groupid.md)
    
## <a name="successful-removeimgroup-operation-response"></a><span data-ttu-id="c39b3-136">Respuesta de operación RemoveImGroup correcta</span><span class="sxs-lookup"><span data-stu-id="c39b3-136">Successful RemoveImGroup operation response</span></span>

<span data-ttu-id="c39b3-137">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **RemoveImGroup** .</span><span class="sxs-lookup"><span data-stu-id="c39b3-137">The following example shows a successful response to a **RemoveImGroup** operation request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveImGroupResponse ResponseClass="Success" 
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="c39b3-138">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="c39b3-138">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c39b3-139">RemoveImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="c39b3-139">RemoveImGroupResponse</span></span>](removeimgroupresponse.md)
    
- [<span data-ttu-id="c39b3-140">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c39b3-140">ResponseCode</span></span>](responsecode.md)
    
## <a name="removeimgroup-operation-errorinvalidimgroupid-error-response"></a><span data-ttu-id="c39b3-141">RemoveImGroup Operation ErrorInvalidImGroupId error Response</span><span class="sxs-lookup"><span data-stu-id="c39b3-141">RemoveImGroup operation ErrorInvalidImGroupId error response</span></span>

<span data-ttu-id="c39b3-142">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **RemoveImGroup** .</span><span class="sxs-lookup"><span data-stu-id="c39b3-142">The following example shows an error response to a **RemoveImGroup** operation request.</span></span> <span data-ttu-id="c39b3-143">La siguiente respuesta de error se produce cuando se intenta quitar un grupo que no existe en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="c39b3-143">The following error response occurs when an attempt is made to remove a group that does not exist in the mailbox.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveImGroupResponse ResponseClass="Error" 
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified Im Group Id is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImGroupId</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="c39b3-144">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="c39b3-144">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c39b3-145">RemoveImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="c39b3-145">RemoveImGroupResponse</span></span>](removeimgroupresponse.md)
    
- [<span data-ttu-id="c39b3-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="c39b3-146">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="c39b3-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c39b3-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c39b3-148">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c39b3-148">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="c39b3-149">Para obtener los códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="c39b3-149">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="removeimgroup-operation-errorinvalididmalformed-error-response"></a><span data-ttu-id="c39b3-150">RemoveImGroup Operation ErrorInvalidIdMalformed error Response</span><span class="sxs-lookup"><span data-stu-id="c39b3-150">RemoveImGroup operation ErrorInvalidIdMalformed error response</span></span>

<span data-ttu-id="c39b3-151">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **RemoveImGroup** .</span><span class="sxs-lookup"><span data-stu-id="c39b3-151">The following example shows an error response to a **RemoveImGroup** operation request.</span></span> <span data-ttu-id="c39b3-152">Cuando se realiza un intento de quitar un grupo con un identificador de grupo con formato incorrecto, se produce la siguiente respuesta de error.</span><span class="sxs-lookup"><span data-stu-id="c39b3-152">The following error response occurs when an attempt is made to remove a group with an incorrectly formatted group identifier.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveImGroupResponse ResponseClass="Error" 
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Id is malformed.</MessageText>
         <ResponseCode>ErrorInvalidIdMalformed</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="c39b3-153">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="c39b3-153">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c39b3-154">RemoveImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="c39b3-154">RemoveImGroupResponse</span></span>](removeimgroupresponse.md)
    
- [<span data-ttu-id="c39b3-155">MessageText</span><span class="sxs-lookup"><span data-stu-id="c39b3-155">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="c39b3-156">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c39b3-156">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c39b3-157">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c39b3-157">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="c39b3-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="c39b3-158">See also</span></span>

- [<span data-ttu-id="c39b3-159">Personas y contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c39b3-159">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="c39b3-160">Operación AddImGroup</span><span class="sxs-lookup"><span data-stu-id="c39b3-160">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="c39b3-161">Operación SetImGroup</span><span class="sxs-lookup"><span data-stu-id="c39b3-161">SetImGroup operation</span></span>](setimgroup-operation.md)
    

