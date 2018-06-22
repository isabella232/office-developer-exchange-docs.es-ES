---
title: Operación GetDiscoverySearchConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8a54a6dc-110c-4972-a8bc-5ddb43c4b857
description: Busque información sobre la EWS GetDiscoverySearchConfiguration operación.
ms.openlocfilehash: a50463e575bf5a4ffdafc357d91563b0ca0486f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764805"
---
# <a name="getdiscoverysearchconfiguration-operation"></a><span data-ttu-id="431ea-103">Operación GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="431ea-103">GetDiscoverySearchConfiguration operation</span></span>

<span data-ttu-id="431ea-104">Obtenga información acerca de la operación de EWS **GetDiscoverySearchConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="431ea-104">Find information about the **GetDiscoverySearchConfiguration** EWS operation.</span></span> 
  
<span data-ttu-id="431ea-105">La operación **GetDiscoverySearchConfiguration** devuelve contiene información de configuración de en contexto, guarda las búsquedas de detección y los buzones de correo que están habilitados para la búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="431ea-105">The **GetDiscoverySearchConfiguration** operation returns configuration information for in-place holds, saved discovery searches, and the mailboxes that are enabled for discovery search.</span></span> 
  
<span data-ttu-id="431ea-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="431ea-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getdiscoverysearchconfiguration-operation"></a><span data-ttu-id="431ea-107">Mediante la operación GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="431ea-107">Using the GetDiscoverySearchConfiguration operation</span></span>

<span data-ttu-id="431ea-108">La operación **GetDiscoverySearchConfiguration** proporciona información de configuración de búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="431ea-108">The **GetDiscoverySearchConfiguration** operation provides configuration information for discovery search.</span></span> <span data-ttu-id="431ea-109">Las solicitudes de pueden contener uno o varios de los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="431ea-109">Requests can contain one or more of the following arguments:</span></span> 
  
1. <span data-ttu-id="431ea-110">[El identificador de búsqueda](searchid.md) : identifica una búsqueda de descubrimiento guardados.</span><span class="sxs-lookup"><span data-stu-id="431ea-110">[SearchId](searchid.md) — Identifies a saved discovery search.</span></span> <span data-ttu-id="431ea-111">Si este argumento se envía en la solicitud, se omiten los valores de los demás argumentos.</span><span class="sxs-lookup"><span data-stu-id="431ea-111">If this argument is sent in the request, the values of the other arguments are ignored.</span></span> 
    
2. <span data-ttu-id="431ea-112">[ExpandGroupMembership](expandgroupmembership.md) : indica si se expande la pertenencia a grupos en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="431ea-112">[ExpandGroupMembership](expandgroupmembership.md) — Indicates whether group membership is expanded in the response.</span></span> <span data-ttu-id="431ea-113">Un valor de **true** indica que se expande la pertenencia a grupos para que se devuelvan todos los buzones que se puede buscar en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="431ea-113">A value of **true** indicates that group membership is expanded so that all searchable mailboxes are returned in the response.</span></span> <span data-ttu-id="431ea-114">Un valor de **false** indica que se devuelve sólo el grupo en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="431ea-114">A value of **false** indicates that only the group is returned in the response.</span></span> 
    
3. <span data-ttu-id="431ea-115">[InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) : indica si se devuelven todos los buzones que admite búsquedos además de la configuración de suspensión en contexto.</span><span class="sxs-lookup"><span data-stu-id="431ea-115">[InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) — Indicates whether all searchable mailboxes are returned in addition to the in-place hold configuration.</span></span> <span data-ttu-id="431ea-116">Un valor de **true** indica que se devuelven sólo las configuraciones de suspensión en contexto.</span><span class="sxs-lookup"><span data-stu-id="431ea-116">A value of **true** indicates that only the in-place hold configurations are returned.</span></span> <span data-ttu-id="431ea-117">Un valor de **false** indica que se devuelven todos los identificadores de buzón de correo que admite búsquedas además de los identificadores de suspensión en contexto.</span><span class="sxs-lookup"><span data-stu-id="431ea-117">A value of **false** indicates that all searchable mailbox identifiers are returned in addition to the in-place hold identifiers.</span></span> <span data-ttu-id="431ea-118">Si este elemento no está presente, el comportamiento predeterminado es el equivalente del valor **false**.</span><span class="sxs-lookup"><span data-stu-id="431ea-118">If this element is not present, the default behavior is the equivalent of the value **false**.</span></span> 
    
### <a name="getdiscoverysearchconfiguration-operation-soap-headers"></a><span data-ttu-id="431ea-119">Encabezados SOAP de operación de GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="431ea-119">GetDiscoverySearchConfiguration operation SOAP headers</span></span>

<span data-ttu-id="431ea-120">La operación de **GetDiscoverySearchConfiguration** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="431ea-120">The **GetDiscoverySearchConfiguration** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="431ea-121">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="431ea-121">**Header name**</span></span>|<span data-ttu-id="431ea-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="431ea-122">**Element**</span></span>|<span data-ttu-id="431ea-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="431ea-123">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="431ea-124">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="431ea-124">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="431ea-125">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="431ea-125">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="431ea-126">Identifica las funciones de servidor que son necesarias en orden para el autor de la llamada realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="431ea-126">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="431ea-127">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="431ea-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="431ea-128">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="431ea-128">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="431ea-129">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="431ea-129">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="431ea-130">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="431ea-130">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="431ea-131">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="431ea-131">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="431ea-132">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="431ea-132">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="431ea-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="431ea-133">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="431ea-134">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="431ea-134">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="431ea-135">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="431ea-135">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getdiscoverysearchconfiguration-operation-request-example-get-the-discovery-search-configuration-for-a-saved-search"></a><span data-ttu-id="431ea-136">Ejemplo de solicitud de operación de GetDiscoverySearchConfiguration: obtener la configuración de búsqueda de detección para una búsqueda guardada</span><span class="sxs-lookup"><span data-stu-id="431ea-136">GetDiscoverySearchConfiguration operation request example: Get the discovery search configuration for a saved search</span></span>

<span data-ttu-id="431ea-137">El siguiente ejemplo de una solicitud de operación **GetDiscoverySearchConfiguration** muestra cómo solicitar la configuración de una búsqueda guardada que se denomina "MyDiscSearchFor-sbrown".</span><span class="sxs-lookup"><span data-stu-id="431ea-137">The following example of a **GetDiscoverySearchConfiguration** operation request shows how to request the configuration of a saved search called "MyDiscSearchFor-sbrown".</span></span> <span data-ttu-id="431ea-138">Se omiten los argumentos para los elementos de [InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) y [ExpandGroupMembership](expandgroupmembership.md) .</span><span class="sxs-lookup"><span data-stu-id="431ea-138">The arguments for the [ExpandGroupMembership](expandgroupmembership.md) and [InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) elements are ignored.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="431ea-139">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="431ea-139">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="431ea-140">GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="431ea-140">GetDiscoverySearchConfiguration</span></span>](getdiscoverysearchconfiguration.md)
    
- [<span data-ttu-id="431ea-141">Identificador de búsqueda</span><span class="sxs-lookup"><span data-stu-id="431ea-141">SearchId</span></span>](searchid.md)
    
- [<span data-ttu-id="431ea-142">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="431ea-142">ExpandGroupMembership</span></span>](expandgroupmembership.md)
    
- [<span data-ttu-id="431ea-143">InPlaceHoldConfigurationOnly</span><span class="sxs-lookup"><span data-stu-id="431ea-143">InPlaceHoldConfigurationOnly</span></span>](inplaceholdconfigurationonly.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-a-single-saved-search"></a><span data-ttu-id="431ea-144">La respuesta es correcta de operación GetDiscoverySearchConfiguration: solicitud para una sola búsqueda guardada</span><span class="sxs-lookup"><span data-stu-id="431ea-144">Successful GetDiscoverySearchConfiguration operation response: Request for a single saved search</span></span>

<span data-ttu-id="431ea-145">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetDiscoverySearchConfiguration** para obtener la configuración de una búsqueda guardada que se denomina "MyDiscSearchFor-sbrown".</span><span class="sxs-lookup"><span data-stu-id="431ea-145">The following example shows a successful response to a **GetDiscoverySearchConfiguration** operation request to get the configuration of a saved search called "MyDiscSearchFor-sbrown".</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="526" MinorBuildNumber="0" Version="Exchange2013" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetDiscoverySearchConfigurationResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <DiscoverySearchConfigurations>
        <DiscoverySearchConfiguration xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="431ea-146">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="431ea-146">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="431ea-147">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="431ea-147">GetDiscoverySearchConfigurationResponse</span></span>](getdiscoverysearchconfigurationresponse.md)
    
- [<span data-ttu-id="431ea-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="431ea-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="431ea-149">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="431ea-149">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md)
    
- [<span data-ttu-id="431ea-150">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="431ea-150">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
    
- [<span data-ttu-id="431ea-151">Identificador de búsqueda</span><span class="sxs-lookup"><span data-stu-id="431ea-151">SearchId</span></span>](searchid.md)
    
- [<span data-ttu-id="431ea-152">SearchQuery</span><span class="sxs-lookup"><span data-stu-id="431ea-152">SearchQuery</span></span>](searchquery.md)
    
- [<span data-ttu-id="431ea-153">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="431ea-153">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
- [<span data-ttu-id="431ea-154">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="431ea-154">SearchableMailbox</span></span>](searchablemailbox.md)
    
- [<span data-ttu-id="431ea-155">GUID</span><span class="sxs-lookup"><span data-stu-id="431ea-155">Guid</span></span>](guid-ex15websvcsotherref.md)
    
- [<span data-ttu-id="431ea-156">PrimarySmtpAddress (cadena)</span><span class="sxs-lookup"><span data-stu-id="431ea-156">PrimarySmtpAddress (string)</span></span>](primarysmtpaddress-string.md)
    
- [<span data-ttu-id="431ea-157">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="431ea-157">IsExternalMailbox</span></span>](isexternalmailbox.md)
    
- [<span data-ttu-id="431ea-158">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="431ea-158">ExternalEmailAddress</span></span>](externalemailaddress.md)
    
- [<span data-ttu-id="431ea-159">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="431ea-159">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="431ea-160">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="431ea-160">IsMembershipGroup</span></span>](ismembershipgroup.md)
    
- [<span data-ttu-id="431ea-161">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="431ea-161">ReferenceId</span></span>](referenceid.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-in-place-holds"></a><span data-ttu-id="431ea-162">La respuesta es correcta de operación GetDiscoverySearchConfiguration: solicitud de suspensiones en contexto</span><span class="sxs-lookup"><span data-stu-id="431ea-162">Successful GetDiscoverySearchConfiguration operation response: Request for in-place holds</span></span>

<span data-ttu-id="431ea-163">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetDiscoverySearchConfiguration** para sólo obtener en contexto contiene.</span><span class="sxs-lookup"><span data-stu-id="431ea-163">The following example shows a successful response to a **GetDiscoverySearchConfiguration** operation request to only get in-place holds.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetDiscoverySearchConfigurationResponse ResponseClass="Success" 
                                               xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <DiscoverySearchConfigurations>
            <DiscoverySearchConfiguration xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearchFor-sbrown</SearchId>
               <SearchQuery>test item</SearchQuery>
               <InPlaceHoldIdentity>3f37d90f53144558a80814ef0272749a9</InPlaceHoldIdentity>
               <ManagedByOrganization/>
            </DiscoverySearchConfiguration>
            <DiscoverySearchConfiguration xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="431ea-164">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="431ea-164">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="431ea-165">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="431ea-165">GetDiscoverySearchConfigurationResponse</span></span>](getdiscoverysearchconfigurationresponse.md)
    
- [<span data-ttu-id="431ea-166">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="431ea-166">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="431ea-167">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="431ea-167">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md)
    
- [<span data-ttu-id="431ea-168">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="431ea-168">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
    
- [<span data-ttu-id="431ea-169">Identificador de búsqueda</span><span class="sxs-lookup"><span data-stu-id="431ea-169">SearchId</span></span>](searchid.md)
    
- [<span data-ttu-id="431ea-170">SearchQuery</span><span class="sxs-lookup"><span data-stu-id="431ea-170">SearchQuery</span></span>](searchquery.md)
    
- [<span data-ttu-id="431ea-171">InPlaceHoldIdentity</span><span class="sxs-lookup"><span data-stu-id="431ea-171">InPlaceHoldIdentity</span></span>](inplaceholdidentity.md)
    
- [<span data-ttu-id="431ea-172">ManagedByOrganization</span><span class="sxs-lookup"><span data-stu-id="431ea-172">ManagedByOrganization</span></span>](managedbyorganization.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-all-saved-discovery-search-configurations"></a><span data-ttu-id="431ea-173">La respuesta es correcta de operación GetDiscoverySearchConfiguration: solicitud de todos los guardan detección configuraciones de búsqueda</span><span class="sxs-lookup"><span data-stu-id="431ea-173">Successful GetDiscoverySearchConfiguration operation response: Request for all saved discovery search configurations</span></span>

<span data-ttu-id="431ea-174">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetDiscoverySearchConfiguration** para obtener todas las búsquedas de descubrimiento guardados.</span><span class="sxs-lookup"><span data-stu-id="431ea-174">The following example shows a successful response to a **GetDiscoverySearchConfiguration** operation request to get all saved discovery searches.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetDiscoverySearchConfigurationResponse ResponseClass="Success" 
                                               xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <DiscoverySearchConfigurations>
            <DiscoverySearchConfiguration xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
            <DiscoverySearchConfiguration xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="431ea-175">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="431ea-175">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="431ea-176">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="431ea-176">GetDiscoverySearchConfigurationResponse</span></span>](getdiscoverysearchconfigurationresponse.md)
    
- [<span data-ttu-id="431ea-177">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="431ea-177">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="431ea-178">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="431ea-178">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md)
    
- [<span data-ttu-id="431ea-179">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="431ea-179">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
    
- [<span data-ttu-id="431ea-180">Identificador de búsqueda</span><span class="sxs-lookup"><span data-stu-id="431ea-180">SearchId</span></span>](searchid.md)
    
- [<span data-ttu-id="431ea-181">SearchQuery</span><span class="sxs-lookup"><span data-stu-id="431ea-181">SearchQuery</span></span>](searchquery.md)
    
- [<span data-ttu-id="431ea-182">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="431ea-182">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
- [<span data-ttu-id="431ea-183">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="431ea-183">SearchableMailbox</span></span>](searchablemailbox.md)
    
- [<span data-ttu-id="431ea-184">GUID</span><span class="sxs-lookup"><span data-stu-id="431ea-184">Guid</span></span>](guid-ex15websvcsotherref.md)
    
- [<span data-ttu-id="431ea-185">PrimarySmtpAddress (cadena)</span><span class="sxs-lookup"><span data-stu-id="431ea-185">PrimarySmtpAddress (string)</span></span>](primarysmtpaddress-string.md)
    
- [<span data-ttu-id="431ea-186">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="431ea-186">IsExternalMailbox</span></span>](isexternalmailbox.md)
    
- [<span data-ttu-id="431ea-187">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="431ea-187">ExternalEmailAddress</span></span>](externalemailaddress.md)
    
- [<span data-ttu-id="431ea-188">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="431ea-188">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="431ea-189">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="431ea-189">IsMembershipGroup</span></span>](ismembershipgroup.md)
    
- [<span data-ttu-id="431ea-190">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="431ea-190">ReferenceId</span></span>](referenceid.md)
    
## <a name="getdiscoverysearchconfiguration-operation-error-response"></a><span data-ttu-id="431ea-191">Respuesta de error de la operación de GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="431ea-191">GetDiscoverySearchConfiguration operation error response</span></span>

<span data-ttu-id="431ea-192">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetDiscoverySearchConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="431ea-192">The following example shows an error response to a **GetDiscoverySearchConfiguration** operation request.</span></span> <span data-ttu-id="431ea-193">Esta es una respuesta a una solicitud para obtener una búsqueda guardada que no se encuentra en el servidor.</span><span class="sxs-lookup"><span data-stu-id="431ea-193">This is a response to a request to get a saved search that is not found on the server.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetDiscoverySearchConfigurationResponse ResponseClass="Error" 
                                               xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Search configuration corresponding to the search id was not found.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <DiscoverySearchConfigurations/>
      </GetDiscoverySearchConfigurationResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="431ea-194">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="431ea-194">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="431ea-195">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="431ea-195">GetDiscoverySearchConfigurationResponse</span></span>](getdiscoverysearchconfigurationresponse.md)
    
- [<span data-ttu-id="431ea-196">MessageText</span><span class="sxs-lookup"><span data-stu-id="431ea-196">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="431ea-197">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="431ea-197">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="431ea-198">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="431ea-198">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="431ea-199">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="431ea-199">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md)
    
<span data-ttu-id="431ea-200">Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="431ea-200">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="431ea-201">Ver también</span><span class="sxs-lookup"><span data-stu-id="431ea-201">See also</span></span>

- [<span data-ttu-id="431ea-202">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="431ea-202">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="431ea-203">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="431ea-203">GetSearchableMailboxes</span></span>](getsearchablemailboxes.md)
    
- [<span data-ttu-id="431ea-204">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="431ea-204">SearchMailboxes</span></span>](searchmailboxes.md)
    
- [<span data-ttu-id="431ea-205">GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="431ea-205">GetHoldOnMailboxes</span></span>](getholdonmailboxes.md)
    
- [<span data-ttu-id="431ea-206">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="431ea-206">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
    
- [<span data-ttu-id="431ea-207">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="431ea-207">GetNonIndexableItemDetails</span></span>](getnonindexableitemdetails.md)
    
- [<span data-ttu-id="431ea-208">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="431ea-208">GetNonIndexableItemStatistics</span></span>](getnonindexableitemstatistics.md)
    

