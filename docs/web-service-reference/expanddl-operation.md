---
title: Operación ExpandDL
manager: sethgros
ms.date: 07/27/2018
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: 1f7837e7-9eff-4e10-9577-c40f7ed6af94
description: La operación ExpandDL expone toda la pertenencia a listas de distribución.
ms.openlocfilehash: 8edaf057538e2c1136465f0ff7937c14477b2c47
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44454053"
---
# <a name="expanddl-operation"></a><span data-ttu-id="58ddb-103">Operación ExpandDL</span><span class="sxs-lookup"><span data-stu-id="58ddb-103">ExpandDL operation</span></span>

<span data-ttu-id="58ddb-104">La operación ExpandDL expone toda la pertenencia a listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="58ddb-104">The ExpandDL operation exposes the full membership of distribution lists.</span></span>
  
## <a name="using-the-expanddl-web-method"></a><span data-ttu-id="58ddb-105">Uso del método Web ExpandDL</span><span class="sxs-lookup"><span data-stu-id="58ddb-105">Using the ExpandDL Web Method</span></span>

<span data-ttu-id="58ddb-106">La operación ExpandDL usa el servicio Web que se encuentra en Exchange. asmx.</span><span class="sxs-lookup"><span data-stu-id="58ddb-106">The ExpandDL operation uses the Web service that is located in Exchange.asmx.</span></span> <span data-ttu-id="58ddb-107">Este método de servicio web acepta un elemento [Mailbox](mailbox.md) que puede contener un elemento secundario [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) para una expansión de una lista de distribución pública o un elemento secundario [Itemid](itemid.md) para la expansión de una lista de distribución privada.</span><span class="sxs-lookup"><span data-stu-id="58ddb-107">This Web service method accepts a [Mailbox](mailbox.md) element that can contain either an [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) child element for an expansion of a public distribution list or an [ItemId](itemid.md) child element for the expansion of a private distribution list.</span></span> 
  
<span data-ttu-id="58ddb-108">Las listas de distribución públicas se pueden expandir con una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="58ddb-108">Public distribution lists can be expanded by using one of the following:</span></span>
  
1. <span data-ttu-id="58ddb-109">Alias de lista de distribución</span><span class="sxs-lookup"><span data-stu-id="58ddb-109">Distribution list alias</span></span>
    
2. <span data-ttu-id="58ddb-110">Dirección del protocolo simple de transferencia de correo (SMTP)</span><span class="sxs-lookup"><span data-stu-id="58ddb-110">The Simple Mail Transfer Protocol (SMTP) address</span></span>
    
3. <span data-ttu-id="58ddb-111">X.400</span><span class="sxs-lookup"><span data-stu-id="58ddb-111">X400</span></span>
    
4. <span data-ttu-id="58ddb-112">X500</span><span class="sxs-lookup"><span data-stu-id="58ddb-112">X500</span></span>
    
5. <span data-ttu-id="58ddb-113">Dirección heredada de Exchange</span><span class="sxs-lookup"><span data-stu-id="58ddb-113">Exchange Legacy address</span></span>
    
6. <span data-ttu-id="58ddb-114">El nombre de la lista de distribución</span><span class="sxs-lookup"><span data-stu-id="58ddb-114">The distribution list name</span></span>
    
7. <span data-ttu-id="58ddb-115">El nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="58ddb-115">The display name</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="58ddb-116">Los nombres para mostrar no son únicos.</span><span class="sxs-lookup"><span data-stu-id="58ddb-116">Display names are not unique.</span></span> <span data-ttu-id="58ddb-117">Varias cuentas pueden compartir el mismo nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="58ddb-117">Multiple accounts can share the same display name.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="58ddb-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58ddb-118">Remarks</span></span>

<span data-ttu-id="58ddb-119">No se admite la expansión recursiva.</span><span class="sxs-lookup"><span data-stu-id="58ddb-119">Recursive expansion is not supported.</span></span> <span data-ttu-id="58ddb-120">Solo se puede expandir una lista de distribución en una sola llamada.</span><span class="sxs-lookup"><span data-stu-id="58ddb-120">Only one distribution list can be expanded in a single call.</span></span> <span data-ttu-id="58ddb-121">Si hay más de una lista de distribución que coincide con los criterios, el servicio Web notifica un error.</span><span class="sxs-lookup"><span data-stu-id="58ddb-121">If more than one distribution list match the criteria, the Web service reports an error.</span></span> <span data-ttu-id="58ddb-122">Una aplicación cliente puede usar la resolución de nombres ambiguos (ANR) para buscar listas de distribución ambiguas y, a continuación, elegir la dirección de correo electrónico correcta de la lista de distribución requerida como un parámetro para la [operación ExpandDL](expanddl-operation.md).</span><span class="sxs-lookup"><span data-stu-id="58ddb-122">A client application can use ambiguous name resolution (ANR) to find ambiguous distribution lists and then chose the correct e-mail address of the required distribution list as a parameter for the [ExpandDL operation](expanddl-operation.md).</span></span> <span data-ttu-id="58ddb-123">Para obtener más información, vea [operación ResolveNames](resolvenames-operation.md).</span><span class="sxs-lookup"><span data-stu-id="58ddb-123">For more information, see [ResolveNames operation](resolvenames-operation.md).</span></span>
  
<span data-ttu-id="58ddb-124">Las listas de distribución pública se encuentran en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="58ddb-124">Public distribution lists are located in Active Directory.</span></span> <span data-ttu-id="58ddb-125">Pueden ser cualquier grupo de distribución dinámico o habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="58ddb-125">They can be any mail-enabled or dynamic distribution group.</span></span> <span data-ttu-id="58ddb-126">El grupo no debe estar oculto en la lista de direcciones y cada miembro debe tener una dirección de correo electrónico no vacía.</span><span class="sxs-lookup"><span data-stu-id="58ddb-126">The group should not be hidden from the address list and each member should have a non-empty e-mail address.</span></span> <span data-ttu-id="58ddb-127">Los miembros de la lista de distribución pueden estar habilitados para correo y contactos, carpetas públicas y listas de distribución habilitadas para correo y grupos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="58ddb-127">Members of the distribution list can be mail-enabled users and contacts, public folders, and mail-enabled distribution lists and dynamic groups.</span></span>
  
<span data-ttu-id="58ddb-128">Las listas de distribución privadas se encuentran en la carpeta de contactos del buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="58ddb-128">Private distribution lists are located in the Contacts folder of a user's mailbox.</span></span> <span data-ttu-id="58ddb-129">Las listas de distribución privadas no tienen direcciones de correo electrónico para que sus identificadores de elemento de almacén se usen en una solicitud de ExpandDL.</span><span class="sxs-lookup"><span data-stu-id="58ddb-129">Private distribution lists do not have e-mail addresses so their store item identifiers are used in an ExpandDL request.</span></span> <span data-ttu-id="58ddb-130">Los miembros de una lista de distribución privada pueden ser usuarios con correo habilitado, contactos o listas de distribución de Active Directory, o de listas de distribución privadas o contactos de una carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="58ddb-130">Members of a private distribution list can be any mail-enabled user, contacts or distribution lists from Active Directory, or contacts or private distribution lists from a user's Contacts folder.</span></span>
  
<span data-ttu-id="58ddb-131">Para los contactos o listas de distribución privadas, los identificadores de elemento se devuelven en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58ddb-131">For contacts or private distribution lists, the item identifiers are returned in the response.</span></span> <span data-ttu-id="58ddb-132">Se puede usar para obtener información sobre el objeto o para expandir la pertenencia a una lista de distribución privada.</span><span class="sxs-lookup"><span data-stu-id="58ddb-132">This can be used to get information about the object or to expand membership in a private distribution list.</span></span>
  
## <a name="expanddl-private-distribution-list-request-example"></a><span data-ttu-id="58ddb-133">Ejemplo de solicitud de lista de distribución privada de ExpandDL</span><span class="sxs-lookup"><span data-stu-id="58ddb-133">ExpandDL Private Distribution List request example</span></span>

### <a name="description"></a><span data-ttu-id="58ddb-134">Description</span><span class="sxs-lookup"><span data-stu-id="58ddb-134">Description</span></span>

<span data-ttu-id="58ddb-135">El siguiente ejemplo de una solicitud ExpandDL muestra cómo crear una solicitud para expandir una lista de distribución privada.</span><span class="sxs-lookup"><span data-stu-id="58ddb-135">The following example of an ExpandDL request shows how to form a request to expand a private distribution list.</span></span>
  
### <a name="code"></a><span data-ttu-id="58ddb-136">Código</span><span class="sxs-lookup"><span data-stu-id="58ddb-136">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:ExpandDL>
      <m:Mailbox>
       <t:EmailAddress>test</t:EmailAddress>
      </m:Mailbox>
    </m:ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="58ddb-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58ddb-137">Comments</span></span>

<span data-ttu-id="58ddb-138">Para expandir una lista de distribución privada, el elemento [Mailbox](mailbox.md) contendrá el elemento [Itemid](itemid.md) que identifica una lista de distribución privada en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="58ddb-138">To expand a private distribution list, the [Mailbox](mailbox.md) element will contain the [ItemId](itemid.md) element that identifies a private distribution list in the user's mailbox.</span></span> 
  
## <a name="expanddl-public-distribution-list-request-example"></a><span data-ttu-id="58ddb-139">Ejemplo de solicitud de lista de distribución pública de ExpandDL</span><span class="sxs-lookup"><span data-stu-id="58ddb-139">ExpandDL Public Distribution List request example</span></span>

### <a name="description"></a><span data-ttu-id="58ddb-140">Description</span><span class="sxs-lookup"><span data-stu-id="58ddb-140">Description</span></span>

<span data-ttu-id="58ddb-141">El siguiente ejemplo de una solicitud ExpandDL muestra cómo crear una solicitud para expandir una lista de distribución pública.</span><span class="sxs-lookup"><span data-stu-id="58ddb-141">The following example of an ExpandDL request shows how to form a request to expand a public distribution list.</span></span> <span data-ttu-id="58ddb-142">En el ejemplo se muestra el uso de un nombre para mostrar para expandir una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="58ddb-142">The example shows the use of a display name to expand a distribution list.</span></span>
  
### <a name="code"></a><span data-ttu-id="58ddb-143">Código</span><span class="sxs-lookup"><span data-stu-id="58ddb-143">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
        <t:Mailbox>
          <t:EmailAddress>TheDistributionList</t:EmailAddress>
        </t:Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="58ddb-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58ddb-144">Comments</span></span>

<span data-ttu-id="58ddb-145">La respuesta a esta solicitud contendrá elementos de **buzón** que identifican cada buzón de correo de la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="58ddb-145">The response to this request will contain **Mailbox** elements that identify each mailbox in the distribution list.</span></span> <span data-ttu-id="58ddb-146">Si una lista de distribución está contenida en una lista de distribución, debe realizarse una expansión de la lista de distribución independiente en la lista de distribución incrustada.</span><span class="sxs-lookup"><span data-stu-id="58ddb-146">If a distribution list is contained within a distribution list, a separate distribution list expansion must be performed on the embedded distribution list.</span></span> <span data-ttu-id="58ddb-147">Si la lista de distribución no tiene miembros o la lista de distribución solicitada no existe, el atributo **ResponseClass** contendrá un valor igual al correcto.</span><span class="sxs-lookup"><span data-stu-id="58ddb-147">If the distribution list has no members or the requested distribution list does not exist, the **ResponseClass** attribute will contain a value equal to Success.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="58ddb-148">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="58ddb-148">Request elements</span></span>

<span data-ttu-id="58ddb-149">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="58ddb-149">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="58ddb-150">ExpandDL</span><span class="sxs-lookup"><span data-stu-id="58ddb-150">ExpandDL</span></span>](expanddl.md)
    
- [<span data-ttu-id="58ddb-151">Buzón</span><span class="sxs-lookup"><span data-stu-id="58ddb-151">Mailbox</span></span>](mailbox.md)
    
- <span data-ttu-id="58ddb-152">[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) se usa para identificar las listas de distribución públicas.</span><span class="sxs-lookup"><span data-stu-id="58ddb-152">[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) is used to identify public distribution lists.</span></span> <span data-ttu-id="58ddb-153">El elemento [Itemid](itemid.md) se usa para identificar las listas de distribución privadas.</span><span class="sxs-lookup"><span data-stu-id="58ddb-153">The [ItemId](itemid.md) element is used to identify private distribution lists.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="58ddb-154">El esquema que describe estos elementos se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="58ddb-154">The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="successful-expanddl-response-example"></a><span data-ttu-id="58ddb-155">Ejemplo de respuesta ExpandDL correcta</span><span class="sxs-lookup"><span data-stu-id="58ddb-155">Successful ExpandDL response example</span></span>

### <a name="description"></a><span data-ttu-id="58ddb-156">Description</span><span class="sxs-lookup"><span data-stu-id="58ddb-156">Description</span></span>

<span data-ttu-id="58ddb-157">El siguiente ejemplo de una respuesta de ExpandDL muestra una respuesta a la solicitud descrita anteriormente.</span><span class="sxs-lookup"><span data-stu-id="58ddb-157">The following example of an ExpandDL response shows a response to the request described above.</span></span> <span data-ttu-id="58ddb-158">La expansión de la lista de distribución describe lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="58ddb-158">The distribution list expansion describes the following:</span></span> 
  
- <span data-ttu-id="58ddb-159">Número de miembros de la lista de distribución que se devuelven en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58ddb-159">The number of members of the distribution list that are returned in the response.</span></span>
    
- <span data-ttu-id="58ddb-160">Si la respuesta contiene todos los miembros de la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="58ddb-160">Whether the response contains all the members of the distribution list.</span></span>
    
- <span data-ttu-id="58ddb-161">El nombre del buzón.</span><span class="sxs-lookup"><span data-stu-id="58ddb-161">The name of the mailbox.</span></span>
    
- <span data-ttu-id="58ddb-162">La dirección de correo electrónico del buzón.</span><span class="sxs-lookup"><span data-stu-id="58ddb-162">The e-mail address of the mailbox.</span></span>
    
- <span data-ttu-id="58ddb-163">El tipo de enrutamiento para el buzón.</span><span class="sxs-lookup"><span data-stu-id="58ddb-163">The routing type for the mailbox.</span></span>
    
- <span data-ttu-id="58ddb-164">El tipo de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="58ddb-164">The type of mailbox.</span></span>
    
> [!NOTE]
> <span data-ttu-id="58ddb-165">El nombre de la lista de distribución no se incluye en la respuesta; por lo tanto, debe realizar un seguimiento del nombre de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="58ddb-165">The distribution list name is not included in the response; therefore, you must keep track of the name from the request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="58ddb-166">Código</span><span class="sxs-lookup"><span data-stu-id="58ddb-166">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ExpandDLResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DLExpansion TotalItemsInView="3" IncludesLastItemInRange="true">
            <t:Mailbox>
              <t:Name>Dan Park</t:Name>
              <t:EmailAddress>dpark@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
            <t:Mailbox>
              <t:Name>Jeff Price</t:Name>
              <t:EmailAddress>jprice@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
            <t:Mailbox>
              <t:Name>Tanja Plate</t:Name>
              <t:EmailAddress>tplate@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
          </m:DLExpansion>
        </m:ExpandDLResponseMessage>
      </m:ResponseMessages>
    </ExpandDLResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="58ddb-167">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="58ddb-167">Successful response elements</span></span>

<span data-ttu-id="58ddb-168">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="58ddb-168">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="58ddb-169">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="58ddb-169">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="58ddb-170">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="58ddb-170">ExpandDLResponse</span></span>](expanddlresponse.md)
    
- [<span data-ttu-id="58ddb-171">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="58ddb-171">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="58ddb-172">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="58ddb-172">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
    
- [<span data-ttu-id="58ddb-173">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="58ddb-173">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="58ddb-174">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="58ddb-174">DLExpansion</span></span>](dlexpansion.md)
    
- [<span data-ttu-id="58ddb-175">Buzón</span><span class="sxs-lookup"><span data-stu-id="58ddb-175">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="58ddb-176">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="58ddb-176">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="58ddb-177">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="58ddb-177">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="58ddb-178">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="58ddb-178">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="58ddb-179">MailboxType</span><span class="sxs-lookup"><span data-stu-id="58ddb-179">MailboxType</span></span>](mailboxtype.md)
    
<span data-ttu-id="58ddb-180">Para buscar otras opciones para el mensaje de respuesta de la operación ExpandDL, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="58ddb-180">To find other options for the response message of the ExpandDL operation, explore the schema hierarchy.</span></span> <span data-ttu-id="58ddb-181">Empiece en el elemento [ExpandDLResponse](expanddlresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="58ddb-181">Start at the [ExpandDLResponse](expanddlresponse.md) element.</span></span> 
  
## <a name="expanddl-error-response"></a><span data-ttu-id="58ddb-182">Respuesta de error de ExpandDL</span><span class="sxs-lookup"><span data-stu-id="58ddb-182">ExpandDL error response</span></span>

### <a name="description"></a><span data-ttu-id="58ddb-183">Description</span><span class="sxs-lookup"><span data-stu-id="58ddb-183">Description</span></span>

<span data-ttu-id="58ddb-184">En el ejemplo siguiente se muestra una respuesta de error a una solicitud ExpandDL.</span><span class="sxs-lookup"><span data-stu-id="58ddb-184">The following example shows an error response to an ExpandDL request.</span></span>
  
### <a name="code"></a><span data-ttu-id="58ddb-185">Código</span><span class="sxs-lookup"><span data-stu-id="58ddb-185">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ExpandDLResponseMessage ResponseClass="Error">
          <m:MessageText>No results are found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ExpandDLResponseMessage>
      </m:ResponseMessages>
    </ExpandDLResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="58ddb-186">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="58ddb-186">Error response elements</span></span>

<span data-ttu-id="58ddb-187">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="58ddb-187">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="58ddb-188">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="58ddb-188">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="58ddb-189">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="58ddb-189">ExpandDLResponse</span></span>](expanddlresponse.md)
    
- [<span data-ttu-id="58ddb-190">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="58ddb-190">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="58ddb-191">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="58ddb-191">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
    
- [<span data-ttu-id="58ddb-192">MessageText</span><span class="sxs-lookup"><span data-stu-id="58ddb-192">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="58ddb-193">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="58ddb-193">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="58ddb-194">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="58ddb-194">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="58ddb-195">Para buscar otras opciones para el mensaje de respuesta de la operación ExpandDL, explore la jerarquía del esquema.</span><span class="sxs-lookup"><span data-stu-id="58ddb-195">To find other options for the response message of the ExpandDL operation, explore the schema hierarchy.</span></span> <span data-ttu-id="58ddb-196">Empiece en el elemento [ExpandDLResponse](expanddlresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="58ddb-196">Start at the [ExpandDLResponse](expanddlresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="58ddb-197">Vea también</span><span class="sxs-lookup"><span data-stu-id="58ddb-197">See also</span></span>

- [<span data-ttu-id="58ddb-198">Operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="58ddb-198">ResolveNames operation</span></span>](resolvenames-operation.md)
- [<span data-ttu-id="58ddb-199">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="58ddb-199">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

