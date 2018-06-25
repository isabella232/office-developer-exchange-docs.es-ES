---
title: Operación SetImGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d48aa07-8152-4c3d-a519-061253e80174
description: Busque información sobre la EWS SetImGroup operación.
ms.openlocfilehash: 80980c25888ab3fcae0a761e115c3ac3d578a013
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837421"
---
# <a name="setimgroup-operation"></a><span data-ttu-id="cb2f6-103">Operación SetImGroup</span><span class="sxs-lookup"><span data-stu-id="cb2f6-103">SetImGroup operation</span></span>

<span data-ttu-id="cb2f6-104">Obtenga información acerca de la operación de EWS **SetImGroup** .</span><span class="sxs-lookup"><span data-stu-id="cb2f6-104">Find information about the **SetImGroup** EWS operation.</span></span> 
  
<span data-ttu-id="cb2f6-105">La operación **SetImGroup** cambia el nombre para mostrar de un grupo (IM) de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-105">The **SetImGroup** operation changes the display name of an instant messaging (IM) group.</span></span> 
  
<span data-ttu-id="cb2f6-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-setimgroup-operation"></a><span data-ttu-id="cb2f6-107">Mediante la operación SetImGroup</span><span class="sxs-lookup"><span data-stu-id="cb2f6-107">Using the SetImGroup operation</span></span>

<span data-ttu-id="cb2f6-108">La operación **SetImGroup** sólo toma un argumento de nombre para mostrar único.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-108">The **SetImGroup** operation only takes a single display name argument.</span></span> 
  
### <a name="setimgroup-operation-soap-headers"></a><span data-ttu-id="cb2f6-109">Encabezados SOAP de operación de SetImGroup</span><span class="sxs-lookup"><span data-stu-id="cb2f6-109">SetImGroup operation SOAP headers</span></span>

<span data-ttu-id="cb2f6-110">La operación de **SetImGroup** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-110">The **SetImGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="cb2f6-111">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="cb2f6-111">**Header name**</span></span>|<span data-ttu-id="cb2f6-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="cb2f6-112">**Element**</span></span>|<span data-ttu-id="cb2f6-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cb2f6-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cb2f6-114">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="cb2f6-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="cb2f6-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="cb2f6-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="cb2f6-116">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="cb2f6-117">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="cb2f6-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="cb2f6-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="cb2f6-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="cb2f6-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="cb2f6-120">Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="cb2f6-121">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="cb2f6-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="cb2f6-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="cb2f6-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="cb2f6-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="cb2f6-124">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="cb2f6-125">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="cb2f6-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="cb2f6-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="cb2f6-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="cb2f6-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="cb2f6-128">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="cb2f6-129">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="setimgroup-operation-request-example"></a><span data-ttu-id="cb2f6-130">Ejemplo de solicitud de operación de SetImGroup</span><span class="sxs-lookup"><span data-stu-id="cb2f6-130">SetImGroup operation request example</span></span>

<span data-ttu-id="cb2f6-131">El siguiente ejemplo de una solicitud de operación **SetImGroup** muestra cómo cambiar un nombre para mostrar de grupo de mensajería instantánea a "MyNewGroupName".</span><span class="sxs-lookup"><span data-stu-id="cb2f6-131">The following example of a **SetImGroup** operation request shows how to change an IM group display name to "MyNewGroupName".</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cb2f6-132">El identificador de almacén de Exchange se ha reducido para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-132">The Exchange store identifier has been shortened to preserve readability.</span></span> 
  
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
      <m:SetImGroup>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkQoTbWAAAAAAQRAAA="
                    ChangeKey="EgAAAA=="/>
         <m:NewDisplayName>MyNewGroupName</m:NewDisplayName>
      </m:SetImGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="cb2f6-133">La solicitud SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="cb2f6-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="cb2f6-134">SetImGroup</span><span class="sxs-lookup"><span data-stu-id="cb2f6-134">SetImGroup</span></span>](setimgroup.md)
    
- [<span data-ttu-id="cb2f6-135">GroupId</span><span class="sxs-lookup"><span data-stu-id="cb2f6-135">GroupId</span></span>](groupid.md)
    
- [<span data-ttu-id="cb2f6-136">NewDisplayName</span><span class="sxs-lookup"><span data-stu-id="cb2f6-136">NewDisplayName</span></span>](newdisplayname.md)
    
## <a name="successful-setimgroup-operation-response"></a><span data-ttu-id="cb2f6-137">Respuesta es correcta de operación SetImGroup</span><span class="sxs-lookup"><span data-stu-id="cb2f6-137">Successful SetImGroup operation response</span></span>

<span data-ttu-id="cb2f6-138">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **SetImGroup** .</span><span class="sxs-lookup"><span data-stu-id="cb2f6-138">The following example shows a successful response to a **SetImGroup** operation request.</span></span> 
  
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
      <SetImGroupResponse ResponseClass="Success" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         </SetImGroupResponse>
      </s:Body>
</s:Envelope>
```

<span data-ttu-id="cb2f6-139">La respuesta SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="cb2f6-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="cb2f6-140">SetImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="cb2f6-140">SetImGroupResponse</span></span>](setimgroupresponse.md)
    
- [<span data-ttu-id="cb2f6-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cb2f6-141">ResponseCode</span></span>](responsecode.md)
    
## <a name="setimgroup-operation-error-response"></a><span data-ttu-id="cb2f6-142">Respuesta de error de la operación de SetImGroup</span><span class="sxs-lookup"><span data-stu-id="cb2f6-142">SetImGroup operation error response</span></span>

<span data-ttu-id="cb2f6-143">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **SetImGroup** .</span><span class="sxs-lookup"><span data-stu-id="cb2f6-143">The following example shows an error response to a **SetImGroup** operation request.</span></span> <span data-ttu-id="cb2f6-144">La siguiente respuesta de error se produce cuando se realiza un intento para cambiar el nombre para mostrar del grupo para el nombre para mostrar del grupo existente.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-144">The following error response occurs when an attempt is made to change the group display name to the existing group display name.</span></span> 
  
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
      <SetImGroupResponse ResponseClass="Error" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>An IM group with the specified display name already exists.</MessageText>
         <ResponseCode>ErrorImGroupDisplayNameAlreadyExists</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </SetImGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="cb2f6-145">La respuesta de error SOAP body contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="cb2f6-145">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="cb2f6-146">SetImGroupResponse</span><span class="sxs-lookup"><span data-stu-id="cb2f6-146">SetImGroupResponse</span></span>](setimgroupresponse.md)
    
- [<span data-ttu-id="cb2f6-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="cb2f6-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="cb2f6-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cb2f6-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="cb2f6-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="cb2f6-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="cb2f6-150">Para códigos de error adicionales que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="cb2f6-150">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cb2f6-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb2f6-151">See also</span></span>

- [<span data-ttu-id="cb2f6-152">Las personas y los contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cb2f6-152">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="cb2f6-153">Operación AddImGroup</span><span class="sxs-lookup"><span data-stu-id="cb2f6-153">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="cb2f6-154">Operación RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="cb2f6-154">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    

