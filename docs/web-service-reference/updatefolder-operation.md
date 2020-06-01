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
ms.openlocfilehash: fb894d9f42358b67f81e9fe8ae41ba61e6f46460
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467364"
---
# <a name="updatefolder-operation"></a><span data-ttu-id="562c8-104">Operación UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="562c8-104">UpdateFolder operation</span></span>

<span data-ttu-id="562c8-105">La operación UpdateFolder se usa para modificar las propiedades de un elemento existente en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="562c8-105">The UpdateFolder operation is used to modify properties of an existing item in the Exchange store.</span></span> <span data-ttu-id="562c8-106">Cada operación UpdateFolder consta de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="562c8-106">Each UpdateFolder operation consists of the following:</span></span>
  
- <span data-ttu-id="562c8-107">Un elemento [FolderId](folderid.md) que especifica la carpeta que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="562c8-107">A [FolderId](folderid.md) element that specifies a folder to update.</span></span> 
    
- <span data-ttu-id="562c8-108">Ruta de acceso interna de un elemento de la carpeta, como se especifica en la forma Folder, que especifica los datos que se van a actualizar.</span><span class="sxs-lookup"><span data-stu-id="562c8-108">An internal path of an element in the folder, as specified by the folder shape, which specifies the data to update.</span></span>
    
- <span data-ttu-id="562c8-109">Una carpeta que contiene el nuevo valor del campo actualizado, si la actualización no es una eliminación.</span><span class="sxs-lookup"><span data-stu-id="562c8-109">A folder that contains the new value of the updated field, if the update is not a deletion.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="562c8-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="562c8-110">Remarks</span></span>

<span data-ttu-id="562c8-111">Se pueden realizar tres acciones de actualización básicas en un elemento.</span><span class="sxs-lookup"><span data-stu-id="562c8-111">Three basic update actions can be performed on an item.</span></span> <span data-ttu-id="562c8-112">Estas acciones se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="562c8-112">These actions are listed in the following table.</span></span>
  
|<span data-ttu-id="562c8-113">**Action**</span><span class="sxs-lookup"><span data-stu-id="562c8-113">**Action**</span></span>|<span data-ttu-id="562c8-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="562c8-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="562c8-115">Anexar</span><span class="sxs-lookup"><span data-stu-id="562c8-115">Append</span></span>  <br/> |<span data-ttu-id="562c8-116">La acción Append agrega datos a una propiedad existente.</span><span class="sxs-lookup"><span data-stu-id="562c8-116">The append action adds data to an existing property.</span></span> <span data-ttu-id="562c8-117">Conserva los datos que hay actualmente.</span><span class="sxs-lookup"><span data-stu-id="562c8-117">It preserves the data that is currently there.</span></span> <span data-ttu-id="562c8-118">Append no es aplicable a todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="562c8-118">Append is not applicable to all properties.</span></span>  <br/> |
|<span data-ttu-id="562c8-119">Set</span><span class="sxs-lookup"><span data-stu-id="562c8-119">Set</span></span>  <br/> |<span data-ttu-id="562c8-120">La acción Set reemplaza los datos de una propiedad si contiene datos o crea la propiedad y establece su valor si no existe.</span><span class="sxs-lookup"><span data-stu-id="562c8-120">The set action replaces data for a property if it contains data, or creates the property and sets its value if it does not exist.</span></span> <span data-ttu-id="562c8-121">La acción Set solo es aplicable a las propiedades modificables.</span><span class="sxs-lookup"><span data-stu-id="562c8-121">The set action is only applicable to writable properties.</span></span>  <br/> |
|<span data-ttu-id="562c8-122">Eliminar</span><span class="sxs-lookup"><span data-stu-id="562c8-122">Delete</span></span>  <br/> |<span data-ttu-id="562c8-123">La acción eliminar quita una propiedad de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="562c8-123">The delete action removes a property from a folder.</span></span> <span data-ttu-id="562c8-124">No es lo mismo que establecerlo en un valor vacío.</span><span class="sxs-lookup"><span data-stu-id="562c8-124">This is different than setting it to an empty value.</span></span> <span data-ttu-id="562c8-125">Una vez completada, la propiedad no existe para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="562c8-125">When complete, the property does not exist for the folder.</span></span> <span data-ttu-id="562c8-126">Delete solo se aplica a propiedades modificables.</span><span class="sxs-lookup"><span data-stu-id="562c8-126">Delete is only applicable to writable properties.</span></span>  <br/> |
   
## <a name="updatefolder-request-example"></a><span data-ttu-id="562c8-127">Ejemplo de solicitud UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="562c8-127">UpdateFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="562c8-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="562c8-128">Description</span></span>

<span data-ttu-id="562c8-129">El siguiente ejemplo de una solicitud UpdateFolder muestra cómo actualizar un nombre para mostrar de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="562c8-129">The following example of an UpdateFolder request shows how to update a folder display name.</span></span> 
  
### <a name="code"></a><span data-ttu-id="562c8-130">Código</span><span class="sxs-lookup"><span data-stu-id="562c8-130">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="562c8-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="562c8-131">Comments</span></span>

<span data-ttu-id="562c8-132">En este ejemplo se cambia el nombre para mostrar de la carpeta a NewFolderName.</span><span class="sxs-lookup"><span data-stu-id="562c8-132">This example changes the display name of the folder to NewFolderName.</span></span>
  
> [!NOTE]
> <span data-ttu-id="562c8-133">Los valores de los atributos **ID** y **changekey** del elemento [FolderId](folderid.md) se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="562c8-133">The values of the **Id** and **ChangeKey** attributes of the [FolderId](folderid.md) element have been shortened for readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="562c8-134">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="562c8-134">Request elements</span></span>

<span data-ttu-id="562c8-135">Los siguientes elementos se usan en la solicitud:</span><span class="sxs-lookup"><span data-stu-id="562c8-135">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="562c8-136">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="562c8-136">UpdateFolder</span></span>](updatefolder.md)
    
- [<span data-ttu-id="562c8-137">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="562c8-137">FolderChanges</span></span>](folderchanges.md)
    
- [<span data-ttu-id="562c8-138">FolderChange</span><span class="sxs-lookup"><span data-stu-id="562c8-138">FolderChange</span></span>](folderchange.md)
    
- [<span data-ttu-id="562c8-139">FolderId</span><span class="sxs-lookup"><span data-stu-id="562c8-139">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="562c8-140">Updates (carpeta)</span><span class="sxs-lookup"><span data-stu-id="562c8-140">Updates (Folder)</span></span>](updates-folder.md)
    
- [<span data-ttu-id="562c8-141">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="562c8-141">SetFolderField</span></span>](setfolderfield.md)
    
- [<span data-ttu-id="562c8-142">FieldURI</span><span class="sxs-lookup"><span data-stu-id="562c8-142">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="562c8-143">Folder</span><span class="sxs-lookup"><span data-stu-id="562c8-143">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="562c8-144">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="562c8-144">DisplayName (string)</span></span>](displayname-string.md)
    
<span data-ttu-id="562c8-145">Vea el esquema para ver los elementos adicionales que puede usar para formar una solicitud de UpdateFolder.</span><span class="sxs-lookup"><span data-stu-id="562c8-145">See the schema for additional elements that you can use to form an UpdateFolder request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="562c8-146">La ubicación predeterminada del esquema está en el directorio virtual de EWS en el equipo que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="562c8-146">The default location of the schema is in the EWS virtual directory on the computer that has the Client Access server role installed.</span></span> 
  
## <a name="updatefolder-response-example"></a><span data-ttu-id="562c8-147">Ejemplo de respuesta UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="562c8-147">UpdateFolder response example</span></span>

### <a name="description"></a><span data-ttu-id="562c8-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="562c8-148">Description</span></span>

<span data-ttu-id="562c8-149">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud UpdateFolder.</span><span class="sxs-lookup"><span data-stu-id="562c8-149">The following example shows a successful response to the UpdateFolder request.</span></span> <span data-ttu-id="562c8-150">En este ejemplo, se devuelve la nueva clave de cambio para reflejar el estado actualizado de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="562c8-150">In this example, the new change key is returned to reflect the updated status of the folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="562c8-151">Código</span><span class="sxs-lookup"><span data-stu-id="562c8-151">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="562c8-152">Comentarios</span><span class="sxs-lookup"><span data-stu-id="562c8-152">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="562c8-153">El identificador de la carpeta y la clave de cambio se han abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="562c8-153">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="562c8-154">El identificador de carpeta que se devuelve en la respuesta representa la carpeta actualizada.</span><span class="sxs-lookup"><span data-stu-id="562c8-154">The folder ID that is returned in the response represents the updated folder.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="562c8-155">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="562c8-155">Successful response elements</span></span>

<span data-ttu-id="562c8-156">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="562c8-156">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="562c8-157">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="562c8-157">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="562c8-158">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="562c8-158">UpdateFolderResponse</span></span>](updatefolderresponse.md)
    
- [<span data-ttu-id="562c8-159">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="562c8-159">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="562c8-160">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="562c8-160">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
    
- [<span data-ttu-id="562c8-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="562c8-161">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="562c8-162">Folders</span><span class="sxs-lookup"><span data-stu-id="562c8-162">Folders</span></span>](folders-ex15websvcsotherref.md)
    
- [<span data-ttu-id="562c8-163">Folder</span><span class="sxs-lookup"><span data-stu-id="562c8-163">Folder</span></span>](folder.md)
    
- [<span data-ttu-id="562c8-164">FolderId</span><span class="sxs-lookup"><span data-stu-id="562c8-164">FolderId</span></span>](folderid.md)
    
## <a name="updatefolder-error-response-example"></a><span data-ttu-id="562c8-165">Ejemplo de respuesta de error UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="562c8-165">UpdateFolder Error response example</span></span>

### <a name="description"></a><span data-ttu-id="562c8-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="562c8-166">Description</span></span>

<span data-ttu-id="562c8-167">En el ejemplo siguiente se muestra una respuesta de error a una solicitud UpdateFolder.</span><span class="sxs-lookup"><span data-stu-id="562c8-167">The following example shows an error response to an UpdateFolder request.</span></span>
  
### <a name="code"></a><span data-ttu-id="562c8-168">Código</span><span class="sxs-lookup"><span data-stu-id="562c8-168">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="562c8-169">Comentarios</span><span class="sxs-lookup"><span data-stu-id="562c8-169">Comments</span></span>

<span data-ttu-id="562c8-170">En este ejemplo se muestra una respuesta de error causada por un atributo **changekey** no válido en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="562c8-170">This example shows an error response that is caused by an invalid **ChangeKey** attribute in the request.</span></span> 
  
### <a name="error-response-elements"></a><span data-ttu-id="562c8-171">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="562c8-171">Error response elements</span></span>

<span data-ttu-id="562c8-172">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="562c8-172">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="562c8-173">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="562c8-173">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="562c8-174">UpdateFolderResponse</span><span class="sxs-lookup"><span data-stu-id="562c8-174">UpdateFolderResponse</span></span>](updatefolderresponse.md)
    
- [<span data-ttu-id="562c8-175">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="562c8-175">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="562c8-176">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="562c8-176">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md)
    
- [<span data-ttu-id="562c8-177">MessageText</span><span class="sxs-lookup"><span data-stu-id="562c8-177">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="562c8-178">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="562c8-178">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="562c8-179">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="562c8-179">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="562c8-180">Folders</span><span class="sxs-lookup"><span data-stu-id="562c8-180">Folders</span></span>](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a><span data-ttu-id="562c8-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="562c8-181">See also</span></span>



- [<span data-ttu-id="562c8-182">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="562c8-182">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

