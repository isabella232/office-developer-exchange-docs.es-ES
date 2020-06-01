---
title: Operación ResolveNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: 6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb
description: La operación ResolveNames resuelve direcciones de correo electrónico ambiguas y nombres para mostrar.
ms.openlocfilehash: 51728addddd2bfb9d35b874ae8c11e83a4c8629b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468281"
---
# <a name="resolvenames-operation"></a><span data-ttu-id="e2fd9-103">Operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="e2fd9-103">ResolveNames operation</span></span>

<span data-ttu-id="e2fd9-104">La operación **ResolveNames** resuelve direcciones de correo electrónico ambiguas y nombres para mostrar.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-104">The **ResolveNames** operation resolves ambiguous email addresses and display names.</span></span> 
  
## <a name="using-the-resolvenames-operation"></a><span data-ttu-id="e2fd9-105">Uso de la operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="e2fd9-105">Using the ResolveNames operation</span></span>

<span data-ttu-id="e2fd9-106">Esta operación puede usarse para comprobar los alias y resolver los nombres para mostrar al usuario del buzón de correo apropiado.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-106">This operation can be used to verify aliases and resolve display names to the appropriate mailbox user.</span></span> <span data-ttu-id="e2fd9-107">Si existen nombres ambiguos, la respuesta de operación **ResolveNames** proporciona información acerca de cada usuario de buzón para que la aplicación cliente pueda resolver los nombres.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-107">If ambiguous names exist, the **ResolveNames** operation response provides information about each mailbox user so that the client application can resolve the names.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e2fd9-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2fd9-108">Remarks</span></span>

<span data-ttu-id="e2fd9-109">La respuesta ResolveNames devuelve un máximo de 100 candidatos.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-109">The ResolveNames response returns a maximum of 100 candidates.</span></span> <span data-ttu-id="e2fd9-110">Los 100 candidatos que se devuelven son los primeros 100 que se encuentran en la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-110">The 100 candidates that are returned are the first 100 that are encountered in the lookup operation.</span></span>
  
<span data-ttu-id="e2fd9-111">Las direcciones de correo electrónico con tipos de enrutamiento prefijados, como SMTP o SIP, se guardan en una matriz de varios valores.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-111">Email addresses with prefixed routing types, such as smtp or sip, are saved in a multivalue array.</span></span> <span data-ttu-id="e2fd9-112">La operación **ResolveNames** realiza una coincidencia parcial con cada valor de la matriz cuando se agrega el tipo de enrutamiento al principio del nombre sin resolver, como "SIP:user1@Contoso.com".</span><span class="sxs-lookup"><span data-stu-id="e2fd9-112">The **ResolveNames** operation performs a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1@Contoso.com".</span></span> <span data-ttu-id="e2fd9-113">Si no especifica un tipo de enrutamiento, **ResolveNames** se establecerá de forma predeterminada en el tipo de enrutamiento de SMTP, lo hará coincidir con una propiedad de dirección SMTP principal y no buscará en la matriz de varios valores.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-113">If you don't specify a routing type, **ResolveNames** will default to the routing type of smtp, match it to a primary smtp address property, and not search the multivalue array.</span></span> 
  
<span data-ttu-id="e2fd9-114">Solo se puede especificar un nombre ambiguo en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-114">Only one ambiguous name can be specified in a single request.</span></span> <span data-ttu-id="e2fd9-115">En primer lugar, se busca en Active Directory y, a continuación, se busca en la carpeta de contactos del usuario.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-115">Active Directory is searched first, and then the user's contact folder is searched.</span></span> <span data-ttu-id="e2fd9-116">Las entradas resueltas de la carpeta de contactos de un usuario tienen una propiedad **Itemid** que no es null, que se puede usar en una solicitud GetItem.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-116">Resolved entries from a user's contact folder have a non-null **ItemId** property, which can then be used in a GetItem request.</span></span> <span data-ttu-id="e2fd9-117">Si es el identificador de una lista de distribución privada, puede usarse en una [operación ExpandDL](expanddl-operation.md).</span><span class="sxs-lookup"><span data-stu-id="e2fd9-117">If it is the ID of a private distribution list, then it can be used in an [ExpandDL operation](expanddl-operation.md).</span></span> <span data-ttu-id="e2fd9-118">Si el atributo **ReturnFullContactData** se establece en **true**, las entradas de Active Directory que se encuentran con la operación **ResolveNames** devolverán propiedades adicionales que describen un [contacto](contact.md).</span><span class="sxs-lookup"><span data-stu-id="e2fd9-118">If the **ReturnFullContactData** attribute is set to **true**, then Active Directory entries found with the **ResolveNames** operation will return additional properties that describe a [Contact](contact.md).</span></span> <span data-ttu-id="e2fd9-119">El atributo **ReturnFullContactData** no afecta a los datos que se devuelven para contactos y listas de distribución privadas de la carpeta de contactos del usuario.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-119">The **ReturnFullContactData** attribute does not affect the data that is returned for contacts and private distribution lists from the user's contact folder.</span></span> 
  
## <a name="resolvenames-request-example"></a><span data-ttu-id="e2fd9-120">Ejemplo de solicitud ResolveNames</span><span class="sxs-lookup"><span data-stu-id="e2fd9-120">ResolveNames request example</span></span>

### <a name="description"></a><span data-ttu-id="e2fd9-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2fd9-121">Description</span></span>

<span data-ttu-id="e2fd9-122">El siguiente ejemplo de una solicitud **ResolveNames** muestra cómo resolver la entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-122">The following example of a **ResolveNames** request shows how to resolve the entry of User.</span></span>
  
### <a name="code"></a><span data-ttu-id="e2fd9-123">Código</span><span class="sxs-lookup"><span data-stu-id="e2fd9-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>User2</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="e2fd9-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2fd9-124">Comments</span></span>

<span data-ttu-id="e2fd9-125">La respuesta a esta solicitud devolverá todas las entradas que empiecen por "Jo" o "mi".</span><span class="sxs-lookup"><span data-stu-id="e2fd9-125">The response to this request will return all entries that start with "Jo" or "Mi."</span></span> <span data-ttu-id="e2fd9-126">Los elementos devueltos son buzones públicos, listas de distribución públicas y privadas y contactos.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-126">The returned items are public mailboxes, public and private distribution lists, and contacts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e2fd9-127">Solo se busca en los contactos de la carpeta de contactos personales predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-127">Only contacts in the default personal Contacts folder are searched.</span></span> 
  
<span data-ttu-id="e2fd9-128">Los siguientes son los posibles resultados de una solicitud de **ResolveNames** :</span><span class="sxs-lookup"><span data-stu-id="e2fd9-128">The following are the possible results for a **ResolveNames** request:</span></span> 
  
- <span data-ttu-id="e2fd9-129">Las respuestas que no contienen una entidad resolved devolverán un valor de atributo **ResponseClass** igual a **error**.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-129">Responses that do not contain a resolved entity will return a **ResponseClass** attribute value equal to **Error**.</span></span> <span data-ttu-id="e2fd9-130">El elemento **MessageText** contendrá " **no se encuentra ningún resultado**".</span><span class="sxs-lookup"><span data-stu-id="e2fd9-130">The **MessageText** element will contain " **No results are found**."</span></span>
    
- <span data-ttu-id="e2fd9-131">Las respuestas que contienen una única entidad resolved devolverán un valor de atributo **ResponseClass** igual a **Success**.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-131">Responses that contain a single resolved entity will return a **ResponseClass** attribute value equal to **Success**.</span></span>
    
- <span data-ttu-id="e2fd9-132">Las respuestas que contienen varias entidades posibles devolverán un valor de atributo **ResponseClass** igual a **ADVERTENCIA**.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-132">Responses that contain multiple possible entities will return a **ResponseClass** attribute value equal to **Warning**.</span></span> <span data-ttu-id="e2fd9-133">En este caso, la entidad no se pudo resolver como una identidad única.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-133">In this case, the entity could not be resolved to a unique identity.</span></span> <span data-ttu-id="e2fd9-134">El elemento **MessageText** contendrá "se encuentran varios resultados".</span><span class="sxs-lookup"><span data-stu-id="e2fd9-134">The **MessageText** element will contain "Multiple results are found."</span></span> 
    
### <a name="request-elements"></a><span data-ttu-id="e2fd9-135">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="e2fd9-135">Request elements</span></span>

<span data-ttu-id="e2fd9-136">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="e2fd9-136">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="e2fd9-137">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="e2fd9-137">ResolveNames</span></span>](resolvenames.md)
    
- [<span data-ttu-id="e2fd9-138">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="e2fd9-138">UnresolvedEntry</span></span>](unresolvedentry.md)
    
## <a name="successful-resolvenames-operation-response-example"></a><span data-ttu-id="e2fd9-139">Ejemplo de respuesta de operación ResolveNames correcta</span><span class="sxs-lookup"><span data-stu-id="e2fd9-139">Successful ResolveNames operation response example</span></span>

### <a name="description"></a><span data-ttu-id="e2fd9-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2fd9-140">Description</span></span>

<span data-ttu-id="e2fd9-141">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud **ResolveNames** .</span><span class="sxs-lookup"><span data-stu-id="e2fd9-141">The following example shows a successful response to a **ResolveNames** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e2fd9-142">Código</span><span class="sxs-lookup"><span data-stu-id="e2fd9-142">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ResolutionSet TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>User2</t:Name>
                <t:EmailAddress>User2@example.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Mailbox</t:MailboxType>
              </t:Mailbox>
              <t:Contact>
                <t:DisplayName>User2</t:DisplayName>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress1">SMTP:User2@example.com</t:Entry>
                </t:EmailAddresses>
                <t:ContactSource>ActiveDirectory</t:ContactSource>
              </t:Contact>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-resolvenames-response-elements"></a><span data-ttu-id="e2fd9-143">Elementos de respuesta ResolveNames correctos</span><span class="sxs-lookup"><span data-stu-id="e2fd9-143">Successful ResolveNames response elements</span></span>

<span data-ttu-id="e2fd9-144">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e2fd9-144">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="e2fd9-145">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e2fd9-145">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="e2fd9-146">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="e2fd9-146">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
    
- [<span data-ttu-id="e2fd9-147">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e2fd9-147">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e2fd9-148">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e2fd9-148">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
    
- [<span data-ttu-id="e2fd9-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e2fd9-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e2fd9-150">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="e2fd9-150">ResolutionSet</span></span>](resolutionset.md)
    
- [<span data-ttu-id="e2fd9-151">Resolución</span><span class="sxs-lookup"><span data-stu-id="e2fd9-151">Resolution</span></span>](resolution.md)
    
- [<span data-ttu-id="e2fd9-152">Buzón</span><span class="sxs-lookup"><span data-stu-id="e2fd9-152">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="e2fd9-153">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="e2fd9-153">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="e2fd9-154">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="e2fd9-154">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="e2fd9-155">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="e2fd9-155">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="e2fd9-156">MailboxType</span><span class="sxs-lookup"><span data-stu-id="e2fd9-156">MailboxType</span></span>](mailboxtype.md)
    
- [<span data-ttu-id="e2fd9-157">Contacto</span><span class="sxs-lookup"><span data-stu-id="e2fd9-157">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="e2fd9-158">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="e2fd9-158">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="e2fd9-159">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="e2fd9-159">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="e2fd9-160">Entrada (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="e2fd9-160">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
- [<span data-ttu-id="e2fd9-161">ContactSource</span><span class="sxs-lookup"><span data-stu-id="e2fd9-161">ContactSource</span></span>](contactsource.md)
    
## <a name="resolvenames-operation-error-response"></a><span data-ttu-id="e2fd9-162">Respuesta de error de operación de ResolveNames</span><span class="sxs-lookup"><span data-stu-id="e2fd9-162">ResolveNames operation error response</span></span>

### <a name="description"></a><span data-ttu-id="e2fd9-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2fd9-163">Description</span></span>

<span data-ttu-id="e2fd9-164">En el ejemplo siguiente se muestra una respuesta de error a una solicitud **ResolveNames** .</span><span class="sxs-lookup"><span data-stu-id="e2fd9-164">The following example shows an error response to a **ResolveNames** request.</span></span> <span data-ttu-id="e2fd9-165">El error se produce al intentar resolver un nombre que no se puede resolver.</span><span class="sxs-lookup"><span data-stu-id="e2fd9-165">The error is caused by trying to resolve a name that cannot be resolved.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e2fd9-166">Código</span><span class="sxs-lookup"><span data-stu-id="e2fd9-166">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Error">
          <m:MessageText>No results were found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="e2fd9-167">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="e2fd9-167">Error response elements</span></span>

<span data-ttu-id="e2fd9-168">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="e2fd9-168">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="e2fd9-169">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e2fd9-169">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="e2fd9-170">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="e2fd9-170">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
    
- [<span data-ttu-id="e2fd9-171">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e2fd9-171">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e2fd9-172">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e2fd9-172">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
    
- [<span data-ttu-id="e2fd9-173">MessageText</span><span class="sxs-lookup"><span data-stu-id="e2fd9-173">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="e2fd9-174">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e2fd9-174">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e2fd9-175">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e2fd9-175">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="e2fd9-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2fd9-176">See also</span></span>



[<span data-ttu-id="e2fd9-177">Operación ExpandDL</span><span class="sxs-lookup"><span data-stu-id="e2fd9-177">ExpandDL operation</span></span>](expanddl-operation.md)


[<span data-ttu-id="e2fd9-178">Uso de la resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="e2fd9-178">Using Name Resolution</span></span>](https://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

