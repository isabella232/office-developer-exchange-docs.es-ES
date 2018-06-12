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
ms.openlocfilehash: 2c2af53dc5dbe1e6fcbc7f3b1174a856e51e4905
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763967"
---
# <a name="createmanagedfolder-operation"></a>Operación CreateManagedFolder

La operación CreateManagedFolder crea una carpeta administrada en el almacén de Exchange.
  
## <a name="using-the-createmanagedfolder-operation"></a>Mediante la operación CreateManagedFolder

La operación CreateManagedFolder agrega una carpeta personalizada administrada al buzón de un usuario. Puede usar el cmdlet **Get-carpeta administrada** del Shell de administración de Exchange para encontrar carpetas administradas disponibles para agregar. Aunque este cmdlet devuelve las carpetas personalizadas administradas y las carpetas administradas de forma predeterminada, sólo administradas personalizados se pueden agregar carpetas. Carpetas personalizadas administradas se identifican mediante el tipo de carpeta ManagedCustomFolder. El espacio de nombres System.DirectoryServices también incluye tipos que se pueden usar para detectar los nombres de las carpetas administradas disponibles. 
  
> [!NOTE]
> No puede usar los servicios Web Exchange para buscar los nombres de las carpetas administradas disponibles para agregar a un buzón de correo. 
  
Puede utilizar las operaciones FindFolder y GetFolder para tener acceso a las carpetas administradas. FindFolder se usa para buscar las carpetas en una carpeta principal especificado. Esto se puede usar para que las carpetas administradas se pueden detectar en una carpeta antes de intentar agregar que un duplicado carpeta administrada personalizada en el mismo directorio. GetFolder se usa después de la operación FindFolder para obtener más información acerca de una carpeta personalizada administrada.
  
## <a name="remarks"></a>Notas

Para obtener información acerca de cómo configurar la directiva de administración (MRM) de registros de mensajería, consulte [cómo crear una directiva de buzón de carpeta administrada](http://go.microsoft.com/fwlink/?LinkId=100975).
  
Para obtener información acerca de cómo quitar las carpetas personalizadas administradas de un buzón de correo, consulte [Remove-carpeta administrada](http://go.microsoft.com/fwlink/?LinkId=100976).
  
## <a name="createmanagedfolder-request-example"></a>Ejemplo de solicitud CreateManagedFolder

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de CreateManagedFolder muestra cómo agregar una carpeta administrada con el nombre de carpeta administrada de prueba a un buzón de correo.
  
> [!NOTE]
> También puede usar el acceso delegado para agregar carpetas personalizadas administradas. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateManagedFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderNames>
        <t:FolderName>Test Managed Folder</t:FolderName>
      </FolderNames>
    </CreateManagedFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>Elementos de solicitud

En la solicitud se usan los siguientes elementos:
  
- [CreateManagedFolder](createmanagedfolder.md)
    
- [Nombres de carpetas](foldernames.md)
    
- [FolderName](foldername.md)
    
Para buscar otras opciones para el mensaje de solicitud de la operación CreateManagedFolder, explore la jerarquía de esquema. Comenzar en el elemento de [CreateManagedFolder](createmanagedfolder.md) . 
  
## <a name="successful-createmanagedfolder-response"></a>Respuesta CreateManagedFolder es correcta

### <a name="description"></a>Descripción

En el ejemplo de código siguiente se muestra una respuesta a una solicitud de CreateManagedFolder correcta.
  
> [!NOTE]
> Los valores de atributo de **identificador** y **ChangeKey** se han abreviado para conservar la legibilidad. 
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a>Elementos de respuesta correcta

En la respuesta se usan los siguientes elementos: 
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Carpetas](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
Para buscar otras opciones para los mensajes de respuesta de la operación CreateManagedFolder, explore la jerarquía de esquema. Comenzar en el elemento de [CreateManagedFolderResponse](createmanagedfolderresponse.md) . 
  
## <a name="createmanagedfolder-error-response"></a>Respuesta de error CreateManagedFolder

### <a name="description"></a>Descripción

En el ejemplo de código siguiente se muestra una respuesta de error a una solicitud de CreateManagedFolder.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

En la respuesta de error, se usan los siguientes elementos:
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Carpetas](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>Ver también



[Operación GetFolder](getfolder-operation.md)
  
[Operación FindFolder](findfolder-operation.md)


[Buscar carpetas](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Adición de las carpetas administradas](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

