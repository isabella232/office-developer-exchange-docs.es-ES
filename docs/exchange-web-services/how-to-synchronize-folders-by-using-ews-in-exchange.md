---
title: Sincronizar carpetas mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d3bbacd1-8e4b-4fd0-8d27-4cbbc045ec3f
description: Descubra cómo usar la API administrada de EWS o EWS para obtener una lista de carpetas, o una lista de carpetas que han cambiado, con el fin de sincronizar a su cliente.
ms.openlocfilehash: 4b0686134d642da34b2890a0e692e3d03e4a9fb1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763182"
---
# <a name="synchronize-folders-by-using-ews-in-exchange"></a>Sincronizar carpetas mediante el uso de EWS en Exchange

Descubra cómo usar la API administrada de EWS o EWS para obtener una lista de carpetas, o una lista de carpetas que han cambiado, con el fin de sincronizar a su cliente.
  
EWS en Exchange usa la sincronización de elementos y la sincronización de carpeta para sincronizar el contenido del buzón de correo entre el cliente y el servidor. Sincronización de carpetas Obtiene la lista inicial de las carpetas de una carpeta raíz y, a continuación, con el tiempo, obtiene los cambios que se han realizado en esas carpetas y obtiene así como las carpetas nuevas.
  
Si está realizando la sincronización de carpetas mediante el uso de API administrada EWS, primera [obtener la lista inicial de carpetas en la carpeta raíz](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma) mediante el método [ExchangeService.SyncFolderHierarchy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) . A continuación, actualiza el valor del parámetro _cSyncState_ durante las llamadas subsiguientes a obtener la lista de las carpetas nuevas y modificadas. 
  
Para realizar la sincronización de carpetas mediante el uso de EWS, solicitar la [lista inicial de las carpetas en la carpeta raíz](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncewsrequest) mediante la operación [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) , analizar la respuesta y, a continuación, en algún momento en el futuro [obtener los cambios a las carpetas en la raíz](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncrespews)y analizar la respuesta. Una vez que el cliente recibe la lista de carpetas iniciales o modificadas, se [realiza una actualización localmente](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps). Cómo y cuándo recuperar los cambios en el futuro depende el [patrón de diseño de la sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) de que la aplicación usa. 
  
## <a name="get-the-list-of-all-folders-or-changed-folders-by-using-the-ews-managed-api"></a>Obtener la lista de todas las carpetas o carpetas modificadas mediante el uso de la API administrada de EWS
<a name="bk_cesyncinitialewsma"> </a>

En el ejemplo de código siguiente se muestra cómo obtener una lista inicial de las carpetas en una carpeta raíz y, a continuación, obtener una lista de los cambios realizados a las carpetas en la carpeta raíz que se han producido desde la sincronización anterior. Durante la llamada inicial al método [ExchangeService.SyncFolderHierarchy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) , establezca el valor de _cSyncState_ en null. Cuando finaliza el método, guarda el valor de _cSyncState_ localmente para usar en la siguiente llamada al método **SyncFolderHierarchy** . En la llamada inicial y las llamadas subsiguientes, se recuperan las carpetas en lotes de diez, mediante el uso de las llamadas sucesivas al método **SyncFolderHierarchy** , hasta que no permanecen cambios más. En este ejemplo se establece el parámetro _propertySet_ a IdOnly para reducir las llamadas a la base de datos de Exchange, que es una [práctica recomendada de sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices). En este ejemplo, se supone que el **servicio** es un enlace de objeto **ExchangeService** válido y que _cSyncState_ representa el estado de sincronización que se ha devuelto por una llamada anterior a **SyncFolderHierarchy**. 
  
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

Después de recuperar la lista de carpetas nuevas o modificadas en el servidor, [crear o actualizar las carpetas en el cliente](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).
  
## <a name="get-the-initial-list-of-folders-by-using-ews"></a>Obtener la lista inicial de las carpetas mediante el uso de EWS
<a name="bk_cesyncewsrequest"> </a>

En el ejemplo siguiente se muestra una solicitud XML para obtener la jerarquía de carpetas inicial mediante la operación [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) . Esto también es la solicitud XML que la API administrada de EWS envía al [recuperar la lista de carpetas iniciales mediante el método SyncFolderHierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma). No se incluye el elemento de [estado de sincronización](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) de la operación [SyncFolderHierarchy](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) debido a que se trata de la sincronización inicial. En este ejemplo se establece el elemento de [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) a **IdOnly** para reducir las llamadas a la base de datos de Exchange, que es una [práctica recomendada de sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

En el ejemplo siguiente se muestra la respuesta XML que es devuelto por el servidor después de procesar la solicitud de operación [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) . La respuesta inicial incluye elementos de [crear](http://msdn.microsoft.com/library/6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1%28Office.15%29.aspx) para todas las carpetas debido a que todas las carpetas se consideran nueva durante la sincronización inicial. Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad y se han eliminado algunos bloques de **creación** del elemento por razones de brevedad. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="785"
                         MinorBuildNumber="6"
                         Version="V2_6"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderHierarchyResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                   xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Después de recuperar la lista de las carpetas nuevas en el servidor, [crear las carpetas en el cliente](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).
  
## <a name="get-the-changes-since-the-last-sync-by-using-ews"></a>Obtener los cambios realizados desde la última sincronización mediante el uso de EWS
<a name="bk_cesyncrespews"> </a>

En el ejemplo siguiente se muestra la solicitud XML para obtener la lista de los cambios realizados a las carpetas en la carpeta raíz mediante la operación [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) . Esto también es la solicitud XML que la API administrada de EWS envía al [recuperar la lista de los cambios realizados en la carpeta raíz](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma). En este ejemplo se establece el valor del elemento de [estado de sincronización](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) en el valor devuelto en la respuesta anterior. Y con fines de demostración, en este ejemplo se establece el elemento de [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) en **AllProperties** en lugar de **IdOnly** para mostrar las propiedades adicionales que se devuelve. Si se establece el elemento [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) en **IdOnly** es una [práctica recomendada de sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices). El valor de **estado de sincronización** se ha acortado para mejorar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

En el ejemplo siguiente se muestra la respuesta XML que es devuelto por el servidor después de procesar la solicitud de [operación SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) desde el cliente. Esta respuesta indica que se ha actualizado una carpeta, se creó una carpeta y se ha eliminado una carpeta desde la sincronización anterior. El valor del elemento de [estado de sincronización](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) , atributos **Id** y **ChangeKey** atributos se han abreviado para mejorar la legibilidad. 
  
Recuerde que la solicitud incluye el **AllProperties**[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx). Esto es sólo para fines de demostración. Se recomienda establecer el elemento de **BaseShape** a **IdOnly** en producción. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
<h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="745" MinorBuildNumber="21" Version="V2_3" 
           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderHierarchyResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Si está utilizando la API administrada de EWS, después de obtener la lista de carpetas nuevas o modificadas, use el método [Folder.Load](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.load%28v=exchg.80%29.aspx) para obtener las propiedades en los elementos nuevos o modificados, compare las propiedades con los valores locales y actualizar o crear las carpetas en el cliente. 
  
Si está usando EWS, use la [operación GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) para obtener las propiedades en las carpetas nuevas o modificadas y actualizar o crear las carpetas en el cliente. 
  
## <a name="see-also"></a>Vea también

- [Sincronización de buzón de correo y EWS en Exchange](mailbox-synchronization-and-ews-in-exchange.md)   
- [Sincronizar elementos mediante el uso de EWS en Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)   
- [Tratamiento de errores relacionados con la sincronización en EWS en Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    

