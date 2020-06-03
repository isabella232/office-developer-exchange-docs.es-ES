---
title: Operación GetSearchableMailboxes
manager: sethgros
ms.date: 01/24/2020
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 47f8ff57-4835-4d2d-9136-44afb31a4cbe
description: Buscar información sobre la operación de EWS de GetSearchableMailboxes.
ms.openlocfilehash: e893a66eb1b638479eeccc6bd7548cb020f37243
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530842"
---
# <a name="getsearchablemailboxes-operation"></a><span data-ttu-id="87d26-103">Operación GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="87d26-103">GetSearchableMailboxes operation</span></span>

> [!IMPORTANT]
> <span data-ttu-id="87d26-104">A partir del 1 de abril de 2020, la operación GetSearchableMailboxes ya no estará disponible en Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="87d26-104">Starting on April 1, 2020, the GetSearchableMailboxes operation will no longer be available in Exchange Online.</span></span> <span data-ttu-id="87d26-105">Esta operación no se verá afectada en las versiones locales de Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="87d26-105">This operation won't be affected in on-premises versions of Exchange Server.</span></span> <span data-ttu-id="87d26-106">Para obtener más información, vea [jubilación de las herramientas de eDiscovery heredadas en Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).</span><span class="sxs-lookup"><span data-stu-id="87d26-106">For more information, see [Retirement of legacy eDiscovery tools in Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).</span></span>

<span data-ttu-id="87d26-107">Buscar información sobre la operación de EWS de **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="87d26-107">Find information about the **GetSearchableMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="87d26-108">La operación **GetSearchableMailboxes** obtiene un conjunto con ámbito de buzones de correo que se pueden buscar para las búsquedas de detección.</span><span class="sxs-lookup"><span data-stu-id="87d26-108">The **GetSearchableMailboxes** operation gets a scoped set of searchable mailboxes for discovery searches.</span></span> <span data-ttu-id="87d26-109">El ámbito de los buzones de correo que se pueden buscar devueltos en la respuesta está determinado por el filtro de búsqueda y si se expande la pertenencia al grupo de distribución.</span><span class="sxs-lookup"><span data-stu-id="87d26-109">The scope of searchable mailboxes returned in the response is determined by the search filter and whether distribution group membership is expanded.</span></span> 

> [!NOTE] 
> <span data-ttu-id="87d26-110">Esta operación está pensada para usarse con el filtro de búsqueda y para recuperar sólo los primeros miles; no está pensada para una recuperación exhaustiva.</span><span class="sxs-lookup"><span data-stu-id="87d26-110">This operation is intended to be used with the search filter and to retrieve only the first few thousands; it's not intended for exhaustive retrieval.</span></span>
  
<span data-ttu-id="87d26-111">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="87d26-111">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getsearchablemailboxes-operation"></a><span data-ttu-id="87d26-112">Uso de la operación GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="87d26-112">Using the GetSearchableMailboxes operation</span></span>

<span data-ttu-id="87d26-113">La operación **GetSearchableMailboxes** obtiene información sobre los buzones de correo que permiten búsquedas.</span><span class="sxs-lookup"><span data-stu-id="87d26-113">The **GetSearchableMailboxes** operation gets information about searchable mailboxes.</span></span> <span data-ttu-id="87d26-114">Se pueden pasar los siguientes argumentos en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="87d26-114">The following arguments can be passed in the request:</span></span> 
  
- <span data-ttu-id="87d26-115">[SearchFilter](searchfilter.md) : acepta un único alias de correo electrónico como argumento.</span><span class="sxs-lookup"><span data-stu-id="87d26-115">[SearchFilter](searchfilter.md) - Accepts a single email alias as an argument.</span></span> 
    
- <span data-ttu-id="87d26-116">[ExpandGroupMembership](expandgroupmembership.md) : indica si la pertenencia al grupo de distribución se expande en los resultados devueltos en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="87d26-116">[ExpandGroupMembership](expandgroupmembership.md) - Indicates whether the distribution group membership is expanded in the results returned in the response.</span></span> 
    
<span data-ttu-id="87d26-117">Si el alias de correo electrónico establecido en el filtro de búsqueda es un grupo de distribución y la pertenencia al grupo de distribución no se expande, la respuesta contendrá la información del buzón del grupo de distribución.</span><span class="sxs-lookup"><span data-stu-id="87d26-117">If the email alias set in the search filter is a distribution group and the distribution group membership is not expanded, the response will contain the mailbox information for the distribution group.</span></span> <span data-ttu-id="87d26-118">Si el alias de correo electrónico establecido en el filtro de búsqueda es un grupo de distribución y se expande la pertenencia al grupo de distribución, la respuesta contendrá la información del buzón para cada buzón de correo que sea miembro del grupo de distribución.</span><span class="sxs-lookup"><span data-stu-id="87d26-118">If the email alias set in the search filter is a distribution group and the distribution group membership is expanded, the response will contain the mailbox information for each mailbox that is a member of the distribution group.</span></span> <span data-ttu-id="87d26-119">Si el filtro de búsqueda contiene un alias de usuario único, la respuesta contendrá la información del buzón de correo del usuario único.</span><span class="sxs-lookup"><span data-stu-id="87d26-119">If the search filter contains a single user's alias, the response will contain the mailbox information for the single user.</span></span> <span data-ttu-id="87d26-120">La respuesta contendrá todos los buzones de correo de búsqueda si el elemento [GetSearchableMailboxes](getsearchablemailboxes.md) está vacío.</span><span class="sxs-lookup"><span data-stu-id="87d26-120">The response will contain all searchable mailboxes if the [GetSearchableMailboxes](getsearchablemailboxes.md) element is empty.</span></span> <span data-ttu-id="87d26-121">Esto es lo mismo que tener un elemento [SearchFilter](searchfilter.md) vacío y el elemento [ExpandGroupMembership](expandgroupmembership.md) establecido en **false**.</span><span class="sxs-lookup"><span data-stu-id="87d26-121">This is the same as having an empty [SearchFilter](searchfilter.md) element and the [ExpandGroupMembership](expandgroupmembership.md) element set to **false**.</span></span>
  
### <a name="getsearchablemailboxes-operation-soap-headers"></a><span data-ttu-id="87d26-122">Encabezados SOAP de operación GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="87d26-122">GetSearchableMailboxes operation SOAP headers</span></span>

<span data-ttu-id="87d26-123">La operación **GetSearchableMailboxes** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="87d26-123">The **GetSearchableMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="87d26-124">Nombre de encabezado</span><span class="sxs-lookup"><span data-stu-id="87d26-124">Header name</span></span>|<span data-ttu-id="87d26-125">Elemento</span><span class="sxs-lookup"><span data-stu-id="87d26-125">Element</span></span>|<span data-ttu-id="87d26-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="87d26-126">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="87d26-127">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="87d26-127">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="87d26-128">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="87d26-128">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="87d26-129">Identifica los roles de servidor que son necesarios para que el autor de la llamada realice la solicitud.</span><span class="sxs-lookup"><span data-stu-id="87d26-129">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="87d26-130">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="87d26-130">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="87d26-131">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="87d26-131">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="87d26-132">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="87d26-132">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="87d26-133">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="87d26-133">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="87d26-134">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="87d26-134">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="87d26-135">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="87d26-135">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="87d26-136">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="87d26-136">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="87d26-137">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="87d26-137">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="87d26-138">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="87d26-138">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getsearchablemailboxes-operation-request-example-request-information-about-a-distribution-group"></a><span data-ttu-id="87d26-139">Ejemplo de solicitud de operación GetSearchableMailboxes: solicitar información sobre un grupo de distribución</span><span class="sxs-lookup"><span data-stu-id="87d26-139">GetSearchableMailboxes operation request example: Request information about a distribution group</span></span>

<span data-ttu-id="87d26-140">El siguiente ejemplo de una solicitud de operación de **GetSearchableMailboxes** muestra cómo obtener la información de buzón para el grupo de distribución lolgroup.</span><span class="sxs-lookup"><span data-stu-id="87d26-140">The following example of a **GetSearchableMailboxes** operation request shows how to get the mailbox information for the lolgroup distribution group.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetSearchableMailboxes>
         <m:SearchFilter>lolgroup</m:SearchFilter>
         <m:ExpandGroupMembership>false</m:ExpandGroupMembership>
      </m:GetSearchableMailboxes>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="87d26-141">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="87d26-141">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="87d26-142">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="87d26-142">GetSearchableMailboxes</span></span>](getsearchablemailboxes.md)   
- [<span data-ttu-id="87d26-143">SearchFilter</span><span class="sxs-lookup"><span data-stu-id="87d26-143">SearchFilter</span></span>](searchfilter.md)    
- [<span data-ttu-id="87d26-144">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="87d26-144">ExpandGroupMembership</span></span>](expandgroupmembership.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-a-distribution-group"></a><span data-ttu-id="87d26-145">Respuesta de operación GetSearchableMailboxes correcta: obtener información sobre un grupo de distribución</span><span class="sxs-lookup"><span data-stu-id="87d26-145">Successful GetSearchableMailboxes operation response: Get information about a distribution group</span></span>

<span data-ttu-id="87d26-146">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetSearchableMailboxes** para obtener la información de detección del grupo de distribución lolgroup.</span><span class="sxs-lookup"><span data-stu-id="87d26-146">The following example shows a successful response to a **GetSearchableMailboxes** operation request to get the discovery information for the lolgroup distribution group.</span></span> 
  
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
      <GetSearchableMailboxesResponse ResponseClass="Success" 
                                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <SearchableMailboxes>
            <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Guid>33a408fe-2574-4e3b-49f5-5e1e000a3035</Guid>
               <PrimarySmtpAddress>LOLgroup@contoso.com</PrimarySmtpAddress>
               <IsExternalMailbox>false</IsExternalMailbox>
               <ExternalEmailAddress/>
               <DisplayName>LOLgroup</DisplayName>
               <IsMembershipGroup>true</IsMembershipGroup>
               <ReferenceId>/o=First/ou=Exchange(FYLT)/cn=Recipients/cn=81213b958a0b5295b13b3f02b812bf1bc-LOLgroup</ReferenceId>
            </SearchableMailbox>
         </SearchableMailboxes>
      </GetSearchableMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="87d26-147">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="87d26-147">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="87d26-148">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="87d26-148">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)   
- [<span data-ttu-id="87d26-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="87d26-149">ResponseCode</span></span>](responsecode.md)   
- [<span data-ttu-id="87d26-150">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="87d26-150">SearchableMailboxes</span></span>](searchablemailboxes.md)    
- [<span data-ttu-id="87d26-151">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="87d26-151">SearchableMailbox</span></span>](searchablemailbox.md)    
- [<span data-ttu-id="87d26-152">Guid</span><span class="sxs-lookup"><span data-stu-id="87d26-152">Guid</span></span>](guid-ex15websvcsotherref.md)    
- [<span data-ttu-id="87d26-153">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="87d26-153">PrimarySmtpAddress</span></span>](primarysmtpaddress.md)    
- [<span data-ttu-id="87d26-154">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="87d26-154">IsExternalMailbox</span></span>](isexternalmailbox.md)   
- [<span data-ttu-id="87d26-155">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="87d26-155">ExternalEmailAddress</span></span>](externalemailaddress.md)    
- [<span data-ttu-id="87d26-156">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="87d26-156">DisplayName (string)</span></span>](displayname-string.md)    
- [<span data-ttu-id="87d26-157">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="87d26-157">IsMembershipGroup</span></span>](ismembershipgroup.md)    
- [<span data-ttu-id="87d26-158">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="87d26-158">ReferenceId</span></span>](referenceid.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-an-expanded-distribution-group"></a><span data-ttu-id="87d26-159">Respuesta de operación GetSearchableMailboxes correcta: obtener información sobre un grupo de distribución expandido</span><span class="sxs-lookup"><span data-stu-id="87d26-159">Successful GetSearchableMailboxes operation response: Get information about an expanded distribution group</span></span>

<span data-ttu-id="87d26-160">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **GetSearchableMailboxes** para obtener la información de detección de los miembros del grupo de distribución lolgroup expandido.</span><span class="sxs-lookup"><span data-stu-id="87d26-160">The following example shows a successful response to a **GetSearchableMailboxes** operation request to get the discovery information about members of the expanded lolgroup distribution group.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="526" MinorBuildNumber="0" Version="Exchange2013" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetSearchableMailboxesResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <SearchableMailboxes>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>e2d42cdf-a227-1ec3-486b-6fa0ebaadb9f5</Guid>
          <PrimarySmtpAddress>JSmith@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Julia Smith</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=0a1fc86f883846152405d60956dd02e7-Julia</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>45d0fff1-6541-459a-a343-52453b30e12ca</Guid>
          <PrimarySmtpAddress>LMoore@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Laura Moore</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=2910d8f8316f4378bbf9338d8f9d714b-Laura</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>3c620d04-8b33-435a-95be-5b939375576</Guid>
          <PrimarySmtpAddress>SBrown@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Steven Brown</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=90312341a742f0e47e392c80a60d13ecf-Steve</ReferenceId>
        </SearchableMailbox>
      </SearchableMailboxes>
    </GetSearchableMailboxesResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="87d26-161">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="87d26-161">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="87d26-162">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="87d26-162">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)    
- [<span data-ttu-id="87d26-163">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="87d26-163">ResponseCode</span></span>](responsecode.md)   
- [<span data-ttu-id="87d26-164">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="87d26-164">SearchableMailboxes</span></span>](searchablemailboxes.md)    
- [<span data-ttu-id="87d26-165">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="87d26-165">SearchableMailbox</span></span>](searchablemailbox.md)    
- [<span data-ttu-id="87d26-166">Guid</span><span class="sxs-lookup"><span data-stu-id="87d26-166">Guid</span></span>](guid-ex15websvcsotherref.md)    
- [<span data-ttu-id="87d26-167">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="87d26-167">PrimarySmtpAddress</span></span>](primarysmtpaddress.md)    
- [<span data-ttu-id="87d26-168">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="87d26-168">IsExternalMailbox</span></span>](isexternalmailbox.md)    
- [<span data-ttu-id="87d26-169">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="87d26-169">ExternalEmailAddress</span></span>](externalemailaddress.md)    
- [<span data-ttu-id="87d26-170">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="87d26-170">DisplayName (string)</span></span>](displayname-string.md)    
- [<span data-ttu-id="87d26-171">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="87d26-171">IsMembershipGroup</span></span>](ismembershipgroup.md)    
- [<span data-ttu-id="87d26-172">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="87d26-172">ReferenceId</span></span>](referenceid.md)
    
## <a name="getsearchablemailboxes-operation-error-response"></a><span data-ttu-id="87d26-173">Respuesta de error de operación de GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="87d26-173">GetSearchableMailboxes operation error response</span></span>

<span data-ttu-id="87d26-174">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="87d26-174">The following example shows an error response to a **GetSearchableMailboxes** operation request.</span></span> <span data-ttu-id="87d26-175">Se trata de una respuesta a una solicitud para obtener todos los buzones de correo que se pueden buscar cuando el argumento **ExpandGroupMembership** está establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="87d26-175">This is a response to a request to get all searchable mailboxes when the **ExpandGroupMembership** argument is set to **true**.</span></span> 
  
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
      <GetSearchableMailboxesResponse ResponseClass="Error" 
                                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot use wildcard or empty query when auto group expansion is enabled.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <SearchableMailboxes/>
      </GetSearchableMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="87d26-176">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="87d26-176">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="87d26-177">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="87d26-177">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)  
- [<span data-ttu-id="87d26-178">MessageText</span><span class="sxs-lookup"><span data-stu-id="87d26-178">MessageText</span></span>](messagetext.md)   
- [<span data-ttu-id="87d26-179">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="87d26-179">ResponseCode</span></span>](responsecode.md)   
- [<span data-ttu-id="87d26-180">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="87d26-180">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) 
- [<span data-ttu-id="87d26-181">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="87d26-181">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
<span data-ttu-id="87d26-182">Para obtener los códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="87d26-182">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="87d26-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="87d26-183">See also</span></span>

- [<span data-ttu-id="87d26-184">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="87d26-184">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)   
- [<span data-ttu-id="87d26-185">Operación SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="87d26-185">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)   
- [<span data-ttu-id="87d26-186">Operación SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="87d26-186">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)   
- [<span data-ttu-id="87d26-187">Operación GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="87d26-187">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)    
- [<span data-ttu-id="87d26-188">Operación GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="87d26-188">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)   
- [<span data-ttu-id="87d26-189">Operación GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="87d26-189">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)   
- [<span data-ttu-id="87d26-190">Operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="87d26-190">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

