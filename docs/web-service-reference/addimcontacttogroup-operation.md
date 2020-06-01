---
title: Operación AddImContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 376acc42-2684-4596-aca1-82a4a10865c9
description: Buscar información sobre la operación de EWS de AddImContactToGroup.
ms.openlocfilehash: a69ee0b355e78e1249383cab612a75bcda8d9e8a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458414"
---
# <a name="addimcontacttogroup-operation"></a><span data-ttu-id="ebc90-103">Operación AddImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="ebc90-103">AddImContactToGroup operation</span></span>

<span data-ttu-id="ebc90-104">Buscar información sobre la operación de EWS de **AddImContactToGroup** .</span><span class="sxs-lookup"><span data-stu-id="ebc90-104">Find information about the **AddImContactToGroup** EWS operation.</span></span> 
  
<span data-ttu-id="ebc90-105">La operación de servicios web Exchange de **AddImContactToGroup** (EWS) agrega un contacto de mensajería instantánea (mi) existente a un grupo.</span><span class="sxs-lookup"><span data-stu-id="ebc90-105">The **AddImContactToGroup** Exchange Web Services (EWS) operation adds an existing instant messaging (IM) contact to a group.</span></span> 
  
<span data-ttu-id="ebc90-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ebc90-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addimcontacttogroup-operation"></a><span data-ttu-id="ebc90-107">Uso de la operación AddImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="ebc90-107">Using the AddImContactToGroup operation</span></span>

<span data-ttu-id="ebc90-108">La operación **AddImContactToGroup** solo puede aceptar contactos de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="ebc90-108">The **AddImContactToGroup** operation can only accept IM contacts.</span></span> <span data-ttu-id="ebc90-109">Si desea agregar un nuevo contacto de mensajería instantánea al almacén de contactos unificados, use la operación [AddNewImContactToGroup](addnewimcontacttogroup-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ebc90-109">If you want to add a new IM contact to the Unified Contact Store, use the [AddNewImContactToGroup](addnewimcontacttogroup-operation.md) operation.</span></span> 
  
<span data-ttu-id="ebc90-110">La operación **AddImContactToGroup** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ebc90-110">The **AddImContactToGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
<span data-ttu-id="ebc90-111">**Tabla 1. Encabezados SOAP de operación AddImContactToGroup**</span><span class="sxs-lookup"><span data-stu-id="ebc90-111">**Table 1. AddImContactToGroup operation SOAP headers**</span></span>

|<span data-ttu-id="ebc90-112">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="ebc90-112">**Header name**</span></span>|<span data-ttu-id="ebc90-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ebc90-113">**Element**</span></span>|<span data-ttu-id="ebc90-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ebc90-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ebc90-115">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="ebc90-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="ebc90-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="ebc90-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="ebc90-117">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="ebc90-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="ebc90-118">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ebc90-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ebc90-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="ebc90-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="ebc90-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="ebc90-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="ebc90-121">Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="ebc90-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="ebc90-122">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ebc90-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ebc90-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="ebc90-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="ebc90-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="ebc90-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="ebc90-125">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="ebc90-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="ebc90-126">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ebc90-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ebc90-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="ebc90-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="ebc90-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ebc90-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="ebc90-129">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ebc90-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="ebc90-130">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="ebc90-130">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="addimcontacttogroup-operation-request-example-add-an-existing-im-contact-to-an-im-group"></a><span data-ttu-id="ebc90-131">Ejemplo de solicitud de operación AddImContactToGroup: agregar un contacto de mi existente a un grupo de mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="ebc90-131">AddImContactToGroup operation request example: Add an existing IM contact to an IM group</span></span>

<span data-ttu-id="ebc90-132">El siguiente ejemplo de una solicitud de operación de **AddImContactToGroup** muestra cómo agregar un contacto de mensajería instantánea existente a un grupo de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="ebc90-132">The following example of an **AddImContactToGroup** operation request shows how to add an existing IM contact an IM group.</span></span> 
  
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
      <m:AddImContactToGroup>
         <m:ContactId Id="AAMkAGQ1MjJjMTBkLTc4Y2AA="
                      ChangeKey="EQAAABYAAABtF8oI7i"/>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkzzAAAQKAAA="
                    ChangeKey="EgAAAA=="/>
      </m:AddImContactToGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="ebc90-133">El cuerpo SOAP de la solicitud contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ebc90-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ebc90-134">AddImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="ebc90-134">AddImContactToGroup</span></span>](addimcontacttogroup.md)
    
- [<span data-ttu-id="ebc90-135">Contacto</span><span class="sxs-lookup"><span data-stu-id="ebc90-135">ContactId</span></span>](contactid.md)
    
- [<span data-ttu-id="ebc90-136">GroupId</span><span class="sxs-lookup"><span data-stu-id="ebc90-136">GroupId</span></span>](groupid.md)
    
## <a name="successful-addimcontacttogroup-operation-response"></a><span data-ttu-id="ebc90-137">Respuesta de operación AddImContactToGroup correcta</span><span class="sxs-lookup"><span data-stu-id="ebc90-137">Successful AddImContactToGroup operation response</span></span>

<span data-ttu-id="ebc90-138">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **AddImContactToGroup** .</span><span class="sxs-lookup"><span data-stu-id="ebc90-138">The following example shows a successful response to an **AddImContactToGroup** operation request.</span></span> 
  
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
      <AddImContactToGroupResponse ResponseClass="Success" 
                                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </AddImContactToGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="ebc90-139">El cuerpo SOAP de respuesta contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ebc90-139">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ebc90-140">AddImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="ebc90-140">AddImContactToGroupResponse</span></span>](addimcontacttogroupresponse.md)
    
- [<span data-ttu-id="ebc90-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ebc90-141">ResponseCode</span></span>](responsecode.md)
    
## <a name="addimcontacttogroup-operation-errorinvalidimcontactid-error-response"></a><span data-ttu-id="ebc90-142">AddImContactToGroup Operation ErrorInvalidImContactId error Response</span><span class="sxs-lookup"><span data-stu-id="ebc90-142">AddImContactToGroup operation ErrorInvalidImContactId error response</span></span>

<span data-ttu-id="ebc90-143">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **AddImContactToGroup** .</span><span class="sxs-lookup"><span data-stu-id="ebc90-143">The following example shows an error response to an **AddImContactToGroup** operation request.</span></span> <span data-ttu-id="ebc90-144">Se produce la siguiente respuesta de error cuando se realiza un intento de agregar un contacto que no es un contacto de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="ebc90-144">The following error response occurs when an attempt is made to add a contact that is not an IM contact.</span></span> 
  
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
      <AddImContactToGroupResponse ResponseClass="Error" 
                                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified Im Contact Id is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImContactId</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         </AddImContactToGroupResponse>
      </s:Body>
</s:Envelope>
```

<span data-ttu-id="ebc90-145">El cuerpo SOAP de respuesta de error contiene los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ebc90-145">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ebc90-146">AddImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="ebc90-146">AddImContactToGroupResponse</span></span>](addimcontacttogroupresponse.md)
    
- [<span data-ttu-id="ebc90-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="ebc90-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="ebc90-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ebc90-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ebc90-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ebc90-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="ebc90-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebc90-150">See also</span></span>

- [<span data-ttu-id="ebc90-151">Operación AddImGroup</span><span class="sxs-lookup"><span data-stu-id="ebc90-151">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="ebc90-152">Operación AddNewImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="ebc90-152">AddNewImContactToGroup operation</span></span>](addnewimcontacttogroup-operation.md)
    
- [<span data-ttu-id="ebc90-153">Operación SetImGroup</span><span class="sxs-lookup"><span data-stu-id="ebc90-153">SetImGroup operation</span></span>](setimgroup-operation.md)
    
- [<span data-ttu-id="ebc90-154">Operación RemoveImGroup</span><span class="sxs-lookup"><span data-stu-id="ebc90-154">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
    
- [<span data-ttu-id="ebc90-155">Operación GetImItemList</span><span class="sxs-lookup"><span data-stu-id="ebc90-155">GetImItemList operation</span></span>](getimitemlist-operation.md)
    
- [<span data-ttu-id="ebc90-156">Personas y contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ebc90-156">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    

