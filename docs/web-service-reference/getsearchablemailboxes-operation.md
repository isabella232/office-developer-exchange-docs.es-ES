---
title: Operación GetSearchableMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 47f8ff57-4835-4d2d-9136-44afb31a4cbe
description: Busque información sobre la EWS GetSearchableMailboxes operación.
ms.openlocfilehash: 5e14288280b23e2555eea4fce0f77743d7d210ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764968"
---
# <a name="getsearchablemailboxes-operation"></a><span data-ttu-id="78a8f-103">Operación GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="78a8f-103">GetSearchableMailboxes operation</span></span>

<span data-ttu-id="78a8f-104">Obtenga información acerca de la operación de EWS **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="78a8f-104">Find information about the **GetSearchableMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="78a8f-105">La operación **GetSearchableMailboxes** Obtiene un conjunto de buzones que admite búsquedos para las búsquedas de detección de ámbito.</span><span class="sxs-lookup"><span data-stu-id="78a8f-105">The **GetSearchableMailboxes** operation gets a scoped set of searchable mailboxes for discovery searches.</span></span> <span data-ttu-id="78a8f-106">El ámbito de los buzones de correo que admite búsquedas devuelto en la respuesta es determinado por el filtro de búsqueda y si se expande la pertenencia a grupos de distribución.</span><span class="sxs-lookup"><span data-stu-id="78a8f-106">The scope of searchable mailboxes returned in the response is determined by the search filter and whether distribution group membership is expanded.</span></span> 
  
<span data-ttu-id="78a8f-107">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="78a8f-107">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getsearchablemailboxes-operation"></a><span data-ttu-id="78a8f-108">Mediante la operación GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="78a8f-108">Using the GetSearchableMailboxes operation</span></span>

<span data-ttu-id="78a8f-109">La operación **GetSearchableMailboxes** obtiene información sobre los buzones que admite búsquedas.</span><span class="sxs-lookup"><span data-stu-id="78a8f-109">The **GetSearchableMailboxes** operation gets information about searchable mailboxes.</span></span> <span data-ttu-id="78a8f-110">En la solicitud se pueden pasar los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="78a8f-110">The following arguments can be passed in the request:</span></span> 
  
- <span data-ttu-id="78a8f-111">[SearchFilter](searchfilter.md) : acepta un alias de correo electrónico única como un argumento.</span><span class="sxs-lookup"><span data-stu-id="78a8f-111">[SearchFilter](searchfilter.md) —Accepts a single email alias as an argument.</span></span> 
    
- <span data-ttu-id="78a8f-112">[ExpandGroupMembership](expandgroupmembership.md) : indica si se expande la pertenencia al grupo de distribución en los resultados devueltos en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="78a8f-112">[ExpandGroupMembership](expandgroupmembership.md) — Indicates whether the distribution group membership is expanded in the results returned in the response.</span></span> 
    
<span data-ttu-id="78a8f-113">Si el alias de correo electrónico establecido en el filtro de búsqueda es un grupo de distribución y no se expande la pertenencia al grupo de distribución, la respuesta contendrá la información de buzón de correo para el grupo de distribución.</span><span class="sxs-lookup"><span data-stu-id="78a8f-113">If the email alias set in the search filter is a distribution group and the distribution group membership is not expanded, the response will contain the mailbox information for the distribution group.</span></span> <span data-ttu-id="78a8f-114">Si el alias de correo electrónico establecido en el filtro de búsqueda es un grupo de distribución y se expande la pertenencia al grupo de distribución, la respuesta contendrá la información de buzón de correo para cada buzón de correo que sea miembro del grupo de distribución.</span><span class="sxs-lookup"><span data-stu-id="78a8f-114">If the email alias set in the search filter is a distribution group and the distribution group membership is expanded, the response will contain the mailbox information for each mailbox that is a member of the distribution group.</span></span> <span data-ttu-id="78a8f-115">Si el filtro de búsqueda contiene alias de un único usuario, la respuesta contendrá la información de buzón de correo para el usuario único.</span><span class="sxs-lookup"><span data-stu-id="78a8f-115">If the search filter contains a single user's alias, the response will contain the mailbox information for the single user.</span></span> <span data-ttu-id="78a8f-116">La respuesta contendrá todos los buzones que admite búsquedos si el elemento [GetSearchableMailboxes](getsearchablemailboxes.md) está vacío.</span><span class="sxs-lookup"><span data-stu-id="78a8f-116">The response will contain all searchable mailboxes if the [GetSearchableMailboxes](getsearchablemailboxes.md) element is empty.</span></span> <span data-ttu-id="78a8f-117">Esto es igual a tener un elemento [SearchFilter](searchfilter.md) vacío y el elemento de [ExpandGroupMembership](expandgroupmembership.md) establecido en **false**.</span><span class="sxs-lookup"><span data-stu-id="78a8f-117">This is the same as having an empty [SearchFilter](searchfilter.md) element and the [ExpandGroupMembership](expandgroupmembership.md) element set to **false**.</span></span>
  
### <a name="getsearchablemailboxes-operation-soap-headers"></a><span data-ttu-id="78a8f-118">Encabezados SOAP de operación de GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="78a8f-118">GetSearchableMailboxes operation SOAP headers</span></span>

<span data-ttu-id="78a8f-119">La operación de **GetSearchableMailboxes** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="78a8f-119">The **GetSearchableMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="78a8f-120">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="78a8f-120">**Header name**</span></span>|<span data-ttu-id="78a8f-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="78a8f-121">**Element**</span></span>|<span data-ttu-id="78a8f-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="78a8f-122">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="78a8f-123">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="78a8f-123">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="78a8f-124">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="78a8f-124">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="78a8f-125">Identifica las funciones de servidor que son necesarias en orden para el autor de la llamada realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="78a8f-125">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="78a8f-126">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="78a8f-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="78a8f-127">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="78a8f-127">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="78a8f-128">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="78a8f-128">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="78a8f-129">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="78a8f-129">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="78a8f-130">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="78a8f-130">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="78a8f-131">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="78a8f-131">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="78a8f-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="78a8f-132">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="78a8f-133">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="78a8f-133">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="78a8f-134">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="78a8f-134">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getsearchablemailboxes-operation-request-example-request-information-about-a-distribution-group"></a><span data-ttu-id="78a8f-135">Ejemplo de solicitud de operación de GetSearchableMailboxes: solicitar información acerca de un grupo de distribución</span><span class="sxs-lookup"><span data-stu-id="78a8f-135">GetSearchableMailboxes operation request example: Request information about a distribution group</span></span>

<span data-ttu-id="78a8f-136">El siguiente ejemplo de una solicitud de operación **GetSearchableMailboxes** muestra cómo obtener la información de buzón de correo para el grupo de distribución lolgroup.</span><span class="sxs-lookup"><span data-stu-id="78a8f-136">The following example of a **GetSearchableMailboxes** operation request shows how to get the mailbox information for the lolgroup distribution group.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="78a8f-137">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="78a8f-137">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="78a8f-138">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="78a8f-138">GetSearchableMailboxes</span></span>](getsearchablemailboxes.md)
    
- [<span data-ttu-id="78a8f-139">SearchFilter</span><span class="sxs-lookup"><span data-stu-id="78a8f-139">SearchFilter</span></span>](searchfilter.md)
    
- [<span data-ttu-id="78a8f-140">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="78a8f-140">ExpandGroupMembership</span></span>](expandgroupmembership.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-a-distribution-group"></a><span data-ttu-id="78a8f-141">La respuesta es correcta de operación GetSearchableMailboxes: obtener información acerca de un grupo de distribución</span><span class="sxs-lookup"><span data-stu-id="78a8f-141">Successful GetSearchableMailboxes operation response: Get information about a distribution group</span></span>

<span data-ttu-id="78a8f-142">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **GetSearchableMailboxes** para obtener la información de detección para el grupo de distribución lolgroup.</span><span class="sxs-lookup"><span data-stu-id="78a8f-142">The following example shows a successful response to a **GetSearchableMailboxes** operation request to get the discovery information for the lolgroup distribution group.</span></span> 
  
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
      <GetSearchableMailboxesResponse ResponseClass="Success" 
                                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <SearchableMailboxes>
            <SearchableMailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="78a8f-143">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="78a8f-143">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="78a8f-144">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="78a8f-144">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)
    
- [<span data-ttu-id="78a8f-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="78a8f-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="78a8f-146">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="78a8f-146">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
- [<span data-ttu-id="78a8f-147">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="78a8f-147">SearchableMailbox</span></span>](searchablemailbox.md)
    
- [<span data-ttu-id="78a8f-148">GUID</span><span class="sxs-lookup"><span data-stu-id="78a8f-148">Guid</span></span>](guid-ex15websvcsotherref.md)
    
- [<span data-ttu-id="78a8f-149">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="78a8f-149">PrimarySmtpAddress</span></span>](primarysmtpaddress.md)
    
- [<span data-ttu-id="78a8f-150">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="78a8f-150">IsExternalMailbox</span></span>](isexternalmailbox.md)
    
- [<span data-ttu-id="78a8f-151">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="78a8f-151">ExternalEmailAddress</span></span>](externalemailaddress.md)
    
- [<span data-ttu-id="78a8f-152">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="78a8f-152">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="78a8f-153">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="78a8f-153">IsMembershipGroup</span></span>](ismembershipgroup.md)
    
- [<span data-ttu-id="78a8f-154">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="78a8f-154">ReferenceId</span></span>](referenceid.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-an-expanded-distribution-group"></a><span data-ttu-id="78a8f-155">La respuesta es correcta de operación GetSearchableMailboxes: obtener información acerca de un grupo de distribución expandido</span><span class="sxs-lookup"><span data-stu-id="78a8f-155">Successful GetSearchableMailboxes operation response: Get information about an expanded distribution group</span></span>

<span data-ttu-id="78a8f-156">En el ejemplo siguiente se muestra una respuesta a una solicitud de operación **GetSearchableMailboxes** para obtener la información de detección sobre los miembros del grupo de distribución expandido lolgroup correcta.</span><span class="sxs-lookup"><span data-stu-id="78a8f-156">The following example shows a successful response to a **GetSearchableMailboxes** operation request to get the discovery information about members of the expanded lolgroup distribution group.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="526" MinorBuildNumber="0" Version="Exchange2013" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetSearchableMailboxesResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <SearchableMailboxes>
        <SearchableMailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>e2d42cdf-a227-1ec3-486b-6fa0ebaadb9f5</Guid>
          <PrimarySmtpAddress>JSmith@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Julia Smith</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=0a1fc86f883846152405d60956dd02e7-Julia</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>45d0fff1-6541-459a-a343-52453b30e12ca</Guid>
          <PrimarySmtpAddress>LMoore@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Laura Moore</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=2910d8f8316f4378bbf9338d8f9d714b-Laura</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="78a8f-157">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="78a8f-157">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="78a8f-158">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="78a8f-158">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)
    
- [<span data-ttu-id="78a8f-159">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="78a8f-159">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="78a8f-160">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="78a8f-160">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
- [<span data-ttu-id="78a8f-161">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="78a8f-161">SearchableMailbox</span></span>](searchablemailbox.md)
    
- [<span data-ttu-id="78a8f-162">GUID</span><span class="sxs-lookup"><span data-stu-id="78a8f-162">Guid</span></span>](guid-ex15websvcsotherref.md)
    
- [<span data-ttu-id="78a8f-163">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="78a8f-163">PrimarySmtpAddress</span></span>](primarysmtpaddress.md)
    
- [<span data-ttu-id="78a8f-164">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="78a8f-164">IsExternalMailbox</span></span>](isexternalmailbox.md)
    
- [<span data-ttu-id="78a8f-165">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="78a8f-165">ExternalEmailAddress</span></span>](externalemailaddress.md)
    
- [<span data-ttu-id="78a8f-166">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="78a8f-166">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="78a8f-167">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="78a8f-167">IsMembershipGroup</span></span>](ismembershipgroup.md)
    
- [<span data-ttu-id="78a8f-168">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="78a8f-168">ReferenceId</span></span>](referenceid.md)
    
## <a name="getsearchablemailboxes-operation-error-response"></a><span data-ttu-id="78a8f-169">Respuesta de error de la operación de GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="78a8f-169">GetSearchableMailboxes operation error response</span></span>

<span data-ttu-id="78a8f-170">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="78a8f-170">The following example shows an error response to a **GetSearchableMailboxes** operation request.</span></span> <span data-ttu-id="78a8f-171">Esta es una respuesta a una solicitud para obtener todos los buzones que admite búsquedos cuando el argumento de **ExpandGroupMembership** está establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="78a8f-171">This is a response to a request to get all searchable mailboxes when the **ExpandGroupMembership** argument is set to **true**.</span></span> 
  
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
      <GetSearchableMailboxesResponse ResponseClass="Error" 
                                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot use wildcard or empty query when auto group expansion is enabled.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <SearchableMailboxes/>
      </GetSearchableMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="78a8f-172">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="78a8f-172">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="78a8f-173">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="78a8f-173">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)
    
- [<span data-ttu-id="78a8f-174">MessageText</span><span class="sxs-lookup"><span data-stu-id="78a8f-174">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="78a8f-175">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="78a8f-175">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="78a8f-176">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="78a8f-176">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="78a8f-177">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="78a8f-177">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
<span data-ttu-id="78a8f-178">Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="78a8f-178">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="78a8f-179">Ver también</span><span class="sxs-lookup"><span data-stu-id="78a8f-179">See also</span></span>

- [<span data-ttu-id="78a8f-180">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="78a8f-180">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="78a8f-181">Operación SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="78a8f-181">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="78a8f-182">Operación SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="78a8f-182">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="78a8f-183">Operación GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="78a8f-183">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="78a8f-184">Operación GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="78a8f-184">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="78a8f-185">Operación GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="78a8f-185">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="78a8f-186">Operación GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="78a8f-186">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

