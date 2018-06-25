---
title: Operación UpdateFolder
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateFolder
api_type:
- schema
ms.assetid: 3494c996-b834-4813-b1ca-d99642d8b4e7
description: 'La operación UpdateFolder se usa para modificar las propiedades de un elemento existente en el almacén de Exchange. Cada operación UpdateFolder consta de lo siguiente:'
ms.openlocfilehash: b33937bb09f0dcbe3d3ed61bbf5233423f320d9c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840812"
---
# <a name="updatefolder-operation"></a><span data-ttu-id="faba1-104">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="faba1-104">UpdateFolder operation</span></span>

<span data-ttu-id="faba1-105">La operación UpdateFolder se usa para modificar las propiedades de un elemento existente en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="faba1-105">The UpdateFolder operation is used to modify properties of an existing item in the Exchange store.</span></span> <span data-ttu-id="faba1-106">Cada operación UpdateFolder consta de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="faba1-106">Each UpdateFolder operation consists of the following:</span></span>
  
- <span data-ttu-id="faba1-107">Un elemento de [FolderId](folderid.md) que especifica una carpeta que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="faba1-107">A [FolderId](folderid.md) element that specifies a folder to update.</span></span> 
    
- <span data-ttu-id="faba1-108">Una ruta de acceso interno de un elemento en la carpeta, tal como se especifica por la forma de carpeta, que especifica los datos que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="faba1-108">An internal path of an element in the folder, as specified by the folder shape, which specifies the data to update.</span></span>
    
- <span data-ttu-id="faba1-109">Una carpeta que contiene el nuevo valor del campo actualizado, si la actualización no es una eliminación.</span><span class="sxs-lookup"><span data-stu-id="faba1-109">A folder that contains the new value of the updated field, if the update is not a deletion.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="faba1-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="faba1-110">Remarks</span></span>

<span data-ttu-id="faba1-111">Tres acciones de actualización básica pueden realizarse en un elemento.</span><span class="sxs-lookup"><span data-stu-id="faba1-111">Three basic update actions can be performed on an item.</span></span> <span data-ttu-id="faba1-112">Estas acciones se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="faba1-112">These actions are listed in the following table.</span></span>
  
|<span data-ttu-id="faba1-113">**Acción**</span><span class="sxs-lookup"><span data-stu-id="faba1-113">**Action**</span></span>|<span data-ttu-id="faba1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="faba1-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="faba1-115">Anexar</span><span class="sxs-lookup"><span data-stu-id="faba1-115">Append</span></span>  <br/> |<span data-ttu-id="faba1-116">La acción de datos anexados agrega datos a una propiedad existente.</span><span class="sxs-lookup"><span data-stu-id="faba1-116">The append action adds data to an existing property.</span></span> <span data-ttu-id="faba1-117">Conserva los datos que está actualmente allí.</span><span class="sxs-lookup"><span data-stu-id="faba1-117">It preserves the data that is currently there.</span></span> <span data-ttu-id="faba1-118">Anexar no es aplicable a todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="faba1-118">Append is not applicable to all properties.</span></span>  <br/> |
|<span data-ttu-id="faba1-119">Activado</span><span class="sxs-lookup"><span data-stu-id="faba1-119">Set</span></span>  <br/> |<span data-ttu-id="faba1-120">La acción de conjunto reemplaza los datos de una propiedad si contiene datos, o crea la propiedad y establece su valor, si no existe.</span><span class="sxs-lookup"><span data-stu-id="faba1-120">The set action replaces data for a property if it contains data, or creates the property and sets its value if it does not exist.</span></span> <span data-ttu-id="faba1-121">La acción de conjunto sólo es aplicable a propiedades modificables.</span><span class="sxs-lookup"><span data-stu-id="faba1-121">The set action is only applicable to writable properties.</span></span>  <br/> |
|<span data-ttu-id="faba1-122">Eliminar</span><span class="sxs-lookup"><span data-stu-id="faba1-122">Delete</span></span>  <br/> |<span data-ttu-id="faba1-123">La acción de eliminación quita una propiedad de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="faba1-123">The delete action removes a property from a folder.</span></span> <span data-ttu-id="faba1-124">Esto es diferente de si se establece en un valor vacío.</span><span class="sxs-lookup"><span data-stu-id="faba1-124">This is different than setting it to an empty value.</span></span> <span data-ttu-id="faba1-125">Cuando haya terminado, la propiedad no existe para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="faba1-125">When complete, the property does not exist for the folder.</span></span> <span data-ttu-id="faba1-126">Eliminar solo es aplicable a las propiedades de escritura.</span><span class="sxs-lookup"><span data-stu-id="faba1-126">Delete is only applicable to writable properties.</span></span>  <br/> |
   
## <a name="updatefolder-request-example"></a><span data-ttu-id="faba1-127">Ejemplo de solicitud UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="faba1-127">UpdateFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="faba1-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="faba1-128">Description</span></span>

<span data-ttu-id="faba1-129">El siguiente ejemplo de una solicitud de UpdateFolder muestra cómo actualizar un nombre de carpeta para mostrar.</span><span class="sxs-lookup"><span data-stu-id="faba1-129">The following example of an UpdateFolder request shows how to update a folder display name.</span></span> 
  
### <a name="code"></a><span data-ttu-id="faba1-130">Código</span><span class="sxs-lookup"><span data-stu-id="faba1-130">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="AScA" ChangeKey="GO3u/"/>
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:DisplayName"/>
              <t:Folder>
                <t:DisplayName>NewFolderName</t:DisplayName>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </FolderChanges>
    </UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="faba1-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="faba1-131">Comments</span></span>

<span data-ttu-id="faba1-132">En este ejemplo se cambia el nombre para mostrar de la carpeta a NewFolderName.</span><span class="sxs-lookup"><span data-stu-id="faba1-132">This example changes the display name of the folder to NewFolderName.</span></span>
  
> [!NOTE]
> <span data-ttu-id="faba1-133">Los valores del **identificador** y **ChangeKey** atributos del elemento [FolderId](folderid.md) se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="faba1-133">The values of the **Id** and **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="faba1-134">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="faba1-134">Request elements</span></span>

<span data-ttu-id="faba1-135">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="faba1-135">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="faba1-136">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="faba1-136">UpdateFolder</span></span>](updatefolder.md)
    
- [<span data-ttu-id="faba1-137">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="faba1-137">FolderChanges</span></span>](folderchanges.md)
    
- [<span data-ttu-id="faba1-138">FolderChange</span><span class="sxs-lookup"><span data-stu-id="faba1-138">FolderChange</span></span>](folderchange.md)
    
- [<span data-ttu-id="faba1-139">FolderId</span><span class="sxs-lookup"><span data-stu-id="faba1-139">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="faba1-140">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="faba1-140">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="faba1-141">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="faba1-141">SetFolderField</span></span>](setfolderfield.md)
    
- [<span data-ttu-id="faba1-142">FieldURI</span><span class="sxs-lookup"><span data-stu-id="faba1-142">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="faba1-143">Folder</span><span class="sxs-lookup"><span data-stu-id="faba1-143">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="faba1-144">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="faba1-144">DisplayName (string)</span></span>](displayname-string.md)
    
<span data-ttu-id="faba1-145">Consulte el esquema para los elementos adicionales que puede usar para crear una solicitud de UpdateFolder.</span><span class="sxs-lookup"><span data-stu-id="faba1-145">See the schema for additional elements that you can use to form an UpdateFolder request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="faba1-146">La ubicación predeterminada del esquema se encuentra en el directorio virtual de EWS en el equipo que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="faba1-146">The default location of the schema is in the EWS virtual directory on the computer that has the Client Access server role installed.</span></span> 
  
## <a name="updatefolder-response-example"></a><span data-ttu-id="faba1-147">Ejemplo de respuesta UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="faba1-147">UpdateFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="faba1-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="faba1-148">Description</span></span>

<span data-ttu-id="faba1-149">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de UpdateFolder.</span><span class="sxs-lookup"><span data-stu-id="faba1-149">The following example shows a successful response to the UpdateFolder request.</span></span> <span data-ttu-id="faba1-150">En este ejemplo, se devuelve la nueva clave de cambio para reflejar el estado actualizado de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="faba1-150">In this example, the new change key is returned to reflect the updated status of the folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="faba1-151">Código</span><span class="sxs-lookup"><span data-stu-id="faba1-151">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AAAlAFVz" ChangeKey="AQAAAB" />
            </t:Folder>
          </m:Folders>
        </m:UpdateFolderResponseMessage>
      </m:ResponseMessages>
    </UpdateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="faba1-152">Comentarios</span><span class="sxs-lookup"><span data-stu-id="faba1-152">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="faba1-153">El identificador de la carpeta y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="faba1-153">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="faba1-154">El identificador de la carpeta que se devuelve en la respuesta representa la carpeta actualizada.</span><span class="sxs-lookup"><span data-stu-id="faba1-154">The folder ID that is returned in the response represents the updated folder.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="faba1-155">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="faba1-155">Successful response elements</span></span>

<span data-ttu-id="faba1-156">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="faba1-156">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="faba1-157">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="faba1-157">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="faba1-158">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="faba1-158">UpdateFolderResponse</span></span>](updatefolderresponse.md)
    
- [<span data-ttu-id="faba1-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="faba1-159">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="faba1-160">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="faba1-160">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
    
- [<span data-ttu-id="faba1-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="faba1-161">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="faba1-162">Carpetas</span><span class="sxs-lookup"><span data-stu-id="faba1-162">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="faba1-163">Folder</span><span class="sxs-lookup"><span data-stu-id="faba1-163">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="faba1-164">FolderId</span><span class="sxs-lookup"><span data-stu-id="faba1-164">FolderId</span></span>](folderid.md)
    
## <a name="updatefolder-error-response-example"></a><span data-ttu-id="faba1-165">Ejemplo de respuesta de UpdateFolder Error</span><span class="sxs-lookup"><span data-stu-id="faba1-165">UpdateFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="faba1-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="faba1-166">Description</span></span>

<span data-ttu-id="faba1-167">En el ejemplo siguiente se muestra una respuesta de error a una solicitud de UpdateFolder.</span><span class="sxs-lookup"><span data-stu-id="faba1-167">The following example shows an error response to an UpdateFolder request.</span></span>
  
### <a name="code"></a><span data-ttu-id="faba1-168">Código</span><span class="sxs-lookup"><span data-stu-id="faba1-168">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateFolderResponseMessage ResponseClass="Error">
          <m:MessageText>The change key is invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidChangeKey</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:UpdateFolderResponseMessage>
      </m:ResponseMessages>
    </UpdateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="faba1-169">Comentarios</span><span class="sxs-lookup"><span data-stu-id="faba1-169">Comments</span></span>

<span data-ttu-id="faba1-170">En este ejemplo se muestra una respuesta de error que está causada por un atributo **ChangeKey** no válido en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="faba1-170">This example shows an error response that is caused by an invalid **ChangeKey** attribute in the request.</span></span> 
  
### <a name="error-response-elements"></a><span data-ttu-id="faba1-171">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="faba1-171">Error response elements</span></span>

<span data-ttu-id="faba1-172">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="faba1-172">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="faba1-173">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="faba1-173">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="faba1-174">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="faba1-174">UpdateFolderResponse</span></span>](updatefolderresponse.md)
    
- [<span data-ttu-id="faba1-175">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="faba1-175">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="faba1-176">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="faba1-176">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
    
- [<span data-ttu-id="faba1-177">MessageText</span><span class="sxs-lookup"><span data-stu-id="faba1-177">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="faba1-178">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="faba1-178">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="faba1-179">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="faba1-179">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="faba1-180">Carpetas</span><span class="sxs-lookup"><span data-stu-id="faba1-180">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="faba1-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="faba1-181">See also</span></span>



- [<span data-ttu-id="faba1-182">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="faba1-182">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

