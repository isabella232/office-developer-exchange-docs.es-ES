---
title: Trabajar con carpetas mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 4b3eb746-74c4-42a0-aa2c-742c147f1871
description: Obtenga información sobre cómo crear, obtener, actualizar y eliminar carpetas con la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: c09c0c76edda4af025a6ac7121fdf9ab9660fcab
ms.sourcegitcommit: eeda51cb037aa25566adb293f25574674fdb2d9e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "45012548"
---
# <a name="work-with-folders-by-using-ews-in-exchange"></a>Trabajar con carpetas mediante EWS en Exchange

Obtenga información sobre cómo crear, obtener, actualizar y eliminar carpetas con la API administrada de EWS o EWS en Exchange.
  
EWS en Exchange usa carpetas para estructurar y organizar buzones de correo. Puede crear carpetas nuevas, obtener, actualizar y eliminar mediante la API administrada de EWS o EWS. Cada uno de los métodos u operaciones enumerados en la siguiente tabla se realiza en un objeto de [carpeta](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) , un tipo de [carpeta](https://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) o [una de las clases o tipos de carpetas derivadas](folders-and-items-in-ews-in-exchange.md#bk_folders).
  
**Tabla 1. Métodos y operaciones para crear, obtener, actualizar y eliminar carpetas**

|**Para**|**Método de la API administrada de EWS**|**Operación de EWS**|
|:-----|:-----|:-----|
|Crear una carpeta  <br/> |[Folder. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|Crear una jerarquía de carpetas  <br/> |No disponible  <br/> |[CreateFolderPath](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |
|Obtener una carpeta  <br/> |[Folder. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> |[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |
|Obtener una jerarquía de carpetas  <br/> |[Folder. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> |[FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |
|Actualizar una carpeta  <br/> |[Folder. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> |[UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|Eliminar una carpeta  <br/> |[Folder. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> |[DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |

<a name="bk_createfolderewsma"> </a>

## <a name="create-a-folder-by-using-the-ews-managed-api"></a>Crear una carpeta mediante la API administrada de EWS

En el siguiente ejemplo de código se muestra cómo usar la clase [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) para crear una nueva carpeta genérica con el [displayName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx) "Custom Folder" y un valor de la propiedad [FolderClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.folderclass%28v=exchg.80%29.aspx) de ipf. Note. El método [Folder. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) guarda la carpeta como una carpeta secundaria de la carpeta Bandeja de entrada. 
  
En estos ejemplos se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange. 
  
```csharp
// Create a custom folder.
Folder folder = new Folder(service);
folder.DisplayName = "Custom Folder";
folder.FolderClass = "IPF.Note";
// Save the folder as a child folder of the Inbox.
folder.Save(WellKnownFolderName.Inbox);
```

Para crear un tipo de carpeta diferente, como [hubiera](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx), [hubiera](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx), [SearchFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx)o [hubiera](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx), cree una nueva instancia de la clase específica (en lugar de la clase de **carpeta** genérica) y no establezca la propiedad **FolderClass** . Por ejemplo, en el siguiente ejemplo de código se muestra cómo crear un nuevo [hubiera](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx).
  
```csharp
// Create a custom Tasks folder.
TasksFolder folder = new TasksFolder(service);
folder.DisplayName = "Custom Tasks";
// Save the folder as a child folder in the Inbox folder.
// This method call results in a CreateFolder call to EWS.
folder.Save(WellKnownFolderName.Inbox);
```

Si se intenta crear una instancia de una clase específica y también se establece la propiedad **FolderClass** , se produce el error [ErrorNoFolderClassOverride](https://msdn.microsoft.com/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx) . 
  
Tenga en cuenta que no puede procesar por lotes la creación de varias carpetas en una sola llamada de método usando la API administrada de EWS.
  
## <a name="create-a-folder-by-using-ews"></a>Crear una carpeta mediante EWS
<a name="bk_createfolderews"> </a>

Puede crear una sola carpeta o varias carpetas con EWS.
  
Para crear una sola carpeta, envíe un mensaje de solicitud de operación [CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) . La solicitud de operación **CreateFolder** indica que la carpeta principal es la bandeja de entrada, el valor de [displayName](https://msdn.microsoft.com/library/e7efbbe1-6629-4d11-bed1-ed899e3f9d77%28Office.15%29.aspx) es "carpeta personalizada" y el valor del elemento [FolderClass](https://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) es ipf. Note. 
  
También es la solicitud XML que la API administrada de EWS envía cuando se crea una nueva carpeta y se llama al método [Folder. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) . 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateFolder>
      <m:ParentFolderId>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderId>
      <m:Folders>
        <t:Folder>
          <t:FolderClass>IPF.Note</t:FolderClass>
          <t:DisplayName>Custom Folder</t:DisplayName>
        </t:Folder>
      </m:Folders>
    </m:CreateFolder>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **CreateFolder** con un mensaje [CreateFolderResponse](https://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) de **NoError**, que indica que la carpeta se ha creado correctamente y el [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) del mensaje que se acaba de crear. 
  
Para crear varias carpetas, incluya varios elementos [Folder](https://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) en el mensaje de solicitud de la operación **CreateFolder** . Todas las carpetas nuevas deben estar en la misma carpeta principal. 
  
## <a name="create-a-folder-hierarchy-by-using-ews"></a>Crear una jerarquía de carpetas mediante EWS
<a name="bk_createfolderhierarchy"> </a>

Puede crear una jerarquía de carpetas en una sola llamada mediante la operación [CreateFolderPath](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) de EWS. La misma funcionalidad no está disponible en la API administrada de EWS. En su lugar, si usa la API administrada de EWS, puede crear carpetas una a una, tal como se muestra en [crear una carpeta mediante EWS](#bk_createfolderews).
  
> [!NOTE]
> La API administrada de EWS no implementa esta funcionalidad. 
  
## <a name="get-a-folder-by-using-the-ews-managed-api"></a>Obtener una carpeta mediante la API administrada de EWS
<a name="bk_getfolderewsma"> </a>

En el ejemplo de código siguiente se muestra cómo usar el método [Folder. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) para obtener la carpeta Bandeja de entrada. Como práctica recomendada, limite las propiedades que se devuelven solo a las necesarias para su aplicación. En este ejemplo se limitan las propiedades de retorno para que solo incluyan la propiedad [ID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) mediante la creación de un objeto [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) y la aplicación del valor [IdOnly](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) a la propiedad [BasePropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset.basepropertyset%28v=exchg.80%29.aspx) . 
  
En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange. 
  
```csharp
// As a best practice, limit the properties returned to only those that are required.
// In this scenario, you only need the FolderId.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly);
// Bind to an existing folder and get only the properties specified in the PropertySet.
// This method call results in a GetFolder call to EWS.
Folder rootfolder = Folder.Bind(service, WellKnownFolderName.Inbox, propSet);
```

Si necesitas devolver propiedades adicionales, agrega propiedades de la clase [FolderSchema](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderschema%28v=exchg.80%29.aspx) a la **PropertySet**o usa uno de los métodos [BIND](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) sobrecargados que devuelve todas las propiedades de primera clase. 
  
Tenga en cuenta que no puede obtener varias carpetas al mismo tiempo mediante la API administrada de EWS. Debe llamar al método **BIND** en cada carpeta por separado. 
  
## <a name="get-a-folder-by-using-ews"></a>Obtener una carpeta mediante EWS
<a name="bk_getfolderews"> </a>

Puede obtener una sola carpeta o varias carpetas con EWS.
  
Para obtener una carpeta única, envíe un mensaje de solicitud de la operación [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) al servidor. En el siguiente ejemplo, [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) se establece en **IdOnly**, por lo que solo se devuelve el [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) de la carpeta especificada. El elemento [FolderIds](https://msdn.microsoft.com/library/3ff9d15a-7220-4785-ae6b-583a7eb82005%28Office.15%29.aspx) indica que la carpeta que se va a recuperar es la carpeta Bandeja de entrada. 
  
También es la solicitud XML que la API administrada de EWS envía cuando se enlaza a una carpeta con el método [Folder. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) . 
  
Para obtener varias carpetas, incluya varios elementos [FolderIds](https://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) en el mensaje de solicitud de la operación **GetFolder** . 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

El siguiente ejemplo de XML muestra el mensaje [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) que se envía desde el servidor al cliente en respuesta a la solicitud de operación **GetFolder** . Solo contiene el valor [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) de la carpeta Bandeja de entrada. Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="800"
                         MinorBuildNumber="16"
                         Version="V2_6"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AAAENAAA=" ChangeKey="AQAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAEkbCr"/>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

## <a name="get-a-folder-hierarchy-by-using-the-ews-managed-api"></a>Obtener una jerarquía de carpetas mediante la API administrada de EWS
<a name="bk_getfolderhierarchyewsma"> </a>

En el ejemplo de código siguiente se muestra cómo recuperar las subcarpetas de una carpeta raíz especificada. En este ejemplo se recuperan las subcarpetas de la carpeta **MsgFolderRoot** , que es la raíz del subárbol IPM (donde se almacenan las carpetas y los elementos del buzón). 
  
En este ejemplo, se crea un objeto de clase [FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) para limitar los resultados de la respuesta del método [Folder. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) . Este escenario limita las propiedades para volver a las siguientes: [ID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx), [displayName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx)y la propiedad extendida que indica si la carpeta es una carpeta oculta. Establezca el valor [FolderView. Traversal](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.traversal%28v=EXCHG.80%29.aspx) en Deep para realizar una búsqueda recursiva de modo que el servidor recupere las subcarpetas y establezca la carpeta raíz en **MsgFolderRoot**, de modo que el servidor devuelva todas las carpetas del usuario (y el servidor no devolverá carpetas del sistema en el subárbol no IPM).
  
En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange. 
  
```csharp
// Create a new folder view, and pass in the maximum number of folders to return.
FolderView view = new FolderView(folderViewSize);
// Create an extended property definition for the PR_ATTR_HIDDEN property,
// so that your results will indicate whether the folder is a hidden folder.
ExtendedPropertyDefinition isHiddenProp = new ExtendedPropertyDefinition(0x10f4, MapiPropertyType.Boolean);
// As a best practice, limit the properties returned to only those required.
// In this case, return the folder ID, DisplayName, and the value of the isHiddenProp
// extended property.
view.PropertySet = new PropertySet(BasePropertySet.IdOnly, FolderSchema.DisplayName, isHiddenProp);
// Indicate a Traversal value of Deep, so that all subfolders are retrieved.
view.Traversal = FolderTraversal.Deep;
// Call FindFolders to retrieve the folder hierarchy, starting with the MsgFolderRoot folder.
// This method call results in a FindFolder call to EWS.
FindFoldersResults findFolderResults = service.FindFolders(WellKnownFolderName.MsgFolderRoot, view);
```

## <a name="get-a-folder-hierarchy-by-using-ews"></a>Obtener una jerarquía de carpetas mediante EWS
<a name="bk_getfolderhierarchyews"> </a>

Los siguientes ejemplos de XML muestran cómo usar la operación [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) para recuperar una jerarquía de carpetas mediante EWS. En este ejemplo se recupera la carpeta **msgfolderroot** , que es la raíz del subárbol IPM y todas sus subcarpetas. El atributo de **recorrido** se establece en **Deep** , por lo que el servidor realiza una búsqueda recursiva de la jerarquía de carpetas y solo devuelve carpetas y subcarpetas dentro de la raíz especificada en la respuesta. En este ejemplo, el elemento [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) se establece en **IdOnly** para que el servidor solo devuelva el elemento [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) . Para que el resultado sea más fácil de entender, incluya el elemento **displayName** en los resultados mediante su inclusión en el elemento [AdditionalProperties](https://msdn.microsoft.com/library/7a269aed-dcfd-4c3e-9e14-094e53828101%28Office.15%29.aspx) de la solicitud, junto con el valor **ExtendedFieldURI** de la propiedad **PR_ATTR_HIDDEN** , para saber si las carpetas están ocultas. 
  
También es la solicitud XML que la API administrada de EWS envía cuando se llama al método [FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) . 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Deep">
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:DisplayName" />
          <t:ExtendedFieldURI PropertyTag="4340"
                              PropertyType="Boolean" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="100"
                               Offset="0"
                               BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="msgfolderroot" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

El siguiente ejemplo de XML muestra el mensaje [FindFolderResponse](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) que se envía desde el servidor al cliente en respuesta a la solicitud de operación **FindFolder** . Contiene solo el [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx), el [displayName](https://msdn.microsoft.com/library/e7efbbe1-6629-4d11-bed1-ed899e3f9d77%28Office.15%29.aspx)y el valor de la propiedad extendida **PR_ATTR_HIDDEN** para todas las subcarpetas de la carpeta **msgrootfolder** Si el elemento [Value](https://msdn.microsoft.com/library/9a30cadd-909e-41b1-b4e9-291643dd89c6%28Office.15%29.aspx) está establecido en true, la carpeta debe estar oculta en la vista de cliente. 
  
También es la respuesta XML que la API administrada de EWS envía cuando se obtienen varias carpetas mediante el método [FindFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) . Los valores de algunos atributos y elementos se han abreviado para facilitar la legibilidad y no se han incluido algunas carpetas por motivos de brevedad. 
  
```xml
<?xml version="1.0" encoding="utf-8"?><s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="815"
                         MinorBuildNumber="6"
                         Version="V2_7"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="16"
                        TotalItemsInView="16"
                        IncludesLastItemInRange="true">
            <t:Folders>
              <t:CalendarFolder>
                <t:FolderId Id="AAAEOAAA="
                            ChangeKey="AgAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAAAAA3"/>
                <t:DisplayName>Calendar</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean"/>
                  <t:Value>false</t:Value>
                </t:ExtendedProperty>
              </t:CalendarFolder>
              <t:ContactsFolder>
                <t:FolderId Id="AAAEPAAA="
                            ChangeKey="AwAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAAAAA4"/>
                <t:DisplayName>Contacts</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean"/>
                  <t:Value>false</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:ContactsFolder>
                <t:FolderId Id="AAAUKAAA="
                            ChangeKey="AwAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAAAAS5"/>
                <t:DisplayName>Recipient Cache</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean"/>
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:Folder>
                <t:FolderId Id="AAAUJAAA="
                            ChangeKey="AQAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAAAASx"/>
                <t:DisplayName>Conversation Action Settings</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean"/>
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
…
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </m:FindFolderResponse>
  </s:Body>
</s:Envelope>
```

## <a name="update-a-folder-by-using-the-ews-managed-api"></a>Actualizar una carpeta mediante la API administrada de EWS
<a name="bk_updatefolderewsma"> </a>

En el siguiente ejemplo de código, se muestra cómo actualizar el nombre para mostrar de una carpeta mediante la API administrada de EWS.
  
En primer lugar, cree un [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) para limitar el número de propiedades que el servidor devuelve en la respuesta [Folder. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) . Le recomendamos que use el **IdOnly** **BasePropertySet** para reducir las llamadas a la base de datos de Exchange. A continuación, use el método **BIND** para enlazar a la carpeta que se va a actualizar. A continuación, actualice la propiedad [displayName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx) y use el método [Folder. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) para guardar los cambios. 
  
En este ejemplo, se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange. La variable local *folderId* es el [identificador](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) de la carpeta que se va a actualizar. 
  
```cs
// As a best practice, only include the ID value in the PropertySet.
PropertySet propertySet = new PropertySet(BasePropertySet.IdOnly);
// Bind to an existing folder and get the FolderId.
// This method call results in a GetFolder call to EWS.
Folder folder = Folder.Bind(service, folderId, propertySet);
// Update the display name of the folder.
folder.DisplayName = "Updated folder name";
// Save the updates.
// This method call results in an UpdateFolder call to EWS.
folder.Update();

```

## <a name="update-a-folder-by-using-ews"></a>Actualizar una carpeta con EWS
<a name="bk_updatefolderews"> </a>

Los siguientes ejemplos de XML muestran cómo actualizar el nombre para mostrar de una carpeta mediante EWS.
  
En primer lugar, envíe un mensaje de solicitud de la operación [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) para obtener la carpeta que se va a actualizar, como se muestra en [obtener una jerarquía de carpetas mediante EWS](#bk_getfolderhierarchyews).
  
A continuación, envíe un mensaje de solicitud de operación de [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) al servidor para actualizar una carpeta. La solicitud de operación **UpdateFolder** actualiza el [displayName](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) a "carpeta personalizada actualizada". 
  
También es la solicitud XML que la API administrada de EWS envía cuando actualiza una carpeta con el método [Folder. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) . Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="OrV9ZAAA=" ChangeKey="AQAAABYAAABVzRdyy/cHS4XTC9itCRdUAAAOrXWb" />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:DisplayName" />
              <t:Folder>
                <t:DisplayName>Updated Custom Folder</t:DisplayName>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **UpdateFolder** con un mensaje [UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) que incluye el valor [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) de **NoError**y el [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) de la carpeta que se actualizó con un valor de atributo **changekey** actualizado. 
  
## <a name="delete-a-folder-by-using-the-ews-managed-api"></a>Eliminar una carpeta mediante la API administrada de EWS
<a name="bk_deletefolderewsma"> </a>

En este artículo se proporciona un ejemplo básico que muestra cómo eliminar una carpeta mediante la API administrada de EWS. Para obtener más información sobre cómo eliminar carpetas, vea [eliminar elementos mediante EWS en Exchange](deleting-items-by-using-ews-in-exchange.md).
  
Para eliminar una carpeta mediante la API administrada de EWS, en primer lugar, use el método [Folder. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) para enlazar con el objeto de servicio a la carpeta que se va a eliminar. A continuación, use el método [Folder. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) para eliminar la carpeta mediante el modo de eliminación de [HardDelete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.deletemode%28v=exchg.80%29.aspx) . 
  
En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange. La variable local *folderId* es el [identificador](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) de la carpeta que se va a eliminar. 
  
```cs
// Bind to an existing folder and get all its properties.
// This method call results in a GetFolder call to EWS.
Folder folder = Folder.Bind(service, folderId);
// HardDelete the folder.
// This method call results in a DeleteFolder call to EWS.
folder.Delete(DeleteMode.HardDelete);
```

## <a name="delete-a-folder-by-using-ews"></a>Eliminación de una carpeta mediante EWS
<a name="bk_deletefolderews"> </a>

En este artículo se proporciona un ejemplo de XML básico en el que se muestra cómo eliminar una carpeta mediante EWS. Para obtener más información sobre cómo eliminar carpetas, vea [eliminar elementos mediante EWS en Exchange](deleting-items-by-using-ews-in-exchange.md).
  
Para eliminar una carpeta mediante EWS, primero envíe un mensaje de solicitud de la operación [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) para obtener la carpeta que se va a actualizar tal y como se muestra en [obtener una carpeta mediante EWS](#bk_getfolderews). 
  
A continuación, envíe un mensaje de solicitud de operación de [DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) al servidor para eliminar la carpeta. La solicitud de operación **DeleteFolder** indica que el **DeleteType** es **HardDelete** e incluye el [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) de la carpeta que se va a eliminar. 
  
También es la solicitud XML que la API administrada de EWS envía cuando se elimina una carpeta con el método [Folder. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) . Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura. 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:DeleteFolder DeleteType="HardDelete">
      <m:FolderIds>
        <t:FolderId Id="OrV9ZAAA=" ChangeKey="AQAAABYAAABVzRdyy/cHS4XTC9itCRdUAAAOrXWf" />
      </m:FolderIds>
    </m:DeleteFolder>
  </soap:Body>
</soap:Envelope>
```

El servidor responde a la solicitud **DeleteFolder** con un mensaje [DeleteFolderResponse](https://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx) que incluye el valor [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) de **NoError**, lo que indica que la eliminación de la carpeta se ha realizado correctamente.
  
## <a name="next-steps"></a>Pasos siguientes
<a name="bk_nextsteps"> </a>

Una vez que haya recuperado las carpetas en el servidor, o haya realizado cambios en las carpetas, es posible que desee [sincronizar la jerarquía de carpetas](how-to-synchronize-folders-by-using-ews-in-exchange.md) o [suscribirse a notificaciones sobre cambios de carpetas](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) en el servidor. 
  
## <a name="see-also"></a>Vea también

- [Carpetas y elementos de EWS en Exchange](folders-and-items-in-ews-in-exchange.md)   
- [Trabajar con elementos de buzón de Exchange mediante EWS en Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)    
- [Eliminación de elementos mediante EWS en Exchange](deleting-items-by-using-ews-in-exchange.md)   
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    

