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
description: La operación GetSharingFolder Obtiene el identificador de la carpeta local de una carpeta compartida especificada.
ms.openlocfilehash: 23adb10b22623fcbc1dd6b33bd674afafdaa8b19
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835670"
---
# <a name="getsharingfolder-operation"></a><span data-ttu-id="cc2d2-103">Operación GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="cc2d2-103">GetSharingFolder operation</span></span>

<span data-ttu-id="cc2d2-104">La operación **GetSharingFolder** Obtiene el identificador de la carpeta local de una carpeta compartida especificada.</span><span class="sxs-lookup"><span data-stu-id="cc2d2-104">The **GetSharingFolder** operation gets the local folder identifier of a specified shared folder.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="cc2d2-105">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="cc2d2-105">SOAP Headers</span></span>

<span data-ttu-id="cc2d2-106">La operación de **GetSharingFolder** puede utilizar los encabezados SOAP que se enumeran y describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="cc2d2-106">The **GetSharingFolder** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="cc2d2-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="cc2d2-107">**Header**</span></span>|<span data-ttu-id="cc2d2-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="cc2d2-108">**Element**</span></span>|<span data-ttu-id="cc2d2-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc2d2-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cc2d2-110">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="cc2d2-110">RequestVersion</span></span>  <br/> |[<span data-ttu-id="cc2d2-111">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="cc2d2-111">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="cc2d2-112">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="cc2d2-112">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="cc2d2-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="cc2d2-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="cc2d2-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="cc2d2-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="cc2d2-115">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cc2d2-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getsharingfolder-request-example"></a><span data-ttu-id="cc2d2-116">Ejemplo de solicitud de GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="cc2d2-116">GetSharingFolder request example</span></span>

### <a name="getting-the-local-folder-identifier-by-specifying-the-sharedfolderid-element-of-the-folder-being-shared"></a><span data-ttu-id="cc2d2-117">Obtener el identificador de la carpeta Local mediante la especificación del elemento SharedFolderId de la carpeta que se está compartida</span><span class="sxs-lookup"><span data-stu-id="cc2d2-117">Getting the Local Folder Identifier by Specifying the SharedFolderId Element of the Folder Being Shared</span></span>

<span data-ttu-id="cc2d2-118">En el ejemplo de código siguiente se muestra cómo formar una solicitud para obtener el identificador de la carpeta local que corresponde a la carpeta que se está compartiendo.</span><span class="sxs-lookup"><span data-stu-id="cc2d2-118">The following code example shows how to form a request to get the identifier of the local folder that corresponds to the folder that is being shared.</span></span> <span data-ttu-id="cc2d2-119">La carpeta que se está compartiendo se identifica con la dirección SMTP del buzón que contiene la carpeta que se está compartiendo y por el elemento [SharedFolderId](sharedfolderid.md) que representa el identificador de esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="cc2d2-119">The folder that is being shared is identified by the SMTP address of the mailbox that contains the folder that is being shared and by the [SharedFolderId](sharedfolderid.md) element that represents the identifier of that folder.</span></span> <span data-ttu-id="cc2d2-120">En este ejemplo, la carpeta que se está compartiendo la propiedad user1@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="cc2d2-120">In this example, the folder that is being shared is owned by user1@contoso.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="cc2d2-121">Código</span><span class="sxs-lookup"><span data-stu-id="cc2d2-121">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="getting-the-local-folder-identifier-by-specifying-the-datatype-element-of-the-folder-being-shared"></a><span data-ttu-id="cc2d2-122">Obtener el identificador de la carpeta Local especificando el tipo del elemento de la carpeta que se está compartida</span><span class="sxs-lookup"><span data-stu-id="cc2d2-122">Getting the Local Folder Identifier by Specifying the DataType Element of the Folder Being Shared</span></span>

<span data-ttu-id="cc2d2-123">En el ejemplo de código siguiente se muestra cómo formar una solicitud para obtener el identificador de la carpeta local que corresponde a la carpeta que se está compartiendo.</span><span class="sxs-lookup"><span data-stu-id="cc2d2-123">The following code example shows how to form a request to get the identifier of the local folder that corresponds to the folder that is being shared.</span></span> <span data-ttu-id="cc2d2-124">La carpeta que se está compartiendo se identifica con la dirección SMTP del buzón que contiene la carpeta que se está compartiendo y por el elemento de [tipo de datos](datatype.md) que representa el tipo de datos en esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="cc2d2-124">The folder that is being shared is identified by the SMTP address of the mailbox that contains the folder that is being shared and by the [DataType](datatype.md) element that represents the type of data in that folder.</span></span> <span data-ttu-id="cc2d2-125">En este ejemplo, la carpeta que se está compartiendo es la carpeta de contactos cuyo propietario es user1@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="cc2d2-125">In this example, the folder that is being shared is the Contacts folder that is owned by user1@contoso.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="cc2d2-126">Código</span><span class="sxs-lookup"><span data-stu-id="cc2d2-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="cc2d2-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc2d2-127">Comments</span></span>

<span data-ttu-id="cc2d2-128">Para obtener información acerca de los valores posibles del elemento de **tipo de datos** , vea el [tipo de datos](datatype.md).</span><span class="sxs-lookup"><span data-stu-id="cc2d2-128">For information about the possible values of the **DataType** element, see [DataType](datatype.md).</span></span>
  
## <a name="successful-getsharingfolder-response"></a><span data-ttu-id="cc2d2-129">GetSharingFolder la respuesta es correcta</span><span class="sxs-lookup"><span data-stu-id="cc2d2-129">Successful GetSharingFolder Response</span></span>

### <a name="description"></a><span data-ttu-id="cc2d2-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc2d2-130">Description</span></span>

<span data-ttu-id="cc2d2-131">En el ejemplo siguiente se muestra una respuesta a una solicitud **GetSharingFolder** correcta.</span><span class="sxs-lookup"><span data-stu-id="cc2d2-131">The following example shows a successful response to a **GetSharingFolder** request.</span></span> <span data-ttu-id="cc2d2-132">El atributo **Id** del elemento [SharingFolderId](sharingfolderid.md) representa el identificador de la carpeta local en la relación de uso compartida.</span><span class="sxs-lookup"><span data-stu-id="cc2d2-132">The **Id** attribute of the [SharingFolderId](sharingfolderid.md) element represents the identifier of the local folder in the sharing relationship.</span></span> 
  
### <a name="code"></a><span data-ttu-id="cc2d2-133">Código</span><span class="sxs-lookup"><span data-stu-id="cc2d2-133">Code</span></span>

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
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingFolderResponseMessage ResponseClass="Success"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:SharingFolderId Id="AAMkAD=" ChangeKey="AwAAA=" />
    </GetSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="getsharingfolder-error-response"></a><span data-ttu-id="cc2d2-134">Respuesta de error de GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="cc2d2-134">GetSharingFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="cc2d2-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc2d2-135">Description</span></span>

<span data-ttu-id="cc2d2-136">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de **GetSharingFolder** .</span><span class="sxs-lookup"><span data-stu-id="cc2d2-136">The following example shows an error response to a **GetSharingFolder** request.</span></span> <span data-ttu-id="cc2d2-137">En este ejemplo, se produjo el error debido a que la solicitud de los elementos de la [SharingFolderId](sharingfolderid.md) y el [tipo de datos](datatype.md) especificados.</span><span class="sxs-lookup"><span data-stu-id="cc2d2-137">In this example, the error occurred because the request specified both the [SharingFolderId](sharingfolderid.md) and [DataType](datatype.md) elements.</span></span> <span data-ttu-id="cc2d2-138">Tenga en cuenta que sólo uno u otro de esos dos elementos puede especificarse, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="cc2d2-138">Note that only one or the other of those two elements can be specified, but not both.</span></span> 
  
### <a name="code"></a><span data-ttu-id="cc2d2-139">Código</span><span class="sxs-lookup"><span data-stu-id="cc2d2-139">Code</span></span>

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
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingFolderResponseMessage ResponseClass="Error" 
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:MessageText>Either DataType or SharedFolderId must be specified, but not both.</m:MessageText>
      <m:ResponseCode>ErrorInvalidGetSharingFolderRequest</m:ResponseCode>
      <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
    </GetSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="cc2d2-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="cc2d2-140">See also</span></span>



[<span data-ttu-id="cc2d2-141">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="cc2d2-141">GetSharingFolder</span></span>](getsharingfolder.md)
  
[<span data-ttu-id="cc2d2-142">GetSharingFolderType</span><span class="sxs-lookup"><span data-stu-id="cc2d2-142">GetSharingFolderType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingFolderType.aspx)
  
[<span data-ttu-id="cc2d2-143">GetSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cc2d2-143">GetSharingFolderResponseMessage</span></span>](getsharingfolderresponsemessage.md)
  
[<span data-ttu-id="cc2d2-144">GetSharingFolderResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="cc2d2-144">GetSharingFolderResponseMessageType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingFolderResponseMessageType.aspx)


[<span data-ttu-id="cc2d2-145">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cc2d2-145">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="cc2d2-146">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="cc2d2-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

