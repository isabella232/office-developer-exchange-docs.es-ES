---
title: FindFolder Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindFolder
api_type:
- schema
ms.assetid: 7a9855aa-06cc-45ba-ad2a-645c15b7d031
description: La operación FindFolder usa los servicios Web de Exchange para buscar las subcarpetas de una carpeta identificada y devuelve un conjunto de propiedades que describen el conjunto de subcarpetas.
ms.openlocfilehash: 655455b46d4a3192b294bee9d85352d95ded49ae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764618"
---
# <a name="findfolder-operation"></a><span data-ttu-id="ab12e-103">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="ab12e-103">FindFolder operation</span></span>

<span data-ttu-id="ab12e-104">La operación **FindFolder** usa los servicios Web de Exchange para buscar las subcarpetas de una carpeta identificada y devuelve un conjunto de propiedades que describen el conjunto de subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="ab12e-104">The **FindFolder** operation uses Exchange Web Services to find subfolders of an identified folder and returns a set of properties that describe the set of subfolders.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ab12e-105">Notas</span><span class="sxs-lookup"><span data-stu-id="ab12e-105">Remarks</span></span>

<span data-ttu-id="ab12e-106">FindFolder devuelve sólo el primer 512 bytes de cualquier propiedad que se pueden transmitir.</span><span class="sxs-lookup"><span data-stu-id="ab12e-106">FindFolder returns only the first 512 bytes of any streamable property.</span></span> <span data-ttu-id="ab12e-107">Para Unicode, devuelve los primeros 255 caracteres mediante el uso de una cadena Unicode terminada en null.</span><span class="sxs-lookup"><span data-stu-id="ab12e-107">For Unicode, it returns the first 255 characters by using a null-terminated Unicode string.</span></span>
  
<span data-ttu-id="ab12e-108">No se puede realizar consultas de recorrido profundo en las carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="ab12e-108">Deep traversal queries cannot be performed on public folders.</span></span>
  
<span data-ttu-id="ab12e-109">Las restricciones se permiten y deben usar sólo las propiedades de carpeta, no las propiedades del elemento.</span><span class="sxs-lookup"><span data-stu-id="ab12e-109">Restrictions are permitted and should use only the folder properties, not the item properties.</span></span> <span data-ttu-id="ab12e-110">Las funcionalidades de ordenación no está disponible para las respuestas **FindFolder** .</span><span class="sxs-lookup"><span data-stu-id="ab12e-110">Sorting functionality is not available for **FindFolder** responses.</span></span> <span data-ttu-id="ab12e-111">Las consultas agrupadas no están disponibles para las consultas de **FindFolder** .</span><span class="sxs-lookup"><span data-stu-id="ab12e-111">Grouped queries are not available for **FindFolder** queries.</span></span> 
  
 <span data-ttu-id="ab12e-112">**Nota** La operación **FindFolder** también se usa para buscar las carpetas administradas.</span><span class="sxs-lookup"><span data-stu-id="ab12e-112">**Note** The **FindFolder** operation is also used to find managed folders.</span></span> 
  
### <a name="soap-headers"></a><span data-ttu-id="ab12e-113">Encabezados SOAP</span><span class="sxs-lookup"><span data-stu-id="ab12e-113">SOAP Headers</span></span>

<span data-ttu-id="ab12e-114">La operación **FindFolder** puede usar los encabezados SOAP que se enumeran y describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab12e-114">The **FindFolder** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="ab12e-115">**Header**</span><span class="sxs-lookup"><span data-stu-id="ab12e-115">**Header**</span></span>|<span data-ttu-id="ab12e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="ab12e-116">**Element**</span></span>|<span data-ttu-id="ab12e-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab12e-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ab12e-118">Suplantación</span><span class="sxs-lookup"><span data-stu-id="ab12e-118">Impersonation</span></span>  <br/> |[<span data-ttu-id="ab12e-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="ab12e-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="ab12e-120">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="ab12e-120">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="ab12e-121">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="ab12e-121">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="ab12e-122">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="ab12e-122">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="ab12e-123">Identifica la referencia cultural de RFC3066 va a usar para tener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="ab12e-123">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="ab12e-124">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="ab12e-124">RequestVersion</span></span>  <br/> |[<span data-ttu-id="ab12e-125">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="ab12e-125">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="ab12e-126">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="ab12e-126">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="ab12e-127">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="ab12e-127">ServerVersion</span></span>  <br/> |[<span data-ttu-id="ab12e-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ab12e-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="ab12e-129">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ab12e-129">Identifies the version of the server that responded to the request.</span></span>  <br/> |
|<span data-ttu-id="ab12e-130">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="ab12e-130">TimeZoneContext</span></span>  <br/> |[<span data-ttu-id="ab12e-131">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="ab12e-131">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="ab12e-132">Identifica la zona horaria que se usará para todas las respuestas desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="ab12e-132">Identifies the time zone to be used for all responses from the server.</span></span>  <br/> |
   
## <a name="findfolder-request-example"></a><span data-ttu-id="ab12e-133">Ejemplo de solicitud FindFolder</span><span class="sxs-lookup"><span data-stu-id="ab12e-133">FindFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="ab12e-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab12e-134">Description</span></span>

<span data-ttu-id="ab12e-135">El siguiente ejemplo de una solicitud de **FindFolder** muestra cómo formar una solicitud para buscar todas las carpetas que se encuentra en una bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="ab12e-135">The following example of a **FindFolder** request shows how to form a request to find all the folders located in an Inbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ab12e-136">Código</span><span class="sxs-lookup"><span data-stu-id="ab12e-136">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="ab12e-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ab12e-137">Comments</span></span>

<span data-ttu-id="ab12e-138">Usa el valor predeterminado para el [BaseShape](baseshape.md), la respuesta que devuelve el nombre de la carpeta, el identificador de la carpeta, el número de subcarpetas, el número de carpetas secundarias que se encuentran en la carpeta y el recuento de elementos no leídos.</span><span class="sxs-lookup"><span data-stu-id="ab12e-138">Using the Default value for the [BaseShape](baseshape.md), the response returns the folder name, the folder ID, the number of subfolders, the number of child folders found in the folder, and the count of unread items.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="ab12e-139">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="ab12e-139">Request elements</span></span>

<span data-ttu-id="ab12e-140">Esta solicitud **FindFolder** incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ab12e-140">This **FindFolder** request includes the following elements:</span></span> 
  
- [<span data-ttu-id="ab12e-141">FindFolder</span><span class="sxs-lookup"><span data-stu-id="ab12e-141">FindFolder</span></span>](findfolder.md)
    
- [<span data-ttu-id="ab12e-142">FolderShape</span><span class="sxs-lookup"><span data-stu-id="ab12e-142">FolderShape</span></span>](foldershape.md)
    
- [<span data-ttu-id="ab12e-143">BaseShape</span><span class="sxs-lookup"><span data-stu-id="ab12e-143">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="ab12e-144">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="ab12e-144">ParentFolderIds</span></span>](parentfolderids.md)
    
- [<span data-ttu-id="ab12e-145">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="ab12e-145">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
 <span data-ttu-id="ab12e-146">Para los elementos de solicitud **FindFolder** adicionales, vea el esquema.</span><span class="sxs-lookup"><span data-stu-id="ab12e-146">For additional **FindFolder** request elements, see the schema.</span></span> 
  
## <a name="findfolder-response-example"></a><span data-ttu-id="ab12e-147">Ejemplo de respuesta FindFolder</span><span class="sxs-lookup"><span data-stu-id="ab12e-147">FindFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="ab12e-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab12e-148">Description</span></span>

<span data-ttu-id="ab12e-149">El siguiente ejemplo de cuerpo de SOAP Simple Object Access Protocol () muestra una respuesta correcta a la solicitud de **FindFolder** .</span><span class="sxs-lookup"><span data-stu-id="ab12e-149">The following Simple Object Access Protocol (SOAP) body example shows a successful response to the **FindFolder** request.</span></span> <span data-ttu-id="ab12e-150">La respuesta contiene los elementos que se devuelven cuando se usa el valor predeterminado para la [BaseShape](baseshape.md) .</span><span class="sxs-lookup"><span data-stu-id="ab12e-150">The response contains the elements that are returned when the Default value for the [BaseShape](baseshape.md) is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ab12e-151">El identificador de la carpeta y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="ab12e-151">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ab12e-152">Código</span><span class="sxs-lookup"><span data-stu-id="ab12e-152">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Folders>
              <t:Folder>
                <t:FolderId Id="AQAnAH" ChangeKey="AQAAABY" />
                <t:DisplayName>TestFolder</t:DisplayName>
                <t:TotalCount>0</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </FindFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="ab12e-153">Elementos de respuesta</span><span class="sxs-lookup"><span data-stu-id="ab12e-153">Response elements</span></span>

<span data-ttu-id="ab12e-154">Las propiedades que se devuelven en la respuesta se determinan mediante el [BaseShape](baseshape.md) y el [AdditionalProperties](additionalproperties.md) si se usan.</span><span class="sxs-lookup"><span data-stu-id="ab12e-154">The properties that are returned in the response are determined by the [BaseShape](baseshape.md) and the [AdditionalProperties](additionalproperties.md) if they are used.</span></span> <span data-ttu-id="ab12e-155">Una respuesta correcta de **FindFolder** incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ab12e-155">A successful **FindFolder** response includes the following elements:</span></span> 
  
- [<span data-ttu-id="ab12e-156">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ab12e-156">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="ab12e-157">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="ab12e-157">FindFolderResponse</span></span>](findfolderresponse.md)
    
- [<span data-ttu-id="ab12e-158">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ab12e-158">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ab12e-159">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ab12e-159">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md)
    
- [<span data-ttu-id="ab12e-160">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ab12e-160">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ab12e-161">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="ab12e-161">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
    
- [<span data-ttu-id="ab12e-162">Carpetas</span><span class="sxs-lookup"><span data-stu-id="ab12e-162">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="ab12e-163">Folder</span><span class="sxs-lookup"><span data-stu-id="ab12e-163">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="ab12e-164">FolderId</span><span class="sxs-lookup"><span data-stu-id="ab12e-164">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="ab12e-165">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="ab12e-165">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="ab12e-166">TotalCount</span><span class="sxs-lookup"><span data-stu-id="ab12e-166">TotalCount</span></span>](totalcount.md)
    
- [<span data-ttu-id="ab12e-167">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="ab12e-167">ChildFolderCount</span></span>](childfoldercount.md)
    
- [<span data-ttu-id="ab12e-168">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="ab12e-168">UnreadCount</span></span>](unreadcount.md)
    
### <a name="comments"></a><span data-ttu-id="ab12e-169">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ab12e-169">Comments</span></span>

 <span data-ttu-id="ab12e-170">**FindFolder** respuestas a una solicitud con la forma de respuesta **AllProperties** no devolverá el [TotalCount](totalcount.md) y los elementos de [UnreadCount](unreadcount.md) para las búsquedas de la carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="ab12e-170">**FindFolder** responses to a request with the **AllProperties** response shape will not return the [TotalCount](totalcount.md) and [UnreadCount](unreadcount.md) elements for public folder searches.</span></span> 
  
## <a name="findfolder-error-response-example"></a><span data-ttu-id="ab12e-171">Ejemplo de respuesta de FindFolder Error</span><span class="sxs-lookup"><span data-stu-id="ab12e-171">FindFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="ab12e-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab12e-172">Description</span></span>

<span data-ttu-id="ab12e-173">El siguiente ejemplo de cuerpo SOAP muestra una respuesta de error que se produce cuando se busca una carpeta que se identifica con un identificador de la carpeta con formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="ab12e-173">The following SOAP body example shows an error response that occurs when you search for a folder that is identified by a malformed folder identifier.</span></span>
  
### <a name="code"></a><span data-ttu-id="ab12e-174">Código</span><span class="sxs-lookup"><span data-stu-id="ab12e-174">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </FindFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="ab12e-175">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="ab12e-175">Error response elements</span></span>

<span data-ttu-id="ab12e-176">La respuesta de error **FindFolder** incluye los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ab12e-176">The **FindFolder** error response includes the following elements:</span></span> 
  
- [<span data-ttu-id="ab12e-177">FindFolderResponse</span><span class="sxs-lookup"><span data-stu-id="ab12e-177">FindFolderResponse</span></span>](findfolderresponse.md)
    
- [<span data-ttu-id="ab12e-178">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ab12e-178">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ab12e-179">MessageText</span><span class="sxs-lookup"><span data-stu-id="ab12e-179">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="ab12e-180">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ab12e-180">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ab12e-181">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ab12e-181">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="additional-information"></a><span data-ttu-id="ab12e-182">Información adicional</span><span class="sxs-lookup"><span data-stu-id="ab12e-182">Additional Information</span></span>

- <span data-ttu-id="ab12e-183">El elemento [DisplayName (string)](displayname-string.md) de carpeta siempre se incluye en la forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ab12e-183">The folder [DisplayName (string)](displayname-string.md) element is always included in the default shape.</span></span> 
    
- <span data-ttu-id="ab12e-184">El elemento [UnreadCount](unreadcount.md) está incluido en las carpetas de tareas y notas.</span><span class="sxs-lookup"><span data-stu-id="ab12e-184">The [UnreadCount](unreadcount.md) element is included in Tasks and Notes folders.</span></span> 
    
- <span data-ttu-id="ab12e-185">Use el valor de **PropertyTag** de 0x672D con un tipo de propiedad de **entero** para identificar una carpeta administrada mediante el elemento [ExtendedFieldURI](extendedfielduri.md) .</span><span class="sxs-lookup"><span data-stu-id="ab12e-185">Use the **PropertyTag** value of 0x672D with a property type of **Integer** to identify a managed folder by using the [ExtendedFieldURI](extendedfielduri.md) element.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ab12e-186">Ver también</span><span class="sxs-lookup"><span data-stu-id="ab12e-186">See also</span></span>



[<span data-ttu-id="ab12e-187">Buscar carpetas</span><span class="sxs-lookup"><span data-stu-id="ab12e-187">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

