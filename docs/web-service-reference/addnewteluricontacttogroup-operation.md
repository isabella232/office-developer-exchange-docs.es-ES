---
title: Operación AddNewTelUriContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9688ce8-2465-45bb-8bd2-94b32ed4885c
description: Obtenga información sobre cómo usar la operación de EWS AddNewTelUriContactToGroup.
ms.openlocfilehash: 34450171776b4215d9c0a39700a309e2e2d755dd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763410"
---
# <a name="addnewteluricontacttogroup-operation"></a><span data-ttu-id="1a3bf-103">Operación AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="1a3bf-103">AddNewTelUriContactToGroup operation</span></span>

<span data-ttu-id="1a3bf-104">Obtenga información sobre cómo usar la operación de EWS **AddNewTelUriContactToGroup** .</span><span class="sxs-lookup"><span data-stu-id="1a3bf-104">Find information about how to use the **AddNewTelUriContactToGroup** EWS operation.</span></span> 
  
<span data-ttu-id="1a3bf-105">La operación **AddNewTelUriContactToGroup** agrega un nuevo contacto a un grupo basado en el número de teléfono de un contacto.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-105">The **AddNewTelUriContactToGroup** operation adds a new contact to a group based on a contact's phone number.</span></span> 
  
<span data-ttu-id="1a3bf-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addnewteluricontacttogroup-operation"></a><span data-ttu-id="1a3bf-107">Mediante la operación AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="1a3bf-107">Using the AddNewTelUriContactToGroup operation</span></span>

<span data-ttu-id="1a3bf-108">Una solicitud de operación **AddNewTelUriContactToGroup** envía URI de TEL de un contacto, el URI del SIP, número de teléfono y el grupo para agregar el contacto a.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-108">An **AddNewTelUriContactToGroup** operation request submits a contact's TEL URI, SIP URI, phone number, and the group to add the contact to.</span></span> <span data-ttu-id="1a3bf-109">Una respuesta de la operación de **AddNewTelUriContactToGroup** crea un rol para el nuevo contacto.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-109">An **AddNewTelUriContactToGroup** operation response creates a persona for the new contact.</span></span> <span data-ttu-id="1a3bf-110">Esta operación permite a los clientes agregar un nuevo contacto, incluso si el contacto no tiene un nombre.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-110">This operation allows clients to add a new contact even if the contact does not have a name.</span></span> 
  
### <a name="addnewteluricontacttogroup-operation-soap-headers"></a><span data-ttu-id="1a3bf-111">Encabezados SOAP de operación de AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="1a3bf-111">AddNewTelUriContactToGroup operation SOAP headers</span></span>

<span data-ttu-id="1a3bf-112">La operación de **AddNewTelUriContactToGroup** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-112">The **AddNewTelUriContactToGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="1a3bf-113">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="1a3bf-113">**Header name**</span></span>|<span data-ttu-id="1a3bf-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="1a3bf-114">**Element**</span></span>|<span data-ttu-id="1a3bf-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1a3bf-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1a3bf-116">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="1a3bf-116">**Impersonation**</span></span> <br/> |[<span data-ttu-id="1a3bf-117">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="1a3bf-117">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="1a3bf-118">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-118">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="1a3bf-119">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-119">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="1a3bf-120">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="1a3bf-120">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="1a3bf-121">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="1a3bf-121">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="1a3bf-122">Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-122">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="1a3bf-123">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-123">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="1a3bf-124">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="1a3bf-124">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="1a3bf-125">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="1a3bf-125">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="1a3bf-126">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-126">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="1a3bf-127">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="1a3bf-128">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="1a3bf-128">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="1a3bf-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="1a3bf-129">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="1a3bf-130">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-130">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="1a3bf-131">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-131">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="addnewteluricontacttogroup-operation-request-example-add-a-new-contact-to-a-group"></a><span data-ttu-id="1a3bf-132">Ejemplo de solicitud de operación de AddNewTelUriContactToGroup: agregar un nuevo contacto a un grupo</span><span class="sxs-lookup"><span data-stu-id="1a3bf-132">AddNewTelUriContactToGroup operation request example: Add a new contact to a group</span></span>

<span data-ttu-id="1a3bf-133">El siguiente ejemplo de una solicitud de operación **AddNewTelUriContactToGroup** muestra cómo crear un nuevo contacto y agregar el nuevo contacto a un grupo de (IM) de mensajería instantáneo mediante el uso de TEL y el URI de SIP del contacto.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-133">The following example of an **AddNewTelUriContactToGroup** operation request shows how to create a new contact and add the new contact to an instant messaging (IM) group by using the contact's TEL and SIP URIs.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1a3bf-134">Todos los identificadores de artículo y cambiar claves en este artículo se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="1a3bf-135">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="1a3bf-135">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="1a3bf-136">AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="1a3bf-136">AddNewTelUriContactToGroup</span></span>](addnewteluricontacttogroup.md)
    
- [<span data-ttu-id="1a3bf-137">TelUriAddress</span><span class="sxs-lookup"><span data-stu-id="1a3bf-137">TelUriAddress</span></span>](teluriaddress.md)
    
- [<span data-ttu-id="1a3bf-138">ImContactSipUriAddress</span><span class="sxs-lookup"><span data-stu-id="1a3bf-138">ImContactSipUriAddress</span></span>](imcontactsipuriaddress.md)
    
- [<span data-ttu-id="1a3bf-139">ImTelephoneNumber</span><span class="sxs-lookup"><span data-stu-id="1a3bf-139">ImTelephoneNumber</span></span>](imtelephonenumber.md)
    
- [<span data-ttu-id="1a3bf-140">GroupId</span><span class="sxs-lookup"><span data-stu-id="1a3bf-140">GroupId</span></span>](groupid.md)
    
## <a name="successful-addnewteluricontacttogroup-operation-response"></a><span data-ttu-id="1a3bf-141">Respuesta es correcta de operación AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="1a3bf-141">Successful AddNewTelUriContactToGroup operation response</span></span>

<span data-ttu-id="1a3bf-142">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **AddNewTelUriContactToGroup** para crear un contacto.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-142">The following example shows a successful response to an **AddNewTelUriContactToGroup** operation request to create a contact.</span></span> <span data-ttu-id="1a3bf-143">La respuesta contiene el identificador de rol asociado para el contacto, el nombre para mostrar del rol, que en este caso se basa en el número de teléfono del contacto, y el identificador del elemento del contacto, que se muestra como parte de la atribución de identificador de origen.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-143">The response contains the associated persona identifier for the contact, the display name of the persona, which in this case is based on the contact's phone number, and the contact's item identifier, which is displayed as part of the source identifier attribution.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"                           
            xmlns:xsd="http://www.w3.org/2001/XMLSchema"
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" />
   </s:Header>
   <s:Body>
      <AddNewTelUriContactToGroupResponse ResponseClass="Success" 
                                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="1a3bf-144">Contiene la respuesta SOAP body siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="1a3bf-144">The response SOAP body contains following elements:</span></span>
  
- [<span data-ttu-id="1a3bf-145">AddNewTelUriContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="1a3bf-145">AddNewTelUriContactToGroupResponse</span></span>](addnewteluricontacttogroupresponse.md)
    
- [<span data-ttu-id="1a3bf-146">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1a3bf-146">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="1a3bf-147">Rol</span><span class="sxs-lookup"><span data-stu-id="1a3bf-147">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="1a3bf-148">PersonaId</span><span class="sxs-lookup"><span data-stu-id="1a3bf-148">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="1a3bf-149">PersonaType</span><span class="sxs-lookup"><span data-stu-id="1a3bf-149">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="1a3bf-150">CreationTime</span><span class="sxs-lookup"><span data-stu-id="1a3bf-150">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="1a3bf-151">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="1a3bf-151">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="1a3bf-152">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="1a3bf-152">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="1a3bf-153">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="1a3bf-153">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="1a3bf-154">Archivar como</span><span class="sxs-lookup"><span data-stu-id="1a3bf-154">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="1a3bf-155">FileAsId</span><span class="sxs-lookup"><span data-stu-id="1a3bf-155">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="1a3bf-156">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="1a3bf-156">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="1a3bf-157">Atribuciones (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="1a3bf-157">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="1a3bf-158">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="1a3bf-158">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="1a3bf-159">Identificador (cadena)</span><span class="sxs-lookup"><span data-stu-id="1a3bf-159">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="1a3bf-160">SourceId</span><span class="sxs-lookup"><span data-stu-id="1a3bf-160">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="1a3bf-161">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="1a3bf-161">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="1a3bf-162">IsWritable</span><span class="sxs-lookup"><span data-stu-id="1a3bf-162">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="1a3bf-163">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="1a3bf-163">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="1a3bf-164">IsHidden</span><span class="sxs-lookup"><span data-stu-id="1a3bf-164">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="1a3bf-165">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="1a3bf-165">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="1a3bf-166">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="1a3bf-166">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="1a3bf-167">Valor</span><span class="sxs-lookup"><span data-stu-id="1a3bf-167">Value</span></span>](value.md)
    
- [<span data-ttu-id="1a3bf-168">Atribuciones (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="1a3bf-168">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="1a3bf-169">Atribución (cadena)</span><span class="sxs-lookup"><span data-stu-id="1a3bf-169">Attribution (string)</span></span>](attribution-string.md)
    
- [<span data-ttu-id="1a3bf-170">OtherTelephones</span><span class="sxs-lookup"><span data-stu-id="1a3bf-170">OtherTelephones</span></span>](othertelephones.md)
    
- [<span data-ttu-id="1a3bf-171">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="1a3bf-171">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md)
    
- [<span data-ttu-id="1a3bf-172">Valor</span><span class="sxs-lookup"><span data-stu-id="1a3bf-172">Value</span></span>](value.md)
    
- [<span data-ttu-id="1a3bf-173">Número</span><span class="sxs-lookup"><span data-stu-id="1a3bf-173">Number</span></span>](number.md)
    
- [<span data-ttu-id="1a3bf-174">Tipo (cadena)</span><span class="sxs-lookup"><span data-stu-id="1a3bf-174">Type (string)</span></span>](type-string.md)
    
- [<span data-ttu-id="1a3bf-175">Atribuciones (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="1a3bf-175">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="1a3bf-176">Atribución (cadena)</span><span class="sxs-lookup"><span data-stu-id="1a3bf-176">Attribution (string)</span></span>](attribution-string.md)
    
## <a name="addnewteluricontacttogroup-operation-error-response-example"></a><span data-ttu-id="1a3bf-177">Ejemplo de respuesta de error de operación de AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="1a3bf-177">AddNewTelUriContactToGroup operation error response example</span></span>

<span data-ttu-id="1a3bf-178">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **AddNewTelUriContactToGroup** cuando el identificador de grupo contiene un valor correcto que no identifica un grupo en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="1a3bf-178">The following example shows an error response to an **AddNewTelUriContactToGroup** operation request when the group identifier contains a well-formed value that does not identify a group in the mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddNewTelUriContactToGroupResponse ResponseClass="Error" 
                                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </AddNewTelUriContactToGroupResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="1a3bf-179">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="1a3bf-179">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="1a3bf-180">AddNewTelUriContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="1a3bf-180">AddNewTelUriContactToGroupResponse</span></span>](addnewteluricontacttogroupresponse.md)
    
- [<span data-ttu-id="1a3bf-181">MessageText</span><span class="sxs-lookup"><span data-stu-id="1a3bf-181">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="1a3bf-182">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1a3bf-182">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="1a3bf-183">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1a3bf-183">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="1a3bf-184">Ver también</span><span class="sxs-lookup"><span data-stu-id="1a3bf-184">See also</span></span>

- [<span data-ttu-id="1a3bf-185">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1a3bf-185">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="1a3bf-186">Las personas y los contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1a3bf-186">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    

