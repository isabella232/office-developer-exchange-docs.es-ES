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
description: La operación UpdateItem se usa para actualizar las propiedades de los elementos de contacto en el almacén de Exchange.
ms.openlocfilehash: 66e1b91ea3154d8a501339aed7b398970e8f5392
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459829"
---
# <a name="updateitem-operation-contact"></a><span data-ttu-id="e9b89-103">Operación UpdateItem (contacto)</span><span class="sxs-lookup"><span data-stu-id="e9b89-103">UpdateItem operation (contact)</span></span>

<span data-ttu-id="e9b89-104">La operación UpdateItem se usa para actualizar las propiedades de los elementos de contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e9b89-104">The UpdateItem operation is used to update contact item properties in the Exchange store.</span></span>
  
## <a name="updateitem-contact-request-example"></a><span data-ttu-id="e9b89-105">Ejemplo de solicitud de UpdateItem (contact)</span><span class="sxs-lookup"><span data-stu-id="e9b89-105">UpdateItem (Contact) request example</span></span>

### <a name="description"></a><span data-ttu-id="e9b89-106">Description</span><span class="sxs-lookup"><span data-stu-id="e9b89-106">Description</span></span>

<span data-ttu-id="e9b89-107">En el ejemplo de código siguiente se muestra cómo actualizar la dirección de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="e9b89-107">The following code example shows how to update the e-mail address of a contact.</span></span>
  
### <a name="code"></a><span data-ttu-id="e9b89-108">Código</span><span class="sxs-lookup"><span data-stu-id="e9b89-108">Code</span></span>

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
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

### <a name="comments"></a><span data-ttu-id="e9b89-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e9b89-109">Comments</span></span>

<span data-ttu-id="e9b89-110">El identificador de elemento se ha abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="e9b89-110">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="e9b89-111">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9b89-111">Request elements</span></span>

<span data-ttu-id="e9b89-112">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="e9b89-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="e9b89-113">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="e9b89-113">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="e9b89-114">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="e9b89-114">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="e9b89-115">ItemChange</span><span class="sxs-lookup"><span data-stu-id="e9b89-115">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="e9b89-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="e9b89-116">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="e9b89-117">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="e9b89-117">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="e9b89-118">SetItemField</span><span class="sxs-lookup"><span data-stu-id="e9b89-118">SetItemField</span></span>](setitemfield.md)
    
- [<span data-ttu-id="e9b89-119">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="e9b89-119">IndexedFieldURI</span></span>](indexedfielduri.md)
    
- [<span data-ttu-id="e9b89-120">Contacto</span><span class="sxs-lookup"><span data-stu-id="e9b89-120">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="e9b89-121">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="e9b89-121">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="e9b89-122">Entrada (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="e9b89-122">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
## <a name="successful-updateitem-contact-response"></a><span data-ttu-id="e9b89-123">Respuesta de UpdateItem (contacto) correcta</span><span class="sxs-lookup"><span data-stu-id="e9b89-123">Successful UpdateItem (Contact) Response</span></span>

### <a name="description"></a><span data-ttu-id="e9b89-124">Description</span><span class="sxs-lookup"><span data-stu-id="e9b89-124">Description</span></span>

<span data-ttu-id="e9b89-125">En el ejemplo de código siguiente se muestra una respuesta UpdateItem correcta.</span><span class="sxs-lookup"><span data-stu-id="e9b89-125">The following code example shows a successful UpdateItem response.</span></span>
  
### <a name="code"></a><span data-ttu-id="e9b89-126">Código</span><span class="sxs-lookup"><span data-stu-id="e9b89-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="e9b89-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e9b89-127">Comments</span></span>

<span data-ttu-id="e9b89-128">El identificador de elemento se ha abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="e9b89-128">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="e9b89-129">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="e9b89-129">Successful response elements</span></span>

<span data-ttu-id="e9b89-130">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e9b89-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="e9b89-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e9b89-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="e9b89-132">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="e9b89-132">UpdateItemResponse</span></span>](updateitemresponse.md)
    
- [<span data-ttu-id="e9b89-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e9b89-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e9b89-134">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e9b89-134">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
    
- [<span data-ttu-id="e9b89-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e9b89-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e9b89-136">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="e9b89-136">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="e9b89-137">Contacto</span><span class="sxs-lookup"><span data-stu-id="e9b89-137">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="e9b89-138">ItemId</span><span class="sxs-lookup"><span data-stu-id="e9b89-138">ItemId</span></span>](itemid.md)
    
## <a name="invalid-updateitem-contact-request-example"></a><span data-ttu-id="e9b89-139">Ejemplo de solicitud de UpdateItem (contacto) no válida</span><span class="sxs-lookup"><span data-stu-id="e9b89-139">Invalid UpdateItem (Contact) request example</span></span>

### <a name="description"></a><span data-ttu-id="e9b89-140">Description</span><span class="sxs-lookup"><span data-stu-id="e9b89-140">Description</span></span>

<span data-ttu-id="e9b89-141">En el ejemplo de código siguiente se muestra una solicitud no válida.</span><span class="sxs-lookup"><span data-stu-id="e9b89-141">The following code example shows an invalid request.</span></span>
  
### <a name="code"></a><span data-ttu-id="e9b89-142">Código</span><span class="sxs-lookup"><span data-stu-id="e9b89-142">Code</span></span>

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
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

### <a name="comments"></a><span data-ttu-id="e9b89-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e9b89-143">Comments</span></span>

<span data-ttu-id="e9b89-144">El identificador de elemento se ha abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="e9b89-144">The item identifier has been shortened to preserve readability.</span></span>
  
## <a name="updateitem-contact-error-response"></a><span data-ttu-id="e9b89-145">Respuesta de error de UpdateItem (contacto)</span><span class="sxs-lookup"><span data-stu-id="e9b89-145">UpdateItem (Contact) error response</span></span>

### <a name="description"></a><span data-ttu-id="e9b89-146">Description</span><span class="sxs-lookup"><span data-stu-id="e9b89-146">Description</span></span>

<span data-ttu-id="e9b89-147">El siguiente ejemplo de código muestra una respuesta de error a una solicitud de UpdateItem (contacto).</span><span class="sxs-lookup"><span data-stu-id="e9b89-147">The following code example shows an error response to an UpdateItem (Contact) request.</span></span>
  
### <a name="code"></a><span data-ttu-id="e9b89-148">Código</span><span class="sxs-lookup"><span data-stu-id="e9b89-148">Code</span></span>

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <soap:Fault>
      <soap:faultcode>Client</soap:faultcode>
      <soap:faultstring>The request failed schema validation.</soap:faultstring>
      <detail>
        <e:ResponseCode xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
        <e:Message xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">The 'Key' attribute is invalid - The value 'EmailAddress4' is invalid according to its data type 'https://schemas.microsoft.com/exchange/services/2006/types:EmailAddressKeyType' - The Enumeration constraint failed.</e:Message>
        <e:Line xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">17</e:Line>
        <e:Position xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">19</e:Position>
      </detail>
    </soap:Fault>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="e9b89-149">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e9b89-149">Comments</span></span>

<span data-ttu-id="e9b89-150">Algunos elementos que se usan en el cuerpo SOAP de una respuesta de error debido a un error de validación de esquema no se definen en los esquemas de mensajes o tipos.</span><span class="sxs-lookup"><span data-stu-id="e9b89-150">Some elements that are used in the SOAP body of an error response that is caused by a schema validation error are not defined in the messages or types schemas.</span></span> <span data-ttu-id="e9b89-151">El elemento **detail** contiene información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="e9b89-151">The **detail** element contains information about the error.</span></span> <span data-ttu-id="e9b89-152">El elemento [ResponseCode](responsecode.md) contiene el código de error.</span><span class="sxs-lookup"><span data-stu-id="e9b89-152">The [ResponseCode](responsecode.md) element contains the error code.</span></span> <span data-ttu-id="e9b89-153">El elemento [Message](message-ex15websvcsotherref.md) contiene una explicación del error, si hay alguno disponible.</span><span class="sxs-lookup"><span data-stu-id="e9b89-153">The [Message](message-ex15websvcsotherref.md) element contains an explanation for the error, if one is available.</span></span> <span data-ttu-id="e9b89-154">El elemento **line** describe el número de línea en el que se produjo el error de validación de esquema.</span><span class="sxs-lookup"><span data-stu-id="e9b89-154">The **Line** element describes the line number where the schema validation error occurred.</span></span> <span data-ttu-id="e9b89-155">El elemento **Position** describe la posición desde el carácter más a la izquierda del documento XML.</span><span class="sxs-lookup"><span data-stu-id="e9b89-155">The **Position** element describes the position from the leftmost character of the XML document.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9b89-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9b89-156">See also</span></span>



[<span data-ttu-id="e9b89-157">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="e9b89-157">UpdateItem operation</span></span>](updateitem-operation.md)

