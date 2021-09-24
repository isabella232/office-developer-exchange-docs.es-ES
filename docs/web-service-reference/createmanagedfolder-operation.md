---
title: Operación CreateManagedFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateManagedFolder
api_type:
- schema
ms.assetid: 60a668a2-b4e9-4db9-ac76-9b181e47b302
description: La operación CreateManagedFolder crea una carpeta administrada en el Exchange almacén.
ms.openlocfilehash: 2b00691fbaba294950a091d5caafb8054f3e2073
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536427"
---
# <a name="createmanagedfolder-operation"></a>Operación CreateManagedFolder

La operación CreateManagedFolder crea una carpeta administrada en el Exchange almacén.
  
## <a name="using-the-createmanagedfolder-operation"></a>Uso de la operación CreateManagedFolder

La operación CreateManagedFolder agrega una carpeta personalizada administrada al buzón de un usuario. Puede usar el cmdlet **Get-ManagedFolder** Exchange Shell de administración para buscar carpetas administradas disponibles para agregar. Aunque este cmdlet devuelve carpetas personalizadas administradas y carpetas predeterminadas administradas, solo se pueden agregar carpetas personalizadas administradas. Las carpetas personalizadas administradas se identifican mediante el tipo de carpeta ManagedCustomFolder. El espacio de nombres System.DirectoryServices también incluye tipos que se pueden usar para detectar los nombres de las carpetas administradas disponibles. 
  
> [!NOTE]
> No puede usar Exchange Web Services para buscar los nombres de las carpetas administradas disponibles para agregar a un buzón. 
  
Puede usar las operaciones FindFolder y GetFolder para obtener acceso a carpetas administradas. FindFolder se usa para buscar carpetas en una carpeta primaria especificada. Esto se puede usar para que las carpetas administradas se puedan detectar en una carpeta antes de intentar agregar una carpeta personalizada administrada duplicada al mismo directorio. GetFolder se usa después de la operación FindFolder para obtener más información sobre una carpeta personalizada administrada.
  
## <a name="remarks"></a>Comentarios

Para obtener información sobre cómo configurar la directiva de administración de registros de mensajería (MRM), vea [How to Create a Managed Folder Mailbox Policy](https://go.microsoft.com/fwlink/?LinkId=100975).
  
Para obtener información sobre cómo quitar carpetas personalizadas administradas de un buzón, vea [Remove-ManagedFolder](https://go.microsoft.com/fwlink/?LinkId=100976).
  
## <a name="createmanagedfolder-request-example"></a>Ejemplo de solicitud CreateManagedFolder

### <a name="description"></a>Description

En el siguiente ejemplo de una solicitud CreateManagedFolder se muestra cómo agregar una carpeta administrada denominada Probar carpeta administrada a un buzón.
  
> [!NOTE]
> También puede usar el acceso delegado para agregar carpetas personalizadas administradas. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateManagedFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderNames>
        <t:FolderName>Test Managed Folder</t:FolderName>
      </FolderNames>
    </CreateManagedFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>Elementos Request

En la solicitud se usan los siguientes elementos:
  
- [CreateManagedFolder](createmanagedfolder.md)
    
- [FolderNames](foldernames.md)
    
- [FolderName](foldername.md)
    
Para buscar otras opciones para el mensaje de solicitud de la operación CreateManagedFolder, explore la jerarquía de esquema. Comience en el [elemento CreateManagedFolder.](createmanagedfolder.md) 
  
## <a name="successful-createmanagedfolder-response"></a>Respuesta correcta de CreateManagedFolder

### <a name="description"></a>Description

En el siguiente ejemplo de código se muestra una respuesta correcta a una solicitud CreateManagedFolder.
  
> [!NOTE]
> Los **valores de** atributo Id y **ChangeKey** se han acortado para conservar la legibilidad. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateManagedFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS0AdX=" ChangeKey="AACADA=="/>
            </t:Folder>
          </m:Folders>
        </m:CreateManagedFolderResponseMessage>
      </m:ResponseMessages>
    </CreateManagedFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>Elementos de respuesta correctos

En la respuesta se usan los siguientes elementos: 
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
Para buscar otras opciones para los mensajes de respuesta de la operación CreateManagedFolder, explore la jerarquía de esquema. Comience en el [elemento CreateManagedFolderResponse.](createmanagedfolderresponse.md) 
  
## <a name="createmanagedfolder-error-response"></a>Respuesta de error CreateManagedFolder

### <a name="description"></a>Description

En el siguiente ejemplo de código se muestra una respuesta de error a una solicitud CreateManagedFolder.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateManagedFolderResponseMessage ResponseClass="Error">
          <m:MessageText>A specified managed folder already exists in the mailbox.</m:MessageText>
          <m:ResponseCode>ErrorManagedFolderAlreadyExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders/>
        </m:CreateManagedFolderResponseMessage>
      </m:ResponseMessages>
    </CreateManagedFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Elementos de respuesta de error

En la respuesta de error se usan los siguientes elementos:
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>Ver también



[Operación GetFolder](getfolder-operation.md)
  
[Operación FindFolder](findfolder-operation.md)


[Buscar carpetas](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Agregar carpetas administradas](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

