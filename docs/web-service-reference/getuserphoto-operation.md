---
title: Operación GetUserPhoto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e
description: Busque información sobre la EWS GetUserPhoto operación.
ms.openlocfilehash: 4465ac7115d96f5b6ef39e467663c9bf1c70e99e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835694"
---
# <a name="getuserphoto-operation"></a><span data-ttu-id="ce2f0-103">Operación GetUserPhoto</span><span class="sxs-lookup"><span data-stu-id="ce2f0-103">GetUserPhoto operation</span></span>

<span data-ttu-id="ce2f0-104">Obtenga información acerca de la operación de EWS **GetUserPhoto** .</span><span class="sxs-lookup"><span data-stu-id="ce2f0-104">Find information about the **GetUserPhoto** EWS operation.</span></span> 
  
<span data-ttu-id="ce2f0-105">La operación **GetUserPhoto** Obtiene una foto de usuario de servicios de dominio de Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="ce2f0-105">The **GetUserPhoto** operation gets a user photo from Active Directory Domain Services (AD DS).</span></span> 
  
<span data-ttu-id="ce2f0-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ce2f0-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getuserphoto-operation"></a><span data-ttu-id="ce2f0-107">Mediante la operación GetUserPhoto</span><span class="sxs-lookup"><span data-stu-id="ce2f0-107">Using the GetUserPhoto operation</span></span>

<span data-ttu-id="ce2f0-108">La operación de **RemoveContactFromImList** es una operación sencilla que acepta la dirección de correo electrónico de un usuario y el tamaño de la foto solicitado y devuelve la secuencia de fotografías en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce2f0-108">The **RemoveContactFromImList** operation is a simple operation that accepts a user's email address and the requested photo size and returns the photo stream in the response.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ce2f0-109">EWS tiene un SOAP y una operación basada en REST para obtener fotos de usuario.</span><span class="sxs-lookup"><span data-stu-id="ce2f0-109">EWS has both a SOAP and a REST-based operation to get user photos.</span></span> <span data-ttu-id="ce2f0-110">Para obtener información acerca de la interfaz REST, vea [obtener fotos de usuario mediante el uso de EWS en Exchange](http://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ce2f0-110">For information about the REST interface, see [Get user photos by using EWS in Exchange](http://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx).</span></span> 
  
### <a name="getuserphoto-operation-soap-headers"></a><span data-ttu-id="ce2f0-111">Encabezados SOAP de operación de GetUserPhoto</span><span class="sxs-lookup"><span data-stu-id="ce2f0-111">GetUserPhoto operation SOAP headers</span></span>

<span data-ttu-id="ce2f0-112">La operación de **GetUserPhoto** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ce2f0-112">The **GetUserPhoto** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="ce2f0-113">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="ce2f0-113">**Header name**</span></span>|<span data-ttu-id="ce2f0-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="ce2f0-114">**Element**</span></span>|<span data-ttu-id="ce2f0-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce2f0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ce2f0-116">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="ce2f0-116">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="ce2f0-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="ce2f0-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="ce2f0-118">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="ce2f0-118">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="ce2f0-119">Este encabezado es aplicable a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce2f0-119">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ce2f0-120">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="ce2f0-120">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="ce2f0-121">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ce2f0-121">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="ce2f0-122">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce2f0-122">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="ce2f0-123">Este encabezado es aplicable a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce2f0-123">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getuserphoto-operation-request-example-get-a-users-photo"></a><span data-ttu-id="ce2f0-124">Ejemplo de solicitud de operación de GetUserPhoto: obtener fotos de un usuario</span><span class="sxs-lookup"><span data-stu-id="ce2f0-124">GetUserPhoto operation request example: Get a user's photo</span></span>

<span data-ttu-id="ce2f0-125">El siguiente ejemplo de una solicitud de operación **GetUserPhoto** muestra cómo obtener la foto de un usuario.</span><span class="sxs-lookup"><span data-stu-id="ce2f0-125">The following example of a **GetUserPhoto** operation request shows how to get a user's photo.</span></span> <span data-ttu-id="ce2f0-126">En este ejemplo se solicita una foto de usuario que es de 48 x 48 píxeles.</span><span class="sxs-lookup"><span data-stu-id="ce2f0-126">This example requests a user photo that is 48x48 pixels.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013"/>
   </soap:Header>
   <soap:Body>
      <m:GetUserPhoto>
         <m:Email>user1@contoso.com</m:Email>
         <m:SizeRequested>HR48x48</m:SizeRequested>
      </m:GetUserPhoto>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="ce2f0-127">En la solicitud SOAP body, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ce2f0-127">The following elements are used in the request SOAP body:</span></span>
  
- [<span data-ttu-id="ce2f0-128">GetUserPhoto</span><span class="sxs-lookup"><span data-stu-id="ce2f0-128">GetUserPhoto</span></span>](getuserphoto.md)
    
- [<span data-ttu-id="ce2f0-129">Correo electrónico (cadena)</span><span class="sxs-lookup"><span data-stu-id="ce2f0-129">Email (String)</span></span>](email-string.md)
    
- [<span data-ttu-id="ce2f0-130">SizeRequested</span><span class="sxs-lookup"><span data-stu-id="ce2f0-130">SizeRequested</span></span>](sizerequested.md)
    
## <a name="successful-getuserphoto-operation-response"></a><span data-ttu-id="ce2f0-131">Respuesta es correcta de operación GetUserPhoto</span><span class="sxs-lookup"><span data-stu-id="ce2f0-131">Successful GetUserPhoto operation response</span></span>

<span data-ttu-id="ce2f0-132">En el ejemplo siguiente se muestra una respuesta correcta a una operación de **GetUserPhoto** para obtener fotos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="ce2f0-132">The following example shows a successful response to a **GetUserPhoto** operation to get a user's photo.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetUserPhotoResponse ResponseClass="Success" 
                            xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <HasChanged>true</HasChanged>
         <PictureData>/9j/4AAQSkZJRgABAQEAYABgAAD/02</PictureData>
      </GetUserPhotoResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="ce2f0-133">En la respuesta SOAP body, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ce2f0-133">The following elements are used in the response SOAP body:</span></span>
  
- [<span data-ttu-id="ce2f0-134">GetUserPhotoResponse</span><span class="sxs-lookup"><span data-stu-id="ce2f0-134">GetUserPhotoResponse</span></span>](getuserphotoresponse.md)
    
- [<span data-ttu-id="ce2f0-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ce2f0-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ce2f0-136">HasChanged</span><span class="sxs-lookup"><span data-stu-id="ce2f0-136">HasChanged</span></span>](haschanged.md)
    
- [<span data-ttu-id="ce2f0-137">GetUserPhotoResponse</span><span class="sxs-lookup"><span data-stu-id="ce2f0-137">GetUserPhotoResponse</span></span>](getuserphotoresponse.md)
    
## <a name="getuserphoto-operation-error-response"></a><span data-ttu-id="ce2f0-138">Respuesta de error de la operación de GetUserPhoto</span><span class="sxs-lookup"><span data-stu-id="ce2f0-138">GetUserPhoto operation error response</span></span>

<span data-ttu-id="ce2f0-139">El elemento envelope de SOAP no devolverá un código de error si intenta obtener una foto de usuario para una dirección de correo electrónico que no existe en la organización.</span><span class="sxs-lookup"><span data-stu-id="ce2f0-139">The SOAP envelope will not return an error code if an attempt is made to get a user photo for an email address that doesn't exist in the organization.</span></span> <span data-ttu-id="ce2f0-140">Se devuelve un código de estado HTTP 500 en la respuesta para indicar que la solicitud se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ce2f0-140">A 500 HTTP status code will be returned in the response to indicate that the request was unsuccessful.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ce2f0-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="ce2f0-141">See also</span></span>

- [<span data-ttu-id="ce2f0-142">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ce2f0-142">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)   
- [<span data-ttu-id="ce2f0-143">Obtener fotografías de usuario mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ce2f0-143">Get user photos by using EWS in Exchange</span></span>](http://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx)
    
