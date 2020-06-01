---
title: Operación FindPeople
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 446106b7-ff2d-4107-90c1-29f4d38ba128
description: Buscar información sobre la operación de EWS de FindPeople.
ms.openlocfilehash: ab5edc3f140e34123ce1f009c401ddd61a0e2598
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462911"
---
# <a name="findpeople-operation"></a><span data-ttu-id="cf56d-103">Operación FindPeople</span><span class="sxs-lookup"><span data-stu-id="cf56d-103">FindPeople operation</span></span>

<span data-ttu-id="cf56d-104">Buscar información sobre la operación de EWS de **FindPeople** .</span><span class="sxs-lookup"><span data-stu-id="cf56d-104">Find information about the **FindPeople** EWS operation.</span></span> 
  
<span data-ttu-id="cf56d-105">La operación **FindPeople** devuelve todos los objetos de rol de una carpeta de contactos especificada o recupera contactos que coinciden con una cadena de consulta especificada.</span><span class="sxs-lookup"><span data-stu-id="cf56d-105">The **FindPeople** operation returns all persona objects from a specified Contacts folder or retrieves contacts that match a specified query string.</span></span> 
  
<span data-ttu-id="cf56d-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cf56d-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-findpeople-operation"></a><span data-ttu-id="cf56d-107">Uso de la operación FindPeople</span><span class="sxs-lookup"><span data-stu-id="cf56d-107">Using the FindPeople operation</span></span>

<span data-ttu-id="cf56d-108">La operación **FindPeople** devuelve información de contacto agregada.</span><span class="sxs-lookup"><span data-stu-id="cf56d-108">The **FindPeople** operation returns aggregated contact information.</span></span> 
  
<span data-ttu-id="cf56d-109">La operación **FindPeople** se basa en la funcionalidad existente de los tipos complejos [Restriction](restriction.md) y [BaseShape](baseshape.md) agregando una restricción de agregación y la capacidad de devolver propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="cf56d-109">The **FindPeople** operation builds on the existing functionality of the [Restriction](restriction.md) and [BaseShape](baseshape.md) complex types by adding an aggregation restriction and the ability to return additional properties.</span></span> <span data-ttu-id="cf56d-110">Mediante el uso de una restricción, un cliente puede especificar filtros como "devolver solo los resultados que tienen una dirección de mensajería instantánea".</span><span class="sxs-lookup"><span data-stu-id="cf56d-110">By using a restriction, a client can specify filters such as "only return results that have an IM address".</span></span> <span data-ttu-id="cf56d-111">El comportamiento de búsqueda predeterminado tiene como objetivo el buzón personal del usuario especificado y la lista global de direcciones (GAL).</span><span class="sxs-lookup"><span data-stu-id="cf56d-111">The default search behavior targets both the specified user's personal mailbox and the global address list (GAL).</span></span> <span data-ttu-id="cf56d-112">Al buscar la GAL como carpeta de búsqueda principal, debe especificar una cadena de consulta en lugar de una restricción, ya que esta operación no permite examinar la GAL.</span><span class="sxs-lookup"><span data-stu-id="cf56d-112">When searching the GAL as the primary search folder, you must specify a query string instead of a restriction, because this operation does not allow for browsing of the GAL.</span></span> 
  
### <a name="findpeople-operation-soap-headers"></a><span data-ttu-id="cf56d-113">Encabezados SOAP de operación FindPeople</span><span class="sxs-lookup"><span data-stu-id="cf56d-113">FindPeople operation SOAP headers</span></span>

<span data-ttu-id="cf56d-114">La operación **FindPeople** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="cf56d-114">The **FindPeople** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="cf56d-115">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="cf56d-115">**Header name**</span></span>|<span data-ttu-id="cf56d-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cf56d-116">**Element**</span></span>|<span data-ttu-id="cf56d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cf56d-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cf56d-118">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="cf56d-118">**Impersonation**</span></span> <br/> |[<span data-ttu-id="cf56d-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="cf56d-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="cf56d-120">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="cf56d-120">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="cf56d-121">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf56d-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="cf56d-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="cf56d-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="cf56d-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="cf56d-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="cf56d-124">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="cf56d-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="cf56d-125">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf56d-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="cf56d-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="cf56d-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="cf56d-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="cf56d-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="cf56d-128">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf56d-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="cf56d-129">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf56d-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="findpeople-operation-request-example"></a><span data-ttu-id="cf56d-130">Ejemplo de solicitud de operación FindPeople</span><span class="sxs-lookup"><span data-stu-id="cf56d-130">FindPeople operation request example</span></span>

<span data-ttu-id="cf56d-131">El siguiente ejemplo de una solicitud de operación de **FindPeople** muestra cómo devolver los primeros 100 contactos de la carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="cf56d-131">The following example of a **FindPeople** operation request shows how to return the first 100 contacts from the Contacts folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:FindPeople>
         <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="100" Offset="0"/>
         <m:ParentFolderId>
            <t:DistinguishedFolderId Id="contacts"/>
         </m:ParentFolderId>
      </m:FindPeople>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="cf56d-132">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="cf56d-132">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="cf56d-133">FindPeople</span><span class="sxs-lookup"><span data-stu-id="cf56d-133">FindPeople</span></span>](findpeople.md)
    
- [<span data-ttu-id="cf56d-134">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="cf56d-134">IndexedPageItemView</span></span>](indexedpageitemview.md)
    
- [<span data-ttu-id="cf56d-135">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="cf56d-135">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)
    
- [<span data-ttu-id="cf56d-136">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="cf56d-136">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
<span data-ttu-id="cf56d-137">El siguiente ejemplo de una solicitud de operación de **FindPeople** muestra cómo devolver los primeros 100 contactos de la GAL mediante una cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="cf56d-137">The following example of a **FindPeople** operation request shows how to return the first 100 contacts from the GAL by using a query string.</span></span> <span data-ttu-id="cf56d-138">La configuración de **DistinguishedFolderId** en "Directory" buscará en la GAL como el origen principal de roles.</span><span class="sxs-lookup"><span data-stu-id="cf56d-138">Setting the **DistinguishedFolderId** to "directory" will search the GAL as the primary source of personas.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
    <m:FindPeople>
      <m:PersonaShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="persona:DisplayName"/>
          <t:FieldURI FieldURI="persona:Title"/>
        </t:AdditionalProperties>
      </m:PersonaShape>
      <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="100" Offset="0"/>
      <m:ParentFolderId>
        <t:DistinguishedFolderId Id="directory"/>
      </m:ParentFolderId>
      <m:QueryString>adams</m:QueryString>
    </m:FindPeople>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-findpeople-operation-response"></a><span data-ttu-id="cf56d-139">Respuesta de operación FindPeople correcta</span><span class="sxs-lookup"><span data-stu-id="cf56d-139">Successful FindPeople operation response</span></span>

<span data-ttu-id="cf56d-140">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **FindPeople** .</span><span class="sxs-lookup"><span data-stu-id="cf56d-140">The following example shows a successful response to a **FindPeople** operation request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope 
   xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
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
    <FindPeopleResponse ResponseClass="Success" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <People>
        <Persona xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <PersonaId Id="AAQkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04ZjU5LWI3MTYzNGNkZmRkYQAQAOjFqObcLmtOlzlRnHdXQjo=" />
          <CreationTime>2012-01-11T22:25:37Z</CreationTime>
          <DisplayName>Terry Adams</DisplayName>
          <DisplayNameFirstLast>Terry Adams</DisplayNameFirstLast>
          <DisplayNameLastFirst>Adams Terry</DisplayNameLastFirst>
          <FileAs>Adams, Terry</FileAs>
          <GivenName>Terry</GivenName>
          <Surname>Adams</Surname>
          <EmailAddress>
            <Name>terry@litwareinc.com</Name>
            <EmailAddress>terry@litwareinc.com</EmailAddress>
            <RoutingType>SMTP</RoutingType>
          </EmailAddress>
          <EmailAddresses>
            <EmailAddress>
              <Name>terry@litwareinc.com</Name>
              <EmailAddress>terry@litwareinc.com</EmailAddress>
              <RoutingType>SMTP</RoutingType>
            </EmailAddress>
            <EmailAddress>
              <Name>tadams@contoso.com</Name>
              <EmailAddress>tadams@contoso.com</EmailAddress>
              <RoutingType>SMTP</RoutingType>
            </EmailAddress>
          </EmailAddresses>
          <RelevanceScore>2147483647</RelevanceScore>
        </Persona>
      </People>
      <TotalNumberOfPeopleInView>1</TotalNumberOfPeopleInView>
    </FindPeopleResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="cf56d-141">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="cf56d-141">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="cf56d-142">FindPeopleResponse</span><span class="sxs-lookup"><span data-stu-id="cf56d-142">FindPeopleResponse</span></span>](findpeopleresponse.md)
    
- [<span data-ttu-id="cf56d-143">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cf56d-143">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="cf56d-144">Personas</span><span class="sxs-lookup"><span data-stu-id="cf56d-144">People</span></span>](people.md)
    
- [<span data-ttu-id="cf56d-145">Rol</span><span class="sxs-lookup"><span data-stu-id="cf56d-145">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="cf56d-146">PersonaId</span><span class="sxs-lookup"><span data-stu-id="cf56d-146">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="cf56d-147">CreationTime</span><span class="sxs-lookup"><span data-stu-id="cf56d-147">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="cf56d-148">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="cf56d-148">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="cf56d-149">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="cf56d-149">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="cf56d-150">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="cf56d-150">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="cf56d-151">FileAs</span><span class="sxs-lookup"><span data-stu-id="cf56d-151">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="cf56d-152">GivenName</span><span class="sxs-lookup"><span data-stu-id="cf56d-152">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="cf56d-153">Apellido</span><span class="sxs-lookup"><span data-stu-id="cf56d-153">Surname</span></span>](surname.md)
    
- [<span data-ttu-id="cf56d-154">EmailAddresses (ArrayOfEmailAddressesType)</span><span class="sxs-lookup"><span data-stu-id="cf56d-154">EmailAddresses (ArrayOfEmailAddressesType)</span></span>](emailaddresses-arrayofemailaddressestype.md)
    
- [<span data-ttu-id="cf56d-155">EmailAddress (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="cf56d-155">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
    
- [<span data-ttu-id="cf56d-156">Nombre (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="cf56d-156">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="cf56d-157">EmailAddress (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="cf56d-157">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
    
- [<span data-ttu-id="cf56d-158">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="cf56d-158">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="cf56d-159">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="cf56d-159">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="cf56d-160">TotalNumberOfPeopleInView</span><span class="sxs-lookup"><span data-stu-id="cf56d-160">TotalNumberOfPeopleInView</span></span>](totalnumberofpeopleinview.md)
    
## <a name="findpeople-operation-error-response"></a><span data-ttu-id="cf56d-161">Respuesta de error de operación de FindPeople</span><span class="sxs-lookup"><span data-stu-id="cf56d-161">FindPeople operation error response</span></span>

<span data-ttu-id="cf56d-162">Para los códigos de error que son genéricos para EWS, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="cf56d-162">For error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf56d-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf56d-163">See also</span></span>

- [<span data-ttu-id="cf56d-164">Personas y contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cf56d-164">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="cf56d-165">Operación GetPersona</span><span class="sxs-lookup"><span data-stu-id="cf56d-165">GetPersona operation</span></span>](getpersona-operation.md)
    

