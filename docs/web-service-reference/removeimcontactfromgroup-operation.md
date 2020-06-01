---
title: Operación RemoveImContactFromGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a190bbec-c71b-4e6a-880b-55854c724d8c
description: Buscar información sobre la operación de EWS de RemoveImContactFromGroup.
ms.openlocfilehash: 4750ef57794c3da540ac36baa8ef6ef093939ea1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466972"
---
# <a name="removeimcontactfromgroup-operation"></a><span data-ttu-id="373a2-103">Operación RemoveImContactFromGroup</span><span class="sxs-lookup"><span data-stu-id="373a2-103">RemoveImContactFromGroup operation</span></span>

<span data-ttu-id="373a2-104">Buscar información sobre la operación de EWS de **RemoveImContactFromGroup** .</span><span class="sxs-lookup"><span data-stu-id="373a2-104">Find information about the **RemoveImContactFromGroup** EWS operation.</span></span> 
  
<span data-ttu-id="373a2-105">La operación **RemoveImContactFromGroup** quita un solo contacto de mensajería instantánea de un grupo de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="373a2-105">The **RemoveImContactFromGroup** operation removes a single IM contact from an IM group.</span></span> 
  
<span data-ttu-id="373a2-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="373a2-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-removeimcontactfromgroup-operation"></a><span data-ttu-id="373a2-107">Uso de la operación RemoveImContactFromGroup</span><span class="sxs-lookup"><span data-stu-id="373a2-107">Using the RemoveImContactFromGroup operation</span></span>

<span data-ttu-id="373a2-108">La operación **RemoveImContactFromGroup** toma dos argumentos: un identificador de elemento de contacto y el grupo de mensajería instantánea (mi) correspondiente del que se quita el contacto.</span><span class="sxs-lookup"><span data-stu-id="373a2-108">The **RemoveImContactFromGroup** operation takes two arguments: a contact item identifier, and the corresponding instant messaging (IM) group from which the contact is removed.</span></span> 
  
### <a name="removeimcontactfromgroup-operation-soap-headers"></a><span data-ttu-id="373a2-109">Encabezados SOAP de operación RemoveImContactFromGroup</span><span class="sxs-lookup"><span data-stu-id="373a2-109">RemoveImContactFromGroup operation SOAP headers</span></span>

<span data-ttu-id="373a2-110">La operación **RemoveImContactFromGroup** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="373a2-110">The **RemoveImContactFromGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="373a2-111">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="373a2-111">**Header name**</span></span>|<span data-ttu-id="373a2-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="373a2-112">**Element**</span></span>|<span data-ttu-id="373a2-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="373a2-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="373a2-114">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="373a2-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="373a2-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="373a2-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="373a2-116">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="373a2-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="373a2-117">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="373a2-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="373a2-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="373a2-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="373a2-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="373a2-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="373a2-120">Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="373a2-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="373a2-121">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="373a2-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="373a2-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="373a2-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="373a2-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="373a2-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="373a2-124">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="373a2-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="373a2-125">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="373a2-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="373a2-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="373a2-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="373a2-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="373a2-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="373a2-128">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="373a2-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="373a2-129">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="373a2-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="removeimcontactfromgroup-operation-request-example"></a><span data-ttu-id="373a2-130">Ejemplo de solicitud de operación RemoveImContactFromGroup</span><span class="sxs-lookup"><span data-stu-id="373a2-130">RemoveImContactFromGroup operation request example</span></span>

<span data-ttu-id="373a2-131">El siguiente ejemplo de una solicitud de operación de **RemoveImContactFromGroup** muestra cómo quitar un contacto de mensajería instantánea de un grupo de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="373a2-131">The following example of a **RemoveImContactFromGroup** operation request shows how to remove an IM contact from an IM group.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="373a2-132">Los identificadores de grupo y contacto se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="373a2-132">The group and contact identifiers have been shortened to preserve readability.</span></span> 
  
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
      <m:RemoveImContactFromGroup>
         <m:ContactId Id="AAMkAGQ1MjJjMTBkLTcAAAAvcAAA="
                      ChangeKey="EQAAABYAAABtF8oI7iVOQ"/>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkbWAAAAAAQKAAA="
                    ChangeKey="EgAAAA=="/>
      </m:RemoveImContactFromGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="373a2-133">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="373a2-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="373a2-134">RemoveImContactFromGroup</span><span class="sxs-lookup"><span data-stu-id="373a2-134">RemoveImContactFromGroup</span></span>](removeimcontactfromgroup.md)
    
- [<span data-ttu-id="373a2-135">Contacto</span><span class="sxs-lookup"><span data-stu-id="373a2-135">ContactId</span></span>](contactid.md)
    
- [<span data-ttu-id="373a2-136">GroupId</span><span class="sxs-lookup"><span data-stu-id="373a2-136">GroupId</span></span>](groupid.md)
    
## <a name="successful-removeimcontactfromgroup-operation-response"></a><span data-ttu-id="373a2-137">Respuesta de operación RemoveImContactFromGroup correcta</span><span class="sxs-lookup"><span data-stu-id="373a2-137">Successful RemoveImContactFromGroup operation response</span></span>

<span data-ttu-id="373a2-138">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **RemoveImContactFromGroup** .</span><span class="sxs-lookup"><span data-stu-id="373a2-138">The following example shows a successful response to a **RemoveImContactFromGroup** operation request.</span></span> 
  
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
      <RemoveImContactFromGroupResponse ResponseClass="Success" 
                                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveImContactFromGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="373a2-139">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="373a2-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="373a2-140">RemoveImContactFromGroupResponse</span><span class="sxs-lookup"><span data-stu-id="373a2-140">RemoveImContactFromGroupResponse</span></span>](removeimcontactfromgroupresponse.md)
    
- [<span data-ttu-id="373a2-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="373a2-141">ResponseCode</span></span>](responsecode.md)
    
## <a name="removeimcontactfromgroup-operation-errorinvalidimcontactid-error-response"></a><span data-ttu-id="373a2-142">RemoveImContactFromGroup Operation ErrorInvalidImContactId error Response</span><span class="sxs-lookup"><span data-stu-id="373a2-142">RemoveImContactFromGroup operation ErrorInvalidImContactId error response</span></span>

<span data-ttu-id="373a2-143">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **RemoveImContactFromGroup** .</span><span class="sxs-lookup"><span data-stu-id="373a2-143">The following example shows an error response to a **RemoveImContactFromGroup** operation request.</span></span> <span data-ttu-id="373a2-144">La siguiente respuesta de error se produce cuando se realiza un intento de quitar un elemento de contacto que no existe en el grupo de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="373a2-144">The following error response occurs when an attempt is made to remove a contact item that does not exist in the IM group.</span></span> 
  
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
      <RemoveImContactFromGroupResponse ResponseClass="Error" 
                                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified Im Contact Id is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImContactId</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveImContactFromGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="373a2-145">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="373a2-145">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="373a2-146">RemoveImContactFromGroupResponse</span><span class="sxs-lookup"><span data-stu-id="373a2-146">RemoveImContactFromGroupResponse</span></span>](removeimcontactfromgroupresponse.md)
    
- [<span data-ttu-id="373a2-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="373a2-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="373a2-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="373a2-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="373a2-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="373a2-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="373a2-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="373a2-150">See also</span></span>

- [<span data-ttu-id="373a2-151">Personas y contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="373a2-151">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="373a2-152">AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="373a2-152">AddDistributionGroupToImList</span></span>](adddistributiongrouptoimlist-operation.md)
    
- [<span data-ttu-id="373a2-153">AddImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="373a2-153">AddImContactToGroup</span></span>](addimcontacttogroup-operation.md)
    
- [<span data-ttu-id="373a2-154">Operación AddImGroup</span><span class="sxs-lookup"><span data-stu-id="373a2-154">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="373a2-155">Operación AddNewImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="373a2-155">AddNewImContactToGroup operation</span></span>](addnewimcontacttogroup-operation.md)
    
- [<span data-ttu-id="373a2-156">Operación GetImItemList</span><span class="sxs-lookup"><span data-stu-id="373a2-156">GetImItemList operation</span></span>](getimitemlist-operation.md)
    
- [<span data-ttu-id="373a2-157">GetImItems</span><span class="sxs-lookup"><span data-stu-id="373a2-157">GetImItems</span></span>](getimitems-operation.md)
    
- [<span data-ttu-id="373a2-158">RemoveContactFromImList</span><span class="sxs-lookup"><span data-stu-id="373a2-158">RemoveContactFromImList</span></span>](removecontactfromimlist-operation.md)
    
- [<span data-ttu-id="373a2-159">RemoveDistributionGroupFromImList</span><span class="sxs-lookup"><span data-stu-id="373a2-159">RemoveDistributionGroupFromImList</span></span>](removedistributiongroupfromimlist-operation.md)
    
- [<span data-ttu-id="373a2-160">Operación RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="373a2-160">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    
- [<span data-ttu-id="373a2-161">Operación SetImGroup</span><span class="sxs-lookup"><span data-stu-id="373a2-161">SetImGroup operation</span></span>](setimgroup-operation.md)
    
- [<span data-ttu-id="373a2-162">SetImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="373a2-162">SetImListMigrationCompleted</span></span>](setimlistmigrationcompleted-operation.md)
    

