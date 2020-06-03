---
title: Operación AddNewTelUriContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9688ce8-2465-45bb-8bd2-94b32ed4885c
description: Busque información sobre cómo usar la operación de EWS de AddNewTelUriContactToGroup.
ms.openlocfilehash: 91228ec627ad928d2f1837c135af24846f811b1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464948"
---
# <a name="addnewteluricontacttogroup-operation"></a><span data-ttu-id="6fb21-103">Operación AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="6fb21-103">AddNewTelUriContactToGroup operation</span></span>

<span data-ttu-id="6fb21-104">Busque información sobre cómo usar la operación de EWS de **AddNewTelUriContactToGroup** .</span><span class="sxs-lookup"><span data-stu-id="6fb21-104">Find information about how to use the **AddNewTelUriContactToGroup** EWS operation.</span></span> 
  
<span data-ttu-id="6fb21-105">La operación **AddNewTelUriContactToGroup** agrega un nuevo contacto a un grupo basado en el número de teléfono de un contacto.</span><span class="sxs-lookup"><span data-stu-id="6fb21-105">The **AddNewTelUriContactToGroup** operation adds a new contact to a group based on a contact's phone number.</span></span> 
  
<span data-ttu-id="6fb21-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6fb21-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addnewteluricontacttogroup-operation"></a><span data-ttu-id="6fb21-107">Uso de la operación AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="6fb21-107">Using the AddNewTelUriContactToGroup operation</span></span>

<span data-ttu-id="6fb21-108">Una solicitud de operación **AddNewTelUriContactToGroup** envía el URI de Tel de un contacto, el URI de SIP, el número de teléfono y el grupo al que se va a agregar el contacto.</span><span class="sxs-lookup"><span data-stu-id="6fb21-108">An **AddNewTelUriContactToGroup** operation request submits a contact's TEL URI, SIP URI, phone number, and the group to add the contact to.</span></span> <span data-ttu-id="6fb21-109">Una respuesta de operación **AddNewTelUriContactToGroup** crea un rol para el nuevo contacto.</span><span class="sxs-lookup"><span data-stu-id="6fb21-109">An **AddNewTelUriContactToGroup** operation response creates a persona for the new contact.</span></span> <span data-ttu-id="6fb21-110">Esta operación permite a los clientes agregar un nuevo contacto incluso si el contacto no tiene un nombre.</span><span class="sxs-lookup"><span data-stu-id="6fb21-110">This operation allows clients to add a new contact even if the contact does not have a name.</span></span> 
  
### <a name="addnewteluricontacttogroup-operation-soap-headers"></a><span data-ttu-id="6fb21-111">Encabezados SOAP de operación AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="6fb21-111">AddNewTelUriContactToGroup operation SOAP headers</span></span>

<span data-ttu-id="6fb21-112">La operación **AddNewTelUriContactToGroup** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6fb21-112">The **AddNewTelUriContactToGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="6fb21-113">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="6fb21-113">**Header name**</span></span>|<span data-ttu-id="6fb21-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6fb21-114">**Element**</span></span>|<span data-ttu-id="6fb21-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6fb21-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6fb21-116">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="6fb21-116">**Impersonation**</span></span> <br/> |[<span data-ttu-id="6fb21-117">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="6fb21-117">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="6fb21-118">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="6fb21-118">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="6fb21-119">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="6fb21-119">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="6fb21-120">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="6fb21-120">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="6fb21-121">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="6fb21-121">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="6fb21-122">Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="6fb21-122">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="6fb21-123">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="6fb21-123">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="6fb21-124">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="6fb21-124">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="6fb21-125">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="6fb21-125">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="6fb21-126">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="6fb21-126">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="6fb21-127">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="6fb21-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="6fb21-128">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="6fb21-128">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="6fb21-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="6fb21-129">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="6fb21-130">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6fb21-130">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="6fb21-131">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="6fb21-131">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="addnewteluricontacttogroup-operation-request-example-add-a-new-contact-to-a-group"></a><span data-ttu-id="6fb21-132">Ejemplo de solicitud de operación AddNewTelUriContactToGroup: agregar un nuevo contacto a un grupo</span><span class="sxs-lookup"><span data-stu-id="6fb21-132">AddNewTelUriContactToGroup operation request example: Add a new contact to a group</span></span>

<span data-ttu-id="6fb21-133">En el siguiente ejemplo de una solicitud de operación de **AddNewTelUriContactToGroup** se muestra cómo crear un nuevo contacto y agregar el nuevo contacto a un grupo de mensajería instantánea (mi) mediante los URI de teléfono y SIP del contacto.</span><span class="sxs-lookup"><span data-stu-id="6fb21-133">The following example of an **AddNewTelUriContactToGroup** operation request shows how to create a new contact and add the new contact to an instant messaging (IM) group by using the contact's TEL and SIP URIs.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6fb21-134">Todos los identificadores de elemento y las claves de cambio de este artículo se han reducido para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="6fb21-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
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
      <m:AddNewTelUriContactToGroup>
         <m:TelUriAddress>tel:5625550100</m:TelUriAddress>
         <m:ImContactSipUriAddress>sip:john@contoso.com</m:ImContactSipUriAddress>
         <m:ImTelephoneNumber>5625550100</m:ImTelephoneNumber>
         <m:GroupId Id="AAMkADEzOTm4QrAABY7+0GAAA="/>
      </m:AddNewTelUriContactToGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="6fb21-135">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="6fb21-135">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="6fb21-136">AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="6fb21-136">AddNewTelUriContactToGroup</span></span>](addnewteluricontacttogroup.md)
    
- [<span data-ttu-id="6fb21-137">TelUriAddress</span><span class="sxs-lookup"><span data-stu-id="6fb21-137">TelUriAddress</span></span>](teluriaddress.md)
    
- [<span data-ttu-id="6fb21-138">ImContactSipUriAddress</span><span class="sxs-lookup"><span data-stu-id="6fb21-138">ImContactSipUriAddress</span></span>](imcontactsipuriaddress.md)
    
- [<span data-ttu-id="6fb21-139">ImTelephoneNumber</span><span class="sxs-lookup"><span data-stu-id="6fb21-139">ImTelephoneNumber</span></span>](imtelephonenumber.md)
    
- [<span data-ttu-id="6fb21-140">GroupId</span><span class="sxs-lookup"><span data-stu-id="6fb21-140">GroupId</span></span>](groupid.md)
    
## <a name="successful-addnewteluricontacttogroup-operation-response"></a><span data-ttu-id="6fb21-141">Respuesta de operación AddNewTelUriContactToGroup correcta</span><span class="sxs-lookup"><span data-stu-id="6fb21-141">Successful AddNewTelUriContactToGroup operation response</span></span>

<span data-ttu-id="6fb21-142">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **AddNewTelUriContactToGroup** para crear un contacto.</span><span class="sxs-lookup"><span data-stu-id="6fb21-142">The following example shows a successful response to an **AddNewTelUriContactToGroup** operation request to create a contact.</span></span> <span data-ttu-id="6fb21-143">La respuesta contiene el identificador de rol asociado del contacto, el nombre para mostrar del rol, que en este caso se basa en el número de teléfono del contacto y el identificador de elemento del contacto, que se muestra como parte de la atribución del identificador de origen.</span><span class="sxs-lookup"><span data-stu-id="6fb21-143">The response contains the associated persona identifier for the contact, the display name of the persona, which in this case is based on the contact's phone number, and the contact's item identifier, which is displayed as part of the source identifier attribution.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"                           
            xmlns:xsd="http://www.w3.org/2001/XMLSchema"
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
   </s:Header>
   <s:Body>
      <AddNewTelUriContactToGroupResponse ResponseClass="Success" 
                                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <Persona>
            <t:PersonaId Id="AAQkADE686dX3s="/>
            <t:PersonaType>Person</t:PersonaType>
            <t:CreationTime>2012-10-29T23:10:13Z</t:CreationTime>
            <t:DisplayName/>
            <t:DisplayNameFirstLast>5625550100</t:DisplayNameFirstLast>
            <t:DisplayNameLastFirst>5625550100</t:DisplayNameLastFirst>
            <t:FileAs/>
            <t:FileAsId >None</t:FileAsId>
            <t:RelevanceScore >2147483647</t:RelevanceScore>
            <t:Attributions>
               <t:Attribution>
                  <t:Id>0</t:Id>
                  <t:SourceId Id="ABhHuhCAAA=" ChangeKey="EQAAABxFU"/>
                  <t:DisplayName>Lync Contacts</t:DisplayName>
                  <t:IsWritable>false</t:IsWritable>
                  <t:IsQuickContact>true</t:IsQuickContact>
                  <t:IsHidden>false</t:IsHidden>
               </t:Attribution>
            </t:Attributions>
            <t:FileAsIds>
               <t:StringAttributedValue>
                  <t:Value>None</t:Value>
                  <t:Attributions>
                     <t:Attribution>0</t:Attribution>
                  </t:Attributions>
               </t:StringAttributedValue>
            </t:FileAsIds>
            <t:OtherTelephones>
               <t:PhoneNumberAttributedValue>
                  <t:Value>
                     <t:Number>5625550100</t:Number>
                     <t:Type>Other</t:Type>
                  </t:Value>
                  <t:Attributions>
                     <t:Attribution>0</t:Attribution>
                  </t:Attributions>
               </t:PhoneNumberAttributedValue>
            </t:OtherTelephones>
         </Persona>
      </AddNewTelUriContactToGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="6fb21-144">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="6fb21-144">The response SOAP body contains following elements:</span></span>
  
- [<span data-ttu-id="6fb21-145">AddNewTelUriContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="6fb21-145">AddNewTelUriContactToGroupResponse</span></span>](addnewteluricontacttogroupresponse.md)
    
- [<span data-ttu-id="6fb21-146">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6fb21-146">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="6fb21-147">Rol</span><span class="sxs-lookup"><span data-stu-id="6fb21-147">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="6fb21-148">PersonaId</span><span class="sxs-lookup"><span data-stu-id="6fb21-148">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="6fb21-149">PersonaType</span><span class="sxs-lookup"><span data-stu-id="6fb21-149">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="6fb21-150">CreationTime</span><span class="sxs-lookup"><span data-stu-id="6fb21-150">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="6fb21-151">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="6fb21-151">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="6fb21-152">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="6fb21-152">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="6fb21-153">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="6fb21-153">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="6fb21-154">FileAs</span><span class="sxs-lookup"><span data-stu-id="6fb21-154">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="6fb21-155">FileAsId</span><span class="sxs-lookup"><span data-stu-id="6fb21-155">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="6fb21-156">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="6fb21-156">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="6fb21-157">Atribuciones (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="6fb21-157">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="6fb21-158">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="6fb21-158">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="6fb21-159">ID (cadena)</span><span class="sxs-lookup"><span data-stu-id="6fb21-159">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="6fb21-160">SourceId</span><span class="sxs-lookup"><span data-stu-id="6fb21-160">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="6fb21-161">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="6fb21-161">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="6fb21-162">IsWritable</span><span class="sxs-lookup"><span data-stu-id="6fb21-162">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="6fb21-163">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="6fb21-163">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="6fb21-164">IsHidden</span><span class="sxs-lookup"><span data-stu-id="6fb21-164">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="6fb21-165">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="6fb21-165">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="6fb21-166">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="6fb21-166">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="6fb21-167">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb21-167">Value</span></span>](value.md)
    
- [<span data-ttu-id="6fb21-168">Atribuciones (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="6fb21-168">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="6fb21-169">Atribución (cadena)</span><span class="sxs-lookup"><span data-stu-id="6fb21-169">Attribution (string)</span></span>](attribution-string.md)
    
- [<span data-ttu-id="6fb21-170">OtherTelephones</span><span class="sxs-lookup"><span data-stu-id="6fb21-170">OtherTelephones</span></span>](othertelephones.md)
    
- [<span data-ttu-id="6fb21-171">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="6fb21-171">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md)
    
- [<span data-ttu-id="6fb21-172">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb21-172">Value</span></span>](value.md)
    
- [<span data-ttu-id="6fb21-173">Number</span><span class="sxs-lookup"><span data-stu-id="6fb21-173">Number</span></span>](number.md)
    
- [<span data-ttu-id="6fb21-174">Tipo (cadena)</span><span class="sxs-lookup"><span data-stu-id="6fb21-174">Type (string)</span></span>](type-string.md)
    
- [<span data-ttu-id="6fb21-175">Atribuciones (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="6fb21-175">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="6fb21-176">Atribución (cadena)</span><span class="sxs-lookup"><span data-stu-id="6fb21-176">Attribution (string)</span></span>](attribution-string.md)
    
## <a name="addnewteluricontacttogroup-operation-error-response-example"></a><span data-ttu-id="6fb21-177">Ejemplo de respuesta de error de operación AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="6fb21-177">AddNewTelUriContactToGroup operation error response example</span></span>

<span data-ttu-id="6fb21-178">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **AddNewTelUriContactToGroup** cuando el identificador de grupo contiene un valor bien formado que no identifica a un grupo en el buzón.</span><span class="sxs-lookup"><span data-stu-id="6fb21-178">The following example shows an error response to an **AddNewTelUriContactToGroup** operation request when the group identifier contains a well-formed value that does not identify a group in the mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddNewTelUriContactToGroupResponse ResponseClass="Error" 
                                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </AddNewTelUriContactToGroupResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="6fb21-179">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="6fb21-179">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="6fb21-180">AddNewTelUriContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="6fb21-180">AddNewTelUriContactToGroupResponse</span></span>](addnewteluricontacttogroupresponse.md)
    
- [<span data-ttu-id="6fb21-181">MessageText</span><span class="sxs-lookup"><span data-stu-id="6fb21-181">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="6fb21-182">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6fb21-182">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="6fb21-183">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="6fb21-183">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="6fb21-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="6fb21-184">See also</span></span>

- [<span data-ttu-id="6fb21-185">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6fb21-185">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="6fb21-186">Personas y contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6fb21-186">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    

