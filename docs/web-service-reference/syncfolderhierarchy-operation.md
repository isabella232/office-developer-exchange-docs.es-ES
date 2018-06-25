---
title: Operación SyncFolderHierarchy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchy
api_type:
- schema
ms.assetid: b31916b1-bc6c-4451-a475-b7c5417f752d
description: La operación SyncFolderHierarchy sincroniza las carpetas entre el equipo que ejecuta Microsoft Exchange Server 2010 y el cliente.
ms.openlocfilehash: 33c886d5eec64a9ff2ccc667eedfc2d4cc8dcfd5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840609"
---
# <a name="syncfolderhierarchy-operation"></a>Operación SyncFolderHierarchy

La operación SyncFolderHierarchy sincroniza las carpetas entre el equipo que ejecuta Microsoft Exchange Server 2010 y el cliente.
  
> [!NOTE]
> La operación SyncFolderHierarchy no devuelve carpetas cuando han cambiado las propiedades [UnreadCount](unreadcount.md) o [TotalCount](totalcount.md) . 
  
## <a name="syncfolderhierarchy-request-example"></a>Ejemplo de solicitud SyncFolderHierarchy

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de SyncFolderHierarchy muestra cómo sincronizar a un cliente de jerarquía de carpetas con el servidor de Exchange. En este ejemplo se muestra una jerarquía de carpetas que ya se hayan sincronizado al menos una vez. El elemento de [estado de sincronización](syncstate-ex15websvcsotherref.md) no está incluido en la solicitud para el primer intento sincronizar a un cliente con el servidor de Exchange. La primera solicitud devolverá todas las carpetas en el buzón de correo. El elemento de [estado de sincronización](syncstate-ex15websvcsotherref.md) se devolverán en el [SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md). Este elemento se usa para sincronizar el estado para las solicitudes SyncFolderHierarchy posteriores.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SyncFolderHierarchy  xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </FolderShape>
      <SyncState>H4sIA=</SyncState>
    </SyncFolderHierarchy>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

Los datos con codificación base64 del elemento de [estado de sincronización](syncstate-ex15websvcsotherref.md) se ha acortado para conservar la legibilidad. 
  
### <a name="request-elements"></a>Elementos de solicitud

En la solicitud se usan los siguientes elementos:
  
- [SyncFolderHierarchy](syncfolderhierarchy.md)
    
- [FolderShape](foldershape.md)
    
- [BaseShape](baseshape.md)
    
- [Estado de sincronización](syncstate-ex15websvcsotherref.md)
    
> [!NOTE]
> El esquema que describe estos elementos se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente. 
  
## <a name="successful-syncfolderhierarchy-response"></a>Respuesta SyncFolderHierarchy es correcta

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de SyncFolderHierarchy. En este ejemplo, se ha sincronizado una nueva carpeta.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SyncFolderHierarchyResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAA==</m:SyncState>
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
          <m:Changes>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AQApAHR=" ChangeKey="AQAAABY" />
                <t:ParentFolderId Id="AQApA=" ChangeKey="AQAAAA==" />
                <t:FolderClass>IPF.Note</t:FolderClass>
                <t:DisplayName>NewFolder</t:DisplayName>
                <t:TotalCount>0</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Create>
          </m:Changes>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </SyncFolderHierarchyResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

Los datos con codificación base64 del elemento de [estado de sincronización](syncstate-ex15websvcsotherref.md) y los datos de identificador de la carpeta se han abreviado para conservar la legibilidad. 
  
### <a name="successful-response-elements"></a>Elementos de respuesta correcta

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Estado de sincronización](syncstate-ex15websvcsotherref.md)
    
- [IncludesLastFolderInRange](includeslastfolderinrange.md)
    
- [Cambios (jerarquía)](changes-hierarchy.md)
    
- [Crear (FolderSync)](create-foldersync.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
- [Id](parentfolderid.md)
    
- [FolderClass](folderclass.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
- [TotalCount](totalcount.md)
    
- [ChildFolderCount](childfoldercount.md)
    
- [UnreadCount](unreadcount.md)
    
## <a name="syncfolderhierarchy-error-response"></a>Respuesta de error SyncFolderHierarchy

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de SyncFolderHierarchy. Este error se produjo por un estado de sincronización no válido.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SyncFolderHierarchyResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Error">
          <m:MessageText>Synchronization state data is corrupted or otherwise invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidSyncStateData</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:SyncState />
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </SyncFolderHierarchyResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Elementos de respuesta de error

En la respuesta de error, se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Estado de sincronización](syncstate-ex15websvcsotherref.md)
    
- [IncludesLastFolderInRange](includeslastfolderinrange.md)
    
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

