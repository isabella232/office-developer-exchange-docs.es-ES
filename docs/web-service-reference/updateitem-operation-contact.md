---
title: Operación UpdateItem (contacto)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 298fdd71-a83d-4407-9728-4f0a8e2d857c
description: La operación UpdateItem se utiliza para actualizar las propiedades del elemento de contacto en el almacén de Exchange.
ms.openlocfilehash: f2a501ce8e69068cd30b58011adf4defc68ce365
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840836"
---
# <a name="updateitem-operation-contact"></a><span data-ttu-id="cf8fc-103">Operación UpdateItem (contacto)</span><span class="sxs-lookup"><span data-stu-id="cf8fc-103">UpdateItem operation (contact)</span></span>

<span data-ttu-id="cf8fc-104">La operación UpdateItem se utiliza para actualizar las propiedades del elemento de contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cf8fc-104">The UpdateItem operation is used to update contact item properties in the Exchange store.</span></span>
  
## <a name="updateitem-contact-request-example"></a><span data-ttu-id="cf8fc-105">Ejemplo de solicitud UpdateItem (contacto)</span><span class="sxs-lookup"><span data-stu-id="cf8fc-105">UpdateItem (Contact) request example</span></span>

### <a name="description"></a><span data-ttu-id="cf8fc-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf8fc-106">Description</span></span>

<span data-ttu-id="cf8fc-107">En el ejemplo de código siguiente se muestra cómo actualizar la dirección de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="cf8fc-107">The following code example shows how to update the e-mail address of a contact.</span></span>
  
### <a name="code"></a><span data-ttu-id="cf8fc-108">Código</span><span class="sxs-lookup"><span data-stu-id="cf8fc-108">Code</span></span>

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                ConflictResolution="AlwaysOverwrite">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAA=" ChangeKey="EQAAABYi" />
          <t:Updates>
            <t:SetItemField>
              <t:IndexedFieldURI FieldURI="contacts:EmailAddress" FieldIndex="EmailAddress1"/>
              <t:Contact>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress1">changedemail@example.com</t:Entry>
                </t:EmailAddresses>
              </t:Contact>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="cf8fc-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cf8fc-109">Comments</span></span>

<span data-ttu-id="cf8fc-110">El identificador del elemento se ha acortado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="cf8fc-110">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="cf8fc-111">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="cf8fc-111">Request elements</span></span>

<span data-ttu-id="cf8fc-112">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="cf8fc-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="cf8fc-113">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="cf8fc-113">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="cf8fc-114">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="cf8fc-114">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="cf8fc-115">ItemChange</span><span class="sxs-lookup"><span data-stu-id="cf8fc-115">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="cf8fc-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="cf8fc-116">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="cf8fc-117">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="cf8fc-117">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="cf8fc-118">SetItemField</span><span class="sxs-lookup"><span data-stu-id="cf8fc-118">SetItemField</span></span>](setitemfield.md)
    
- [<span data-ttu-id="cf8fc-119">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="cf8fc-119">IndexedFieldURI</span></span>](indexedfielduri.md)
    
- [<span data-ttu-id="cf8fc-120">Contact</span><span class="sxs-lookup"><span data-stu-id="cf8fc-120">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="cf8fc-121">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="cf8fc-121">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="cf8fc-122">Entrada (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="cf8fc-122">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
## <a name="successful-updateitem-contact-response"></a><span data-ttu-id="cf8fc-123">Respuesta correcta UpdateItem (contacto)</span><span class="sxs-lookup"><span data-stu-id="cf8fc-123">Successful UpdateItem (Contact) Response</span></span>

### <a name="description"></a><span data-ttu-id="cf8fc-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf8fc-124">Description</span></span>

<span data-ttu-id="cf8fc-125">En el ejemplo de código siguiente se muestra una respuesta UpdateItem correcta.</span><span class="sxs-lookup"><span data-stu-id="cf8fc-125">The following code example shows a successful UpdateItem response.</span></span>
  
### <a name="code"></a><span data-ttu-id="cf8fc-126">Código</span><span class="sxs-lookup"><span data-stu-id="cf8fc-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Contact>
              <t:ItemId Id="AAAtAE=" ChangeKey="EQAAABYx" />
            </t:Contact>
          </m:Items>
        </m:UpdateItemResponseMessage>
      </m:ResponseMessages>
    </UpdateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="cf8fc-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cf8fc-127">Comments</span></span>

<span data-ttu-id="cf8fc-128">El identificador del elemento se ha acortado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="cf8fc-128">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="cf8fc-129">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="cf8fc-129">Successful response elements</span></span>

<span data-ttu-id="cf8fc-130">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="cf8fc-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="cf8fc-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="cf8fc-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="cf8fc-132">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="cf8fc-132">UpdateItemResponse</span></span>](updateitemresponse.md)
    
- [<span data-ttu-id="cf8fc-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="cf8fc-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="cf8fc-134">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cf8fc-134">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
    
- [<span data-ttu-id="cf8fc-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cf8fc-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="cf8fc-136">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="cf8fc-136">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="cf8fc-137">Contact</span><span class="sxs-lookup"><span data-stu-id="cf8fc-137">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="cf8fc-138">ItemId</span><span class="sxs-lookup"><span data-stu-id="cf8fc-138">ItemId</span></span>](itemid.md)
    
## <a name="invalid-updateitem-contact-request-example"></a><span data-ttu-id="cf8fc-139">Ejemplo de solicitud UpdateItem (contactos) no válido</span><span class="sxs-lookup"><span data-stu-id="cf8fc-139">Invalid UpdateItem (Contact) request example</span></span>

### <a name="description"></a><span data-ttu-id="cf8fc-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf8fc-140">Description</span></span>

<span data-ttu-id="cf8fc-141">En el ejemplo de código siguiente se muestra una solicitud no válida.</span><span class="sxs-lookup"><span data-stu-id="cf8fc-141">The following code example shows an invalid request.</span></span>
  
### <a name="code"></a><span data-ttu-id="cf8fc-142">Código</span><span class="sxs-lookup"><span data-stu-id="cf8fc-142">Code</span></span>

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                ConflictResolution="AlwaysOverwrite">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEF=" ChangeKey="EQAAABYi" />
          <t:Updates>
            <t:SetItemField>
              <t:IndexedFieldURI FieldURI="contacts:EmailAddress" FieldIndex="EmailAddress4"/>
              <t:Contact>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress4">changedemail2@example.com</t:Entry>
                </t:EmailAddresses>
              </t:Contact>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="cf8fc-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cf8fc-143">Comments</span></span>

<span data-ttu-id="cf8fc-144">El identificador del elemento se ha acortado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="cf8fc-144">The item identifier has been shortened to preserve readability.</span></span>
  
## <a name="updateitem-contact-error-response"></a><span data-ttu-id="cf8fc-145">Respuesta de error UpdateItem (contacto)</span><span class="sxs-lookup"><span data-stu-id="cf8fc-145">UpdateItem (Contact) error response</span></span>

### <a name="description"></a><span data-ttu-id="cf8fc-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf8fc-146">Description</span></span>

<span data-ttu-id="cf8fc-147">En el ejemplo de código siguiente se muestra una respuesta de error a una solicitud de UpdateItem (contactos).</span><span class="sxs-lookup"><span data-stu-id="cf8fc-147">The following code example shows an error response to an UpdateItem (Contact) request.</span></span>
  
### <a name="code"></a><span data-ttu-id="cf8fc-148">Código</span><span class="sxs-lookup"><span data-stu-id="cf8fc-148">Code</span></span>

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <soap:Fault>
      <soap:faultcode>Client</soap:faultcode>
      <soap:faultstring>The request failed schema validation.</soap:faultstring>
      <detail>
        <e:ResponseCode xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
        <e:Message xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">The 'Key' attribute is invalid - The value 'EmailAddress4' is invalid according to its data type 'http://schemas.microsoft.com/exchange/services/2006/types:EmailAddressKeyType' - The Enumeration constraint failed.</e:Message>
        <e:Line xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">17</e:Line>
        <e:Position xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">19</e:Position>
      </detail>
    </soap:Fault>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="cf8fc-149">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cf8fc-149">Comments</span></span>

<span data-ttu-id="cf8fc-150">Algunos elementos que se usan en el cuerpo SOAP de una respuesta de error que está causado por un error de validación de esquema no están definidos en los esquemas de mensajes o tipos.</span><span class="sxs-lookup"><span data-stu-id="cf8fc-150">Some elements that are used in the SOAP body of an error response that is caused by a schema validation error are not defined in the messages or types schemas.</span></span> <span data-ttu-id="cf8fc-151">El elemento de **detalle** contiene información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="cf8fc-151">The **detail** element contains information about the error.</span></span> <span data-ttu-id="cf8fc-152">El elemento [ResponseCode](responsecode.md) contiene el código de error.</span><span class="sxs-lookup"><span data-stu-id="cf8fc-152">The [ResponseCode](responsecode.md) element contains the error code.</span></span> <span data-ttu-id="cf8fc-153">El elemento de [mensaje](message-ex15websvcsotherref.md) contiene una explicación para el error, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="cf8fc-153">The [Message](message-ex15websvcsotherref.md) element contains an explanation for the error, if one is available.</span></span> <span data-ttu-id="cf8fc-154">El elemento de **línea** describe el número de línea donde se produjo el error de validación de esquema.</span><span class="sxs-lookup"><span data-stu-id="cf8fc-154">The **Line** element describes the line number where the schema validation error occurred.</span></span> <span data-ttu-id="cf8fc-155">El elemento de la **posición** describe la posición de carácter del extremo izquierdo del documento XML.</span><span class="sxs-lookup"><span data-stu-id="cf8fc-155">The **Position** element describes the position from the leftmost character of the XML document.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cf8fc-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf8fc-156">See also</span></span>



[<span data-ttu-id="cf8fc-157">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="cf8fc-157">UpdateItem operation</span></span>](updateitem-operation.md)

