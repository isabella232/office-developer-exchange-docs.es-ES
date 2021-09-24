---
title: Sincronizar carpetas mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: d3bbacd1-8e4b-4fd0-8d27-4cbbc045ec3f
description: Descubra cómo usar la API administrada ews o EWS para obtener una lista de carpetas, o una lista de carpetas que han cambiado, para sincronizar el cliente.
ms.openlocfilehash: f22cb3b4ba92da9c044e08e7164d116293cf43ff
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521098"
---
# <a name="synchronize-folders-by-using-ews-in-exchange"></a>Sincronizar carpetas mediante EWS en Exchange

Descubra cómo usar la API administrada ews o EWS para obtener una lista de carpetas, o una lista de carpetas que han cambiado, para sincronizar el cliente.
  
EWS en Exchange usa la sincronización de elementos y la sincronización de carpetas para sincronizar el contenido del buzón entre el cliente y el servidor. La sincronización de carpetas obtiene la lista inicial de carpetas de una carpeta raíz y, a continuación, con el tiempo, obtiene los cambios realizados en esas carpetas y obtiene nuevas carpetas también.
  
Si está realizando la sincronización de carpetas mediante la API administrada ews, primero obtiene la lista inicial de carpetas en la carpeta [raíz](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma) mediante el método [ExchangeService.SyncFolderHierarchy.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) A continuación, actualice el valor del parámetro  _cSyncState_ durante las llamadas posteriores para obtener la lista de carpetas nuevas y modificadas. 
  
Para realizar la sincronización de carpetas mediante EWS, debe solicitar la lista inicial de carpetas de la carpeta raíz mediante [](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncrespews)la operación [SyncFolderHierarchy,](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) analizar la respuesta y, a continuación, en algún momento del futuro obtener los cambios en las carpetas de la raíz y analizar la respuesta. [](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncewsrequest) Después de que el cliente recibe la lista de carpetas iniciales o modificadas, [realiza actualizaciones localmente.](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps) Cómo y cuándo recuperar los cambios en el futuro depende del patrón de diseño [de sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) que esté usando la aplicación. 
  
## <a name="get-the-list-of-all-folders-or-changed-folders-by-using-the-ews-managed-api"></a>Obtener la lista de todas las carpetas o carpetas modificadas mediante la API administrada de EWS
<a name="bk_cesyncinitialewsma"> </a>

En el siguiente ejemplo de código se muestra cómo obtener una lista inicial de carpetas en una carpeta raíz y, a continuación, obtener una lista de los cambios realizados en las carpetas de la carpeta raíz que se han producido desde la sincronización anterior. Durante la llamada inicial al método [ExchangeService.SyncFolderHierarchy,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) establezca el  _valor cSyncState_ en null. Cuando se complete el método, guarde el _valor cSyncState_ localmente para usarlo en la siguiente llamada al método **SyncFolderHierarchy.** Tanto en la llamada inicial como en las llamadas posteriores, las carpetas se recuperan en lotes de diez, mediante llamadas sucesivas al método **SyncFolderHierarchy,** hasta que no quedan más cambios. En este ejemplo se establece el parámetro _propertySet_ en IdOnly para reducir las llamadas a la base de datos Exchange, que es un [procedimiento recomendado de sincronización.](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices) En este ejemplo, se supone que **el** servicio es un enlace de objetos **ExchangeService** válido y que  _cSyncState_ representa el estado de sincronización devuelto por una llamada anterior a **SyncFolderHierarchy**. 
  
```cs
// Get a list of all folders in the mailbox by calling SyncFolderHierarchy.
// The folderId parameter must be set to the root folder to synchronize. 
// The propertySet parameter is set to IdOnly to reduce calls to the Exchange database
// because any additional properties result in additional calls to the Exchange database. 
// The syncState parameter is set to cSyncState, which should be null in the initial call, 
// and should be set to the sync state returned by the previous SyncFolderHierarchy call 
// in subsequent calls.
ChangeCollection<FolderChange> fcc = service.SyncFolderHierarchy(new FolderId(WellKnownFolderName.Root), PropertySet.IdOnly, cSyncState);
// If the count of changes is zero, there are no changes to synchronize.
if (fcc.Count == 0)
{
    Console.WriteLine("There are no folders to synchronize.");
}
// Otherwise, write all the changes included in the response 
// to the console. 
// For the initial synchronization, all the changes will be of type
// ChangeType.Create.
else
{
    foreach (FolderChange fc in fcc)
    {
        Console.WriteLine("ChangeType: " + fc.ChangeType.ToString());
        Console.WriteLine("FolderId: " + fc.FolderId);
        Console.WriteLine("===========");
    }
}
// Save the sync state for use in future SyncFolderItems requests.
// The sync state is used by the server to determine what changes to report
// to the client.
string fSyncState = fcc.SyncState;

```

Después de recuperar la lista de carpetas nuevas o modificadas en el servidor, cree o actualice las [carpetas en el cliente](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).
  
## <a name="get-the-initial-list-of-folders-by-using-ews"></a>Obtener la lista inicial de carpetas mediante EWS
<a name="bk_cesyncewsrequest"> </a>

En el ejemplo siguiente se muestra una solicitud XML para obtener la jerarquía de carpetas inicial mediante la [operación SyncFolderHierarchy.](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) Esta es también la solicitud XML que envía la API administrada ews al recuperar la lista de carpetas iniciales mediante el [método SyncFolderHierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma). El [elemento SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) de la [operación SyncFolderHierarchy](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) no se incluye porque se trata de la sincronización inicial. En este ejemplo se establece el [elemento BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) en **IdOnly** para reducir las llamadas a la base de datos Exchange, que es un [procedimiento recomendado de sincronización.](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:SyncFolderHierarchy>
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </m:FolderShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="root" />
      </m:SyncFolderId>
    </m:SyncFolderHierarchy>
  </soap:Body>
</soap:Envelope>
```

En el siguiente ejemplo se muestra la respuesta XML que devuelve el servidor después de que procesa la solicitud de operación [SyncFolderHierarchy.](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) La respuesta inicial incluye [Crear](https://msdn.microsoft.com/library/6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1%28Office.15%29.aspx) elementos para todas las carpetas porque todas las carpetas se consideran nuevas durante una sincronización inicial. Los valores de algunos atributos y elementos se han acortado para mejorar la legibilidad y algunos **bloques de** elementos Create se quitaron por brevedad. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="785"
                         MinorBuildNumber="6"
                         Version="V2_6"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                   xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAA==</m:SyncState>
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
          <m:Changes>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADM="
                            ChangeKey="AQAAABYA"/>
              </t:Folder>
            </t:Create>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADMzM="
                            ChangeKey="AQAAABY"/>
              </t:Folder>
            </t:Create>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkAD/AAA="
                            ChangeKey="AQAAABYA"/>
              </t:Folder>
            </t:Create>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADBh="
                            ChangeKey="AQAAABYA"/>
              </t:Folder>
            </t:Create>
            ...
          </m:Changes>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderHierarchyResponse>
  </s:Body>
</s:Envelope>
```

Después de recuperar la lista de carpetas nuevas en el servidor, [cree las carpetas en el cliente](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).
  
## <a name="get-the-changes-since-the-last-sync-by-using-ews"></a>Obtener los cambios desde la última sincronización mediante EWS
<a name="bk_cesyncrespews"> </a>

En el ejemplo siguiente se muestra la solicitud XML para obtener la lista de cambios en las carpetas de la carpeta raíz mediante la [operación SyncFolderHierarchy.](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) También es la solicitud XML que envía la API administrada ews al recuperar la lista de [cambios en la carpeta raíz](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma). En este ejemplo se establece [el valor del elemento SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) en el valor devuelto en la respuesta anterior. Y para fines de demostración, este ejemplo establece el elemento [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) en **AllProperties** en lugar de **IdOnly** para mostrar las propiedades adicionales devueltas. Establecer el [elemento BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) en **IdOnly** es un [procedimiento recomendado de sincronización.](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices) El valor de **SyncState** se ha acortado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:SyncFolderHierarchy>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="root" />
      </m:SyncFolderId>
      <m:SyncState>H4sIAA==</m:SyncState>
    </m:SyncFolderHierarchy>
  </soap:Body>
</soap:Envelope>
```

En el ejemplo siguiente se muestra la respuesta XML que devuelve el servidor después de que procesa la solicitud de operación [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) del cliente. Esta respuesta indica que se actualizó una carpeta, se creó una carpeta y se eliminó una desde la sincronización anterior. El valor del [elemento SyncState,](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) **los atributos Id** y los atributos **ChangeKey** se han acortado para mejorar la legibilidad. 
  
Recuerde que la solicitud incluía **la BaseShape AllProperties**[](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx). Esto es solo para fines de demostración. Se recomienda establecer el elemento **BaseShape** en **IdOnly** en producción. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
<h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="745" MinorBuildNumber="21" Version="V2_3" 
           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAA</m:SyncState>
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
          <m:Changes>
            <t:Update>
              <t:Folder>
                <t:FolderId Id="AAMkADM=" ChangeKey="AQAAABY" />
                <t:ParentFolderId Id="AQMkADMzADI1==" ChangeKey="AQAAAA==" />
                <t:FolderClass>IPF.Note</t:FolderClass>
                <t:DisplayName>Meeting Notes</t:DisplayName>
                <t:TotalCount>3</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:EffectiveRights>
                  <t:CreateAssociated>true</t:CreateAssociated>
                  <t:CreateContents>true</t:CreateContents>
                  <t:CreateHierarchy>true</t:CreateHierarchy>
                  <t:Delete>true</t:Delete>
                  <t:Modify>true</t:Modify>
                  <t:Read>true</t:Read>
                  <t:ViewPrivateItems>true</t:ViewPrivateItems>
                </t:EffectiveRights>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Update>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADMzM=" ChangeKey="AQAAABYAA" />
                <t:ParentFolderId Id="AQMkO67A==" ChangeKey="AQAAAA==" />
                <t:FolderClass>IPF.Note</t:FolderClass>
                <t:DisplayName>Schedules</t:DisplayName>
                <t:TotalCount>0</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:EffectiveRights>
                  <t:CreateAssociated>true</t:CreateAssociated>
                  <t:CreateContents>true</t:CreateContents>
                  <t:CreateHierarchy>true</t:CreateHierarchy>
                  <t:Delete>true</t:Delete>
                  <t:Modify>true</t:Modify>
                  <t:Read>true</t:Read>
                  <t:ViewPrivateItems>true</t:ViewPrivateItems>
                </t:EffectiveRights>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Create>
            <t:Delete>
              <t:FolderId Id="AAMkAD/AAA=" ChangeKey="AQAAAA==" />
            </t:Delete>
          </m:Changes>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderHierarchyResponse>
  </s:Body>
</s:Envelope>

```

## <a name="update-the-client"></a>Actualizar el cliente
<a name="bk_nextsteps"> </a>

Si usa la API administrada ews, después de obtener la lista de carpetas nuevas o modificadas, use el método [Folder.Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.load%28v=exchg.80%29.aspx) para obtener propiedades en los elementos nuevos o modificados, comparar las propiedades con los valores locales y actualizar o crear las carpetas en el cliente. 
  
Si usa EWS, use la operación [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) para obtener propiedades en las carpetas nuevas o modificadas y actualizar o crear las carpetas en el cliente. 
  
## <a name="see-also"></a>Ver también

- [Sincronización del buzón y EWS en Exchange](mailbox-synchronization-and-ews-in-exchange.md)   
- [Sincronizar elementos mediante EWS en Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)   
- [Controlar errores relacionados con la sincronización en EWS en Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    

