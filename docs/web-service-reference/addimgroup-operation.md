---
title: Operación AddImGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6df6e504-b7c8-4773-b10f-ffa5defac229
description: Buscar información sobre la operación de EWS de AddImGroup.
ms.openlocfilehash: 38ed12a741d46fe998dc0079ed13973ce9edf5ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462818"
---
# <a name="addimgroup-operation"></a><span data-ttu-id="6675c-103">Operación AddImGroup</span><span class="sxs-lookup"><span data-stu-id="6675c-103">AddImGroup operation</span></span>

<span data-ttu-id="6675c-104">Buscar información sobre la operación de EWS de **AddImGroup** .</span><span class="sxs-lookup"><span data-stu-id="6675c-104">Find information about the **AddImGroup** EWS operation.</span></span> 
  
<span data-ttu-id="6675c-105">La operación de servicios web Exchange de **AddImGroup** (EWS) agrega un nuevo grupo de mensajería instantánea (mi) a un buzón.</span><span class="sxs-lookup"><span data-stu-id="6675c-105">The **AddImGroup** Exchange Web Services (EWS) operation adds a new instant messaging (IM) group to a mailbox.</span></span> 
  
<span data-ttu-id="6675c-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6675c-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addimgroup-operation"></a><span data-ttu-id="6675c-107">Uso de la operación AddImGroup</span><span class="sxs-lookup"><span data-stu-id="6675c-107">Using the AddImGroup operation</span></span>

<span data-ttu-id="6675c-108">La operación **AddImGroup** sólo toma un único argumento nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="6675c-108">The **AddImGroup** operation only takes a single display name argument.</span></span> 
  
<span data-ttu-id="6675c-109">Esta operación devuelve el nombre para mostrar, el tipo de grupo y el identificador del almacén de Exchange del nuevo grupo.</span><span class="sxs-lookup"><span data-stu-id="6675c-109">This operation returns the display name, group type, and Exchange store identifier of the new group.</span></span>
  
<span data-ttu-id="6675c-110">La operación **AddImGroup** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6675c-110">The **AddImGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="6675c-111">**Tabla 1. Encabezados SOAP de operación AddImGroup**</span><span class="sxs-lookup"><span data-stu-id="6675c-111">**Table 1. AddImGroup operation SOAP headers**</span></span>

|<span data-ttu-id="6675c-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="6675c-112">**Header name**</span></span>|<span data-ttu-id="6675c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6675c-113">**Element**</span></span>|<span data-ttu-id="6675c-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6675c-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6675c-115">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="6675c-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="6675c-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="6675c-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="6675c-117">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="6675c-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="6675c-118">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="6675c-118">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="6675c-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="6675c-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="6675c-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="6675c-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="6675c-121">Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="6675c-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="6675c-122">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="6675c-122">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="6675c-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="6675c-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="6675c-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="6675c-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="6675c-125">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="6675c-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="6675c-126">Esto es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="6675c-126">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="6675c-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="6675c-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="6675c-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="6675c-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="6675c-129">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6675c-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="6675c-130">Esto es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="6675c-130">This is applicable to a response.</span></span>  <br/> |
   
## <a name="addimgroup-operation-request-example-create-a-new-im-group"></a><span data-ttu-id="6675c-131">Ejemplo de solicitud de operación AddImGroup: crear un nuevo grupo de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="6675c-131">AddImGroup operation request example: Create a new IM group</span></span>

<span data-ttu-id="6675c-132">El siguiente ejemplo de una solicitud de operación de **AddImGroup** muestra cómo crear un grupo de mensajería instantánea denominado MyCustomerGroup.</span><span class="sxs-lookup"><span data-stu-id="6675c-132">The following example of an **AddImGroup** operation request shows how to create an IM group named MyCustomerGroup.</span></span> 
  
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
      <m:AddImGroup>
         <m:DisplayName>MyCustomGroup</m:DisplayName>
      </m:AddImGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="6675c-133">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="6675c-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="6675c-134">AddImGroup</span><span class="sxs-lookup"><span data-stu-id="6675c-134">AddImGroup</span></span>](addimgroup.md)
    
- [<span data-ttu-id="6675c-135">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="6675c-135">DisplayName (string)</span></span>](displayname-string.md)
    
## <a name="successful-addimgroup-operation-response"></a><span data-ttu-id="6675c-136">Respuesta de operación AddImGroup correcta</span><span class="sxs-lookup"><span data-stu-id="6675c-136">Successful AddImGroup operation response</span></span>

<span data-ttu-id="6675c-137">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **AddImGroup** .</span><span class="sxs-lookup"><span data-stu-id="6675c-137">The following example shows a successful response to an **AddImGroup** operation request.</span></span> 
  
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
      <AddImGroupResponse ResponseClass="Success"
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImGroup>
            <DisplayName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">MyCustomGroup</DisplayName>
            <GroupType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">IPM.DistList.MOC.UserGroup</GroupType>
            <ExchangeStoreId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04ZjU5LWI3MAAA="
                             ChangeKey="EgAAAA=="
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/types"/>
         </ImGroup>
      </AddImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="6675c-138">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="6675c-138">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="6675c-139">AddImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="6675c-139">AddImGroupResponse</span></span>](addimgroupresponse.md)
    
- [<span data-ttu-id="6675c-140">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6675c-140">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="6675c-141">Desagrupo</span><span class="sxs-lookup"><span data-stu-id="6675c-141">ImGroup</span></span>](imgroup.md)
    
- [<span data-ttu-id="6675c-142">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="6675c-142">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="6675c-143">GroupType</span><span class="sxs-lookup"><span data-stu-id="6675c-143">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="6675c-144">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="6675c-144">ExchangeStoreId</span></span>](exchangestoreid.md)
    
## <a name="addimgroup-operation-error-response"></a><span data-ttu-id="6675c-145">Respuesta de error de operación de AddImGroup</span><span class="sxs-lookup"><span data-stu-id="6675c-145">AddImGroup operation error response</span></span>

<span data-ttu-id="6675c-146">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **AddImGroup** .</span><span class="sxs-lookup"><span data-stu-id="6675c-146">The following example shows an error response to an **AddImGroup** operation request.</span></span> <span data-ttu-id="6675c-147">Se trata de una respuesta a una solicitud que contiene un carácter que no se puede usar en un nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="6675c-147">This is a response to a request that contains a character that cannot be used in a display name.</span></span> <span data-ttu-id="6675c-148">Tenga en cuenta que se trata de un error de SOAP y no de un mensaje de error basado en esquema.</span><span class="sxs-lookup"><span data-stu-id="6675c-148">Note that this is a SOAP fault and not a schema-based error message.</span></span> <span data-ttu-id="6675c-149">El nombre para mostrar enviado en la solicitud es ~! @ # $% ^ &amp; y el error se produce en el &amp; personaje.</span><span class="sxs-lookup"><span data-stu-id="6675c-149">The display name submitted in the request is ~!@#$%^&amp;, and the error occurs on the &amp; character.</span></span> <span data-ttu-id="6675c-150">El &amp; carácter se produjo en la undécimo línea y el carácter 33 en la carga de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6675c-150">The &amp; character occurred on the 11th line and 33rd character in the request payload.</span></span> <span data-ttu-id="6675c-151">Se devolvió la respuesta con un código HTTP 500.</span><span class="sxs-lookup"><span data-stu-id="6675c-151">The response was returned with an HTTP 500 code.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Body>
      <s:Fault>
         <faultcode xmlns:a="https://schemas.microsoft.com/exchange/services/2006/types">a:ErrorSchemaValidation</faultcode>
         <faultstring xml:lang="en-US">The request failed schema validation: An error occurred while parsing EntityName. Line 11, position 33.</faultstring>
         <detail>
            <e:ResponseCode xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
            <e:Message xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">The request failed schema validation.</e:Message>
            <t:MessageXml xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
               <t:LineNumber>11</t:LineNumber>
               <t:LinePosition>33</t:LinePosition>
               <t:Violation>An error occurred while parsing EntityName. Line 11, position 33.</t:Violation>
            </t:MessageXml>
         </detail>
      </s:Fault>
   </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="6675c-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="6675c-152">See also</span></span>

- [<span data-ttu-id="6675c-153">Personas y contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6675c-153">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="6675c-154">Operación RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="6675c-154">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    
- [<span data-ttu-id="6675c-155">SetImGroup</span><span class="sxs-lookup"><span data-stu-id="6675c-155">SetImGroup</span></span>](setimgroup.md)
    

