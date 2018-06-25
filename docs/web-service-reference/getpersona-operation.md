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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764944"
---
# <a name="getpersona-operation"></a><span data-ttu-id="2c517-103">Operación GetPersona</span><span class="sxs-lookup"><span data-stu-id="2c517-103">GetPersona operation</span></span>

<span data-ttu-id="2c517-104">Obtenga información acerca de la operación de EWS **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="2c517-104">Find information about the **GetPersona** EWS operation.</span></span> 
  
<span data-ttu-id="2c517-105">La operación **GetPersona** devuelve un conjunto de propiedades que están asociados con un rol.</span><span class="sxs-lookup"><span data-stu-id="2c517-105">The **GetPersona** operation returns a set of properties that are associated with a persona.</span></span> 
  
<span data-ttu-id="2c517-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2c517-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getpersona-operation"></a><span data-ttu-id="2c517-107">Mediante la operación GetPersona</span><span class="sxs-lookup"><span data-stu-id="2c517-107">Using the GetPersona operation</span></span>

<span data-ttu-id="2c517-108">La operación **GetPersona** proporciona acceso a información de contacto agregada en el formulario de un rol.</span><span class="sxs-lookup"><span data-stu-id="2c517-108">The **GetPersona** operation provides access to aggregated contact information in the form of a persona.</span></span> <span data-ttu-id="2c517-109">El elemento [PersonaId](personaid.md) en la solicitud identifica el rol para devolver en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c517-109">The [PersonaId](personaid.md) element in the request identifies the persona to return in the response.</span></span> <span data-ttu-id="2c517-110">La respuesta puede contener un conjunto predeterminado de propiedades de rol o un conjunto de propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2c517-110">The response can contain a default set of persona properties or a custom property set.</span></span> <span data-ttu-id="2c517-111">Se recomienda que especifique una propiedad personalizada que se establezca de manera que las propiedades no utilizadas no se procesan y se envían desde el servidor al cliente.</span><span class="sxs-lookup"><span data-stu-id="2c517-111">We recommend that you specify a custom property set so that unused properties are not processed and sent from the server to the client.</span></span> 
  
### <a name="getpersona-operation-soap-headers"></a><span data-ttu-id="2c517-112">Encabezados SOAP de operación de GetPersona</span><span class="sxs-lookup"><span data-stu-id="2c517-112">GetPersona operation SOAP headers</span></span>

<span data-ttu-id="2c517-113">La operación de **GetPersona** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2c517-113">The **GetPersona** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="2c517-114">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="2c517-114">**Header name**</span></span>|<span data-ttu-id="2c517-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c517-115">**Element**</span></span>|<span data-ttu-id="2c517-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2c517-116">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2c517-117">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="2c517-117">**Impersonation**</span></span> <br/> |[<span data-ttu-id="2c517-118">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="2c517-118">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="2c517-119">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="2c517-119">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="2c517-120">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="2c517-120">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="2c517-121">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="2c517-121">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="2c517-122">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="2c517-122">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="2c517-123">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="2c517-123">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="2c517-124">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="2c517-124">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="2c517-125">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="2c517-125">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="2c517-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2c517-126">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="2c517-127">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2c517-127">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="2c517-128">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c517-128">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getpersona-operation-request-example-return-a-default-set-of-properties-for-a-persona"></a><span data-ttu-id="2c517-129">Ejemplo de solicitud de operación de GetPersona: devolver un conjunto predeterminado de propiedades para un rol</span><span class="sxs-lookup"><span data-stu-id="2c517-129">GetPersona operation request example: Return a default set of properties for a persona</span></span>

<span data-ttu-id="2c517-130">El siguiente ejemplo de una solicitud de operación **GetPersona** muestra cómo devolver un conjunto predeterminado de propiedades que están asociados con un rol.</span><span class="sxs-lookup"><span data-stu-id="2c517-130">The following example of a **GetPersona** operation request shows how to return a default set of properties that are associated with a persona.</span></span> 
  
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

<span data-ttu-id="2c517-131">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="2c517-131">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2c517-132">GetPersona</span><span class="sxs-lookup"><span data-stu-id="2c517-132">GetPersona</span></span>](getpersona.md)
    
- [<span data-ttu-id="2c517-133">PersonaId</span><span class="sxs-lookup"><span data-stu-id="2c517-133">PersonaId</span></span>](personaid.md)
    
## <a name="successful-getpersona-operation-response"></a><span data-ttu-id="2c517-134">Respuesta es correcta de operación GetPersona</span><span class="sxs-lookup"><span data-stu-id="2c517-134">Successful GetPersona operation response</span></span>

<span data-ttu-id="2c517-135">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="2c517-135">The following example shows a successful response to a **GetPersona** operation request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2c517-136">Todos los identificadores de artículo y cambiar claves en este artículo se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="2c517-136">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
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

<span data-ttu-id="2c517-137">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="2c517-137">The response SOAP body contains the following elements:</span></span>
  
- <span data-ttu-id="2c517-138">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2c517-138">GetPersonaResponseMessage</span></span>
    
- [<span data-ttu-id="2c517-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2c517-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2c517-140">Rol</span><span class="sxs-lookup"><span data-stu-id="2c517-140">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="2c517-141">PersonaId</span><span class="sxs-lookup"><span data-stu-id="2c517-141">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="2c517-142">PersonaType</span><span class="sxs-lookup"><span data-stu-id="2c517-142">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="2c517-143">CreationTime</span><span class="sxs-lookup"><span data-stu-id="2c517-143">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="2c517-144">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="2c517-144">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="2c517-145">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="2c517-145">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="2c517-146">Archivar como</span><span class="sxs-lookup"><span data-stu-id="2c517-146">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="2c517-147">FileAsId</span><span class="sxs-lookup"><span data-stu-id="2c517-147">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="2c517-148">GivenName</span><span class="sxs-lookup"><span data-stu-id="2c517-148">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="2c517-149">Apellido</span><span class="sxs-lookup"><span data-stu-id="2c517-149">Surname</span></span>](surname.md)
    
- [<span data-ttu-id="2c517-150">CompanyName</span><span class="sxs-lookup"><span data-stu-id="2c517-150">CompanyName</span></span>](companyname.md)
    
- [<span data-ttu-id="2c517-151">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="2c517-151">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="2c517-152">Atribuciones (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="2c517-152">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="2c517-153">Atribución (cadena)</span><span class="sxs-lookup"><span data-stu-id="2c517-153">Attribution (string)</span></span>](attribution-string.md)
    
- [<span data-ttu-id="2c517-154">Identificador (cadena)</span><span class="sxs-lookup"><span data-stu-id="2c517-154">ID (String)</span></span>](id-string.md)
    
- <span data-ttu-id="2c517-155">[SourceId](sourceid.md) SourceId</span><span class="sxs-lookup"><span data-stu-id="2c517-155">[SourceId](sourceid.md) SourceId</span></span> 
    
- [<span data-ttu-id="2c517-156">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="2c517-156">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="2c517-157">IsWritable</span><span class="sxs-lookup"><span data-stu-id="2c517-157">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="2c517-158">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="2c517-158">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="2c517-159">IsHidden</span><span class="sxs-lookup"><span data-stu-id="2c517-159">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="2c517-160">FolderId</span><span class="sxs-lookup"><span data-stu-id="2c517-160">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="2c517-161">DisplayNames</span><span class="sxs-lookup"><span data-stu-id="2c517-161">DisplayNames</span></span>](displaynames.md)
    
- [<span data-ttu-id="2c517-162">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="2c517-162">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="2c517-163">Valor (ArrayOfStringValueType)</span><span class="sxs-lookup"><span data-stu-id="2c517-163">Value (ArrayOfStringValueType)</span></span>](value-arrayofstringvaluetype.md)
    
- [<span data-ttu-id="2c517-164">Atribuciones (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="2c517-164">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="2c517-165">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="2c517-165">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="2c517-166">FileAses</span><span class="sxs-lookup"><span data-stu-id="2c517-166">FileAses</span></span>](fileases.md)
    
- [<span data-ttu-id="2c517-167">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="2c517-167">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="2c517-168">GivenNames</span><span class="sxs-lookup"><span data-stu-id="2c517-168">GivenNames</span></span>](givennames.md)
    
- [<span data-ttu-id="2c517-169">Apellidos</span><span class="sxs-lookup"><span data-stu-id="2c517-169">Surnames</span></span>](surnames.md)
    
- [<span data-ttu-id="2c517-170">MobilePhones</span><span class="sxs-lookup"><span data-stu-id="2c517-170">MobilePhones</span></span>](mobilephones.md)
    
- [<span data-ttu-id="2c517-171">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="2c517-171">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md)
    
- [<span data-ttu-id="2c517-172">Valor (PersonaPhoneNumberType)</span><span class="sxs-lookup"><span data-stu-id="2c517-172">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md)
    
- [<span data-ttu-id="2c517-173">Número</span><span class="sxs-lookup"><span data-stu-id="2c517-173">Number</span></span>](number.md)
    
- [<span data-ttu-id="2c517-174">Tipo (cadena)</span><span class="sxs-lookup"><span data-stu-id="2c517-174">Type (string)</span></span>](type-string.md)
    
- [<span data-ttu-id="2c517-175">CompanyNames</span><span class="sxs-lookup"><span data-stu-id="2c517-175">CompanyNames</span></span>](companynames.md)
    
## <a name="getpersona-operation-error-response"></a><span data-ttu-id="2c517-176">Respuesta de error de la operación de GetPersona</span><span class="sxs-lookup"><span data-stu-id="2c517-176">GetPersona operation error response</span></span>

<span data-ttu-id="2c517-177">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="2c517-177">The following example shows an error response to a **GetPersona** operation request.</span></span> <span data-ttu-id="2c517-178">Esta es una respuesta a una solicitud que contiene un identificador de rol especificado incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="2c517-178">This is a response to a request that contains an incorrectly specified persona identifier.</span></span> 
  
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

<span data-ttu-id="2c517-179">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="2c517-179">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2c517-180">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2c517-180">GetPersonaResponseMessage</span></span>](getpersonaresponsemessage.md)
    
- [<span data-ttu-id="2c517-181">MessageText</span><span class="sxs-lookup"><span data-stu-id="2c517-181">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="2c517-182">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2c517-182">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2c517-183">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2c517-183">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="2c517-184">Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="2c517-184">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2c517-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c517-185">See also</span></span>

- [<span data-ttu-id="2c517-186">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2c517-186">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="2c517-187">Las personas y los contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2c517-187">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="2c517-188">Operación FindPeople</span><span class="sxs-lookup"><span data-stu-id="2c517-188">FindPeople operation</span></span>](findpeople-operation.md)
    

