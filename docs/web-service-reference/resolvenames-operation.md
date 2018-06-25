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
description: La ResolveNames operación las direcciones de correo electrónico ambigua resuelve y nombres para mostrar.
ms.openlocfilehash: 8443cf834dfdf104daeaaa92fdee3742c3fa3719
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837162"
---
# <a name="resolvenames-operation"></a><span data-ttu-id="143bc-103">Operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="143bc-103">ResolveNames operation</span></span>

<span data-ttu-id="143bc-104">La **ResolveNames** operación las direcciones de correo electrónico ambigua resuelve y nombres para mostrar.</span><span class="sxs-lookup"><span data-stu-id="143bc-104">The **ResolveNames** operation resolves ambiguous email addresses and display names.</span></span> 
  
## <a name="using-the-resolvenames-operation"></a><span data-ttu-id="143bc-105">Mediante la operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="143bc-105">Using the ResolveNames operation</span></span>

<span data-ttu-id="143bc-106">Esta operación puede usarse para comprobar los alias y resolver nombres para mostrar para el usuario del buzón correspondiente.</span><span class="sxs-lookup"><span data-stu-id="143bc-106">This operation can be used to verify aliases and resolve display names to the appropriate mailbox user.</span></span> <span data-ttu-id="143bc-107">Si existen nombres ambiguos, la respuesta de la operación **ResolveNames** proporciona información acerca de cada usuario de buzón de correo para que la aplicación cliente pueda resolver los nombres.</span><span class="sxs-lookup"><span data-stu-id="143bc-107">If ambiguous names exist, the **ResolveNames** operation response provides information about each mailbox user so that the client application can resolve the names.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="143bc-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="143bc-108">Remarks</span></span>

<span data-ttu-id="143bc-109">La respuesta ResolveNames devuelve un máximo de 100 candidatos.</span><span class="sxs-lookup"><span data-stu-id="143bc-109">The ResolveNames response returns a maximum of 100 candidates.</span></span> <span data-ttu-id="143bc-110">Los candidatos de 100 que se devuelven son los 100 primeros que se encuentran en la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="143bc-110">The 100 candidates that are returned are the first 100 that are encountered in the lookup operation.</span></span>
  
<span data-ttu-id="143bc-111">Direcciones de correo electrónico con tipos de enrutamiento de prefijo, como smtp o sip, se guardan en una matriz con varios valores.</span><span class="sxs-lookup"><span data-stu-id="143bc-111">Email addresses with prefixed routing types, such as smtp or sip, are saved in a multivalue array.</span></span> <span data-ttu-id="143bc-112">La operación **ResolveNames** lleva a cabo a una coincidencia parcial con respecto a cada valor de dicha matriz al agregar el tipo de distribución al principio del nombre sin resolver, como "sip:User1@Contoso.com".</span><span class="sxs-lookup"><span data-stu-id="143bc-112">The **ResolveNames** operation performs a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1@Contoso.com".</span></span> <span data-ttu-id="143bc-113">Si no especifica un tipo de distribución, **ResolveNames** de forma predeterminada en el tipo de distribución de smtp, match a una propiedad de dirección smtp principal y no buscar en la matriz con varios valores.</span><span class="sxs-lookup"><span data-stu-id="143bc-113">If you don't specify a routing type, **ResolveNames** will default to the routing type of smtp, match it to a primary smtp address property, and not search the multivalue array.</span></span> 
  
<span data-ttu-id="143bc-114">Nombre ambiguo solo se puede especificar en una única solicitud.</span><span class="sxs-lookup"><span data-stu-id="143bc-114">Only one ambiguous name can be specified in a single request.</span></span> <span data-ttu-id="143bc-115">Active Directory se busca en primer lugar y, a continuación, se busca la carpeta de contactos del usuario.</span><span class="sxs-lookup"><span data-stu-id="143bc-115">Active Directory is searched first, and then the user's contact folder is searched.</span></span> <span data-ttu-id="143bc-116">Resuelto las entradas de la carpeta de contactos de un usuario tienen una propiedad de **ItemId** no es null, que, a continuación, se puede usar en una solicitud GetItem.</span><span class="sxs-lookup"><span data-stu-id="143bc-116">Resolved entries from a user's contact folder have a non-null **ItemId** property, which can then be used in a GetItem request.</span></span> <span data-ttu-id="143bc-117">Si es el identificador de una lista de distribución privada, a continuación, se puede utilizar en una [operación de ExpandDL](expanddl-operation.md).</span><span class="sxs-lookup"><span data-stu-id="143bc-117">If it is the ID of a private distribution list, then it can be used in an [ExpandDL operation](expanddl-operation.md).</span></span> <span data-ttu-id="143bc-118">Si el atributo **ReturnFullContactData** está establecido en **true**, las entradas de Active Directory que se encuentra con la operación **ResolveNames** devolverá las propiedades adicionales que describen a un [contacto](contact.md).</span><span class="sxs-lookup"><span data-stu-id="143bc-118">If the **ReturnFullContactData** attribute is set to **true**, then Active Directory entries found with the **ResolveNames** operation will return additional properties that describe a [Contact](contact.md).</span></span> <span data-ttu-id="143bc-119">El atributo **ReturnFullContactData** no afecta a los datos que se devuelven para los contactos y private las listas de distribución desde la carpeta de contactos del usuario.</span><span class="sxs-lookup"><span data-stu-id="143bc-119">The **ReturnFullContactData** attribute does not affect the data that is returned for contacts and private distribution lists from the user's contact folder.</span></span> 
  
## <a name="resolvenames-request-example"></a><span data-ttu-id="143bc-120">Ejemplo de solicitud ResolveNames</span><span class="sxs-lookup"><span data-stu-id="143bc-120">ResolveNames request example</span></span>

### <a name="description"></a><span data-ttu-id="143bc-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="143bc-121">Description</span></span>

<span data-ttu-id="143bc-122">El siguiente ejemplo de una solicitud de **ResolveNames** muestra cómo resolver la entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="143bc-122">The following example of a **ResolveNames** request shows how to resolve the entry of User.</span></span>
  
### <a name="code"></a><span data-ttu-id="143bc-123">Código</span><span class="sxs-lookup"><span data-stu-id="143bc-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>User2</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="143bc-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="143bc-124">Comments</span></span>

<span data-ttu-id="143bc-125">La respuesta a esta solicitud devolverá todas las entradas que empiecen por "Jo" o "Mi".</span><span class="sxs-lookup"><span data-stu-id="143bc-125">The response to this request will return all entries that start with "Jo" or "Mi."</span></span> <span data-ttu-id="143bc-126">Los elementos devueltos son públicas buzones, listas de distribución públicas y privadas y contactos.</span><span class="sxs-lookup"><span data-stu-id="143bc-126">The returned items are public mailboxes, public and private distribution lists, and contacts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="143bc-127">Se buscan sólo los contactos de la carpeta de contactos personal de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="143bc-127">Only contacts in the default personal Contacts folder are searched.</span></span> 
  
<span data-ttu-id="143bc-128">Los siguientes son los resultados posibles para una solicitud de **ResolveNames** :</span><span class="sxs-lookup"><span data-stu-id="143bc-128">The following are the possible results for a **ResolveNames** request:</span></span> 
  
- <span data-ttu-id="143bc-129">Las respuestas que no contienen una entidad resuelta devolverá un valor de atributo de **ResponseClass** igual a **Error**.</span><span class="sxs-lookup"><span data-stu-id="143bc-129">Responses that do not contain a resolved entity will return a **ResponseClass** attribute value equal to **Error**.</span></span> <span data-ttu-id="143bc-130">El elemento **MessageText** contendrá " **No se encontraron resultados**".</span><span class="sxs-lookup"><span data-stu-id="143bc-130">The **MessageText** element will contain " **No results are found**."</span></span>
    
- <span data-ttu-id="143bc-131">Las respuestas que contienen una única entidad resuelta devolverá un valor de atributo de **ResponseClass** igual a **correcto**.</span><span class="sxs-lookup"><span data-stu-id="143bc-131">Responses that contain a single resolved entity will return a **ResponseClass** attribute value equal to **Success**.</span></span>
    
- <span data-ttu-id="143bc-132">Las respuestas que contienen varias entidades posibles devolverá un valor de atributo de **ResponseClass** igual a la **Advertencia**.</span><span class="sxs-lookup"><span data-stu-id="143bc-132">Responses that contain multiple possible entities will return a **ResponseClass** attribute value equal to **Warning**.</span></span> <span data-ttu-id="143bc-133">En este caso, la entidad no se pudo resolver a una identidad única.</span><span class="sxs-lookup"><span data-stu-id="143bc-133">In this case, the entity could not be resolved to a unique identity.</span></span> <span data-ttu-id="143bc-134">El elemento **MessageText** contendrá "se encuentran varios resultados".</span><span class="sxs-lookup"><span data-stu-id="143bc-134">The **MessageText** element will contain "Multiple results are found."</span></span> 
    
### <a name="request-elements"></a><span data-ttu-id="143bc-135">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="143bc-135">Request elements</span></span>

<span data-ttu-id="143bc-136">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="143bc-136">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="143bc-137">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="143bc-137">ResolveNames</span></span>](resolvenames.md)
    
- [<span data-ttu-id="143bc-138">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="143bc-138">UnresolvedEntry</span></span>](unresolvedentry.md)
    
## <a name="successful-resolvenames-operation-response-example"></a><span data-ttu-id="143bc-139">Ejemplo de respuesta correcto de la operación de ResolveNames</span><span class="sxs-lookup"><span data-stu-id="143bc-139">Successful ResolveNames operation response example</span></span>

### <a name="description"></a><span data-ttu-id="143bc-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="143bc-140">Description</span></span>

<span data-ttu-id="143bc-141">En el ejemplo siguiente se muestra una respuesta a una solicitud de **ResolveNames** correcta.</span><span class="sxs-lookup"><span data-stu-id="143bc-141">The following example shows a successful response to a **ResolveNames** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="143bc-142">Código</span><span class="sxs-lookup"><span data-stu-id="143bc-142">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-resolvenames-response-elements"></a><span data-ttu-id="143bc-143">Elementos de respuesta ResolveNames correctos</span><span class="sxs-lookup"><span data-stu-id="143bc-143">Successful ResolveNames response elements</span></span>

<span data-ttu-id="143bc-144">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="143bc-144">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="143bc-145">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="143bc-145">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="143bc-146">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="143bc-146">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
    
- [<span data-ttu-id="143bc-147">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="143bc-147">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="143bc-148">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="143bc-148">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
    
- [<span data-ttu-id="143bc-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="143bc-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="143bc-150">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="143bc-150">ResolutionSet</span></span>](resolutionset.md)
    
- [<span data-ttu-id="143bc-151">Resoluci?n</span><span class="sxs-lookup"><span data-stu-id="143bc-151">Resolution</span></span>](resolution.md)
    
- [<span data-ttu-id="143bc-152">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="143bc-152">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="143bc-153">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="143bc-153">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="143bc-154">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="143bc-154">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="143bc-155">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="143bc-155">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="143bc-156">MailboxType</span><span class="sxs-lookup"><span data-stu-id="143bc-156">MailboxType</span></span>](mailboxtype.md)
    
- [<span data-ttu-id="143bc-157">Contact</span><span class="sxs-lookup"><span data-stu-id="143bc-157">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="143bc-158">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="143bc-158">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="143bc-159">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="143bc-159">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="143bc-160">Entrada (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="143bc-160">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
- [<span data-ttu-id="143bc-161">ContactSource</span><span class="sxs-lookup"><span data-stu-id="143bc-161">ContactSource</span></span>](contactsource.md)
    
## <a name="resolvenames-operation-error-response"></a><span data-ttu-id="143bc-162">Respuesta de error de la operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="143bc-162">ResolveNames operation error response</span></span>

### <a name="description"></a><span data-ttu-id="143bc-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="143bc-163">Description</span></span>

<span data-ttu-id="143bc-164">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de **ResolveNames** .</span><span class="sxs-lookup"><span data-stu-id="143bc-164">The following example shows an error response to a **ResolveNames** request.</span></span> <span data-ttu-id="143bc-165">El error está causado por intenta resolver un nombre que no se puede resolver.</span><span class="sxs-lookup"><span data-stu-id="143bc-165">The error is caused by trying to resolve a name that cannot be resolved.</span></span> 
  
### <a name="code"></a><span data-ttu-id="143bc-166">Código</span><span class="sxs-lookup"><span data-stu-id="143bc-166">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="143bc-167">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="143bc-167">Error response elements</span></span>

<span data-ttu-id="143bc-168">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="143bc-168">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="143bc-169">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="143bc-169">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="143bc-170">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="143bc-170">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
    
- [<span data-ttu-id="143bc-171">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="143bc-171">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="143bc-172">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="143bc-172">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
    
- [<span data-ttu-id="143bc-173">MessageText</span><span class="sxs-lookup"><span data-stu-id="143bc-173">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="143bc-174">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="143bc-174">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="143bc-175">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="143bc-175">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="143bc-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="143bc-176">See also</span></span>



[<span data-ttu-id="143bc-177">Operación de ExpandDL</span><span class="sxs-lookup"><span data-stu-id="143bc-177">ExpandDL operation</span></span>](expanddl-operation.md)


[<span data-ttu-id="143bc-178">Uso de la resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="143bc-178">Using Name Resolution</span></span>](http://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

