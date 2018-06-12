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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840812"
---
# <a name="updatefolder-operation"></a>Operación UpdateFolder

La operación UpdateFolder se usa para modificar las propiedades de un elemento existente en el almacén de Exchange. Cada operación UpdateFolder consta de lo siguiente:
  
- Un elemento de [FolderId](folderid.md) que especifica una carpeta que se debe actualizar. 
    
- Una ruta de acceso interno de un elemento en la carpeta, tal como se especifica por la forma de carpeta, que especifica los datos que se va a actualizar.
    
- Una carpeta que contiene el nuevo valor del campo actualizado, si la actualización no es una eliminación.
    
## <a name="remarks"></a>Notas

Tres acciones de actualización básica pueden realizarse en un elemento. Estas acciones se enumeran en la siguiente tabla.
  
|**Acción**|**Descripción**|
|:-----|:-----|
|Anexar  <br/> |La acción de datos anexados agrega datos a una propiedad existente. Conserva los datos que está actualmente allí. Anexar no es aplicable a todas las propiedades.  <br/> |
|Activado  <br/> |La acción de conjunto reemplaza los datos de una propiedad si contiene datos, o crea la propiedad y establece su valor, si no existe. La acción de conjunto sólo es aplicable a propiedades modificables.  <br/> |
|Eliminar  <br/> |La acción de eliminación quita una propiedad de una carpeta. Esto es diferente de si se establece en un valor vacío. Cuando haya terminado, la propiedad no existe para la carpeta. Eliminar solo es aplicable a las propiedades de escritura.  <br/> |
   
## <a name="updatefolder-request-example"></a>Ejemplo de solicitud UpdateFolder

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de UpdateFolder muestra cómo actualizar un nombre de carpeta para mostrar. 
  
### <a name="code"></a>Código

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

### <a name="comments"></a>Comentarios

En este ejemplo se cambia el nombre para mostrar de la carpeta a NewFolderName.
  
> [!NOTE]
> Los valores del **identificador** y **ChangeKey** atributos del elemento [FolderId](folderid.md) se han abreviado para mejorar la legibilidad. 
  
### <a name="request-elements"></a>Elementos de solicitud

En la solicitud se usan los siguientes elementos:
  
- [UpdateFolder](updatefolder.md)
    
- [FolderChanges](folderchanges.md)
    
- [FolderChange](folderchange.md)
    
- [FolderId](folderid.md)
    
- [Actualizaciones (elemento)](updates-item.md)
    
- [SetFolderField](setfolderfield.md)
    
- [FieldURI](fielduri.md)
    
- [Folder](folder.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
Consulte el esquema para los elementos adicionales que puede usar para crear una solicitud de UpdateFolder.
  
> [!NOTE]
> La ubicación predeterminada del esquema se encuentra en el directorio virtual de EWS en el equipo que tenga instalado el rol de servidor de acceso de cliente. 
  
## <a name="updatefolder-response-example"></a>Ejemplo de respuesta UpdateFolder

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de UpdateFolder. En este ejemplo, se devuelve la nueva clave de cambio para reflejar el estado actualizado de la carpeta.
  
### <a name="code"></a>Código

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

### <a name="comments"></a>Comentarios

> [!NOTE]
> El identificador de la carpeta y la clave de cambio se han abreviado para conservar la legibilidad. 
  
El identificador de la carpeta que se devuelve en la respuesta representa la carpeta actualizada.
  
### <a name="successful-response-elements"></a>Elementos de respuesta correcta

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateFolderResponse](updatefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateFolderResponseMessage](updatefolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Carpetas](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
## <a name="updatefolder-error-response-example"></a>Ejemplo de respuesta de UpdateFolder Error

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de UpdateFolder.
  
### <a name="code"></a>Código

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

### <a name="comments"></a>Comentarios

En este ejemplo se muestra una respuesta de error que está causada por un atributo **ChangeKey** no válido en la solicitud. 
  
### <a name="error-response-elements"></a>Elementos de respuesta de error

En la respuesta de error, se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateFolderResponse](updatefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateFolderResponseMessage](updatefolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Carpetas](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

