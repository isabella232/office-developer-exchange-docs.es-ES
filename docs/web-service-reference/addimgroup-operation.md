---
title: Operación AddImGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6df6e504-b7c8-4773-b10f-ffa5defac229
description: Busque información sobre la EWS AddImGroup operación.
ms.openlocfilehash: 91236f9ad2236b3f6bee600b9d57bcf736090ed7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763399"
---
# <a name="addimgroup-operation"></a><span data-ttu-id="39fc4-103">Operación AddImGroup</span><span class="sxs-lookup"><span data-stu-id="39fc4-103">AddImGroup operation</span></span>

<span data-ttu-id="39fc4-104">Obtenga información acerca de la operación de EWS **AddImGroup** .</span><span class="sxs-lookup"><span data-stu-id="39fc4-104">Find information about the **AddImGroup** EWS operation.</span></span> 
  
<span data-ttu-id="39fc4-105">La operación de Exchange Web Services (EWS) **AddImGroup** agrega un nuevo grupo de mensajería instantánea a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="39fc4-105">The **AddImGroup** Exchange Web Services (EWS) operation adds a new instant messaging (IM) group to a mailbox.</span></span> 
  
<span data-ttu-id="39fc4-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="39fc4-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addimgroup-operation"></a><span data-ttu-id="39fc4-107">Mediante la operación AddImGroup</span><span class="sxs-lookup"><span data-stu-id="39fc4-107">Using the AddImGroup operation</span></span>

<span data-ttu-id="39fc4-108">La operación **AddImGroup** sólo toma un argumento de nombre para mostrar único.</span><span class="sxs-lookup"><span data-stu-id="39fc4-108">The **AddImGroup** operation only takes a single display name argument.</span></span> 
  
<span data-ttu-id="39fc4-109">Esta operación devuelve el nombre para mostrar, el tipo de grupo y el identificador de almacén de Exchange del nuevo grupo.</span><span class="sxs-lookup"><span data-stu-id="39fc4-109">This operation returns the display name, group type, and Exchange store identifier of the new group.</span></span>
  
<span data-ttu-id="39fc4-110">La operación de **AddImGroup** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="39fc4-110">The **AddImGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="39fc4-111">**La tabla 1. Encabezados SOAP de operación de AddImGroup**</span><span class="sxs-lookup"><span data-stu-id="39fc4-111">**Table 1. AddImGroup operation SOAP headers**</span></span>

|<span data-ttu-id="39fc4-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="39fc4-112">**Header name**</span></span>|<span data-ttu-id="39fc4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="39fc4-113">**Element**</span></span>|<span data-ttu-id="39fc4-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="39fc4-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="39fc4-115">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="39fc4-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="39fc4-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="39fc4-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="39fc4-117">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="39fc4-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="39fc4-118">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="39fc4-118">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="39fc4-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="39fc4-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="39fc4-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="39fc4-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="39fc4-121">Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.</span><span class="sxs-lookup"><span data-stu-id="39fc4-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="39fc4-122">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="39fc4-122">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="39fc4-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="39fc4-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="39fc4-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="39fc4-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="39fc4-125">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="39fc4-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="39fc4-126">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="39fc4-126">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="39fc4-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="39fc4-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="39fc4-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="39fc4-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="39fc4-129">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="39fc4-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="39fc4-130">Esto es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="39fc4-130">This is applicable to a response.</span></span>  <br/> |
   
## <a name="addimgroup-operation-request-example-create-a-new-im-group"></a><span data-ttu-id="39fc4-131">Ejemplo de solicitud de operación de AddImGroup: crear un nuevo grupo de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="39fc4-131">AddImGroup operation request example: Create a new IM group</span></span>

<span data-ttu-id="39fc4-132">El siguiente ejemplo de una solicitud de operación **AddImGroup** muestra cómo crear un grupo de mensajería instantánea denominado MyCustomerGroup.</span><span class="sxs-lookup"><span data-stu-id="39fc4-132">The following example of an **AddImGroup** operation request shows how to create an IM group named MyCustomerGroup.</span></span> 
  
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
      <m:AddImGroup>
         <m:DisplayName>MyCustomGroup</m:DisplayName>
      </m:AddImGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="39fc4-133">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="39fc4-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="39fc4-134">AddImGroup</span><span class="sxs-lookup"><span data-stu-id="39fc4-134">AddImGroup</span></span>](addimgroup.md)
    
- [<span data-ttu-id="39fc4-135">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="39fc4-135">DisplayName (string)</span></span>](displayname-string.md)
    
## <a name="successful-addimgroup-operation-response"></a><span data-ttu-id="39fc4-136">Respuesta es correcta de operación AddImGroup</span><span class="sxs-lookup"><span data-stu-id="39fc4-136">Successful AddImGroup operation response</span></span>

<span data-ttu-id="39fc4-137">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **AddImGroup** .</span><span class="sxs-lookup"><span data-stu-id="39fc4-137">The following example shows a successful response to an **AddImGroup** operation request.</span></span> 
  
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
      <AddImGroupResponse ResponseClass="Success"
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImGroup>
            <DisplayName xmlns="http://schemas.microsoft.com/exchange/services/2006/types">MyCustomGroup</DisplayName>
            <GroupType xmlns="http://schemas.microsoft.com/exchange/services/2006/types">IPM.DistList.MOC.UserGroup</GroupType>
            <ExchangeStoreId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04ZjU5LWI3MAAA="
                             ChangeKey="EgAAAA=="
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/types"/>
         </ImGroup>
      </AddImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="39fc4-138">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="39fc4-138">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="39fc4-139">AddImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="39fc4-139">AddImGroupResponse</span></span>](addimgroupresponse.md)
    
- [<span data-ttu-id="39fc4-140">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="39fc4-140">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="39fc4-141">ImGroup</span><span class="sxs-lookup"><span data-stu-id="39fc4-141">ImGroup</span></span>](imgroup.md)
    
- [<span data-ttu-id="39fc4-142">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="39fc4-142">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="39fc4-143">GroupType</span><span class="sxs-lookup"><span data-stu-id="39fc4-143">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="39fc4-144">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="39fc4-144">ExchangeStoreId</span></span>](exchangestoreid.md)
    
## <a name="addimgroup-operation-error-response"></a><span data-ttu-id="39fc4-145">Respuesta de error de la operación de AddImGroup</span><span class="sxs-lookup"><span data-stu-id="39fc4-145">AddImGroup operation error response</span></span>

<span data-ttu-id="39fc4-146">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **AddImGroup** .</span><span class="sxs-lookup"><span data-stu-id="39fc4-146">The following example shows an error response to an **AddImGroup** operation request.</span></span> <span data-ttu-id="39fc4-147">Esta es una respuesta a una solicitud que contiene un carácter que no se puede usar en un nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="39fc4-147">This is a response to a request that contains a character that cannot be used in a display name.</span></span> <span data-ttu-id="39fc4-148">Tenga en cuenta que esto es un error de SOAP y no un mensaje de error basada en el esquema.</span><span class="sxs-lookup"><span data-stu-id="39fc4-148">Note that this is a SOAP fault and not a schema-based error message.</span></span> <span data-ttu-id="39fc4-149">Es el nombre para mostrar enviado en la solicitud ~! @# $% ^&amp;, y se produce el error en la &amp; caracteres.</span><span class="sxs-lookup"><span data-stu-id="39fc4-149">The display name submitted in the request is ~!@#$%^&amp;, and the error occurs on the &amp; character.</span></span> <span data-ttu-id="39fc4-150">El &amp; se ha producido un carácter en el carácter de línea y 33rd 11 en la carga de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="39fc4-150">The &amp; character occurred on the 11th line and 33rd character in the request payload.</span></span> <span data-ttu-id="39fc4-151">La respuesta se devuelve con un código de error HTTP 500.</span><span class="sxs-lookup"><span data-stu-id="39fc4-151">The response was returned with an HTTP 500 code.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Body>
      <s:Fault>
         <faultcode xmlns:a="http://schemas.microsoft.com/exchange/services/2006/types">a:ErrorSchemaValidation</faultcode>
         <faultstring xml:lang="en-US">The request failed schema validation: An error occurred while parsing EntityName. Line 11, position 33.</faultstring>
         <detail>
            <e:ResponseCode xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
            <e:Message xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">The request failed schema validation.</e:Message>
            <t:MessageXml xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
               <t:LineNumber>11</t:LineNumber>
               <t:LinePosition>33</t:LinePosition>
               <t:Violation>An error occurred while parsing EntityName. Line 11, position 33.</t:Violation>
            </t:MessageXml>
         </detail>
      </s:Fault>
   </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="39fc4-152">Ver también</span><span class="sxs-lookup"><span data-stu-id="39fc4-152">See also</span></span>

- [<span data-ttu-id="39fc4-153">Las personas y los contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="39fc4-153">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="39fc4-154">Operación RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="39fc4-154">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    
- [<span data-ttu-id="39fc4-155">SetImGroup</span><span class="sxs-lookup"><span data-stu-id="39fc4-155">SetImGroup</span></span>](setimgroup.md)
    

