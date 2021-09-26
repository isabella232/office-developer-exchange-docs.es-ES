---
title: Operación UpdateFolder
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UpdateFolder
api_type:
- schema
ms.assetid: 3494c996-b834-4813-b1ca-d99642d8b4e7
description: 'La operación UpdateFolder se usa para modificar las propiedades de un elemento existente en el Exchange almacén. Cada operación UpdateFolder consta de lo siguiente:'
ms.openlocfilehash: be8e39e13681cea34e312158c348c60a94374bec
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541766"
---
# <a name="updatefolder-operation"></a>Operación UpdateFolder

La operación UpdateFolder se usa para modificar las propiedades de un elemento existente en el Exchange almacén. Cada operación UpdateFolder consta de lo siguiente:
  
- Elemento [FolderId](folderid.md) que especifica una carpeta que se debe actualizar. 
    
- Una ruta de acceso interna de un elemento de la carpeta, como especifica la forma de la carpeta, que especifica los datos que se actualizarán.
    
- Carpeta que contiene el nuevo valor del campo actualizado, si la actualización no es una eliminación.
    
## <a name="remarks"></a>Comentarios

Se pueden realizar tres acciones básicas de actualización en un elemento. Estas acciones se enumeran en la tabla siguiente.
  
|**Action**|**Descripción**|
|:-----|:-----|
|Anexar  <br/> |La acción append agrega datos a una propiedad existente. Conserva los datos que hay actualmente. Append no es aplicable a todas las propiedades.  <br/> |
|Set  <br/> |La acción set reemplaza los datos de una propiedad si contiene datos o crea la propiedad y establece su valor si no existe. La acción set solo se aplica a las propiedades que se pueden escribir.  <br/> |
|Eliminar  <br/> |La acción eliminar quita una propiedad de una carpeta. Esto es diferente de establecerlo en un valor vacío. Cuando se completa, la propiedad no existe para la carpeta. Eliminar solo se aplica a las propiedades que se pueden escribir.  <br/> |
   
## <a name="updatefolder-request-example"></a>Ejemplo de solicitud UpdateFolder

### <a name="description"></a>Description

En el siguiente ejemplo de una solicitud UpdateFolder se muestra cómo actualizar un nombre para mostrar de carpeta. 
  
### <a name="code"></a>Código

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

### <a name="comments"></a>Comentarios

En este ejemplo se cambia el nombre para mostrar de la carpeta a NewFolderName.
  
> [!NOTE]
> Los valores de los **atributos Id** y **ChangeKey** del [elemento FolderId](folderid.md) se han acortado para mejorar la legibilidad. 
  
### <a name="request-elements"></a>Elementos Request

En la solicitud se usan los siguientes elementos:
  
- [UpdateFolder](updatefolder.md)
    
- [FolderChanges](folderchanges.md)
    
- [FolderChange](folderchange.md)
    
- [FolderId](folderid.md)
    
- [Updates (Carpeta)](updates-folder.md)
    
- [SetFolderField](setfolderfield.md)
    
- [FieldURI](fielduri.md)
    
- [Folder](folder.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
Consulte el esquema para ver los elementos adicionales que puede usar para formar una solicitud UpdateFolder.
  
> [!NOTE]
> La ubicación predeterminada del esquema se encuentra en el directorio virtual EWS del equipo que tiene instalado el rol de servidor Acceso de cliente. 
  
## <a name="updatefolder-response-example"></a>Ejemplo de respuesta UpdateFolder

### <a name="description"></a>Description

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud UpdateFolder. En este ejemplo, se devuelve la nueva clave de cambio para reflejar el estado actualizado de la carpeta.
  
### <a name="code"></a>Código

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

### <a name="comments"></a>Comentarios

> [!NOTE]
> El identificador de carpeta y la clave de cambio se han acortado para conservar la legibilidad. 
  
El identificador de carpeta que se devuelve en la respuesta representa la carpeta actualizada.
  
### <a name="successful-response-elements"></a>Elementos de respuesta correctos

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateFolderResponse](updatefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateFolderResponseMessage](updatefolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
## <a name="updatefolder-error-response-example"></a>Ejemplo de respuesta de error UpdateFolder

### <a name="description"></a>Description

En el siguiente ejemplo se muestra una respuesta de error a una solicitud UpdateFolder.
  
### <a name="code"></a>Código

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

### <a name="comments"></a>Comentarios

En este ejemplo se muestra una respuesta de error causada por un atributo **ChangeKey** no válido en la solicitud. 
  
### <a name="error-response-elements"></a>Elementos de respuesta de error

En la respuesta de error se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateFolderResponse](updatefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateFolderResponseMessage](updatefolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>Consulte también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

