---
title: Operación AddDistributionGroupToImList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5aa9bec8-71cf-4a6e-8ec8-b4965b40fd4a
description: Buscar información sobre la operación de EWS de AddDistributionGroupToImList.
ms.openlocfilehash: e68e21b6994af5773f5cf991d55129e1db3367ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463695"
---
# <a name="adddistributiongrouptoimlist-operation"></a><span data-ttu-id="dd65a-103">Operación AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="dd65a-103">AddDistributionGroupToImList operation</span></span>

<span data-ttu-id="dd65a-104">Buscar información sobre la operación de EWS de **AddDistributionGroupToImList** .</span><span class="sxs-lookup"><span data-stu-id="dd65a-104">Find information about the **AddDistributionGroupToImList** EWS operation.</span></span> 
  
<span data-ttu-id="dd65a-105">La operación de servicios web Exchange de **AddDistributionGroupToImList** (EWS) agrega un grupo de distribución a la lista de mensajería instantánea en el almacén de contactos unificados.</span><span class="sxs-lookup"><span data-stu-id="dd65a-105">The **AddDistributionGroupToImList** Exchange Web Services (EWS) operation adds a distribution group to the instant messaging (IM) list in the Unified Contact Store.</span></span> 
  
<span data-ttu-id="dd65a-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dd65a-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-adddistributiongrouptoimlist-operation"></a><span data-ttu-id="dd65a-107">Uso de la operación AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="dd65a-107">Using the AddDistributionGroupToImList operation</span></span>

<span data-ttu-id="dd65a-108">La operación **AddDistributionGroupToImList** toma un argumento único que identifica un grupo de distribución para agregarlo a la lista de mi.</span><span class="sxs-lookup"><span data-stu-id="dd65a-108">The **AddDistributionGroupToImList** operation takes a single argument that identifies a distribution group to add to the IM list.</span></span> <span data-ttu-id="dd65a-109">Esta operación no crea un grupo de distribución; el grupo de distribución ya debe estar creado.</span><span class="sxs-lookup"><span data-stu-id="dd65a-109">This operation does not create a distribution group; the distribution group must already be created.</span></span> 
  
<span data-ttu-id="dd65a-110">Esta operación puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="dd65a-110">This operation can use the SOAP headers that are listed in the following table.</span></span>
  
<span data-ttu-id="dd65a-111">**Tabla 1. Encabezados SOAP de operación AddDistributionGroupToImList**</span><span class="sxs-lookup"><span data-stu-id="dd65a-111">**Table 1. AddDistributionGroupToImList operation SOAP headers**</span></span>

|<span data-ttu-id="dd65a-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="dd65a-112">**Header name**</span></span>|<span data-ttu-id="dd65a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dd65a-113">**Element**</span></span>|<span data-ttu-id="dd65a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd65a-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dd65a-115">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="dd65a-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="dd65a-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="dd65a-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="dd65a-117">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="dd65a-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="dd65a-118">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="dd65a-118">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="dd65a-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="dd65a-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="dd65a-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="dd65a-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="dd65a-121">Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="dd65a-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="dd65a-122">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="dd65a-122">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="dd65a-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="dd65a-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="dd65a-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="dd65a-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="dd65a-125">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="dd65a-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="dd65a-126">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="dd65a-126">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="dd65a-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="dd65a-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="dd65a-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="dd65a-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="dd65a-129">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dd65a-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="dd65a-130">Esto es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="dd65a-130">This is applicable to a response.</span></span>  <br/> |
   
## <a name="adddistributiongrouptoimlist-operation-request-example"></a><span data-ttu-id="dd65a-131">Ejemplo de solicitud de operación AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="dd65a-131">AddDistributionGroupToImList operation request example</span></span>

<span data-ttu-id="dd65a-132">El siguiente ejemplo de una solicitud de operación de **AddDistributionGroupToImList** muestra cómo agregar un grupo de distribución a la lista de mi.</span><span class="sxs-lookup"><span data-stu-id="dd65a-132">The following example of an **AddDistributionGroupToImList** operation request shows how to add a distribution group to the IM list.</span></span> 
  
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
      <m:AddDistributionGroupToImList>
         <m:SmtpAddress>distributionlist1@example.com</m:SmtpAddress>
      </m:AddDistributionGroupToImList>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="dd65a-133">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="dd65a-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="dd65a-134">AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="dd65a-134">AddDistributionGroupToImList</span></span>](adddistributiongrouptoimlist.md)   
- [<span data-ttu-id="dd65a-135">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="dd65a-135">SmtpAddress</span></span>](smtpaddress.md)
    
## <a name="successful-adddistributiongrouptoimlist-operation-response"></a><span data-ttu-id="dd65a-136">Respuesta de operación AddDistributionGroupToImList correcta</span><span class="sxs-lookup"><span data-stu-id="dd65a-136">Successful AddDistributionGroupToImList operation response</span></span>

<span data-ttu-id="dd65a-137">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **AddDistributionGroupToImList** .</span><span class="sxs-lookup"><span data-stu-id="dd65a-137">The following example shows a successful response to an **AddDistributionGroupToImList** operation request.</span></span> 
  
<span data-ttu-id="dd65a-138">La respuesta correcta contiene el nombre para mostrar del grupo de distribución, la clase de almacén de Exchange para el grupo de distribución y el identificador de EWS del nuevo grupo de distribución.</span><span class="sxs-lookup"><span data-stu-id="dd65a-138">The successful response contains the distribution group display name, the Exchange store class for the distribution group, and the EWS identifier of the new distribution group.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"
            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
            xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="dd65a-139">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="dd65a-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="dd65a-140">AddDistributionGroupToImListResponse</span><span class="sxs-lookup"><span data-stu-id="dd65a-140">AddDistributionGroupToImListResponse</span></span>](adddistributiongrouptoimlistresponse.md)
    
- [<span data-ttu-id="dd65a-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="dd65a-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="dd65a-142">Desagrupo</span><span class="sxs-lookup"><span data-stu-id="dd65a-142">ImGroup</span></span>](imgroup.md)
    
- [<span data-ttu-id="dd65a-143">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="dd65a-143">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="dd65a-144">GroupType</span><span class="sxs-lookup"><span data-stu-id="dd65a-144">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="dd65a-145">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="dd65a-145">ExchangeStoreId</span></span>](exchangestoreid.md)
    
## <a name="adddistributiongrouptoimlist-operation-errorinvalidimdistributiongroupsmtpaddress-error-response"></a><span data-ttu-id="dd65a-146">AddDistributionGroupToImList Operation ErrorInvalidImDistributionGroupSmtpAddress error Response</span><span class="sxs-lookup"><span data-stu-id="dd65a-146">AddDistributionGroupToImList operation ErrorInvalidImDistributionGroupSmtpAddress error response</span></span>

<span data-ttu-id="dd65a-147">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **AddDistributionGroupToImList** .</span><span class="sxs-lookup"><span data-stu-id="dd65a-147">The following example shows an error response to an **AddDistributionGroupToImList** operation request.</span></span> <span data-ttu-id="dd65a-148">La siguiente respuesta de error se produce cuando se realiza un intento de agregar un grupo de distribución que no existe en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="dd65a-148">The following error response occurs when an attempt is made to add a distribution group that does not exist in the Exchange store.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddDistributionGroupToImListResponse ResponseClass="Error" 
                                            xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified IM distribution group SMTP address is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImDistributionGroupSmtpAddress</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </AddDistributionGroupToImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="dd65a-149">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="dd65a-149">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="dd65a-150">AddDistributionGroupToImListResponse</span><span class="sxs-lookup"><span data-stu-id="dd65a-150">AddDistributionGroupToImListResponse</span></span>](adddistributiongrouptoimlistresponse.md)
    
- [<span data-ttu-id="dd65a-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="dd65a-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="dd65a-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="dd65a-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="dd65a-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd65a-153">See also</span></span>

- [<span data-ttu-id="dd65a-154">Personas y contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="dd65a-154">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)   
- [<span data-ttu-id="dd65a-155">AddImGroup</span><span class="sxs-lookup"><span data-stu-id="dd65a-155">AddImGroup</span></span>](addimgroup-operation.md)   
- [<span data-ttu-id="dd65a-156">RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="dd65a-156">RemoveImGroup</span></span>](removeimgroup-operation.md)
    

