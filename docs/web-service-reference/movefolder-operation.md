---
title: Operación MoveFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MoveFolder
api_type:
- schema
ms.assetid: c7233966-6c87-4a14-8156-b1610760176d
description: La operación MoveFolder mueve carpetas de una carpeta especificada y las coloca en otra carpeta.
ms.openlocfilehash: e0b0e93bd070354d03c511382b6096f2d3a07508
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523869"
---
# <a name="movefolder-operation"></a>Operación MoveFolder

La operación MoveFolder mueve carpetas de una carpeta especificada y las coloca en otra carpeta.
  
## <a name="remarks"></a>Comentarios

La operación MoveFolder es similar a la operación CopyFolder. No se pueden mover carpetas distinguidas. Puede mover varias carpetas a la vez a la carpeta de destino.
  
## <a name="movefolder-request-example"></a>Ejemplo de solicitud MoveFolder

### <a name="description"></a>Description

En el siguiente ejemplo de una solicitud MoveFolder se muestra cómo formar una solicitud para mover una carpeta identificada por [folderId](folderid.md) y colocar la carpeta en la carpeta distinguida correo electrónico no deseado. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ToFolderId>
        <t:DistinguishedFolderId Id="junkemail"/>
      </ToFolderId>
      <FolderIds>
        <t:FolderId Id="AScAc"/>
      </FolderIds>
    </MoveFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

> [!NOTE]
> El valor del atributo ID del [elemento FolderId](folderid.md) se ha acortado para su legibilidad. 
  
### <a name="request-elements"></a>Elementos Request

Esta solicitud MoveFolder incluye los siguientes elementos:
  
- [MoveFolder](movefolder.md)
    
- [ToFolderId](tofolderid.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [FolderIds](folderids.md)
    
- [FolderId](folderid.md)
    
Consulte el esquema para ver los elementos adicionales que puede usar para formar una solicitud MoveFolder.
  
> [!NOTE]
> La ubicación predeterminada del esquema se encuentra en el directorio virtual EWS del equipo que tiene instalado el rol de servidor Acceso de cliente. 
  
## <a name="successful-movefolder-response-example"></a>Ejemplo de respuesta correcta de MoveFolder

### <a name="description"></a>Description

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud MoveFolder. 
  
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
    <MoveFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AAAlAFV" ChangeKey="AQAAAB" />
            </t:Folder>
          </m:Folders>
        </m:MoveFolderResponseMessage>
      </m:ResponseMessages>
    </MoveFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

> [!NOTE]
> El identificador de carpeta y la clave de cambio se han acortado para conservar la legibilidad. 
  
El FolderId que se devuelve en la respuesta representa la carpeta que se movió a la nueva ubicación de la carpeta.
  
### <a name="response-elements"></a>Elementos de respuesta

La respuesta MoveFolder incluye los siguientes elementos:
  
- [MoveFolderResponse](movefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MoveFolderResponseMessage](movefolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
## <a name="movefolder-error-response-example"></a>Ejemplo de respuesta de error MoveFolder

### <a name="description"></a>Description

En el ejemplo siguiente se muestra una respuesta de error que se produce al intentar mover una carpeta distinguida.
  
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
    <MoveFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Cannot move distinguished folder.</m:MessageText>
          <m:ResponseCode>ErrorMoveDistinguishedFolder</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:MoveFolderResponseMessage>
      </m:ResponseMessages>
    </MoveFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Elementos de respuesta de error

La respuesta de error MoveFolder incluye los siguientes elementos:
  
- [MoveFolderResponse](movefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MoveFolderResponseMessage](movefolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>Ver también



[Operación CopyFolder](copyfolder-operation.md)

