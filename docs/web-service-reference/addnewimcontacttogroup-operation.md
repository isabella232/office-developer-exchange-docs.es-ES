---
title: Operación AddNewImContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cb5525f-faa3-48f1-9551-df55ffc26f46
description: Buscar información sobre la operación de EWS de AddNewImContactToGroup.
ms.openlocfilehash: e91cc067b4161b366e6713a9adc16873e63b1562
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465032"
---
# <a name="addnewimcontacttogroup-operation"></a><span data-ttu-id="83f1b-103">Operación AddNewImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="83f1b-103">AddNewImContactToGroup operation</span></span>

<span data-ttu-id="83f1b-104">Buscar información sobre la operación de EWS de **AddNewImContactToGroup** .</span><span class="sxs-lookup"><span data-stu-id="83f1b-104">Find information about the **AddNewImContactToGroup** EWS operation.</span></span> 
  
<span data-ttu-id="83f1b-105">La operación **AddNewImContactToGroup** agrega un nuevo contacto a un grupo de mensajería instantánea (mi).</span><span class="sxs-lookup"><span data-stu-id="83f1b-105">The **AddNewImContactToGroup** operation adds a new contact to an instant messaging (IM) group.</span></span> 
  
<span data-ttu-id="83f1b-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="83f1b-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addnewimcontacttogroup-operation"></a><span data-ttu-id="83f1b-107">Uso de la operación AddNewImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="83f1b-107">Using the AddNewImContactToGroup operation</span></span>

<span data-ttu-id="83f1b-108">La operación **AddNewImContactToGroup** toma los tres argumentos siguientes para agregar un nuevo contacto a un grupo de mensajería instantánea:</span><span class="sxs-lookup"><span data-stu-id="83f1b-108">The **AddNewImContactToGroup** operation takes the following three arguments to add a new contact to an IM group:</span></span> 
  
- <span data-ttu-id="83f1b-109">Propiedad **IMAddress** : identifica la dirección de mi del contacto.</span><span class="sxs-lookup"><span data-stu-id="83f1b-109">**ImAddress** property - Identifies the contact's IM address.</span></span> <span data-ttu-id="83f1b-110">Esta propiedad es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="83f1b-110">This property is required.</span></span> 
    
- <span data-ttu-id="83f1b-111">**DisplayName** Property: identifica el nombre para mostrar del contacto.</span><span class="sxs-lookup"><span data-stu-id="83f1b-111">**DisplayName** property - Identifies the contact's display name.</span></span> 
    
- <span data-ttu-id="83f1b-112">**GROUPID** propiedad: identifica el grupo al que se agrega el contacto.</span><span class="sxs-lookup"><span data-stu-id="83f1b-112">**GroupId** property - Identifies the group that the contact is added to.</span></span> 
    
<span data-ttu-id="83f1b-113">Esta operación devuelve el rol del contacto que se agregó al grupo.</span><span class="sxs-lookup"><span data-stu-id="83f1b-113">This operation returns the persona of the contact that was added to the group.</span></span>
  
### <a name="addnewimcontacttogroup-operation-soap-headers"></a><span data-ttu-id="83f1b-114">Encabezados SOAP de operación AddNewImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="83f1b-114">AddNewImContactToGroup operation SOAP headers</span></span>

<span data-ttu-id="83f1b-115">La operación **AddNewImContactToGroup** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="83f1b-115">The **AddNewImContactToGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="83f1b-116">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="83f1b-116">**Header name**</span></span>|<span data-ttu-id="83f1b-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="83f1b-117">**Element**</span></span>|<span data-ttu-id="83f1b-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="83f1b-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="83f1b-119">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="83f1b-119">**Impersonation**</span></span> <br/> |[<span data-ttu-id="83f1b-120">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="83f1b-120">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="83f1b-121">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="83f1b-121">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="83f1b-122">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="83f1b-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="83f1b-123">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="83f1b-123">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="83f1b-124">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="83f1b-124">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="83f1b-125">Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="83f1b-125">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="83f1b-126">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="83f1b-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="83f1b-127">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="83f1b-127">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="83f1b-128">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="83f1b-128">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="83f1b-129">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="83f1b-129">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="83f1b-130">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="83f1b-130">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="83f1b-131">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="83f1b-131">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="83f1b-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="83f1b-132">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="83f1b-133">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="83f1b-133">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="83f1b-134">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="83f1b-134">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="addnewimcontacttogroup-operation-request-example-add-a-new-im-contact-to-a-group"></a><span data-ttu-id="83f1b-135">Ejemplo de solicitud de operación AddNewImContactToGroup: agregar un nuevo contacto de mensajería instantánea a un grupo</span><span class="sxs-lookup"><span data-stu-id="83f1b-135">AddNewImContactToGroup operation request example: Add a new IM contact to a group</span></span>

<span data-ttu-id="83f1b-136">El siguiente ejemplo de una solicitud de operación de **AddNewImContactToGroup** muestra cómo agregar un nuevo contacto a un grupo de mensajería instantánea existente.</span><span class="sxs-lookup"><span data-stu-id="83f1b-136">The following example of an **AddNewImContactToGroup** operation request shows how to add a new contact to an existing IM group.</span></span> <span data-ttu-id="83f1b-137">El valor de la propiedad **GROUPID** de este ejemplo se ha devuelto a partir de los resultados de la [operación AddImGroup](addimgroup-operation.md).</span><span class="sxs-lookup"><span data-stu-id="83f1b-137">The **GroupId** property value for this example was returned from results of the [AddImGroup operation](addimgroup-operation.md).</span></span> <span data-ttu-id="83f1b-138">La propiedad **ExchangeStoreId** contiene el valor de la propiedad **GROUPID** .</span><span class="sxs-lookup"><span data-stu-id="83f1b-138">The **ExchangeStoreId** property contains the **GroupId** property value.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:AddNewImContactToGroup>
         <m:ImAddress>tsmith@contoso.com</m:ImAddress>
         <m:DisplayName>Tony Smith</m:DisplayName>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDAAAQKAAA="
                    ChangeKey="EgAAAA=="/>
      </m:AddNewImContactToGroup>
   </soap:Body>
</soap:Envelope>
```

> [!NOTE]
> <span data-ttu-id="83f1b-139">El valor del **GROUPID** se ha reducido para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="83f1b-139">The **GroupId** value has been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="83f1b-140">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="83f1b-140">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="83f1b-141">AddNewImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="83f1b-141">AddNewImContactToGroup</span></span>](addnewimcontacttogroup.md)
    
- [<span data-ttu-id="83f1b-142">IMAddress (cadena)</span><span class="sxs-lookup"><span data-stu-id="83f1b-142">ImAddress (String)</span></span>](imaddress-string.md)
    
- [<span data-ttu-id="83f1b-143">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="83f1b-143">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="83f1b-144">GroupId</span><span class="sxs-lookup"><span data-stu-id="83f1b-144">GroupId</span></span>](groupid.md)
    
## <a name="successful-addnewimcontacttogroup-operation-response"></a><span data-ttu-id="83f1b-145">Respuesta de operación AddNewImContactToGroup correcta</span><span class="sxs-lookup"><span data-stu-id="83f1b-145">Successful AddNewImContactToGroup operation response</span></span>

<span data-ttu-id="83f1b-146">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **AddNewImContactToGroup** .</span><span class="sxs-lookup"><span data-stu-id="83f1b-146">The following example shows a successful response to an **AddNewImContactToGroup** operation request.</span></span> <span data-ttu-id="83f1b-147">La respuesta contiene el rol del contacto recién creado.</span><span class="sxs-lookup"><span data-stu-id="83f1b-147">The response contains the persona of the newly created contact.</span></span> <span data-ttu-id="83f1b-148">El contacto se agrega a la carpeta contactos rápidos de Exchange.</span><span class="sxs-lookup"><span data-stu-id="83f1b-148">The contact is added to the Quick Contacts folder in Exchange.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="83f1b-149">Los identificadores se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="83f1b-149">Identifiers have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="349" 
                         MinorBuildNumber="0" 
                         Version="Exchange2013" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <AddNewImContactToGroupResponse ResponseClass="Success" 
                                    xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Persona>
        <PersonaId Id="AAQkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04ZjU5LWI3MTYzNGNkZmRkYQAQAJ3EkhEEXN5KufGbSYJanZk=" 
                   xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
        <PersonaType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Person</PersonaType>
        <CreationTime xmlns="https://schemas.microsoft.com/exchange/services/2006/types">2012-01-05T23:06:58Z</CreationTime>
        <DisplayName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Tony Smith</DisplayName>
        <DisplayNameFirstLast xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Tony Smith</DisplayNameFirstLast>
        <DisplayNameLastFirst xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Tony Smith</DisplayNameLastFirst>
        <FileAsId xmlns="https://schemas.microsoft.com/exchange/services/2006/types">None</FileAsId>
        <EmailAddress xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Tony Smith</Name>
          <Address>tsmith@contoso.com</Address>
          <RoutingType>SMTP</RoutingType>
        </EmailAddress>
        <EmailAddresses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <EmailAddress>
            <Name>Tony Smith</Name>
            <Address>tsmith@contoso.com</Address>
            <RoutingType>SMTP</RoutingType>
          </EmailAddress>
        </EmailAddresses>
        <ImAddress xmlns="https://schemas.microsoft.com/exchange/services/2006/types">tsmith@contoso.com</ImAddress>
        <RelevanceScore xmlns="https://schemas.microsoft.com/exchange/services/2006/types">2147483647</RelevanceScore>
        <Attributions xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Attribution>
            <Id>0</Id>
            <SourceId Id="BtF8oI7iVOQatt/bhQoTbWAAAAAAvcAAA=" 
                      ChangeKey="EQAAABYAAABtF8oIQoTbWAAAAAAyg" />
            <DisplayName>Outlook</DisplayName>
            <IsWritable>true</IsWritable>
            <IsQuickContact>true</IsQuickContact>
            <IsHidden>false</IsHidden>
            <FolderId Id="AAMkAGQ1MjJjMTBkLTc4YhQoTbWAAAAAAvZAAA=" 
                      ChangeKey="AQAAAA==" />
          </Attribution>
        </Attributions>
        <DisplayNames xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <StringAttributedValue>
            <Value>Tony Smith</Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </StringAttributedValue>
        </DisplayNames>
        <FileAsIds xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <StringAttributedValue>
            <Value>None</Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </StringAttributedValue>
        </FileAsIds>
        <Emails1 xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <EmailAddressAttributedValue>
            <Value>
              <Name>Tony Smith</Name>
              <Address>tsmith@contoso.com</Address>
              <RoutingType>SMTP</RoutingType>
            </Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </EmailAddressAttributedValue>
        </Emails1>
        <ImAddresses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <StringAttributedValue>
            <Value>tsmith@contoso.com</Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </StringAttributedValue>
        </ImAddresses>
      </Persona>
    </AddNewImContactToGroupResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="83f1b-150">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="83f1b-150">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="83f1b-151">AddNewImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="83f1b-151">AddNewImContactToGroupResponse</span></span>](addnewimcontacttogroupresponse.md)
    
- [<span data-ttu-id="83f1b-152">Rol</span><span class="sxs-lookup"><span data-stu-id="83f1b-152">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="83f1b-153">PersonaId</span><span class="sxs-lookup"><span data-stu-id="83f1b-153">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="83f1b-154">PersonaType</span><span class="sxs-lookup"><span data-stu-id="83f1b-154">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="83f1b-155">CreationTime</span><span class="sxs-lookup"><span data-stu-id="83f1b-155">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="83f1b-156">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="83f1b-156">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="83f1b-157">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="83f1b-157">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="83f1b-158">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="83f1b-158">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="83f1b-159">FileAsId</span><span class="sxs-lookup"><span data-stu-id="83f1b-159">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="83f1b-160">EmailAddress (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="83f1b-160">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
    
- [<span data-ttu-id="83f1b-161">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="83f1b-161">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="83f1b-162">Address (cadena)</span><span class="sxs-lookup"><span data-stu-id="83f1b-162">Address (string)</span></span>](address-string.md)
    
- [<span data-ttu-id="83f1b-163">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="83f1b-163">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="83f1b-164">IMAddress (cadena)</span><span class="sxs-lookup"><span data-stu-id="83f1b-164">ImAddress (String)</span></span>](imaddress-string.md)
    
- [<span data-ttu-id="83f1b-165">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="83f1b-165">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="83f1b-166">Atribuciones (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="83f1b-166">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="83f1b-167">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="83f1b-167">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="83f1b-168">ID (cadena)</span><span class="sxs-lookup"><span data-stu-id="83f1b-168">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="83f1b-169">SourceId</span><span class="sxs-lookup"><span data-stu-id="83f1b-169">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="83f1b-170">IsWritable</span><span class="sxs-lookup"><span data-stu-id="83f1b-170">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="83f1b-171">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="83f1b-171">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="83f1b-172">IsHidden</span><span class="sxs-lookup"><span data-stu-id="83f1b-172">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="83f1b-173">FolderId</span><span class="sxs-lookup"><span data-stu-id="83f1b-173">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="83f1b-174">DisplayNames</span><span class="sxs-lookup"><span data-stu-id="83f1b-174">DisplayNames</span></span>](displaynames.md)
    
- [<span data-ttu-id="83f1b-175">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="83f1b-175">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="83f1b-176">Valor (ArrayOfStringValueType)</span><span class="sxs-lookup"><span data-stu-id="83f1b-176">Value (ArrayOfStringValueType)</span></span>](value-arrayofstringvaluetype.md)
    
- [<span data-ttu-id="83f1b-177">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="83f1b-177">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="83f1b-178">Emails1</span><span class="sxs-lookup"><span data-stu-id="83f1b-178">Emails1</span></span>](emails1.md)
    
- [<span data-ttu-id="83f1b-179">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="83f1b-179">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md)
    
- [<span data-ttu-id="83f1b-180">Indirecciones</span><span class="sxs-lookup"><span data-stu-id="83f1b-180">ImAddresses</span></span>](imaddresses.md)
    
## <a name="addnewimcontacttogroup-operation-error-response"></a><span data-ttu-id="83f1b-181">Respuesta de error de operación de AddNewImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="83f1b-181">AddNewImContactToGroup operation error response</span></span>

<span data-ttu-id="83f1b-182">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **AddNewImContactToGroup** .</span><span class="sxs-lookup"><span data-stu-id="83f1b-182">The following example shows an error response to a **AddNewImContactToGroup** operation request.</span></span> <span data-ttu-id="83f1b-183">Se trata de una respuesta a una solicitud para agregar un contacto a un grupo que no está en el buzón de correo del solicitante.</span><span class="sxs-lookup"><span data-stu-id="83f1b-183">This is a response to a request to add a contact to a group that is not in the requester's mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="578" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddNewImContactToGroupResponse ResponseClass="Error" 
                                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>No mailbox with such guid.</MessageText>
         <ResponseCode>ErrorNonExistentMailbox</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <MessageXml>
            <t:Value Name="MailboxGuid" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">d5fasdadcw3d-23de-2341-8f59-b71523fsddda</t:Value>
         </MessageXml>
      </AddNewImContactToGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="83f1b-184">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="83f1b-184">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="83f1b-185">AddNewImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="83f1b-185">AddNewImContactToGroupResponse</span></span>](addnewimcontacttogroupresponse.md)
    
- [<span data-ttu-id="83f1b-186">MessageText</span><span class="sxs-lookup"><span data-stu-id="83f1b-186">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="83f1b-187">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="83f1b-187">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="83f1b-188">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="83f1b-188">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="83f1b-189">MessageXml</span><span class="sxs-lookup"><span data-stu-id="83f1b-189">MessageXml</span></span>](messagexml.md)
    
<span data-ttu-id="83f1b-190">Para obtener los códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="83f1b-190">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="83f1b-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="83f1b-191">See also</span></span>



[<span data-ttu-id="83f1b-192">Operación AddImGroup</span><span class="sxs-lookup"><span data-stu-id="83f1b-192">AddImGroup operation</span></span>](addimgroup-operation.md)
  
[<span data-ttu-id="83f1b-193">Operación AddImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="83f1b-193">AddImContactToGroup operation</span></span>](addimcontacttogroup-operation.md)
  
[<span data-ttu-id="83f1b-194">Operación AddImGroup</span><span class="sxs-lookup"><span data-stu-id="83f1b-194">AddImGroup operation</span></span>](addimgroup-operation.md)
  
[<span data-ttu-id="83f1b-195">Operación RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="83f1b-195">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
  
[<span data-ttu-id="83f1b-196">Operación SetImGroup</span><span class="sxs-lookup"><span data-stu-id="83f1b-196">SetImGroup operation</span></span>](setimgroup-operation.md)


[<span data-ttu-id="83f1b-197">Personas y contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="83f1b-197">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)

