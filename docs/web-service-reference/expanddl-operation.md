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
description: La operación de ExpandDL expone la pertenencia completa de las listas de distribución.
ms.openlocfilehash: 4af6198ff15407b7fb71cdb4010ff6ce035460d0
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353745"
---
# <a name="expanddl-operation"></a><span data-ttu-id="81d64-103">Operación ExpandDL</span><span class="sxs-lookup"><span data-stu-id="81d64-103">ExpandDL operation</span></span>

<span data-ttu-id="81d64-104">La operación de ExpandDL expone la pertenencia completa de las listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="81d64-104">The ExpandDL operation exposes the full membership of distribution lists.</span></span>
  
## <a name="using-the-expanddl-web-method"></a><span data-ttu-id="81d64-105">Mediante el método Web ExpandDL</span><span class="sxs-lookup"><span data-stu-id="81d64-105">Using the ExpandDL Web Method</span></span>

<span data-ttu-id="81d64-106">La operación de ExpandDL usa el servicio Web que se encuentra en Exchange.asmx.</span><span class="sxs-lookup"><span data-stu-id="81d64-106">The ExpandDL operation uses the Web service that is located in Exchange.asmx.</span></span> <span data-ttu-id="81d64-107">Este método de servicio Web acepta un elemento de [buzón de correo](mailbox.md) que puede contener un elemento secundario de [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) para una expansión de una lista de distribución pública o un elemento secundario de [ItemId](itemid.md) para la expansión de privado lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="81d64-107">This Web service method accepts a [Mailbox](mailbox.md) element that can contain either an [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) child element for an expansion of a public distribution list or an [ItemId](itemid.md) child element for the expansion of a private distribution list.</span></span> 
  
<span data-ttu-id="81d64-108">Listas de distribución públicas pueden ampliarse mediante uno de los procedimientos siguientes:</span><span class="sxs-lookup"><span data-stu-id="81d64-108">Public distribution lists can be expanded by using one of the following:</span></span>
  
1. <span data-ttu-id="81d64-109">Alias de la lista de distribución</span><span class="sxs-lookup"><span data-stu-id="81d64-109">Distribution list alias</span></span>
    
2. <span data-ttu-id="81d64-110">La dirección de Protocolo Simple de transferencia de correo (SMTP)</span><span class="sxs-lookup"><span data-stu-id="81d64-110">The Simple Mail Transfer Protocol (SMTP) address</span></span>
    
3. <span data-ttu-id="81d64-111">X400</span><span class="sxs-lookup"><span data-stu-id="81d64-111">X400</span></span>
    
4. <span data-ttu-id="81d64-112">X500</span><span class="sxs-lookup"><span data-stu-id="81d64-112">X500</span></span>
    
5. <span data-ttu-id="81d64-113">Dirección de Exchange heredado</span><span class="sxs-lookup"><span data-stu-id="81d64-113">Exchange Legacy address</span></span>
    
6. <span data-ttu-id="81d64-114">El nombre de la lista de distribución</span><span class="sxs-lookup"><span data-stu-id="81d64-114">The distribution list name</span></span>
    
7. <span data-ttu-id="81d64-115">El nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="81d64-115">The display name</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="81d64-116">Nombres para mostrar no son únicos.</span><span class="sxs-lookup"><span data-stu-id="81d64-116">Display names are not unique.</span></span> <span data-ttu-id="81d64-117">Varias cuentas pueden compartir el mismo nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="81d64-117">Multiple accounts can share the same display name.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="81d64-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81d64-118">Remarks</span></span>

<span data-ttu-id="81d64-119">No se admite la expansión de recursiva.</span><span class="sxs-lookup"><span data-stu-id="81d64-119">Recursive expansion is not supported.</span></span> <span data-ttu-id="81d64-120">Lista de distribución de un solo se puede expandir en una sola llamada.</span><span class="sxs-lookup"><span data-stu-id="81d64-120">Only one distribution list can be expanded in a single call.</span></span> <span data-ttu-id="81d64-121">Si más de una lista de distribución coinciden con los criterios, el servicio Web de informes de un error.</span><span class="sxs-lookup"><span data-stu-id="81d64-121">If more than one distribution list match the criteria, the Web service reports an error.</span></span> <span data-ttu-id="81d64-122">Una aplicación cliente puede usar resolución de nombres ambiguos (ANR) para encontrar la distribución ambiguo se enumera y, a continuación, eligió la dirección de correo electrónico correcta de la lista de distribución necesarios como un parámetro para la [operación de ExpandDL](expanddl-operation.md).</span><span class="sxs-lookup"><span data-stu-id="81d64-122">A client application can use ambiguous name resolution (ANR) to find ambiguous distribution lists and then chose the correct e-mail address of the required distribution list as a parameter for the [ExpandDL operation](expanddl-operation.md).</span></span> <span data-ttu-id="81d64-123">Para obtener más información, vea [ResolveNames operación](resolvenames-operation.md).</span><span class="sxs-lookup"><span data-stu-id="81d64-123">For more information, see [ResolveNames operation](resolvenames-operation.md).</span></span>
  
<span data-ttu-id="81d64-124">Listas de distribución públicas se encuentran en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="81d64-124">Public distribution lists are located in Active Directory.</span></span> <span data-ttu-id="81d64-125">Pueden ser cualquier grupo de distribución dinámico o habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="81d64-125">They can be any mail-enabled or dynamic distribution group.</span></span> <span data-ttu-id="81d64-126">El grupo no debería estar oculto desde la lista de direcciones y cada miembro debe tener una dirección de correo electrónico no está vacía.</span><span class="sxs-lookup"><span data-stu-id="81d64-126">The group should not be hidden from the address list and each member should have a non-empty e-mail address.</span></span> <span data-ttu-id="81d64-127">Los miembros de la lista de distribución pueden ser usuarios habilitados para correo y contactos, carpetas públicas y las listas de distribución habilitados para correo y grupos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="81d64-127">Members of the distribution list can be mail-enabled users and contacts, public folders, and mail-enabled distribution lists and dynamic groups.</span></span>
  
<span data-ttu-id="81d64-128">Listas de distribución privadas se encuentran en la carpeta de contactos del buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="81d64-128">Private distribution lists are located in the Contacts folder of a user's mailbox.</span></span> <span data-ttu-id="81d64-129">Listas de distribución privadas no tienen direcciones de correo electrónico para que sus identificadores de elemento de almacenamiento se usan en una solicitud de ExpandDL.</span><span class="sxs-lookup"><span data-stu-id="81d64-129">Private distribution lists do not have e-mail addresses so their store item identifiers are used in an ExpandDL request.</span></span> <span data-ttu-id="81d64-130">Los miembros de una lista de distribución privada pueden ser cualquier usuario habilitado para correo, contactos o listas de distribución de Active Directory o listas de contactos o distribución privada de carpeta de contactos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="81d64-130">Members of a private distribution list can be any mail-enabled user, contacts or distribution lists from Active Directory, or contacts or private distribution lists from a user's Contacts folder.</span></span>
  
<span data-ttu-id="81d64-131">Para los contactos o listas de distribución privadas, se devuelven los identificadores de elemento en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="81d64-131">For contacts or private distribution lists, the item identifiers are returned in the response.</span></span> <span data-ttu-id="81d64-132">Esto se puede usar para obtener información sobre el objeto o para expandir la pertenencia en una lista de distribución privada.</span><span class="sxs-lookup"><span data-stu-id="81d64-132">This can be used to get information about the object or to expand membership in a private distribution list.</span></span>
  
## <a name="expanddl-private-distribution-list-request-example"></a><span data-ttu-id="81d64-133">Ejemplo de solicitud de la lista de distribución privada de ExpandDL</span><span class="sxs-lookup"><span data-stu-id="81d64-133">ExpandDL Private Distribution List request example</span></span>

### <a name="description"></a><span data-ttu-id="81d64-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="81d64-134">Description</span></span>

<span data-ttu-id="81d64-135">El siguiente ejemplo de una solicitud de ExpandDL muestra cómo formar una solicitud para expandir una lista de distribución privada.</span><span class="sxs-lookup"><span data-stu-id="81d64-135">The following example of an ExpandDL request shows how to form a request to expand a private distribution list.</span></span>
  
### <a name="code"></a><span data-ttu-id="81d64-136">Código</span><span class="sxs-lookup"><span data-stu-id="81d64-136">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

### <a name="comments"></a><span data-ttu-id="81d64-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81d64-137">Comments</span></span>

<span data-ttu-id="81d64-138">Para expandir una lista de distribución privada, el elemento de [buzón de correo](mailbox.md) contendrá el elemento de [ItemId](itemid.md) que identifica una lista de distribución privada en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="81d64-138">To expand a private distribution list, the [Mailbox](mailbox.md) element will contain the [ItemId](itemid.md) element that identifies a private distribution list in the user's mailbox.</span></span> 
  
## <a name="expanddl-public-distribution-list-request-example"></a><span data-ttu-id="81d64-139">Ejemplo de solicitud de la lista de distribución públicas ExpandDL</span><span class="sxs-lookup"><span data-stu-id="81d64-139">ExpandDL Public Distribution List request example</span></span>

### <a name="description"></a><span data-ttu-id="81d64-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="81d64-140">Description</span></span>

<span data-ttu-id="81d64-141">El siguiente ejemplo de una solicitud de ExpandDL muestra cómo formar una solicitud para expandir una lista de distribución públicas.</span><span class="sxs-lookup"><span data-stu-id="81d64-141">The following example of an ExpandDL request shows how to form a request to expand a public distribution list.</span></span> <span data-ttu-id="81d64-142">En el ejemplo se muestra el uso de un nombre para mostrar para expandir una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="81d64-142">The example shows the use of a display name to expand a distribution list.</span></span>
  
### <a name="code"></a><span data-ttu-id="81d64-143">Código</span><span class="sxs-lookup"><span data-stu-id="81d64-143">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <t:Mailbox>
          <t:EmailAddress>TheDistributionList</t:EmailAddress>
        </t:Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="81d64-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81d64-144">Comments</span></span>

<span data-ttu-id="81d64-145">La respuesta a esta solicitud contendrá los elementos de **buzón de correo** que identifican cada buzón de correo en la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="81d64-145">The response to this request will contain **Mailbox** elements that identify each mailbox in the distribution list.</span></span> <span data-ttu-id="81d64-146">Si una lista de distribución está dentro de una lista de distribución, debe realizarse una expansión de lista de distribución independiente en la lista de distribución incrustado.</span><span class="sxs-lookup"><span data-stu-id="81d64-146">If a distribution list is contained within a distribution list, a separate distribution list expansion must be performed on the embedded distribution list.</span></span> <span data-ttu-id="81d64-147">Si la lista de distribución no tiene miembros o la lista de distribución solicitado no existe, el atributo **ResponseClass** contendrá un valor igual a correcto.</span><span class="sxs-lookup"><span data-stu-id="81d64-147">If the distribution list has no members or the requested distribution list does not exist, the **ResponseClass** attribute will contain a value equal to Success.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="81d64-148">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="81d64-148">Request elements</span></span>

<span data-ttu-id="81d64-149">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="81d64-149">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="81d64-150">ExpandDL</span><span class="sxs-lookup"><span data-stu-id="81d64-150">ExpandDL</span></span>](expanddl.md)
    
- [<span data-ttu-id="81d64-151">Mailbox</span><span class="sxs-lookup"><span data-stu-id="81d64-151">Mailbox</span></span>](mailbox.md)
    
- <span data-ttu-id="81d64-152">[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) se usa para identificar las listas de distribución públicas.</span><span class="sxs-lookup"><span data-stu-id="81d64-152">[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) is used to identify public distribution lists.</span></span> <span data-ttu-id="81d64-153">El elemento [ItemId](itemid.md) se usa para identificar las listas de distribución privadas.</span><span class="sxs-lookup"><span data-stu-id="81d64-153">The [ItemId](itemid.md) element is used to identify private distribution lists.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="81d64-154">El esquema que describe estos elementos se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="81d64-154">The schema that describes these elements is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="successful-expanddl-response-example"></a><span data-ttu-id="81d64-155">Ejemplo de respuesta correcta de ExpandDL</span><span class="sxs-lookup"><span data-stu-id="81d64-155">Successful ExpandDL response example</span></span>

### <a name="description"></a><span data-ttu-id="81d64-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="81d64-156">Description</span></span>

<span data-ttu-id="81d64-157">El siguiente ejemplo de una respuesta ExpandDL muestra una respuesta a la solicitud que se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="81d64-157">The following example of an ExpandDL response shows a response to the request described above.</span></span> <span data-ttu-id="81d64-158">La expansión de la lista de distribución describe lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="81d64-158">The distribution list expansion describes the following:</span></span> 
  
- <span data-ttu-id="81d64-159">El número de miembros de la lista de distribución que se devuelven en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="81d64-159">The number of members of the distribution list that are returned in the response.</span></span>
    
- <span data-ttu-id="81d64-160">Si la respuesta contiene a todos los miembros de la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="81d64-160">Whether the response contains all the members of the distribution list.</span></span>
    
- <span data-ttu-id="81d64-161">El nombre del buzón.</span><span class="sxs-lookup"><span data-stu-id="81d64-161">The name of the mailbox.</span></span>
    
- <span data-ttu-id="81d64-162">La dirección de correo electrónico del buzón.</span><span class="sxs-lookup"><span data-stu-id="81d64-162">The e-mail address of the mailbox.</span></span>
    
- <span data-ttu-id="81d64-163">El tipo de distribución para el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="81d64-163">The routing type for the mailbox.</span></span>
    
- <span data-ttu-id="81d64-164">El tipo de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="81d64-164">The type of mailbox.</span></span>
    
> [!NOTE]
> <span data-ttu-id="81d64-165">El nombre de la lista de distribución no se incluye en la respuesta; por lo tanto, debe realizar un seguimiento del nombre de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="81d64-165">The distribution list name is not included in the response; therefore, you must keep track of the name from the request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="81d64-166">Código</span><span class="sxs-lookup"><span data-stu-id="81d64-166">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a><span data-ttu-id="81d64-167">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="81d64-167">Successful response elements</span></span>

<span data-ttu-id="81d64-168">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="81d64-168">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="81d64-169">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="81d64-169">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="81d64-170">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="81d64-170">ExpandDLResponse</span></span>](expanddlresponse.md)
    
- [<span data-ttu-id="81d64-171">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="81d64-171">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="81d64-172">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="81d64-172">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
    
- [<span data-ttu-id="81d64-173">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="81d64-173">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="81d64-174">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="81d64-174">DLExpansion</span></span>](dlexpansion.md)
    
- [<span data-ttu-id="81d64-175">Mailbox</span><span class="sxs-lookup"><span data-stu-id="81d64-175">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="81d64-176">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="81d64-176">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="81d64-177">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="81d64-177">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="81d64-178">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="81d64-178">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="81d64-179">MailboxType</span><span class="sxs-lookup"><span data-stu-id="81d64-179">MailboxType</span></span>](mailboxtype.md)
    
<span data-ttu-id="81d64-180">Para buscar otras opciones para el mensaje de respuesta de la operación de ExpandDL, explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="81d64-180">To find other options for the response message of the ExpandDL operation, explore the schema hierarchy.</span></span> <span data-ttu-id="81d64-181">Comenzar en el elemento de [ExpandDLResponse](expanddlresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="81d64-181">Start at the [ExpandDLResponse](expanddlresponse.md) element.</span></span> 
  
## <a name="expanddl-error-response"></a><span data-ttu-id="81d64-182">Respuesta de error de ExpandDL</span><span class="sxs-lookup"><span data-stu-id="81d64-182">ExpandDL error response</span></span>

### <a name="description"></a><span data-ttu-id="81d64-183">Descripción</span><span class="sxs-lookup"><span data-stu-id="81d64-183">Description</span></span>

<span data-ttu-id="81d64-184">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de ExpandDL.</span><span class="sxs-lookup"><span data-stu-id="81d64-184">The following example shows an error response to an ExpandDL request.</span></span>
  
### <a name="code"></a><span data-ttu-id="81d64-185">Código</span><span class="sxs-lookup"><span data-stu-id="81d64-185">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="81d64-186">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="81d64-186">Error response elements</span></span>

<span data-ttu-id="81d64-187">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="81d64-187">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="81d64-188">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="81d64-188">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="81d64-189">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="81d64-189">ExpandDLResponse</span></span>](expanddlresponse.md)
    
- [<span data-ttu-id="81d64-190">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="81d64-190">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="81d64-191">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="81d64-191">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
    
- [<span data-ttu-id="81d64-192">MessageText</span><span class="sxs-lookup"><span data-stu-id="81d64-192">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="81d64-193">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="81d64-193">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="81d64-194">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="81d64-194">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="81d64-195">Para buscar otras opciones para el mensaje de respuesta de la operación de ExpandDL, explore la jerarquía de esquema.</span><span class="sxs-lookup"><span data-stu-id="81d64-195">To find other options for the response message of the ExpandDL operation, explore the schema hierarchy.</span></span> <span data-ttu-id="81d64-196">Comenzar en el elemento de [ExpandDLResponse](expanddlresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="81d64-196">Start at the [ExpandDLResponse](expanddlresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="81d64-197">Vea también</span><span class="sxs-lookup"><span data-stu-id="81d64-197">See also</span></span>

- [<span data-ttu-id="81d64-198">Operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="81d64-198">ResolveNames operation</span></span>](resolvenames-operation.md)
- [<span data-ttu-id="81d64-199">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="81d64-199">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

