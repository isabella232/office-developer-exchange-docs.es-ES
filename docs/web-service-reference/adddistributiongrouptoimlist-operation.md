---
title: Operación AddDistributionGroupToImList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5aa9bec8-71cf-4a6e-8ec8-b4965b40fd4a
description: Busque información sobre la EWS AddDistributionGroupToImList operación.
ms.openlocfilehash: 7c562c317890a4cffb9e5844ea41c1096a8595b4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763393"
---
# <a name="adddistributiongrouptoimlist-operation"></a><span data-ttu-id="b54a1-103">Operación AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="b54a1-103">AddDistributionGroupToImList operation</span></span>

<span data-ttu-id="b54a1-104">Obtenga información acerca de la operación de EWS **AddDistributionGroupToImList** .</span><span class="sxs-lookup"><span data-stu-id="b54a1-104">Find information about the **AddDistributionGroupToImList** EWS operation.</span></span> 
  
<span data-ttu-id="b54a1-105">La operación de Exchange Web Services (EWS) **AddDistributionGroupToImList** agrega un grupo de distribución a la lista (IM) en el almacén de contactos unificados de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="b54a1-105">The **AddDistributionGroupToImList** Exchange Web Services (EWS) operation adds a distribution group to the instant messaging (IM) list in the Unified Contact Store.</span></span> 
  
<span data-ttu-id="b54a1-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b54a1-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-adddistributiongrouptoimlist-operation"></a><span data-ttu-id="b54a1-107">Mediante la operación AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="b54a1-107">Using the AddDistributionGroupToImList operation</span></span>

<span data-ttu-id="b54a1-108">La operación de **AddDistributionGroupToImList** toma un argumento único que identifica un grupo de distribución para agregar a la lista de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="b54a1-108">The **AddDistributionGroupToImList** operation takes a single argument that identifies a distribution group to add to the IM list.</span></span> <span data-ttu-id="b54a1-109">Esta operación no crea un grupo de distribución; el grupo de distribución debe estar ya creado.</span><span class="sxs-lookup"><span data-stu-id="b54a1-109">This operation does not create a distribution group; the distribution group must already be created.</span></span> 
  
<span data-ttu-id="b54a1-110">Esta operación puede usar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="b54a1-110">This operation can use the SOAP headers that are listed in the following table.</span></span>
  
<span data-ttu-id="b54a1-111">**La tabla 1. Encabezados SOAP de operación de AddDistributionGroupToImList**</span><span class="sxs-lookup"><span data-stu-id="b54a1-111">**Table 1. AddDistributionGroupToImList operation SOAP headers**</span></span>

|<span data-ttu-id="b54a1-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="b54a1-112">**Header name**</span></span>|<span data-ttu-id="b54a1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b54a1-113">**Element**</span></span>|<span data-ttu-id="b54a1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b54a1-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b54a1-115">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="b54a1-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="b54a1-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="b54a1-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="b54a1-117">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="b54a1-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="b54a1-118">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="b54a1-118">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="b54a1-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="b54a1-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="b54a1-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="b54a1-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="b54a1-121">Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.</span><span class="sxs-lookup"><span data-stu-id="b54a1-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="b54a1-122">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="b54a1-122">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="b54a1-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="b54a1-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="b54a1-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="b54a1-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="b54a1-125">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="b54a1-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="b54a1-126">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="b54a1-126">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="b54a1-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="b54a1-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="b54a1-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="b54a1-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="b54a1-129">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b54a1-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="b54a1-130">Esto es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="b54a1-130">This is applicable to a response.</span></span>  <br/> |
   
## <a name="adddistributiongrouptoimlist-operation-request-example"></a><span data-ttu-id="b54a1-131">Ejemplo de solicitud de operación de AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="b54a1-131">AddDistributionGroupToImList operation request example</span></span>

<span data-ttu-id="b54a1-132">El siguiente ejemplo de una solicitud de operación **AddDistributionGroupToImList** muestra cómo agregar un grupo de distribución a la lista de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="b54a1-132">The following example of an **AddDistributionGroupToImList** operation request shows how to add a distribution group to the IM list.</span></span> 
  
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
      <m:AddDistributionGroupToImList>
         <m:SmtpAddress>distributionlist1@example.com</m:SmtpAddress>
      </m:AddDistributionGroupToImList>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b54a1-133">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="b54a1-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="b54a1-134">AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="b54a1-134">AddDistributionGroupToImList</span></span>](adddistributiongrouptoimlist.md)   
- [<span data-ttu-id="b54a1-135">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="b54a1-135">SmtpAddress</span></span>](smtpaddress.md)
    
## <a name="successful-adddistributiongrouptoimlist-operation-response"></a><span data-ttu-id="b54a1-136">Respuesta es correcta de operación AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="b54a1-136">Successful AddDistributionGroupToImList operation response</span></span>

<span data-ttu-id="b54a1-137">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **AddDistributionGroupToImList** .</span><span class="sxs-lookup"><span data-stu-id="b54a1-137">The following example shows a successful response to an **AddDistributionGroupToImList** operation request.</span></span> 
  
<span data-ttu-id="b54a1-138">La respuesta correcta contiene el nombre para mostrar de grupo de distribución, la clase de almacén de Exchange para el grupo de distribución y el identificador de EWS del nuevo grupo de distribución.</span><span class="sxs-lookup"><span data-stu-id="b54a1-138">The successful response contains the distribution group display name, the Exchange store class for the distribution group, and the EWS identifier of the new distribution group.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"
            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
            xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <s:Header>
      <t:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013"/>
   </s:Header>
   <s:Body>
      <m:AddDistributionGroupToImListResponse ResponseClass="Success">
         <m:ResponseCode>NoError</m:ResponseCode>
         <m:ImGroup>
            <t:DisplayName>distributionlist1@example.com</t:DisplayName>
            <t:GroupType>IPM.DistList.MOC.DG</t:GroupType>
            <t:ExchangeStoreId Id="AAMkAGQ1MjJjAA=" 
                             ChangeKey="EgAAAA=="/>
      </m:ImGroup>
      </m:AddDistributionGroupToImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="b54a1-139">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="b54a1-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="b54a1-140">AddDistributionGroupToImListResponse</span><span class="sxs-lookup"><span data-stu-id="b54a1-140">AddDistributionGroupToImListResponse</span></span>](adddistributiongrouptoimlistresponse.md)
    
- [<span data-ttu-id="b54a1-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b54a1-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="b54a1-142">ImGroup</span><span class="sxs-lookup"><span data-stu-id="b54a1-142">ImGroup</span></span>](imgroup.md)
    
- [<span data-ttu-id="b54a1-143">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="b54a1-143">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="b54a1-144">GroupType</span><span class="sxs-lookup"><span data-stu-id="b54a1-144">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="b54a1-145">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="b54a1-145">ExchangeStoreId</span></span>](exchangestoreid.md)
    
## <a name="adddistributiongrouptoimlist-operation-errorinvalidimdistributiongroupsmtpaddress-error-response"></a><span data-ttu-id="b54a1-146">Operación AddDistributionGroupToImList respuesta de error de ErrorInvalidImDistributionGroupSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="b54a1-146">AddDistributionGroupToImList operation ErrorInvalidImDistributionGroupSmtpAddress error response</span></span>

<span data-ttu-id="b54a1-147">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **AddDistributionGroupToImList** .</span><span class="sxs-lookup"><span data-stu-id="b54a1-147">The following example shows an error response to an **AddDistributionGroupToImList** operation request.</span></span> <span data-ttu-id="b54a1-148">La siguiente respuesta de error se produce cuando se realiza un intento para agregar un grupo de distribución que no existe en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b54a1-148">The following error response occurs when an attempt is made to add a distribution group that does not exist in the Exchange store.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddDistributionGroupToImListResponse ResponseClass="Error" 
                                            xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified IM distribution group SMTP address is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImDistributionGroupSmtpAddress</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </AddDistributionGroupToImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="b54a1-149">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="b54a1-149">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="b54a1-150">AddDistributionGroupToImListResponse</span><span class="sxs-lookup"><span data-stu-id="b54a1-150">AddDistributionGroupToImListResponse</span></span>](adddistributiongrouptoimlistresponse.md)
    
- [<span data-ttu-id="b54a1-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="b54a1-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="b54a1-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b54a1-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="b54a1-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="b54a1-153">See also</span></span>

- [<span data-ttu-id="b54a1-154">Las personas y los contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b54a1-154">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)   
- [<span data-ttu-id="b54a1-155">AddImGroup</span><span class="sxs-lookup"><span data-stu-id="b54a1-155">AddImGroup</span></span>](addimgroup-operation.md)   
- [<span data-ttu-id="b54a1-156">RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="b54a1-156">RemoveImGroup</span></span>](removeimgroup-operation.md)
    

