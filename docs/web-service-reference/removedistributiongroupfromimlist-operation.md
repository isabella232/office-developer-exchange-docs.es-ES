---
title: Operación RemoveDistributionGroupFromImList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 252bddf2-98b6-4824-b548-2fba2bda5384
description: Busque información sobre la EWS RemoveDistributionGroupFromImList operación.
ms.openlocfilehash: 9999f98a5698dd33c22e22fdf86bd00a2d053b52
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837096"
---
# <a name="removedistributiongroupfromimlist-operation"></a><span data-ttu-id="f3d6f-103">Operación RemoveDistributionGroupFromImList</span><span class="sxs-lookup"><span data-stu-id="f3d6f-103">RemoveDistributionGroupFromImList operation</span></span>

<span data-ttu-id="f3d6f-104">Obtenga información acerca de la operación de EWS **RemoveDistributionGroupFromImList** .</span><span class="sxs-lookup"><span data-stu-id="f3d6f-104">Find information about the **RemoveDistributionGroupFromImList** EWS operation.</span></span> 
  
<span data-ttu-id="f3d6f-105">La operación **RemoveDistributionGroupFromImList** quita un grupo de distribución de la lista de mensajería instantánea (mi) de Lync cuando Lync usa Exchange para el almacén de contactos.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-105">The **RemoveDistributionGroupFromImList** operation removes a distribution group from the Lync instant messaging (IM) list when Lync uses Exchange for the contact store.</span></span> 
  
<span data-ttu-id="f3d6f-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-removedistributiongroupfromimlist-operation"></a><span data-ttu-id="f3d6f-107">Mediante la operación RemoveDistributionGroupFromImList</span><span class="sxs-lookup"><span data-stu-id="f3d6f-107">Using the RemoveDistributionGroupFromImList operation</span></span>

<span data-ttu-id="f3d6f-108">La operación de **RemoveDistributionGroupFromImList** acepta un argumento único que identifica un grupo de distribución para quitar de la lista de Lync IM almacenada en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-108">The **RemoveDistributionGroupFromImList** operation accepts a single argument that identifies a distribution group to remove from the Lync IM list stored on an Exchange server.</span></span> 
  
### <a name="removedistributiongroupfromimlist-operation-soap-headers"></a><span data-ttu-id="f3d6f-109">Encabezados SOAP de operación de RemoveDistributionGroupFromImList</span><span class="sxs-lookup"><span data-stu-id="f3d6f-109">RemoveDistributionGroupFromImList operation SOAP headers</span></span>

<span data-ttu-id="f3d6f-110">La operación de **RemoveDistributionGroupFromImList** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-110">The **RemoveDistributionGroupFromImList** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="f3d6f-111">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="f3d6f-111">**Header name**</span></span>|<span data-ttu-id="f3d6f-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="f3d6f-112">**Element**</span></span>|<span data-ttu-id="f3d6f-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f3d6f-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f3d6f-114">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="f3d6f-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="f3d6f-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="f3d6f-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="f3d6f-116">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="f3d6f-117">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f3d6f-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="f3d6f-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="f3d6f-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="f3d6f-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="f3d6f-120">Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="f3d6f-121">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f3d6f-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="f3d6f-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="f3d6f-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f3d6f-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f3d6f-124">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="f3d6f-125">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f3d6f-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="f3d6f-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="f3d6f-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f3d6f-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f3d6f-128">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="f3d6f-129">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="removedistributiongroupfromimlist-operation-request-example-remove-a-distribution-group-from-an-im-list"></a><span data-ttu-id="f3d6f-130">Ejemplo de solicitud de operación de RemoveDistributionGroupFromImList: quitar un grupo de distribución de una lista de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="f3d6f-130">RemoveDistributionGroupFromImList operation request example: Remove a distribution group from an IM list</span></span>

<span data-ttu-id="f3d6f-131">El siguiente ejemplo de una solicitud de operación **RemoveDistributionGroupFromImList** muestra cómo quitar un grupo de distribución de un grupo de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-131">The following example of a **RemoveDistributionGroupFromImList** operation request shows how to remove a distribution group from an IM group.</span></span> <span data-ttu-id="f3d6f-132">La operación **RemoveDistributionGroupFromImList** acepta el identificador del grupo único para identificar el grupo de distribución para quitar de la lista de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-132">The **RemoveDistributionGroupFromImList** operation accepts the unique group identifier to identify the distribution group to remove from the IM list.</span></span> <span data-ttu-id="f3d6f-133">El elemento [ExchangeStoreId](exchangestoreid.md) que se devuelve en la respuesta de la [operación de GetImItemList](getimitemlist-operation.md) y la [operación de AddDistributionGroupToImList](adddistributiongrouptoimlist-operation.md) identifica los grupos de distribución que se pueden quitar de la lista de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-133">The [ExchangeStoreId](exchangestoreid.md) element that is returned in the response for the [GetImItemList operation](getimitemlist-operation.md) and the [AddDistributionGroupToImList operation](adddistributiongrouptoimlist-operation.md) identifies distribution groups that can be removed from the IM list.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f3d6f-134">Todos los identificadores de artículo y cambiar claves en este artículo se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:RemoveDistributionGroupFromImList>
         <m:GroupId Id="AAMkADEzO4QrAABmEh5oAAA="/>
      </m:RemoveDistributionGroupFromImList>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="f3d6f-135">En la solicitud SOAP body, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="f3d6f-135">The following elements are used in the request SOAP body:</span></span>
  
- [<span data-ttu-id="f3d6f-136">RemoveDistributionGroupFromImList</span><span class="sxs-lookup"><span data-stu-id="f3d6f-136">RemoveDistributionGroupFromImList</span></span>](removedistributiongroupfromimlist.md)
    
- [<span data-ttu-id="f3d6f-137">GroupId</span><span class="sxs-lookup"><span data-stu-id="f3d6f-137">GroupId</span></span>](groupid.md)
    
## <a name="successful-removedistributiongroupfromimlist-operation-response"></a><span data-ttu-id="f3d6f-138">Respuesta es correcta de operación RemoveDistributionGroupFromImList</span><span class="sxs-lookup"><span data-stu-id="f3d6f-138">Successful RemoveDistributionGroupFromImList operation response</span></span>

<span data-ttu-id="f3d6f-139">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **RemoveDistributionGroupFromImList** a una quitar un grupo de distribución desde un grupo de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-139">The following example shows a successful response to a **RemoveDistributionGroupFromImList** operation request to a remove a distribution group from an IM group.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveDistributionGroupFromImListResponse ResponseClass="Success" 
                                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveDistributionGroupFromImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="f3d6f-140">En la respuesta SOAP body, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="f3d6f-140">The following elements are used in the response SOAP body:</span></span>
  
- [<span data-ttu-id="f3d6f-141">RemoveDistributionGroupFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="f3d6f-141">RemoveDistributionGroupFromImListResponse</span></span>](removedistributiongroupfromimlistresponse.md)
    
- [<span data-ttu-id="f3d6f-142">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f3d6f-142">ResponseCode</span></span>](responsecode.md)
    
## <a name="removedistributiongroupfromimlist-operation-error-response-example"></a><span data-ttu-id="f3d6f-143">Ejemplo de respuesta de error de operación de RemoveDistributionGroupFromImList</span><span class="sxs-lookup"><span data-stu-id="f3d6f-143">RemoveDistributionGroupFromImList operation error response example</span></span>

<span data-ttu-id="f3d6f-144">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **RemoveDistributionGroupFromImList** .</span><span class="sxs-lookup"><span data-stu-id="f3d6f-144">The following example shows an error response to a **RemoveDistributionGroupFromImList** operation request.</span></span> <span data-ttu-id="f3d6f-145">Esta es una respuesta a una solicitud para quitar un grupo de distribución que ya se ha quitado el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f3d6f-145">This is a response to a request to remove a distribution group that has already been removed from the mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveDistributionGroupFromImListResponse ResponseClass="Error" 
                                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveDistributionGroupFromImListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="f3d6f-146">En el cuerpo del mensaje SOAP de respuesta de error se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="f3d6f-146">The following elements are used in the error response SOAP body:</span></span>
  
- [<span data-ttu-id="f3d6f-147">RemoveDistributionGroupFromImListResponse</span><span class="sxs-lookup"><span data-stu-id="f3d6f-147">RemoveDistributionGroupFromImListResponse</span></span>](removedistributiongroupfromimlistresponse.md)
    
- [<span data-ttu-id="f3d6f-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="f3d6f-148">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="f3d6f-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f3d6f-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f3d6f-150">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f3d6f-150">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="f3d6f-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3d6f-151">See also</span></span>

- [<span data-ttu-id="f3d6f-152">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f3d6f-152">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="f3d6f-153">Operación GetImItemList</span><span class="sxs-lookup"><span data-stu-id="f3d6f-153">GetImItemList operation</span></span>](getimitemlist-operation.md)
    
- [<span data-ttu-id="f3d6f-154">Operación AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="f3d6f-154">AddDistributionGroupToImList operation</span></span>](adddistributiongrouptoimlist-operation.md)
    
- [<span data-ttu-id="f3d6f-155">Las personas y los contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f3d6f-155">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx#What)
    

