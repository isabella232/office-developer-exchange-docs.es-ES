---
title: Operación CopyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CopyFolder
api_type:
- schema
ms.assetid: c7ea0d68-9793-4144-b378-d99536776db9
description: La operación CopyFolder copia carpetas de un buzón.
ms.openlocfilehash: 7bfe9c85f3782f751e23b79afe193c9369a4720c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510345"
---
# <a name="copyfolder-operation"></a>Operación CopyFolder

La operación CopyFolder copia carpetas de un buzón.
  
## <a name="using-the-copyfolder-operation"></a>Uso de la operación CopyFolder

La operación CopyFolder es similar a la [operación MoveFolder](movefolder-operation.md). Copia las carpetas identificadas y devuelve el **identificador** **y changekey** de las carpetas copiadas. 
  
## <a name="copyfolder-request-example"></a>Ejemplo de solicitud CopyFolder

### <a name="description"></a>Descripción

En el siguiente ejemplo de una solicitud CopyFolder se muestra cómo copiar carpetas en la carpeta Bandeja de entrada.
  
> [!NOTE]
> El valor del atributo **Id** del [elemento FolderId](folderid.md) se ha acortado para su legibilidad. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CopyFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ToFolderId>
        <t:DistinguishedFolderId Id="inbox"/>
      </ToFolderId>
      <FolderIds>
        <t:FolderId Id="AS4A=" ChangeKey="fsVU4=="/>
        <t:FolderId Id="AS4AU=" ChangeKey="fsVU4o=="/>
      </FolderIds>
    </CopyFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

Las carpetas se pueden identificar mediante el elemento [DistinguishedFolderId](distinguishedfolderid.md) o [el elemento FolderId](folderid.md) para su uso en los elementos [ToFolderId](tofolderid.md) o [FolderIds.](folderids.md) 
  
### <a name="request-elements"></a>Elementos Request

En la solicitud se usan los siguientes elementos:
  
- [CopyFolder](copyfolder.md)
    
- [ToFolderId](tofolderid.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [FolderIds](folderids.md)
    
- [FolderId](folderid.md)
    
> [!NOTE]
> El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente. 
  
Para buscar otras opciones para el mensaje de solicitud de la operación CopyFolder, explore la jerarquía de esquema. Comience en el [elemento CopyFolder.](copyfolder.md) 
  
## <a name="successful-copyfolder-response"></a>Respuesta correcta de CopyFolder

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud CopyFolder. 
  
> [!NOTE]
> El identificador de carpeta y la clave de cambio se han acortado para conservar la legibilidad. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn=" ChangeKey="fsVU4o==" />
            </t:Folder>
          </m:Folders>
        </m:CopyFolderResponseMessage>
      </m:ResponseMessages>
    </CopyFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a>Comentario

El [elemento FolderId](folderid.md) que se devuelve en la respuesta representa la carpeta que se copió en la nueva ubicación de carpeta. 
  
### <a name="response-elements"></a>Elementos de respuesta

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CopyFolderResponse](copyfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CopyFolderResponseMessage](copyfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
Para buscar otras opciones para el mensaje de respuesta de la operación CopyFolder, explore la jerarquía de esquema. Comience en el [elemento CopyFolderResponse.](copyfolderresponse.md) 
  
## <a name="copyfolder-error-response"></a>Respuesta de error CopyFolder

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta de error a una solicitud CopyFolder. El error se produjo porque ya existe una carpeta con el mismo nombre para mostrar.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyFolderResponseMessage ResponseClass="Error">
          <m:MessageText>The move or copy operation failed.</m:MessageText>
          <m:ResponseCode>ErrorMoveCopyFailed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:CopyFolderResponseMessage>
      </m:ResponseMessages>
    </CopyFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Elementos de respuesta de error

En la respuesta de error se usan los siguientes elementos:
  
- [CopyFolderResponse](copyfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CopyFolderResponseMessage](copyfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
Para buscar otras opciones para el mensaje de respuesta de error de la operación CopyFolder, explore la jerarquía de esquema. Comience en el [elemento CopyFolderResponse.](copyfolderresponse.md) 
  
## <a name="see-also"></a>Ver también

- [Operación MoveFolder](movefolder-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

