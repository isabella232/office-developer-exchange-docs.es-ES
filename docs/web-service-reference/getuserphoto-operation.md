---
title: Operación GetUserPhoto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e
description: Buscar información sobre la operación de EWS de GetUserPhoto.
ms.openlocfilehash: 6769842d31519f0aac2cf9bda10c1cab70558301
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461817"
---
# <a name="getuserphoto-operation"></a><span data-ttu-id="8f1f6-103">Operación GetUserPhoto</span><span class="sxs-lookup"><span data-stu-id="8f1f6-103">GetUserPhoto operation</span></span>

<span data-ttu-id="8f1f6-104">Buscar información sobre la operación de EWS de **GetUserPhoto** .</span><span class="sxs-lookup"><span data-stu-id="8f1f6-104">Find information about the **GetUserPhoto** EWS operation.</span></span> 
  
<span data-ttu-id="8f1f6-105">La operación **GetUserPhoto** obtiene una foto de usuario de los servicios de dominio de Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="8f1f6-105">The **GetUserPhoto** operation gets a user photo from Active Directory Domain Services (AD DS).</span></span> 
  
<span data-ttu-id="8f1f6-106">Esta operación se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8f1f6-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getuserphoto-operation"></a><span data-ttu-id="8f1f6-107">Uso de la operación GetUserPhoto</span><span class="sxs-lookup"><span data-stu-id="8f1f6-107">Using the GetUserPhoto operation</span></span>

<span data-ttu-id="8f1f6-108">La operación **RemoveContactFromImList** es una operación sencilla que acepta la dirección de correo electrónico de un usuario y el tamaño de la foto solicitada y devuelve la secuencia de fotos en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f1f6-108">The **RemoveContactFromImList** operation is a simple operation that accepts a user's email address and the requested photo size and returns the photo stream in the response.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8f1f6-109">EWS tiene una operación SOAP y basada en REST para obtener fotos de usuario.</span><span class="sxs-lookup"><span data-stu-id="8f1f6-109">EWS has both a SOAP and a REST-based operation to get user photos.</span></span> <span data-ttu-id="8f1f6-110">Para obtener información sobre la interfaz de REST, vea [obtener fotos de usuario mediante EWS en Exchange](https://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8f1f6-110">For information about the REST interface, see [Get user photos by using EWS in Exchange](https://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx).</span></span> 
  
### <a name="getuserphoto-operation-soap-headers"></a><span data-ttu-id="8f1f6-111">Encabezados SOAP de operación GetUserPhoto</span><span class="sxs-lookup"><span data-stu-id="8f1f6-111">GetUserPhoto operation SOAP headers</span></span>

<span data-ttu-id="8f1f6-112">La operación **GetUserPhoto** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8f1f6-112">The **GetUserPhoto** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="8f1f6-113">**Nombre de encabezado**</span><span class="sxs-lookup"><span data-stu-id="8f1f6-113">**Header name**</span></span>|<span data-ttu-id="8f1f6-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8f1f6-114">**Element**</span></span>|<span data-ttu-id="8f1f6-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8f1f6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8f1f6-116">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="8f1f6-116">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="8f1f6-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="8f1f6-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="8f1f6-118">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="8f1f6-118">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="8f1f6-119">Este encabezado se aplica a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f1f6-119">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="8f1f6-120">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="8f1f6-120">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="8f1f6-121">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8f1f6-121">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="8f1f6-122">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f1f6-122">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="8f1f6-123">Este encabezado se aplica a una respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f1f6-123">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getuserphoto-operation-request-example-get-a-users-photo"></a><span data-ttu-id="8f1f6-124">Ejemplo de solicitud de operación GetUserPhoto: obtener la foto de un usuario</span><span class="sxs-lookup"><span data-stu-id="8f1f6-124">GetUserPhoto operation request example: Get a user's photo</span></span>

<span data-ttu-id="8f1f6-125">El siguiente ejemplo de una solicitud de operación de **GetUserPhoto** muestra cómo obtener la foto de un usuario.</span><span class="sxs-lookup"><span data-stu-id="8f1f6-125">The following example of a **GetUserPhoto** operation request shows how to get a user's photo.</span></span> <span data-ttu-id="8f1f6-126">En este ejemplo se solicita una foto de usuario que es de 48x48 píxeles.</span><span class="sxs-lookup"><span data-stu-id="8f1f6-126">This example requests a user photo that is 48x48 pixels.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="8f1f6-127">Los siguientes elementos se usan en el cuerpo SOAP de la solicitud:</span><span class="sxs-lookup"><span data-stu-id="8f1f6-127">The following elements are used in the request SOAP body:</span></span>
  
- [<span data-ttu-id="8f1f6-128">GetUserPhoto</span><span class="sxs-lookup"><span data-stu-id="8f1f6-128">GetUserPhoto</span></span>](getuserphoto.md)
    
- [<span data-ttu-id="8f1f6-129">Email (cadena)</span><span class="sxs-lookup"><span data-stu-id="8f1f6-129">Email (String)</span></span>](email-string.md)
    
- [<span data-ttu-id="8f1f6-130">SizeRequested</span><span class="sxs-lookup"><span data-stu-id="8f1f6-130">SizeRequested</span></span>](sizerequested.md)
    
## <a name="successful-getuserphoto-operation-response"></a><span data-ttu-id="8f1f6-131">Respuesta de operación GetUserPhoto correcta</span><span class="sxs-lookup"><span data-stu-id="8f1f6-131">Successful GetUserPhoto operation response</span></span>

<span data-ttu-id="8f1f6-132">En el siguiente ejemplo se muestra una respuesta correcta a una operación **GetUserPhoto** para obtener la foto de un usuario.</span><span class="sxs-lookup"><span data-stu-id="8f1f6-132">The following example shows a successful response to a **GetUserPhoto** operation to get a user's photo.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetUserPhotoResponse ResponseClass="Success" 
                            xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <HasChanged>true</HasChanged>
         <PictureData>/9j/4AAQSkZJRgABAQEAYABgAAD/02</PictureData>
      </GetUserPhotoResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="8f1f6-133">Los siguientes elementos se usan en el cuerpo SOAP de la respuesta:</span><span class="sxs-lookup"><span data-stu-id="8f1f6-133">The following elements are used in the response SOAP body:</span></span>
  
- [<span data-ttu-id="8f1f6-134">GetUserPhotoResponse</span><span class="sxs-lookup"><span data-stu-id="8f1f6-134">GetUserPhotoResponse</span></span>](getuserphotoresponse.md)
    
- [<span data-ttu-id="8f1f6-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8f1f6-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8f1f6-136">HasChanged</span><span class="sxs-lookup"><span data-stu-id="8f1f6-136">HasChanged</span></span>](haschanged.md)
    
- [<span data-ttu-id="8f1f6-137">GetUserPhotoResponse</span><span class="sxs-lookup"><span data-stu-id="8f1f6-137">GetUserPhotoResponse</span></span>](getuserphotoresponse.md)
    
## <a name="getuserphoto-operation-error-response"></a><span data-ttu-id="8f1f6-138">Respuesta de error de operación de GetUserPhoto</span><span class="sxs-lookup"><span data-stu-id="8f1f6-138">GetUserPhoto operation error response</span></span>

<span data-ttu-id="8f1f6-139">El envoltorio SOAP no devolverá un código de error si se realiza un intento de obtener una foto de usuario para una dirección de correo electrónico que no existe en la organización.</span><span class="sxs-lookup"><span data-stu-id="8f1f6-139">The SOAP envelope will not return an error code if an attempt is made to get a user photo for an email address that doesn't exist in the organization.</span></span> <span data-ttu-id="8f1f6-140">Se devolverá un código de Estado HTTP 500 en la respuesta para indicar que la solicitud no se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8f1f6-140">A 500 HTTP status code will be returned in the response to indicate that the request was unsuccessful.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8f1f6-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f1f6-141">See also</span></span>

- [<span data-ttu-id="8f1f6-142">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8f1f6-142">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)   
- [<span data-ttu-id="8f1f6-143">Obtener fotos de usuario mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8f1f6-143">Get user photos by using EWS in Exchange</span></span>](https://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx)
    

