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
ms.openlocfilehash: 6b002d531c7011b18ae1f88adfc2923d5a51e81c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840874"
---
# <a name="uploaditems-operation"></a><span data-ttu-id="663c2-103">Operación UploadItems</span><span class="sxs-lookup"><span data-stu-id="663c2-103">UploadItems operation</span></span>

<span data-ttu-id="663c2-104">La operación **UploadItems** carga una secuencia de elementos en un buzón de Exchange.</span><span class="sxs-lookup"><span data-stu-id="663c2-104">The **UploadItems** operation uploads a stream of items into an Exchange mailbox.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="663c2-105">La operación **UploadItems** está restringida en MicrosoftExchange Server 2010 Service Pack 1 (SP1) a una carga de importación máximo de 25 MB de datos con codificación base64.</span><span class="sxs-lookup"><span data-stu-id="663c2-105">The **UploadItems** operation is restricted in MicrosoftExchange Server 2010 Service Pack 1 (SP1) to a maximum import payload of 25MB of base64 encoded data.</span></span> <span data-ttu-id="663c2-106">La configuración se puede modificar en el archivo web.config.</span><span class="sxs-lookup"><span data-stu-id="663c2-106">The setting can be altered in the web.config file.</span></span> 
  
## <a name="uploaditems-request-example"></a><span data-ttu-id="663c2-107">Ejemplo de solicitud de UploadItems</span><span class="sxs-lookup"><span data-stu-id="663c2-107">UploadItems request example</span></span>

### <a name="description"></a><span data-ttu-id="663c2-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="663c2-108">Description</span></span>

<span data-ttu-id="663c2-109">El siguiente ejemplo de una solicitud de **UploadItems** muestra cómo cargar dos elementos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="663c2-109">The following example of an **UploadItems** request shows how to upload two items into a mailbox.</span></span> <span data-ttu-id="663c2-110">El primer elemento es un nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="663c2-110">The first item is a new item.</span></span> <span data-ttu-id="663c2-111">El segundo elemento es una versión actualizada de un elemento existente en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="663c2-111">The second item is an updated version of an existing item in the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="663c2-112">Código</span><span class="sxs-lookup"><span data-stu-id="663c2-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="663c2-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="663c2-113">Comments</span></span>

<span data-ttu-id="663c2-114">Identificadores y los datos de elemento se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="663c2-114">Identifiers and the item data have been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="663c2-115">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="663c2-115">Request elements</span></span>

<span data-ttu-id="663c2-116">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="663c2-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="663c2-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="663c2-117">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="663c2-118">UploadItems</span><span class="sxs-lookup"><span data-stu-id="663c2-118">UploadItems</span></span>](uploaditems.md)
    
- [<span data-ttu-id="663c2-119">Elementos (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="663c2-119">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md)
    
- [<span data-ttu-id="663c2-120">Elemento (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="663c2-120">Item (UploadItemType)</span></span>](item-uploaditemtype.md)
    
- [<span data-ttu-id="663c2-121">Id</span><span class="sxs-lookup"><span data-stu-id="663c2-121">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="663c2-122">Datos (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="663c2-122">Data (base64Binary)</span></span>](data-base64binary.md)
    
- [<span data-ttu-id="663c2-123">ItemId</span><span class="sxs-lookup"><span data-stu-id="663c2-123">ItemId</span></span>](itemid.md)
    
## <a name="successful-uploaditems-response-example"></a><span data-ttu-id="663c2-124">Ejemplo de respuesta correcta de UploadItems</span><span class="sxs-lookup"><span data-stu-id="663c2-124">Successful UploadItems response example</span></span>

### <a name="description"></a><span data-ttu-id="663c2-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="663c2-125">Description</span></span>

<span data-ttu-id="663c2-126">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de **UploadItems** .</span><span class="sxs-lookup"><span data-stu-id="663c2-126">The following example shows a successful response to the **UploadItems** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="663c2-127">Código</span><span class="sxs-lookup"><span data-stu-id="663c2-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14"
                         MinorVersion="1"
                         MajorBuildNumber="164"
                         MinorBuildNumber="0"
                         Version="Exchange2010_SP1"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:UploadItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="663c2-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="663c2-128">Comments</span></span>

<span data-ttu-id="663c2-129">Identificadores de elemento se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="663c2-129">Item identifiers have been shortened to preserve readability.</span></span>
  
### <a name="response-elements"></a><span data-ttu-id="663c2-130">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="663c2-130">Response elements</span></span>

<span data-ttu-id="663c2-131">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="663c2-131">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="663c2-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="663c2-132">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="663c2-133">UploadItemsResponse</span><span class="sxs-lookup"><span data-stu-id="663c2-133">UploadItemsResponse</span></span>](uploaditemsresponse.md)
    
- [<span data-ttu-id="663c2-134">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="663c2-134">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="663c2-135">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="663c2-135">UploadItemsResponseMessage</span></span>](uploaditemsresponsemessage.md)
    
- [<span data-ttu-id="663c2-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="663c2-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="663c2-137">ItemId</span><span class="sxs-lookup"><span data-stu-id="663c2-137">ItemId</span></span>](itemid.md)
    
## <a name="uploaditems-error-response-example"></a><span data-ttu-id="663c2-138">Ejemplo de respuesta de UploadItems Error</span><span class="sxs-lookup"><span data-stu-id="663c2-138">UploadItems Error response example</span></span>

### <a name="description"></a><span data-ttu-id="663c2-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="663c2-139">Description</span></span>

<span data-ttu-id="663c2-140">En el ejemplo siguiente se muestra una respuesta a la solicitud de **UploadItems** que contiene un error debido a un intento de actualizar un elemento que no se encuentra en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="663c2-140">The following example shows a response to the **UploadItems** request that contains an error caused by an attempt to update an item that cannot be found in the mailbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="663c2-141">Código</span><span class="sxs-lookup"><span data-stu-id="663c2-141">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="164" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:UploadItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="error-response-elements"></a><span data-ttu-id="663c2-142">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="663c2-142">Error response elements</span></span>

<span data-ttu-id="663c2-143">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="663c2-143">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="663c2-144">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="663c2-144">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="663c2-145">UploadItemsResponse</span><span class="sxs-lookup"><span data-stu-id="663c2-145">UploadItemsResponse</span></span>](uploaditemsresponse.md)
    
- [<span data-ttu-id="663c2-146">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="663c2-146">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="663c2-147">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="663c2-147">UploadItemsResponseMessage</span></span>](uploaditemsresponsemessage.md)
    
- [<span data-ttu-id="663c2-148">MessageText</span><span class="sxs-lookup"><span data-stu-id="663c2-148">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="663c2-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="663c2-149">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="663c2-150">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="663c2-150">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="663c2-151">Ver también</span><span class="sxs-lookup"><span data-stu-id="663c2-151">See also</span></span>



[<span data-ttu-id="663c2-152">Operación ExportItems</span><span class="sxs-lookup"><span data-stu-id="663c2-152">ExportItems operation</span></span>](exportitems-operation.md)


[<span data-ttu-id="663c2-153">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="663c2-153">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="663c2-154">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="663c2-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

