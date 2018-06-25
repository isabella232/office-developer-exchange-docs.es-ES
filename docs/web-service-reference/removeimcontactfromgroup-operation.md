---
title: Operación RemoveImContactFromGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a190bbec-c71b-4e6a-880b-55854c724d8c
description: Busque información sobre la EWS RemoveImContactFromGroup operación.
ms.openlocfilehash: 8c9af251014dbddabb439ed5bf5dc35580da6a90
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837099"
---
# <a name="removeimcontactfromgroup-operation"></a><span data-ttu-id="f7776-103">Operación RemoveImContactFromGroup</span><span class="sxs-lookup"><span data-stu-id="f7776-103">RemoveImContactFromGroup operation</span></span>

<span data-ttu-id="f7776-104">Obtenga información acerca de la operación de EWS **RemoveImContactFromGroup** .</span><span class="sxs-lookup"><span data-stu-id="f7776-104">Find information about the **RemoveImContactFromGroup** EWS operation.</span></span> 
  
<span data-ttu-id="f7776-105">La operación **RemoveImContactFromGroup** quita un único contacto de mensajería instantánea de un grupo de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="f7776-105">The **RemoveImContactFromGroup** operation removes a single IM contact from an IM group.</span></span> 
  
<span data-ttu-id="f7776-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f7776-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-removeimcontactfromgroup-operation"></a><span data-ttu-id="f7776-107">Mediante la operación RemoveImContactFromGroup</span><span class="sxs-lookup"><span data-stu-id="f7776-107">Using the RemoveImContactFromGroup operation</span></span>

<span data-ttu-id="f7776-108">La operación **RemoveImContactFromGroup** toma dos argumentos: un identificador de elemento de contacto y el grupo (IM) desde la que se quita el contacto de mensajería de instantánea correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f7776-108">The **RemoveImContactFromGroup** operation takes two arguments: a contact item identifier, and the corresponding instant messaging (IM) group from which the contact is removed.</span></span> 
  
### <a name="removeimcontactfromgroup-operation-soap-headers"></a><span data-ttu-id="f7776-109">Encabezados SOAP de operación de RemoveImContactFromGroup</span><span class="sxs-lookup"><span data-stu-id="f7776-109">RemoveImContactFromGroup operation SOAP headers</span></span>

<span data-ttu-id="f7776-110">La operación de **RemoveImContactFromGroup** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f7776-110">The **RemoveImContactFromGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="f7776-111">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="f7776-111">**Header name**</span></span>|<span data-ttu-id="f7776-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="f7776-112">**Element**</span></span>|<span data-ttu-id="f7776-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f7776-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f7776-114">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="f7776-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="f7776-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="f7776-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="f7776-116">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="f7776-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="f7776-117">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f7776-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f7776-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="f7776-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="f7776-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="f7776-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="f7776-120">Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.</span><span class="sxs-lookup"><span data-stu-id="f7776-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="f7776-121">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f7776-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f7776-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="f7776-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="f7776-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f7776-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f7776-124">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="f7776-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="f7776-125">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="f7776-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f7776-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="f7776-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="f7776-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f7776-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f7776-128">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f7776-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="f7776-129">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7776-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="removeimcontactfromgroup-operation-request-example"></a><span data-ttu-id="f7776-130">Ejemplo de solicitud de operación de RemoveImContactFromGroup</span><span class="sxs-lookup"><span data-stu-id="f7776-130">RemoveImContactFromGroup operation request example</span></span>

<span data-ttu-id="f7776-131">El siguiente ejemplo de una solicitud de operación **RemoveImContactFromGroup** muestra cómo quitar un contacto de mensajería instantánea de un grupo de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="f7776-131">The following example of a **RemoveImContactFromGroup** operation request shows how to remove an IM contact from an IM group.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f7776-132">Los identificadores de grupo y contactos se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="f7776-132">The group and contact identifiers have been shortened to preserve readability.</span></span> 
  
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
      <m:RemoveImContactFromGroup>
         <m:ContactId Id="AAMkAGQ1MjJjMTBkLTcAAAAvcAAA="
                      ChangeKey="EQAAABYAAABtF8oI7iVOQ"/>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkbWAAAAAAQKAAA="
                    ChangeKey="EgAAAA=="/>
      </m:RemoveImContactFromGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="f7776-133">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="f7776-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f7776-134">RemoveImContactFromGroup</span><span class="sxs-lookup"><span data-stu-id="f7776-134">RemoveImContactFromGroup</span></span>](removeimcontactfromgroup.md)
    
- [<span data-ttu-id="f7776-135">ID de contacto</span><span class="sxs-lookup"><span data-stu-id="f7776-135">ContactId</span></span>](contactid.md)
    
- [<span data-ttu-id="f7776-136">GroupId</span><span class="sxs-lookup"><span data-stu-id="f7776-136">GroupId</span></span>](groupid.md)
    
## <a name="successful-removeimcontactfromgroup-operation-response"></a><span data-ttu-id="f7776-137">Respuesta es correcta de operación RemoveImContactFromGroup</span><span class="sxs-lookup"><span data-stu-id="f7776-137">Successful RemoveImContactFromGroup operation response</span></span>

<span data-ttu-id="f7776-138">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **RemoveImContactFromGroup** .</span><span class="sxs-lookup"><span data-stu-id="f7776-138">The following example shows a successful response to a **RemoveImContactFromGroup** operation request.</span></span> 
  
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
      <RemoveImContactFromGroupResponse ResponseClass="Success" 
                                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveImContactFromGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="f7776-139">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="f7776-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f7776-140">RemoveImContactFromGroupResponse</span><span class="sxs-lookup"><span data-stu-id="f7776-140">RemoveImContactFromGroupResponse</span></span>](removeimcontactfromgroupresponse.md)
    
- [<span data-ttu-id="f7776-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f7776-141">ResponseCode</span></span>](responsecode.md)
    
## <a name="removeimcontactfromgroup-operation-errorinvalidimcontactid-error-response"></a><span data-ttu-id="f7776-142">Operación RemoveImContactFromGroup respuesta de error de ErrorInvalidImContactId</span><span class="sxs-lookup"><span data-stu-id="f7776-142">RemoveImContactFromGroup operation ErrorInvalidImContactId error response</span></span>

<span data-ttu-id="f7776-143">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **RemoveImContactFromGroup** .</span><span class="sxs-lookup"><span data-stu-id="f7776-143">The following example shows an error response to a **RemoveImContactFromGroup** operation request.</span></span> <span data-ttu-id="f7776-144">La siguiente respuesta de error se produce cuando se realiza un intento para quitar un elemento de contacto que no existe en el grupo de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="f7776-144">The following error response occurs when an attempt is made to remove a contact item that does not exist in the IM group.</span></span> 
  
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
      <RemoveImContactFromGroupResponse ResponseClass="Error" 
                                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified Im Contact Id is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImContactId</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveImContactFromGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="f7776-145">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="f7776-145">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f7776-146">RemoveImContactFromGroupResponse</span><span class="sxs-lookup"><span data-stu-id="f7776-146">RemoveImContactFromGroupResponse</span></span>](removeimcontactfromgroupresponse.md)
    
- [<span data-ttu-id="f7776-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="f7776-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="f7776-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f7776-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f7776-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f7776-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="f7776-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7776-150">See also</span></span>

- [<span data-ttu-id="f7776-151">Las personas y los contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f7776-151">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="f7776-152">AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="f7776-152">AddDistributionGroupToImList</span></span>](adddistributiongrouptoimlist-operation.md)
    
- [<span data-ttu-id="f7776-153">AddImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="f7776-153">AddImContactToGroup</span></span>](addimcontacttogroup-operation.md)
    
- [<span data-ttu-id="f7776-154">Operación AddImGroup</span><span class="sxs-lookup"><span data-stu-id="f7776-154">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="f7776-155">Operación AddNewImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="f7776-155">AddNewImContactToGroup operation</span></span>](addnewimcontacttogroup-operation.md)
    
- [<span data-ttu-id="f7776-156">Operación GetImItemList</span><span class="sxs-lookup"><span data-stu-id="f7776-156">GetImItemList operation</span></span>](getimitemlist-operation.md)
    
- [<span data-ttu-id="f7776-157">GetImItems</span><span class="sxs-lookup"><span data-stu-id="f7776-157">GetImItems</span></span>](getimitems-operation.md)
    
- [<span data-ttu-id="f7776-158">RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="f7776-158">RemoveContactFromImList</span></span>](removecontactfromimlist-operation.md)
    
- [<span data-ttu-id="f7776-159">RemoveDistributionGroupFromImList</span><span class="sxs-lookup"><span data-stu-id="f7776-159">RemoveDistributionGroupFromImList</span></span>](removedistributiongroupfromimlist-operation.md)
    
- [<span data-ttu-id="f7776-160">Operación RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="f7776-160">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    
- [<span data-ttu-id="f7776-161">Operación SetImGroup</span><span class="sxs-lookup"><span data-stu-id="f7776-161">SetImGroup operation</span></span>](setimgroup-operation.md)
    
- [<span data-ttu-id="f7776-162">SetImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="f7776-162">SetImListMigrationCompleted</span></span>](setimlistmigrationcompleted-operation.md)
    

