---
title: Operación CreateManagedFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateManagedFolder
api_type:
- schema
ms.assetid: 60a668a2-b4e9-4db9-ac76-9b181e47b302
description: La operación CreateManagedFolder crea una carpeta administrada en el almacén de Exchange.
ms.openlocfilehash: 779c730b55b9b441644108a6837f9e22d39cc2f4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44444596"
---
# <a name="createmanagedfolder-operation"></a>Operación CreateManagedFolder

La operación CreateManagedFolder crea una carpeta administrada en el almacén de Exchange.
  
## <a name="using-the-createmanagedfolder-operation"></a>Uso de la operación CreateManagedFolder

La operación CreateManagedFolder agrega una carpeta personalizada administrada al buzón de un usuario. Puede usar el cmdlet **Get-ManagedFolder** del shell de administración de Exchange para buscar las carpetas administradas que se pueden agregar. Aunque este cmdlet devuelve las carpetas personalizadas administradas y las carpetas predeterminadas administradas, solo se pueden agregar carpetas personalizadas administradas. Las carpetas personalizadas administradas se identifican mediante el tipo de carpeta ManagedCustomFolder. El espacio de nombres System. DirectoryServices también incluye tipos que se pueden usar para detectar los nombres de las carpetas administradas disponibles. 
  
> [!NOTE]
> No puede usar los servicios web Exchange para encontrar los nombres de las carpetas administradas disponibles para agregar a un buzón de correo. 
  
Puede usar las operaciones FindFolder y GetFolder para tener acceso a las carpetas administradas. FindFolder se usa para buscar carpetas en una carpeta principal especificada. Esto puede usarse para que las carpetas administradas se puedan detectar en una carpeta antes de intentar agregar una carpeta personalizada administrada duplicada al mismo directorio. GetFolder se usa después de la operación FindFolder para obtener más información acerca de una carpeta administrada personalizada.
  
## <a name="remarks"></a>Comentarios

Para obtener información acerca de cómo configurar la Directiva de administración de registros de mensajes (MRM), consulte [How to Create a Managed Folder Mailbox Policy](https://go.microsoft.com/fwlink/?LinkId=100975).
  
Para obtener información acerca de cómo quitar las carpetas personalizadas administradas de un buzón de correo, vea [Remove-ManagedFolder](https://go.microsoft.com/fwlink/?LinkId=100976).
  
## <a name="createmanagedfolder-request-example"></a>Ejemplo de solicitud CreateManagedFolder

### <a name="description"></a>Description

El siguiente ejemplo de una solicitud de CreateManagedFolder muestra cómo agregar una carpeta administrada llamada test Managed Folder a un buzón de correo.
  
> [!NOTE]
> También puede usar acceso delegado para agregar carpetas administradas personalizadas. 
  
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

### <a name="request-elements"></a>Elementos de solicitud

Los siguientes elementos se usan en la solicitud:
  
- [CreateManagedFolder](createmanagedfolder.md)
    
- [FolderNames](foldernames.md)
    
- [FolderName](foldername.md)
    
Para buscar otras opciones para el mensaje de solicitud de la operación CreateManagedFolder, explore la jerarquía del esquema. Empiece en el elemento [CreateManagedFolder](createmanagedfolder.md) . 
  
## <a name="successful-createmanagedfolder-response"></a>Respuesta CreateManagedFolder correcta

### <a name="description"></a>Description

En el ejemplo de código siguiente se muestra una respuesta correcta a una solicitud CreateManagedFolder.
  
> [!NOTE]
> Los valores de atributo **ID** y **changekey** se han abreviado para preservar la legibilidad. 
  
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

### <a name="successful-response-elements"></a>Elementos Response correcto

En la respuesta se usan los siguientes elementos: 
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
Para buscar otras opciones de los mensajes de respuesta de la operación CreateManagedFolder, explore la jerarquía del esquema. Empiece en el elemento [CreateManagedFolderResponse](createmanagedfolderresponse.md) . 
  
## <a name="createmanagedfolder-error-response"></a>Respuesta de error de CreateManagedFolder

### <a name="description"></a>Description

El siguiente ejemplo de código muestra una respuesta de error a una solicitud CreateManagedFolder.
  
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

Los siguientes elementos se usan en la respuesta de error:
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>Vea también



[Operación GetFolder](getfolder-operation.md)
  
[Operación FindFolder](findfolder-operation.md)


[Buscar carpetas](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Adición de carpetas administradas](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

