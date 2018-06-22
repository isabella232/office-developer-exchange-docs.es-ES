---
title: Operación GetPersona
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e2146df0-53d0-4caf-9758-b600bbc14b6a
description: Busque información sobre la EWS GetPersona operación.
ms.openlocfilehash: c6ac357eaa34e9bae2fe0a79a4a2d02449100e78
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764944"
---
# <a name="getpersona-operation"></a><span data-ttu-id="ab0be-103">Operación GetPersona</span><span class="sxs-lookup"><span data-stu-id="ab0be-103">GetPersona operation</span></span>

<span data-ttu-id="ab0be-104">Obtenga información acerca de la operación de EWS **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="ab0be-104">Find information about the **GetPersona** EWS operation.</span></span> 
  
<span data-ttu-id="ab0be-105">La operación **GetPersona** devuelve un conjunto de propiedades que están asociados con un rol.</span><span class="sxs-lookup"><span data-stu-id="ab0be-105">The **GetPersona** operation returns a set of properties that are associated with a persona.</span></span> 
  
<span data-ttu-id="ab0be-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ab0be-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getpersona-operation"></a><span data-ttu-id="ab0be-107">Mediante la operación GetPersona</span><span class="sxs-lookup"><span data-stu-id="ab0be-107">Using the GetPersona operation</span></span>

<span data-ttu-id="ab0be-108">La operación **GetPersona** proporciona acceso a información de contacto agregada en el formulario de un rol.</span><span class="sxs-lookup"><span data-stu-id="ab0be-108">The **GetPersona** operation provides access to aggregated contact information in the form of a persona.</span></span> <span data-ttu-id="ab0be-109">El elemento [PersonaId](personaid.md) en la solicitud identifica el rol para devolver en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ab0be-109">The [PersonaId](personaid.md) element in the request identifies the persona to return in the response.</span></span> <span data-ttu-id="ab0be-110">La respuesta puede contener un conjunto predeterminado de propiedades de rol o un conjunto de propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="ab0be-110">The response can contain a default set of persona properties or a custom property set.</span></span> <span data-ttu-id="ab0be-111">Se recomienda que especifique una propiedad personalizada que se establezca de manera que las propiedades no utilizadas no se procesan y se envían desde el servidor al cliente.</span><span class="sxs-lookup"><span data-stu-id="ab0be-111">We recommend that you specify a custom property set so that unused properties are not processed and sent from the server to the client.</span></span> 
  
### <a name="getpersona-operation-soap-headers"></a><span data-ttu-id="ab0be-112">Encabezados SOAP de operación de GetPersona</span><span class="sxs-lookup"><span data-stu-id="ab0be-112">GetPersona operation SOAP headers</span></span>

<span data-ttu-id="ab0be-113">La operación de **GetPersona** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ab0be-113">The **GetPersona** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="ab0be-114">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="ab0be-114">**Header name**</span></span>|<span data-ttu-id="ab0be-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ab0be-115">**Element**</span></span>|<span data-ttu-id="ab0be-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab0be-116">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ab0be-117">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="ab0be-117">**Impersonation**</span></span> <br/> |[<span data-ttu-id="ab0be-118">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="ab0be-118">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="ab0be-119">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="ab0be-119">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="ab0be-120">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ab0be-120">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ab0be-121">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="ab0be-121">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="ab0be-122">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="ab0be-122">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="ab0be-123">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="ab0be-123">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="ab0be-124">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ab0be-124">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ab0be-125">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="ab0be-125">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="ab0be-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ab0be-126">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="ab0be-127">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ab0be-127">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="ab0be-128">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="ab0be-128">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getpersona-operation-request-example-return-a-default-set-of-properties-for-a-persona"></a><span data-ttu-id="ab0be-129">Ejemplo de solicitud de operación de GetPersona: devolver un conjunto predeterminado de propiedades para un rol</span><span class="sxs-lookup"><span data-stu-id="ab0be-129">GetPersona operation request example: Return a default set of properties for a persona</span></span>

<span data-ttu-id="ab0be-130">El siguiente ejemplo de una solicitud de operación **GetPersona** muestra cómo devolver un conjunto predeterminado de propiedades que están asociados con un rol.</span><span class="sxs-lookup"><span data-stu-id="ab0be-130">The following example of a **GetPersona** operation request shows how to return a default set of properties that are associated with a persona.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013"/>
   </soap:Header>
   <soap:Body xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <GetPersona>
         <PersonaId Id="AAQkADEzAQAKtOtR/l4MlLqHWORfhSYKU="/>
      </GetPersona>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="ab0be-131">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ab0be-131">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ab0be-132">GetPersona</span><span class="sxs-lookup"><span data-stu-id="ab0be-132">GetPersona</span></span>](getpersona.md)
    
- [<span data-ttu-id="ab0be-133">PersonaId</span><span class="sxs-lookup"><span data-stu-id="ab0be-133">PersonaId</span></span>](personaid.md)
    
## <a name="successful-getpersona-operation-response"></a><span data-ttu-id="ab0be-134">Respuesta es correcta de operación GetPersona</span><span class="sxs-lookup"><span data-stu-id="ab0be-134">Successful GetPersona operation response</span></span>

<span data-ttu-id="ab0be-135">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="ab0be-135">The following example shows a successful response to a **GetPersona** operation request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ab0be-136">Todos los identificadores de artículo y cambiar claves en este artículo se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="ab0be-136">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="432" 
                           MinorBuildNumber="5" 
                           Version="Exchange2013"
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                     xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetPersonaResponseMessage ResponseClass="Success"
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <Persona>
            <PersonaId Id="AAQkADEzAQAKtOtR="
              xmlns="http://schemas.microsoft.com/exchange/services/2006/types"/>
            <PersonaType xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Person</PersonaType>
            <CreationTime xmlns="http://schemas.microsoft.com/exchange/services/2006/types">2012-06-01T17:00:34Z</CreationTime>
            <DisplayName xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Brian Johnson</DisplayName>
            <DisplayNameFirstLast xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Brian Johnson</DisplayNameFirstLast>
            <DisplayNameLastFirst xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Johnson Brian</DisplayNameLastFirst>
            <FileAs xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Johnson, Brian</FileAs>
            <FileAsId xmlns="http://schemas.microsoft.com/exchange/services/2006/types">None</FileAsId>
            <GivenName xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Brian</GivenName>
            <Surname xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Johnsoon</Surname>
            <CompanyName xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Contoso</CompanyName>
            <RelevanceScore xmlns="http://schemas.microsoft.com/exchange/services/2006/types">4255550110</RelevanceScore>
            <Attributions xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <Attribution>
                  <Id>0</Id>
                  <SourceId Id="AAMkA =" ChangeKey="EQAAABY+"/>
                  <DisplayName>Outlook</DisplayName>
                  <IsWritable>true</IsWritable>
                  <IsQuickContact>false</IsQuickContact>
                  <IsHidden>false</IsHidden>
                  <FolderId Id="AAMkA=" ChangeKey="AQAAAA=="/>
               </Attribution>
            </Attributions>
            <DisplayNames xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Brian Johnson</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </DisplayNames>
            <FileAses xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Johnson, Brian</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </FileAses>
            <FileAsIds xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>None</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </FileAsIds>
            <GivenNames xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Brian</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </GivenNames>
            <Surnames xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Johnson</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </Surnames>
            <MobilePhones xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <PhoneNumberAttributedValue>
                  <Value>
                     <Number>(425)555-0110</Number>
                     <Type>Mobile</Type>
                  </Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </PhoneNumberAttributedValue>
            </MobilePhones>
            <CompanyNames xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Contoso</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </CompanyNames>
         </Persona>
      </GetPersonaResponseMessage>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="ab0be-137">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ab0be-137">The response SOAP body contains the following elements:</span></span>
  
- <span data-ttu-id="ab0be-138">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ab0be-138">GetPersonaResponseMessage</span></span>
    
- [<span data-ttu-id="ab0be-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ab0be-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ab0be-140">Rol</span><span class="sxs-lookup"><span data-stu-id="ab0be-140">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="ab0be-141">PersonaId</span><span class="sxs-lookup"><span data-stu-id="ab0be-141">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="ab0be-142">PersonaType</span><span class="sxs-lookup"><span data-stu-id="ab0be-142">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="ab0be-143">CreationTime</span><span class="sxs-lookup"><span data-stu-id="ab0be-143">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="ab0be-144">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="ab0be-144">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="ab0be-145">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="ab0be-145">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="ab0be-146">Archivar como</span><span class="sxs-lookup"><span data-stu-id="ab0be-146">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="ab0be-147">FileAsId</span><span class="sxs-lookup"><span data-stu-id="ab0be-147">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="ab0be-148">GivenName</span><span class="sxs-lookup"><span data-stu-id="ab0be-148">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="ab0be-149">Apellido</span><span class="sxs-lookup"><span data-stu-id="ab0be-149">Surname</span></span>](surname.md)
    
- [<span data-ttu-id="ab0be-150">CompanyName</span><span class="sxs-lookup"><span data-stu-id="ab0be-150">CompanyName</span></span>](companyname.md)
    
- [<span data-ttu-id="ab0be-151">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="ab0be-151">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="ab0be-152">Atribuciones (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="ab0be-152">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="ab0be-153">Atribución (cadena)</span><span class="sxs-lookup"><span data-stu-id="ab0be-153">Attribution (string)</span></span>](attribution-string.md)
    
- [<span data-ttu-id="ab0be-154">Identificador (cadena)</span><span class="sxs-lookup"><span data-stu-id="ab0be-154">ID (String)</span></span>](id-string.md)
    
- <span data-ttu-id="ab0be-155">[SourceId](sourceid.md) SourceId</span><span class="sxs-lookup"><span data-stu-id="ab0be-155">[SourceId](sourceid.md) SourceId</span></span> 
    
- [<span data-ttu-id="ab0be-156">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="ab0be-156">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="ab0be-157">IsWritable</span><span class="sxs-lookup"><span data-stu-id="ab0be-157">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="ab0be-158">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="ab0be-158">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="ab0be-159">IsHidden</span><span class="sxs-lookup"><span data-stu-id="ab0be-159">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="ab0be-160">FolderId</span><span class="sxs-lookup"><span data-stu-id="ab0be-160">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="ab0be-161">DisplayNames</span><span class="sxs-lookup"><span data-stu-id="ab0be-161">DisplayNames</span></span>](displaynames.md)
    
- [<span data-ttu-id="ab0be-162">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="ab0be-162">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="ab0be-163">Valor (ArrayOfStringValueType)</span><span class="sxs-lookup"><span data-stu-id="ab0be-163">Value (ArrayOfStringValueType)</span></span>](value-arrayofstringvaluetype.md)
    
- [<span data-ttu-id="ab0be-164">Atribuciones (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="ab0be-164">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="ab0be-165">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="ab0be-165">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="ab0be-166">FileAses</span><span class="sxs-lookup"><span data-stu-id="ab0be-166">FileAses</span></span>](fileases.md)
    
- [<span data-ttu-id="ab0be-167">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="ab0be-167">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="ab0be-168">GivenNames</span><span class="sxs-lookup"><span data-stu-id="ab0be-168">GivenNames</span></span>](givennames.md)
    
- [<span data-ttu-id="ab0be-169">Apellidos</span><span class="sxs-lookup"><span data-stu-id="ab0be-169">Surnames</span></span>](surnames.md)
    
- [<span data-ttu-id="ab0be-170">MobilePhones</span><span class="sxs-lookup"><span data-stu-id="ab0be-170">MobilePhones</span></span>](mobilephones.md)
    
- [<span data-ttu-id="ab0be-171">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="ab0be-171">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md)
    
- [<span data-ttu-id="ab0be-172">Valor (PersonaPhoneNumberType)</span><span class="sxs-lookup"><span data-stu-id="ab0be-172">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md)
    
- [<span data-ttu-id="ab0be-173">Número</span><span class="sxs-lookup"><span data-stu-id="ab0be-173">Number</span></span>](number.md)
    
- [<span data-ttu-id="ab0be-174">Tipo (cadena)</span><span class="sxs-lookup"><span data-stu-id="ab0be-174">Type (string)</span></span>](type-string.md)
    
- [<span data-ttu-id="ab0be-175">CompanyNames</span><span class="sxs-lookup"><span data-stu-id="ab0be-175">CompanyNames</span></span>](companynames.md)
    
## <a name="getpersona-operation-error-response"></a><span data-ttu-id="ab0be-176">Respuesta de error de la operación de GetPersona</span><span class="sxs-lookup"><span data-stu-id="ab0be-176">GetPersona operation error response</span></span>

<span data-ttu-id="ab0be-177">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="ab0be-177">The following example shows an error response to a **GetPersona** operation request.</span></span> <span data-ttu-id="ab0be-178">Esta es una respuesta a una solicitud que contiene un identificador de rol especificado incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="ab0be-178">This is a response to a request that contains an incorrectly specified persona identifier.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="578" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetPersonaResponseMessage ResponseClass="Error" 
                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Id is malformed.</MessageText>
         <ResponseCode>ErrorInvalidIdMalformed</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetPersonaResponseMessage>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="ab0be-179">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ab0be-179">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ab0be-180">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ab0be-180">GetPersonaResponseMessage</span></span>](getpersonaresponsemessage.md)
    
- [<span data-ttu-id="ab0be-181">MessageText</span><span class="sxs-lookup"><span data-stu-id="ab0be-181">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="ab0be-182">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ab0be-182">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ab0be-183">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ab0be-183">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="ab0be-184">Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="ab0be-184">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ab0be-185">Ver también</span><span class="sxs-lookup"><span data-stu-id="ab0be-185">See also</span></span>

- [<span data-ttu-id="ab0be-186">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ab0be-186">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="ab0be-187">Las personas y los contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ab0be-187">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="ab0be-188">Operación FindPeople</span><span class="sxs-lookup"><span data-stu-id="ab0be-188">FindPeople operation</span></span>](findpeople-operation.md)
    

