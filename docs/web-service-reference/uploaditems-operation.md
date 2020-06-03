---
title: Operación UploadItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UploadItems
api_type:
- schema
ms.assetid: a88cbe99-7968-454d-a545-4f92c330909f
description: La operación UploadItems carga una secuencia de elementos en un buzón de Exchange.
ms.openlocfilehash: 57e722c7775baa090736875077781cee869c3b01
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468505"
---
# <a name="uploaditems-operation"></a><span data-ttu-id="24f27-103">Operación UploadItems</span><span class="sxs-lookup"><span data-stu-id="24f27-103">UploadItems operation</span></span>

<span data-ttu-id="24f27-104">La operación **UploadItems** carga una secuencia de elementos en un buzón de Exchange.</span><span class="sxs-lookup"><span data-stu-id="24f27-104">The **UploadItems** operation uploads a stream of items into an Exchange mailbox.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="24f27-105">La operación **UploadItems** está restringida en MicrosoftExchange Server 2010 Service Pack 1 (SP1) a una carga máxima de importación de 25 MB de datos codificados con Base64.</span><span class="sxs-lookup"><span data-stu-id="24f27-105">The **UploadItems** operation is restricted in MicrosoftExchange Server 2010 Service Pack 1 (SP1) to a maximum import payload of 25MB of base64 encoded data.</span></span> <span data-ttu-id="24f27-106">La configuración se puede modificar en el archivo Web. config.</span><span class="sxs-lookup"><span data-stu-id="24f27-106">The setting can be altered in the web.config file.</span></span> 
  
## <a name="uploaditems-request-example"></a><span data-ttu-id="24f27-107">Ejemplo de solicitud UploadItems</span><span class="sxs-lookup"><span data-stu-id="24f27-107">UploadItems request example</span></span>

### <a name="description"></a><span data-ttu-id="24f27-108">Description</span><span class="sxs-lookup"><span data-stu-id="24f27-108">Description</span></span>

<span data-ttu-id="24f27-109">El siguiente ejemplo de una solicitud **UploadItems** muestra cómo cargar dos elementos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="24f27-109">The following example of an **UploadItems** request shows how to upload two items into a mailbox.</span></span> <span data-ttu-id="24f27-110">El primer elemento es un nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="24f27-110">The first item is a new item.</span></span> <span data-ttu-id="24f27-111">El segundo elemento es una versión actualizada de un elemento existente en el buzón.</span><span class="sxs-lookup"><span data-stu-id="24f27-111">The second item is an updated version of an existing item in the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="24f27-112">Código</span><span class="sxs-lookup"><span data-stu-id="24f27-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UploadItems>
      <m:Items>
        <t:Item CreateAction="CreateNew">
          <t:ParentFolderId Id="AQMkADhhOGIgAAAA==" ChangeKey="AQAAAA=="/>
          <t:Data>
            AQAAAAgAAAAAAAAAAQAAAAMAAAAYAAAAAQAAAAcDAgAAAAAAwAAAAA
            AAAEYAJACABAAAAAYAAAABDqSAAAACAAAAcSMAAOSECEBbAAAAL089
            RklSU1QgT1JHQU5JWkFUSU9OL09VPUVYQ0hBTkdFIEFETUlOSVNUUk
            FUSVZFIEdST1VQIChGWURJQk9IRjIzU1BETFQpL0NOPVJFQ0lQSUVO
            VFMvQ049AAMAFwABAAAAsIQaABIAAABJAFAATQAuAE4AbwB0AGUAAA
            ALACMAAAADACYAAAAAAAsAKQAAAAMALgAAAAAAAwA2AAAAAACwhw4=
          </t:Data>
        </t:Item>
        <t:Item CreateAction="Update">
          <t:ParentFolderId Id="AQMkADhhOGIgAAAB==" ChangeKey="AQAAAA=="/>
          <t:ItemId Id="AAMkADhhOGU0MGM7AAA=" ChangeKey="CQAAAA=="/>
          <t:Data>
            AQAAAAgAAAAAAAAAAQAAAAMAAAAYAAAAAQAAAAcDAgAAAAAAwAAAAA
            AAAEYAJACABAAAAAYAAAABDqSAAAACAAAANiAAAOSECEBbAAAAL089
            RklSU1QgT1JHQU5JWkFUSU9OL09VPUVYQ0hBTkdFIEFETUlOSVNUUk
            FUSVZFIEdST1VQIChGWURJQk9IRjIzU1BETFQpL0NOPVJFQ0lQSUVO
            VFMvQ049AAMAFwABAAAAsIQaABIAAABJAFAATQAuAE4AbwB0AGUAAA
            ALACMAAAALACkAAAADADYAAAAAALCENwAyAAAASQBuAHQAZQByAGUA
            cwB0AGkAbgBnACAALQAgAGYAcgBvAG0AIABFAFcAUwBNAEEAAABAAD
            kAgJ2chyHuygECATsAZQAAAEVYOi9PPUZJUlNUIE9SR0FOSVpBVBMO
          </t:Data>
        </t:Item>
      </m:Items>
    </m:UploadItems>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="24f27-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="24f27-113">Comments</span></span>

<span data-ttu-id="24f27-114">Los identificadores y los datos de elemento se acortan para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="24f27-114">Identifiers and the item data have been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="24f27-115">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="24f27-115">Request elements</span></span>

<span data-ttu-id="24f27-116">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="24f27-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="24f27-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="24f27-117">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="24f27-118">UploadItems</span><span class="sxs-lookup"><span data-stu-id="24f27-118">UploadItems</span></span>](uploaditems.md)
    
- [<span data-ttu-id="24f27-119">Elementos (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="24f27-119">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md)
    
- [<span data-ttu-id="24f27-120">Item (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="24f27-120">Item (UploadItemType)</span></span>](item-uploaditemtype.md)
    
- [<span data-ttu-id="24f27-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="24f27-121">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="24f27-122">Datos (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="24f27-122">Data (base64Binary)</span></span>](data-base64binary.md)
    
- [<span data-ttu-id="24f27-123">ItemId</span><span class="sxs-lookup"><span data-stu-id="24f27-123">ItemId</span></span>](itemid.md)
    
## <a name="successful-uploaditems-response-example"></a><span data-ttu-id="24f27-124">Ejemplo de respuesta UploadItems correcta</span><span class="sxs-lookup"><span data-stu-id="24f27-124">Successful UploadItems response example</span></span>

### <a name="description"></a><span data-ttu-id="24f27-125">Description</span><span class="sxs-lookup"><span data-stu-id="24f27-125">Description</span></span>

<span data-ttu-id="24f27-126">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud **UploadItems** .</span><span class="sxs-lookup"><span data-stu-id="24f27-126">The following example shows a successful response to the **UploadItems** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="24f27-127">Código</span><span class="sxs-lookup"><span data-stu-id="24f27-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14"
                         MinorVersion="1"
                         MajorBuildNumber="164"
                         MinorBuildNumber="0"
                         Version="Exchange2010_SP1"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:UploadItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                           xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:UploadItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkADhhUFZ/AAA=" ChangeKey="CQAAABYAAABsMBS3hrihS7voMf0GPIQeAAAAULQm"/>
        </m:UploadItemsResponseMessage>
        <m:UploadItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ItemId Id="AAMkADhhOGZ7AAA=" ChangeKey="CQAAABYAAABsMBS3hrihS7voMf0GPIQeAAAAULQn"/>
        </m:UploadItemsResponseMessage>
      </m:ResponseMessages>
    </m:UploadItemsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="comments"></a><span data-ttu-id="24f27-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="24f27-128">Comments</span></span>

<span data-ttu-id="24f27-129">Los identificadores de elemento se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="24f27-129">Item identifiers have been shortened to preserve readability.</span></span>
  
### <a name="response-elements"></a><span data-ttu-id="24f27-130">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="24f27-130">Response elements</span></span>

<span data-ttu-id="24f27-131">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="24f27-131">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="24f27-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="24f27-132">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="24f27-133">UploadItemsResponse</span><span class="sxs-lookup"><span data-stu-id="24f27-133">UploadItemsResponse</span></span>](uploaditemsresponse.md)
    
- [<span data-ttu-id="24f27-134">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="24f27-134">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="24f27-135">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="24f27-135">UploadItemsResponseMessage</span></span>](uploaditemsresponsemessage.md)
    
- [<span data-ttu-id="24f27-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="24f27-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="24f27-137">ItemId</span><span class="sxs-lookup"><span data-stu-id="24f27-137">ItemId</span></span>](itemid.md)
    
## <a name="uploaditems-error-response-example"></a><span data-ttu-id="24f27-138">Ejemplo de respuesta de error UploadItems</span><span class="sxs-lookup"><span data-stu-id="24f27-138">UploadItems Error response example</span></span>

### <a name="description"></a><span data-ttu-id="24f27-139">Description</span><span class="sxs-lookup"><span data-stu-id="24f27-139">Description</span></span>

<span data-ttu-id="24f27-140">En el ejemplo siguiente se muestra una respuesta a la solicitud **UploadItems** que contiene un error provocado por un intento de actualizar un elemento que no se encuentra en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="24f27-140">The following example shows a response to the **UploadItems** request that contains an error caused by an attempt to update an item that cannot be found in the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="24f27-141">Código</span><span class="sxs-lookup"><span data-stu-id="24f27-141">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="164" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:UploadItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:UploadItemsResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:UploadItemsResponseMessage>
      </m:ResponseMessages>
    </m:UploadItemsResponse>
  </s:Body>
</s:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="24f27-142">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="24f27-142">Error response elements</span></span>

<span data-ttu-id="24f27-143">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="24f27-143">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="24f27-144">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="24f27-144">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="24f27-145">UploadItemsResponse</span><span class="sxs-lookup"><span data-stu-id="24f27-145">UploadItemsResponse</span></span>](uploaditemsresponse.md)
    
- [<span data-ttu-id="24f27-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="24f27-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="24f27-147">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="24f27-147">UploadItemsResponseMessage</span></span>](uploaditemsresponsemessage.md)
    
- [<span data-ttu-id="24f27-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="24f27-148">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="24f27-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="24f27-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="24f27-150">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="24f27-150">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="24f27-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="24f27-151">See also</span></span>



[<span data-ttu-id="24f27-152">Operación ExportItems</span><span class="sxs-lookup"><span data-stu-id="24f27-152">ExportItems operation</span></span>](exportitems-operation.md)


[<span data-ttu-id="24f27-153">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="24f27-153">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="24f27-154">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="24f27-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

