---
title: Operación GetDiscoverySearchConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8a54a6dc-110c-4972-a8bc-5ddb43c4b857
description: Buscar información sobre la operación de EWS de GetDiscoverySearchConfiguration.
ms.openlocfilehash: 4db435988a9954b921e7851986b6f92ffedbad94
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461026"
---
# <a name="getdiscoverysearchconfiguration-operation"></a><span data-ttu-id="a3b9a-103">Operación GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3b9a-103">GetDiscoverySearchConfiguration operation</span></span>

<span data-ttu-id="a3b9a-104">Buscar información sobre la operación de EWS de **GetDiscoverySearchConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="a3b9a-104">Find information about the **GetDiscoverySearchConfiguration** EWS operation.</span></span> 
  
<span data-ttu-id="a3b9a-105">La operación **GetDiscoverySearchConfiguration** devuelve información de configuración para las suspensiones locales, las búsquedas de detección guardadas y los buzones que están habilitados para la búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-105">The **GetDiscoverySearchConfiguration** operation returns configuration information for in-place holds, saved discovery searches, and the mailboxes that are enabled for discovery search.</span></span> 
  
<span data-ttu-id="a3b9a-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getdiscoverysearchconfiguration-operation"></a><span data-ttu-id="a3b9a-107">Uso de la operación GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3b9a-107">Using the GetDiscoverySearchConfiguration operation</span></span>

<span data-ttu-id="a3b9a-108">La operación **GetDiscoverySearchConfiguration** proporciona información de configuración para la búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-108">The **GetDiscoverySearchConfiguration** operation provides configuration information for discovery search.</span></span> <span data-ttu-id="a3b9a-109">Las solicitudes pueden contener uno o varios de los siguientes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a3b9a-109">Requests can contain one or more of the following arguments:</span></span> 
  
1. <span data-ttu-id="a3b9a-110">[SearchId](searchid.md) : identifica una búsqueda de detección guardada.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-110">[SearchId](searchid.md) — Identifies a saved discovery search.</span></span> <span data-ttu-id="a3b9a-111">Si se envía este argumento en la solicitud, se omiten los valores de los demás argumentos.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-111">If this argument is sent in the request, the values of the other arguments are ignored.</span></span> 
    
2. <span data-ttu-id="a3b9a-112">[ExpandGroupMembership](expandgroupmembership.md) : indica si la pertenencia al grupo se expande en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-112">[ExpandGroupMembership](expandgroupmembership.md) — Indicates whether group membership is expanded in the response.</span></span> <span data-ttu-id="a3b9a-113">Un valor de **true** indica que la pertenencia a grupos se expande para que todos los buzones de correo que se pueden buscar se devuelvan en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-113">A value of **true** indicates that group membership is expanded so that all searchable mailboxes are returned in the response.</span></span> <span data-ttu-id="a3b9a-114">Un valor de **false** indica que solo se devuelve el grupo en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-114">A value of **false** indicates that only the group is returned in the response.</span></span> 
    
3. <span data-ttu-id="a3b9a-115">[InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) : indica si todos los buzones de correo que se pueden buscar se devuelven además de la configuración de conservación local.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-115">[InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) — Indicates whether all searchable mailboxes are returned in addition to the in-place hold configuration.</span></span> <span data-ttu-id="a3b9a-116">Un valor de **true** indica que solo se devuelven las configuraciones de conservación local.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-116">A value of **true** indicates that only the in-place hold configurations are returned.</span></span> <span data-ttu-id="a3b9a-117">Un valor de **false** indica que se devuelven todos los identificadores de buzones de correo que se pueden buscar, además de los identificadores de retención local.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-117">A value of **false** indicates that all searchable mailbox identifiers are returned in addition to the in-place hold identifiers.</span></span> <span data-ttu-id="a3b9a-118">Si este elemento no está presente, el comportamiento predeterminado es el equivalente del valor **false**.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-118">If this element is not present, the default behavior is the equivalent of the value **false**.</span></span> 
    
### <a name="getdiscoverysearchconfiguration-operation-soap-headers"></a><span data-ttu-id="a3b9a-119">Encabezados SOAP de operación GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3b9a-119">GetDiscoverySearchConfiguration operation SOAP headers</span></span>

<span data-ttu-id="a3b9a-120">La operación **GetDiscoverySearchConfiguration** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-120">The **GetDiscoverySearchConfiguration** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="a3b9a-121">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="a3b9a-121">**Header name**</span></span>|<span data-ttu-id="a3b9a-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a3b9a-122">**Element**</span></span>|<span data-ttu-id="a3b9a-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3b9a-123">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a3b9a-124">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="a3b9a-124">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="a3b9a-125">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="a3b9a-125">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="a3b9a-126">Identifica los roles de servidor que son necesarios para que el autor de la llamada realice la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-126">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="a3b9a-127">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="a3b9a-128">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="a3b9a-128">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="a3b9a-129">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="a3b9a-129">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="a3b9a-130">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-130">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="a3b9a-131">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-131">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="a3b9a-132">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="a3b9a-132">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="a3b9a-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a3b9a-133">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="a3b9a-134">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-134">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="a3b9a-135">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-135">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getdiscoverysearchconfiguration-operation-request-example-get-the-discovery-search-configuration-for-a-saved-search"></a><span data-ttu-id="a3b9a-136">Ejemplo de solicitud de operación GetDiscoverySearchConfiguration: obtener la configuración de búsqueda de detección para una búsqueda guardada</span><span class="sxs-lookup"><span data-stu-id="a3b9a-136">GetDiscoverySearchConfiguration operation request example: Get the discovery search configuration for a saved search</span></span>

<span data-ttu-id="a3b9a-137">El siguiente ejemplo de una solicitud de operación de **GetDiscoverySearchConfiguration** muestra cómo solicitar la configuración de una búsqueda guardada denominada "MyDiscSearchFor-sbrown".</span><span class="sxs-lookup"><span data-stu-id="a3b9a-137">The following example of a **GetDiscoverySearchConfiguration** operation request shows how to request the configuration of a saved search called "MyDiscSearchFor-sbrown".</span></span> <span data-ttu-id="a3b9a-138">Se omiten los argumentos de los elementos [ExpandGroupMembership](expandgroupmembership.md) y [InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) .</span><span class="sxs-lookup"><span data-stu-id="a3b9a-138">The arguments for the [ExpandGroupMembership](expandgroupmembership.md) and [InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) elements are ignored.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetDiscoverySearchConfiguration>
         <m:SearchId>MyDiscSearchFor-sbrown</m:SearchId>
         <m:ExpandGroupMembership>true</m:ExpandGroupMembership>
         <m:InPlaceHoldConfigurationOnly>false</m:InPlaceHoldConfigurationOnly>
      </m:GetDiscoverySearchConfiguration>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="a3b9a-139">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="a3b9a-139">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="a3b9a-140">GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3b9a-140">GetDiscoverySearchConfiguration</span></span>](getdiscoverysearchconfiguration.md)
    
- [<span data-ttu-id="a3b9a-141">SearchId</span><span class="sxs-lookup"><span data-stu-id="a3b9a-141">SearchId</span></span>](searchid.md)
    
- [<span data-ttu-id="a3b9a-142">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="a3b9a-142">ExpandGroupMembership</span></span>](expandgroupmembership.md)
    
- [<span data-ttu-id="a3b9a-143">InPlaceHoldConfigurationOnly</span><span class="sxs-lookup"><span data-stu-id="a3b9a-143">InPlaceHoldConfigurationOnly</span></span>](inplaceholdconfigurationonly.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-a-single-saved-search"></a><span data-ttu-id="a3b9a-144">Respuesta de operación GetDiscoverySearchConfiguration correcta: solicitud de una búsqueda guardada única</span><span class="sxs-lookup"><span data-stu-id="a3b9a-144">Successful GetDiscoverySearchConfiguration operation response: Request for a single saved search</span></span>

<span data-ttu-id="a3b9a-145">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **GetDiscoverySearchConfiguration** para obtener la configuración de una búsqueda guardada denominada "MyDiscSearchFor-sbrown".</span><span class="sxs-lookup"><span data-stu-id="a3b9a-145">The following example shows a successful response to a **GetDiscoverySearchConfiguration** operation request to get the configuration of a saved search called "MyDiscSearchFor-sbrown".</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="526" MinorBuildNumber="0" Version="Exchange2013" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetDiscoverySearchConfigurationResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <DiscoverySearchConfigurations>
        <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <SearchId>MyDiscSearchFor-sbrown</SearchId>
          <SearchQuery>test item</SearchQuery>
          <SearchableMailboxes>
            <SearchableMailbox>
              <Guid>3c620d04-8b22-432e-92be-5b9321599576</Guid>
              <PrimarySmtpAddress>SBrown@contoso.com</PrimarySmtpAddress>
              <IsExternalMailbox>false</IsExternalMailbox>
              <ExternalEmailAddress/>
              <DisplayName>Steven Brown</DisplayName>
              <IsMembershipGroup>false</IsMembershipGroup>
              <ReferenceId>/o=First/ou=Exchange(FYDILT)/cn=Recipients/cn=313ecf-Steve</ReferenceId>
            </SearchableMailbox>
          </SearchableMailboxes>
        </DiscoverySearchConfiguration>
      </DiscoverySearchConfigurations>
    </GetDiscoverySearchConfigurationResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="a3b9a-146">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="a3b9a-146">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="a3b9a-147">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="a3b9a-147">GetDiscoverySearchConfigurationResponse</span></span>](getdiscoverysearchconfigurationresponse.md)
    
- [<span data-ttu-id="a3b9a-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a3b9a-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a3b9a-149">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="a3b9a-149">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md)
    
- [<span data-ttu-id="a3b9a-150">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3b9a-150">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
    
- [<span data-ttu-id="a3b9a-151">SearchId</span><span class="sxs-lookup"><span data-stu-id="a3b9a-151">SearchId</span></span>](searchid.md)
    
- [<span data-ttu-id="a3b9a-152">SearchQuery</span><span class="sxs-lookup"><span data-stu-id="a3b9a-152">SearchQuery</span></span>](searchquery.md)
    
- [<span data-ttu-id="a3b9a-153">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="a3b9a-153">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
- [<span data-ttu-id="a3b9a-154">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="a3b9a-154">SearchableMailbox</span></span>](searchablemailbox.md)
    
- [<span data-ttu-id="a3b9a-155">Guid</span><span class="sxs-lookup"><span data-stu-id="a3b9a-155">Guid</span></span>](guid-ex15websvcsotherref.md)
    
- [<span data-ttu-id="a3b9a-156">PrimarySmtpAddress (cadena)</span><span class="sxs-lookup"><span data-stu-id="a3b9a-156">PrimarySmtpAddress (string)</span></span>](primarysmtpaddress-string.md)
    
- [<span data-ttu-id="a3b9a-157">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="a3b9a-157">IsExternalMailbox</span></span>](isexternalmailbox.md)
    
- [<span data-ttu-id="a3b9a-158">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="a3b9a-158">ExternalEmailAddress</span></span>](externalemailaddress.md)
    
- [<span data-ttu-id="a3b9a-159">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="a3b9a-159">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="a3b9a-160">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="a3b9a-160">IsMembershipGroup</span></span>](ismembershipgroup.md)
    
- [<span data-ttu-id="a3b9a-161">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="a3b9a-161">ReferenceId</span></span>](referenceid.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-in-place-holds"></a><span data-ttu-id="a3b9a-162">Respuesta de operación GetDiscoverySearchConfiguration correcta: solicitud de retenciones locales</span><span class="sxs-lookup"><span data-stu-id="a3b9a-162">Successful GetDiscoverySearchConfiguration operation response: Request for in-place holds</span></span>

<span data-ttu-id="a3b9a-163">En el siguiente ejemplo se muestra una respuesta correcta a una solicitud de operación **GetDiscoverySearchConfiguration** para obtener solo las suspensiones locales.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-163">The following example shows a successful response to a **GetDiscoverySearchConfiguration** operation request to only get in-place holds.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetDiscoverySearchConfigurationResponse ResponseClass="Success" 
                                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <DiscoverySearchConfigurations>
            <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearchFor-sbrown</SearchId>
               <SearchQuery>test item</SearchQuery>
               <InPlaceHoldIdentity>3f37d90f53144558a80814ef0272749a9</InPlaceHoldIdentity>
               <ManagedByOrganization/>
            </DiscoverySearchConfiguration>
            <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearch</SearchId>
               <SearchQuery>test</SearchQuery>
               <InPlaceHoldIdentity>6ea486f0f3f140efb044682a2e782abdf</InPlaceHoldIdentity>
               <ManagedByOrganization/>
            </DiscoverySearchConfiguration>
         </DiscoverySearchConfigurations>
      </GetDiscoverySearchConfigurationResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="a3b9a-164">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="a3b9a-164">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="a3b9a-165">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="a3b9a-165">GetDiscoverySearchConfigurationResponse</span></span>](getdiscoverysearchconfigurationresponse.md)
    
- [<span data-ttu-id="a3b9a-166">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a3b9a-166">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a3b9a-167">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="a3b9a-167">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md)
    
- [<span data-ttu-id="a3b9a-168">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3b9a-168">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
    
- [<span data-ttu-id="a3b9a-169">SearchId</span><span class="sxs-lookup"><span data-stu-id="a3b9a-169">SearchId</span></span>](searchid.md)
    
- [<span data-ttu-id="a3b9a-170">SearchQuery</span><span class="sxs-lookup"><span data-stu-id="a3b9a-170">SearchQuery</span></span>](searchquery.md)
    
- [<span data-ttu-id="a3b9a-171">InPlaceHoldIdentity</span><span class="sxs-lookup"><span data-stu-id="a3b9a-171">InPlaceHoldIdentity</span></span>](inplaceholdidentity.md)
    
- [<span data-ttu-id="a3b9a-172">ManagedByOrganization</span><span class="sxs-lookup"><span data-stu-id="a3b9a-172">ManagedByOrganization</span></span>](managedbyorganization.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-all-saved-discovery-search-configurations"></a><span data-ttu-id="a3b9a-173">Respuesta de operación GetDiscoverySearchConfiguration correcta: solicitud de todas las configuraciones de búsqueda de detección guardadas</span><span class="sxs-lookup"><span data-stu-id="a3b9a-173">Successful GetDiscoverySearchConfiguration operation response: Request for all saved discovery search configurations</span></span>

<span data-ttu-id="a3b9a-174">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **GetDiscoverySearchConfiguration** para obtener todas las búsquedas de detección guardadas.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-174">The following example shows a successful response to a **GetDiscoverySearchConfiguration** operation request to get all saved discovery searches.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetDiscoverySearchConfigurationResponse ResponseClass="Success" 
                                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <DiscoverySearchConfigurations>
            <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearchFor-sbrown</SearchId>
               <SearchQuery>test item</SearchQuery>
               <SearchableMailboxes>
                  <SearchableMailbox>
                     <Guid>3c620d04-8b33-435e-95be-5b9351599576</Guid>
                     <PrimarySmtpAddress>SBrown@contoso.com</PrimarySmtpAddress>
                     <IsExternalMailbox>false</IsExternalMailbox>
                     <ExternalEmailAddress/>
                     <DisplayName>Steven Brown</DisplayName>
                     <IsMembershipGroup>false</IsMembershipGroup>
                     <ReferenceId>/o=First/ou=Exchange (FYLT)/cn=Recipients/cn=35381a742f0e47e395c8601a60d13ecz-Steve</ReferenceId>
                  </SearchableMailbox>
               </SearchableMailboxes>
            </DiscoverySearchConfiguration>
            <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearch</SearchId>
               <SearchQuery>test</SearchQuery>
               <SearchableMailboxes>
                  <SearchableMailbox>
                     <Guid>e788c4b0-54a2-458c-83b2-22d5bb02b23f</Guid>
                     <PrimarySmtpAddress>Administrator@contoso.com</PrimarySmtpAddress>
                     <IsExternalMailbox>false</IsExternalMailbox>
                     <ExternalEmailAddress/>
                     <DisplayName>Administrator</DisplayName>
                     <IsMembershipGroup>false</IsMembershipGroup>
                     <ReferenceId>/o=First/ou=Exchange (FYLT)/cn=Recipients/cn=ebez7871332d4595abe1c62962911a58-Admin</ReferenceId>
                  </SearchableMailbox>
                  <SearchableMailbox>
                     <Guid>6f6cff39-8967-4a60-b43f-328413c25199</Guid>
                     <PrimarySmtpAddress>ADavis@contoso.com</PrimarySmtpAddress>
                     <IsExternalMailbox>false</IsExternalMailbox>
                     <ExternalEmailAddress/>
                     <DisplayName>Anthony Davis</DisplayName>
                     <IsMembershipGroup>false</IsMembershipGroup>
                     <ReferenceId>/o=First/ou=Exchange (FYLT)/cn=Recipients/cn=f10c9f70519844beb04101d8f40c572z-Antho</ReferenceId>
                  </SearchableMailbox>
               </SearchableMailboxes>
            </DiscoverySearchConfiguration>
         </DiscoverySearchConfigurations>
      </GetDiscoverySearchConfigurationResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="a3b9a-175">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="a3b9a-175">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="a3b9a-176">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="a3b9a-176">GetDiscoverySearchConfigurationResponse</span></span>](getdiscoverysearchconfigurationresponse.md)
    
- [<span data-ttu-id="a3b9a-177">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a3b9a-177">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a3b9a-178">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="a3b9a-178">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md)
    
- [<span data-ttu-id="a3b9a-179">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3b9a-179">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
    
- [<span data-ttu-id="a3b9a-180">SearchId</span><span class="sxs-lookup"><span data-stu-id="a3b9a-180">SearchId</span></span>](searchid.md)
    
- [<span data-ttu-id="a3b9a-181">SearchQuery</span><span class="sxs-lookup"><span data-stu-id="a3b9a-181">SearchQuery</span></span>](searchquery.md)
    
- [<span data-ttu-id="a3b9a-182">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="a3b9a-182">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
- [<span data-ttu-id="a3b9a-183">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="a3b9a-183">SearchableMailbox</span></span>](searchablemailbox.md)
    
- [<span data-ttu-id="a3b9a-184">Guid</span><span class="sxs-lookup"><span data-stu-id="a3b9a-184">Guid</span></span>](guid-ex15websvcsotherref.md)
    
- [<span data-ttu-id="a3b9a-185">PrimarySmtpAddress (cadena)</span><span class="sxs-lookup"><span data-stu-id="a3b9a-185">PrimarySmtpAddress (string)</span></span>](primarysmtpaddress-string.md)
    
- [<span data-ttu-id="a3b9a-186">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="a3b9a-186">IsExternalMailbox</span></span>](isexternalmailbox.md)
    
- [<span data-ttu-id="a3b9a-187">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="a3b9a-187">ExternalEmailAddress</span></span>](externalemailaddress.md)
    
- [<span data-ttu-id="a3b9a-188">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="a3b9a-188">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="a3b9a-189">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="a3b9a-189">IsMembershipGroup</span></span>](ismembershipgroup.md)
    
- [<span data-ttu-id="a3b9a-190">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="a3b9a-190">ReferenceId</span></span>](referenceid.md)
    
## <a name="getdiscoverysearchconfiguration-operation-error-response"></a><span data-ttu-id="a3b9a-191">Respuesta de error de operación de GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3b9a-191">GetDiscoverySearchConfiguration operation error response</span></span>

<span data-ttu-id="a3b9a-192">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetDiscoverySearchConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="a3b9a-192">The following example shows an error response to a **GetDiscoverySearchConfiguration** operation request.</span></span> <span data-ttu-id="a3b9a-193">Se trata de una respuesta a una solicitud para obtener una búsqueda guardada que no se encuentra en el servidor.</span><span class="sxs-lookup"><span data-stu-id="a3b9a-193">This is a response to a request to get a saved search that is not found on the server.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetDiscoverySearchConfigurationResponse ResponseClass="Error" 
                                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Search configuration corresponding to the search id was not found.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <DiscoverySearchConfigurations/>
      </GetDiscoverySearchConfigurationResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="a3b9a-194">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="a3b9a-194">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="a3b9a-195">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="a3b9a-195">GetDiscoverySearchConfigurationResponse</span></span>](getdiscoverysearchconfigurationresponse.md)
    
- [<span data-ttu-id="a3b9a-196">MessageText</span><span class="sxs-lookup"><span data-stu-id="a3b9a-196">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="a3b9a-197">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="a3b9a-197">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="a3b9a-198">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="a3b9a-198">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="a3b9a-199">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="a3b9a-199">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md)
    
<span data-ttu-id="a3b9a-200">Para obtener los códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="a3b9a-200">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a3b9a-201">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3b9a-201">See also</span></span>

- [<span data-ttu-id="a3b9a-202">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a3b9a-202">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="a3b9a-203">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="a3b9a-203">GetSearchableMailboxes</span></span>](getsearchablemailboxes.md)
    
- [<span data-ttu-id="a3b9a-204">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="a3b9a-204">SearchMailboxes</span></span>](searchmailboxes.md)
    
- [<span data-ttu-id="a3b9a-205">GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="a3b9a-205">GetHoldOnMailboxes</span></span>](getholdonmailboxes.md)
    
- [<span data-ttu-id="a3b9a-206">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="a3b9a-206">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
    
- [<span data-ttu-id="a3b9a-207">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="a3b9a-207">GetNonIndexableItemDetails</span></span>](getnonindexableitemdetails.md)
    
- [<span data-ttu-id="a3b9a-208">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="a3b9a-208">GetNonIndexableItemStatistics</span></span>](getnonindexableitemstatistics.md)
    

