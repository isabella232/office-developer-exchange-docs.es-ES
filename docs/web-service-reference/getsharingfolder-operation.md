---
title: Operación GetSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingFolder
api_type:
- schema
ms.assetid: 75fee92a-a7f8-4a62-ad2b-17acbaada186
description: La operación GetSharingFolder obtiene el identificador de la carpeta local de una carpeta compartida especificada.
ms.openlocfilehash: cf66eb390b0287e89bb8402f26a2e728868a2b18
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460515"
---
# <a name="getsharingfolder-operation"></a><span data-ttu-id="468a9-103">Operación GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="468a9-103">GetSharingFolder operation</span></span>

<span data-ttu-id="468a9-104">La operación **GetSharingFolder** obtiene el identificador de la carpeta local de una carpeta compartida especificada.</span><span class="sxs-lookup"><span data-stu-id="468a9-104">The **GetSharingFolder** operation gets the local folder identifier of a specified shared folder.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="468a9-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="468a9-105">SOAP Headers</span></span>

<span data-ttu-id="468a9-106">La operación **GetSharingFolder** puede usar los encabezados SOAP que se enumeran y describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="468a9-106">The **GetSharingFolder** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="468a9-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="468a9-107">**Header**</span></span>|<span data-ttu-id="468a9-108">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="468a9-108">**Element**</span></span>|<span data-ttu-id="468a9-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="468a9-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="468a9-110">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="468a9-110">RequestVersion</span></span>  <br/> |[<span data-ttu-id="468a9-111">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="468a9-111">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="468a9-112">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="468a9-112">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="468a9-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="468a9-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="468a9-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="468a9-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="468a9-115">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="468a9-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getsharingfolder-request-example"></a><span data-ttu-id="468a9-116">Ejemplo de solicitud GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="468a9-116">GetSharingFolder request example</span></span>

### <a name="getting-the-local-folder-identifier-by-specifying-the-sharedfolderid-element-of-the-folder-being-shared"></a><span data-ttu-id="468a9-117">Obtener el identificador de la carpeta local especificando el elemento SharedFolderId de la carpeta que se va a compartir</span><span class="sxs-lookup"><span data-stu-id="468a9-117">Getting the Local Folder Identifier by Specifying the SharedFolderId Element of the Folder Being Shared</span></span>

<span data-ttu-id="468a9-118">En el ejemplo de código siguiente se muestra cómo crear una solicitud para obtener el identificador de la carpeta local que corresponde a la carpeta que se está compartiendo.</span><span class="sxs-lookup"><span data-stu-id="468a9-118">The following code example shows how to form a request to get the identifier of the local folder that corresponds to the folder that is being shared.</span></span> <span data-ttu-id="468a9-119">La carpeta que se comparte se identifica por la dirección SMTP del buzón de correo que contiene la carpeta compartida y por el elemento [SharedFolderId](sharedfolderid.md) que representa el identificador de dicha carpeta.</span><span class="sxs-lookup"><span data-stu-id="468a9-119">The folder that is being shared is identified by the SMTP address of the mailbox that contains the folder that is being shared and by the [SharedFolderId](sharedfolderid.md) element that represents the identifier of that folder.</span></span> <span data-ttu-id="468a9-120">En este ejemplo, la carpeta que se comparte es propiedad de user1@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="468a9-120">In this example, the folder that is being shared is owned by user1@contoso.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="468a9-121">Código</span><span class="sxs-lookup"><span data-stu-id="468a9-121">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <m:GetSharingFolder>
      <m:SmtpAddress>user1@contoso.com</m:SmtpAddress>
      <m:SharedFolderId>AAMkA=</m:SharedFolderId>
    </m:GetSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="getting-the-local-folder-identifier-by-specifying-the-datatype-element-of-the-folder-being-shared"></a><span data-ttu-id="468a9-122">Obtener el identificador de la carpeta local especificando el elemento DataType de la carpeta que se va a compartir</span><span class="sxs-lookup"><span data-stu-id="468a9-122">Getting the Local Folder Identifier by Specifying the DataType Element of the Folder Being Shared</span></span>

<span data-ttu-id="468a9-123">En el ejemplo de código siguiente se muestra cómo crear una solicitud para obtener el identificador de la carpeta local que corresponde a la carpeta que se está compartiendo.</span><span class="sxs-lookup"><span data-stu-id="468a9-123">The following code example shows how to form a request to get the identifier of the local folder that corresponds to the folder that is being shared.</span></span> <span data-ttu-id="468a9-124">La carpeta que se comparte se identifica por la dirección SMTP del buzón de correo que contiene la carpeta compartida y por el elemento [DataType](datatype.md) que representa el tipo de datos de esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="468a9-124">The folder that is being shared is identified by the SMTP address of the mailbox that contains the folder that is being shared and by the [DataType](datatype.md) element that represents the type of data in that folder.</span></span> <span data-ttu-id="468a9-125">En este ejemplo, la carpeta que se comparte es la carpeta contactos que es propiedad de user1@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="468a9-125">In this example, the folder that is being shared is the Contacts folder that is owned by user1@contoso.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="468a9-126">Código</span><span class="sxs-lookup"><span data-stu-id="468a9-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <m:GetSharingFolder>
      <m:SmtpAddress>user1@contoso.com</m:SmtpAddress>
      <m:DataType>Contacts</m:DataType>
    </m:GetSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="468a9-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="468a9-127">Comments</span></span>

<span data-ttu-id="468a9-128">Para obtener información sobre los valores posibles del elemento **DataType** , vea [DataType](datatype.md).</span><span class="sxs-lookup"><span data-stu-id="468a9-128">For information about the possible values of the **DataType** element, see [DataType](datatype.md).</span></span>
  
## <a name="successful-getsharingfolder-response"></a><span data-ttu-id="468a9-129">Respuesta GetSharingFolder correcta</span><span class="sxs-lookup"><span data-stu-id="468a9-129">Successful GetSharingFolder Response</span></span>

### <a name="description"></a><span data-ttu-id="468a9-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="468a9-130">Description</span></span>

<span data-ttu-id="468a9-131">En el ejemplo siguiente se muestra una respuesta correcta a una solicitud **GetSharingFolder** .</span><span class="sxs-lookup"><span data-stu-id="468a9-131">The following example shows a successful response to a **GetSharingFolder** request.</span></span> <span data-ttu-id="468a9-132">El atributo **ID** del elemento [SharingFolderId](sharingfolderid.md) representa el identificador de la carpeta local en la relación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="468a9-132">The **Id** attribute of the [SharingFolderId](sharingfolderid.md) element represents the identifier of the local folder in the sharing relationship.</span></span> 
  
### <a name="code"></a><span data-ttu-id="468a9-133">Código</span><span class="sxs-lookup"><span data-stu-id="468a9-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingFolderResponseMessage ResponseClass="Success"
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:SharingFolderId Id="AAMkAD=" ChangeKey="AwAAA=" />
    </GetSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="getsharingfolder-error-response"></a><span data-ttu-id="468a9-134">Respuesta de error de GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="468a9-134">GetSharingFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="468a9-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="468a9-135">Description</span></span>

<span data-ttu-id="468a9-136">En el ejemplo siguiente se muestra una respuesta de error a una solicitud **GetSharingFolder** .</span><span class="sxs-lookup"><span data-stu-id="468a9-136">The following example shows an error response to a **GetSharingFolder** request.</span></span> <span data-ttu-id="468a9-137">En este ejemplo, el error se produjo porque la solicitud especificó los elementos [SharingFolderId](sharingfolderid.md) y [DataType](datatype.md) .</span><span class="sxs-lookup"><span data-stu-id="468a9-137">In this example, the error occurred because the request specified both the [SharingFolderId](sharingfolderid.md) and [DataType](datatype.md) elements.</span></span> <span data-ttu-id="468a9-138">Tenga en cuenta que solo se puede especificar uno de estos dos elementos, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="468a9-138">Note that only one or the other of those two elements can be specified, but not both.</span></span> 
  
### <a name="code"></a><span data-ttu-id="468a9-139">Código</span><span class="sxs-lookup"><span data-stu-id="468a9-139">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingFolderResponseMessage ResponseClass="Error" 
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:MessageText>Either DataType or SharedFolderId must be specified, but not both.</m:MessageText>
      <m:ResponseCode>ErrorInvalidGetSharingFolderRequest</m:ResponseCode>
      <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
    </GetSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="468a9-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="468a9-140">See also</span></span>



[<span data-ttu-id="468a9-141">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="468a9-141">GetSharingFolder</span></span>](getsharingfolder.md)
  
[<span data-ttu-id="468a9-142">GetSharingFolderType</span><span class="sxs-lookup"><span data-stu-id="468a9-142">GetSharingFolderType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingFolderType.aspx)
  
[<span data-ttu-id="468a9-143">GetSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="468a9-143">GetSharingFolderResponseMessage</span></span>](getsharingfolderresponsemessage.md)
  
[<span data-ttu-id="468a9-144">GetSharingFolderResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="468a9-144">GetSharingFolderResponseMessageType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingFolderResponseMessageType.aspx)


[<span data-ttu-id="468a9-145">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="468a9-145">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="468a9-146">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="468a9-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

