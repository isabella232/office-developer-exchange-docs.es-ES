---
title: Operación CreateFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateFolder
api_type:
- schema
ms.assetid: 6f6c334c-b190-4e55-8f0a-38f2a018d1b3
description: La operación CreateFolder crea carpetas, carpetas de calendario, carpetas de contactos, carpetas de tareas y carpetas de búsqueda.
ms.openlocfilehash: 125a6d212e5eaf85ace71c048de809f3a05ba9b6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457553"
---
# <a name="createfolder-operation"></a>Operación CreateFolder

La operación CreateFolder crea carpetas, carpetas de calendario, carpetas de contactos, carpetas de tareas y carpetas de búsqueda.
  
## <a name="createfolder-request-example"></a>Ejemplo de solicitud CreateFolder

### <a name="description"></a>Description

El siguiente ejemplo de una solicitud CreateFolder muestra cómo formar una solicitud para crear dos nuevas carpetas en la raíz del buzón.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ParentFolderId>
        <t:DistinguishedFolderId Id="msgfolderroot"/>
      </ParentFolderId>
      <Folders>
        <t:Folder>
          <t:DisplayName>Folder1</t:DisplayName>
        </t:Folder>
        <t:Folder>
          <t:DisplayName>Folder2</t:DisplayName>
        </t:Folder>
      </Folders>
    </CreateFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>Elementos de solicitud

Los siguientes elementos se usan en la solicitud:
  
- [CreateFolder](createfolder.md)
    
- [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
> [!NOTE]
> El esquema que describe estos elementos se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes. 
  
Para buscar otras opciones para el mensaje de solicitud de la operación CreateFolder, explore la jerarquía del esquema. Empiece en el elemento [CreateFolder](createfolder.md) . 
  
> [!NOTE]
> Si crea una carpeta de búsqueda con una restricción mediante la propiedad **Calendar: Organizer** , una llamada a la carpeta Get posterior devolverá la restricción con el **mensaje: de** la propiedad en su ubicación. Estas dos propiedades se asignan a la misma propiedad MAPI subyacente. 
  
La operación CreateFolder admite la creación de una clase de carpeta personalizada solo cuando se crea la carpeta mediante un elemento de tipo Folder genérico y se establece el elemento **FolderClass** . 
  
## <a name="successful-createfolder-response-example"></a>Ejemplo de respuesta CreateFolder correcta

### <a name="description"></a>Description

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud CreateFolder. En este ejemplo, la respuesta devuelve los identificadores de las nuevas carpetas.
  
> [!NOTE]
> El identificador de la carpeta y la clave de cambio se han abreviado para preservar la legibilidad. 
  
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
    <CreateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn==" />
            </t:Folder>
          </m:Folders>
        </m:CreateFolderResponseMessage>
        <m:CreateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn==" />
            </t:Folder>
          </m:Folders>
        </m:CreateFolderResponseMessage>
      </m:ResponseMessages>
    </CreateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>Elementos Response correcto

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateFolderResponse](createfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateFolderResponseMessage](createfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
Para buscar otras opciones para el mensaje de respuesta de la operación CreateFolder, explore la jerarquía del esquema. Empiece en el elemento [CreateFolderResponse](createfolderresponse.md) . 
  
## <a name="createfolder-error-response"></a>Respuesta de error CreateFolder

### <a name="description"></a>Description

En el ejemplo siguiente se muestra una respuesta de error a una solicitud CreateFolder.
  
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
    <CreateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateFolderResponseMessage ResponseClass="Error">
          <m:MessageText>A folder with the specified name already exists.</m:MessageText>
          <m:ResponseCode>ErrorFolderExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:CreateFolderResponseMessage>
      </m:ResponseMessages>
    </CreateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Elementos de respuesta de error

Los siguientes elementos se usan en la respuesta de error:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateFolderResponse](createfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateFolderResponseMessage](createfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
Para buscar otras opciones para el mensaje de respuesta de error de la operación CreateFolder, explore la jerarquía del esquema. Empiece en el elemento [CreateFolderResponse](createfolderresponse.md) . 
  
## <a name="see-also"></a>Vea también



[Operación FindItem](finditem-operation.md)
  
[Operación FindFolder](findfolder-operation.md)
  
 **CreateFolderType**


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


[Creación de carpetas (servicios Web de Exchange)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

