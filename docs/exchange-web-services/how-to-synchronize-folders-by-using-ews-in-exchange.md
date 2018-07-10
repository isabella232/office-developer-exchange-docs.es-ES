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
# <a name="synchronize-folders-by-using-ews-in-exchange"></a><span data-ttu-id="82558-103">Sincronizar carpetas mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="82558-103">Synchronize folders by using EWS in Exchange</span></span>

<span data-ttu-id="82558-104">Descubra cómo usar la API administrada de EWS o EWS para obtener una lista de carpetas, o una lista de carpetas que han cambiado, con el fin de sincronizar a su cliente.</span><span class="sxs-lookup"><span data-stu-id="82558-104">Find out how to use the EWS Managed API or EWS to get a list of folders, or a list of folders that have changed, in order to synchronize your client.</span></span>
  
<span data-ttu-id="82558-105">EWS en Exchange usa la sincronización de elementos y la sincronización de carpeta para sincronizar el contenido del buzón de correo entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="82558-105">EWS in Exchange uses item synchronization and folder synchronization to sync mailbox content between the client and server.</span></span> <span data-ttu-id="82558-106">Sincronización de carpetas Obtiene la lista inicial de las carpetas de una carpeta raíz y, a continuación, con el tiempo, obtiene los cambios que se han realizado en esas carpetas y obtiene así como las carpetas nuevas.</span><span class="sxs-lookup"><span data-stu-id="82558-106">Folder synchronization gets the initial list of folders from a root folder and then, over time, gets changes that were made to those folders and gets new folders as well.</span></span>
  
<span data-ttu-id="82558-107">Si está realizando la sincronización de carpetas mediante el uso de API administrada EWS, primera [obtener la lista inicial de carpetas en la carpeta raíz](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma) mediante el método [ExchangeService.SyncFolderHierarchy](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="82558-107">If you're performing folder synchronization by using the EWS Managed API, you first [get the initial list of folders in the root folder](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma) by using the [ExchangeService.SyncFolderHierarchy](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="82558-108">A continuación, actualiza el valor del parámetro _cSyncState_ durante las llamadas subsiguientes a obtener la lista de las carpetas nuevas y modificadas.</span><span class="sxs-lookup"><span data-stu-id="82558-108">You then update the value of the  _cSyncState_ parameter during subsequent calls to get the list of new and changed folders.</span></span> 
  
<span data-ttu-id="82558-109">Para realizar la sincronización de carpetas mediante el uso de EWS, solicitar la [lista inicial de las carpetas en la carpeta raíz](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncewsrequest) mediante la operación [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) , analizar la respuesta y, a continuación, en algún momento en el futuro [obtener los cambios a las carpetas en la raíz](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncrespews)y analizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="82558-109">To perform folder synchronization by using EWS, you request the [initial list of folders in the root folder](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncewsrequest) by using the [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation, parse the response, and then at some point in the future [get the changes to the folders in the root](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncrespews), and parse the response.</span></span> <span data-ttu-id="82558-110">Una vez que el cliente recibe la lista de carpetas iniciales o modificadas, se [realiza una actualización localmente](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="82558-110">After the client receives the list of initial or changed folders, it [makes updates locally](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span></span> <span data-ttu-id="82558-111">Cómo y cuándo recuperar los cambios en el futuro depende el [patrón de diseño de la sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) de que la aplicación usa.</span><span class="sxs-lookup"><span data-stu-id="82558-111">How and when you retrieve changes in the future depends on the [synchronization design pattern](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) your application is using.</span></span> 
  
## <a name="get-the-list-of-all-folders-or-changed-folders-by-using-the-ews-managed-api"></a><span data-ttu-id="82558-112">Obtener la lista de todas las carpetas o carpetas modificadas mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="82558-112">Get the list of all folders or changed folders by using the EWS Managed API</span></span>
<span data-ttu-id="82558-113"><a name="bk_cesyncinitialewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="82558-113"></span></span>

<span data-ttu-id="82558-114">En el ejemplo de código siguiente se muestra cómo obtener una lista inicial de las carpetas en una carpeta raíz y, a continuación, obtener una lista de los cambios realizados a las carpetas en la carpeta raíz que se han producido desde la sincronización anterior.</span><span class="sxs-lookup"><span data-stu-id="82558-114">The following code example shows how to get an initial list of folders in a root folder and then get a list of changes to folders in the root folder that have occurred since the previous synchronization.</span></span> <span data-ttu-id="82558-115">Durante la llamada inicial al método [ExchangeService.SyncFolderHierarchy](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) , establezca el valor de _cSyncState_ en null.</span><span class="sxs-lookup"><span data-stu-id="82558-115">During the initial call to the [ExchangeService.SyncFolderHierarchy](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) method, set the  _cSyncState_ value to null.</span></span> <span data-ttu-id="82558-116">Cuando finaliza el método, guarda el valor de _cSyncState_ localmente para usar en la siguiente llamada al método **SyncFolderHierarchy** .</span><span class="sxs-lookup"><span data-stu-id="82558-116">When the method completes, save the  _cSyncState_ value locally to use in the next **SyncFolderHierarchy** method call.</span></span> <span data-ttu-id="82558-117">En la llamada inicial y las llamadas subsiguientes, se recuperan las carpetas en lotes de diez, mediante el uso de las llamadas sucesivas al método **SyncFolderHierarchy** , hasta que no permanecen cambios más.</span><span class="sxs-lookup"><span data-stu-id="82558-117">In both the initial call and the subsequent calls, the folders are retrieved in batches of ten, by using successive calls to the **SyncFolderHierarchy** method, until no more changes remain.</span></span> <span data-ttu-id="82558-118">En este ejemplo se establece el parámetro _propertySet_ a IdOnly para reducir las llamadas a la base de datos de Exchange, que es una [práctica recomendada de sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span><span class="sxs-lookup"><span data-stu-id="82558-118">This example sets the  _propertySet_ parameter to IdOnly to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="82558-119">En este ejemplo, se supone que el **servicio** es un enlace de objeto **ExchangeService** válido y que _cSyncState_ representa el estado de sincronización que se ha devuelto por una llamada anterior a **SyncFolderHierarchy**.</span><span class="sxs-lookup"><span data-stu-id="82558-119">In this example, we assume that **service** is a valid **ExchangeService** object binding and that  _cSyncState_ represents the sync state that was returned by a prior call to **SyncFolderHierarchy**.</span></span> 
  
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

<span data-ttu-id="82558-120">Después de recuperar la lista de carpetas nuevas o modificadas en el servidor, [crear o actualizar las carpetas en el cliente](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="82558-120">After you retrieve the list of new or changed folders on the server, [create or update the folders on the client](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span></span>
  
## <a name="get-the-initial-list-of-folders-by-using-ews"></a><span data-ttu-id="82558-121">Obtener la lista inicial de las carpetas mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="82558-121">Get the initial list of folders by using EWS</span></span>
<span data-ttu-id="82558-122"><a name="bk_cesyncewsrequest"> </a></span><span class="sxs-lookup"><span data-stu-id="82558-122"></span></span>

<span data-ttu-id="82558-123">En el ejemplo siguiente se muestra una solicitud XML para obtener la jerarquía de carpetas inicial mediante la operación [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="82558-123">The following example shows an XML request to get the initial folder hierarchy by using the [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="82558-124">Esto también es la solicitud XML que la API administrada de EWS envía al [recuperar la lista de carpetas iniciales mediante el método SyncFolderHierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma).</span><span class="sxs-lookup"><span data-stu-id="82558-124">This is also the XML request that the EWS Managed API sends when [retrieving the list of initial folders by using the SyncFolderHierarchy method](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma).</span></span> <span data-ttu-id="82558-125">No se incluye el elemento de [estado de sincronización](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) de la operación [SyncFolderHierarchy](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) debido a que se trata de la sincronización inicial.</span><span class="sxs-lookup"><span data-stu-id="82558-125">The [SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element of the [SyncFolderHierarchy](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) operation is not included because this is the initial synchronization.</span></span> <span data-ttu-id="82558-126">En este ejemplo se establece el elemento de [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) a **IdOnly** para reducir las llamadas a la base de datos de Exchange, que es una [práctica recomendada de sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span><span class="sxs-lookup"><span data-stu-id="82558-126">This example sets the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span>
  
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

<span data-ttu-id="82558-127">En el ejemplo siguiente se muestra la respuesta XML que es devuelto por el servidor después de procesar la solicitud de operación [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="82558-127">The following example shows the XML response that is returned by the server after it processes the [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation request.</span></span> <span data-ttu-id="82558-128">La respuesta inicial incluye elementos de [crear](http://msdn.microsoft.com/library/6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1%28Office.15%29.aspx) para todas las carpetas debido a que todas las carpetas se consideran nueva durante la sincronización inicial.</span><span class="sxs-lookup"><span data-stu-id="82558-128">The initial response includes [Create](http://msdn.microsoft.com/library/6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1%28Office.15%29.aspx) elements for all folders because all folders are considered new during an initial synchronization.</span></span> <span data-ttu-id="82558-129">Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad y se han eliminado algunos bloques de **creación** del elemento por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="82558-129">The values of some attributes and elements have been shortened for readability, and some **Create** element blocks were removed for brevity.</span></span> 
  
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

<span data-ttu-id="82558-130">Después de recuperar la lista de las carpetas nuevas en el servidor, [crear las carpetas en el cliente](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="82558-130">After you retrieve the list of new folders on the server, [create the folders on the client](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span></span>
  
## <a name="get-the-changes-since-the-last-sync-by-using-ews"></a><span data-ttu-id="82558-131">Obtener los cambios realizados desde la última sincronización mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="82558-131">Get the changes since the last sync by using EWS</span></span>
<span data-ttu-id="82558-132"><a name="bk_cesyncrespews"> </a></span><span class="sxs-lookup"><span data-stu-id="82558-132"></span></span>

<span data-ttu-id="82558-133">En el ejemplo siguiente se muestra la solicitud XML para obtener la lista de los cambios realizados a las carpetas en la carpeta raíz mediante la operación [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="82558-133">The following example shows the XML request to get the list of changes to folders in the root folder by using the [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="82558-134">Esto también es la solicitud XML que la API administrada de EWS envía al [recuperar la lista de los cambios realizados en la carpeta raíz](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma).</span><span class="sxs-lookup"><span data-stu-id="82558-134">This is also the XML request that the EWS Managed API sends when [retrieving the list of changes to the root folder](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma).</span></span> <span data-ttu-id="82558-135">En este ejemplo se establece el valor del elemento de [estado de sincronización](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) en el valor devuelto en la respuesta anterior.</span><span class="sxs-lookup"><span data-stu-id="82558-135">This example sets the [SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element value to the value returned in the previous response.</span></span> <span data-ttu-id="82558-136">Y con fines de demostración, en este ejemplo se establece el elemento de [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) en **AllProperties** en lugar de **IdOnly** para mostrar las propiedades adicionales que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="82558-136">And for demonstration purposes, this example sets the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **AllProperties** instead of **IdOnly** to show the additional properties returned.</span></span> <span data-ttu-id="82558-137">Si se establece el elemento [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) en **IdOnly** es una [práctica recomendada de sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span><span class="sxs-lookup"><span data-stu-id="82558-137">Setting the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="82558-138">El valor de **estado de sincronización** se ha acortado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="82558-138">The value of **SyncState** has been shortened for readability.</span></span> 
  
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

<span data-ttu-id="82558-139">En el ejemplo siguiente se muestra la respuesta XML que es devuelto por el servidor después de procesar la solicitud de [operación SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) desde el cliente.</span><span class="sxs-lookup"><span data-stu-id="82558-139">The following example shows the XML response that is returned by the server after it processes the [SyncFolderHierarchy operation](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) request from the client.</span></span> <span data-ttu-id="82558-140">Esta respuesta indica que se ha actualizado una carpeta, se creó una carpeta y se ha eliminado una carpeta desde la sincronización anterior.</span><span class="sxs-lookup"><span data-stu-id="82558-140">This response indicates that one folder was updated, one folder was created, and one folder was deleted since the prior synchronization.</span></span> <span data-ttu-id="82558-141">El valor del elemento de [estado de sincronización](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) , atributos **Id** y **ChangeKey** atributos se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="82558-141">The value of the [SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element, **Id** attributes, and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
<span data-ttu-id="82558-142">Recuerde que la solicitud incluye el **AllProperties**[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="82558-142">Remember that the request included the **AllProperties**[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx).</span></span> <span data-ttu-id="82558-143">Esto es sólo para fines de demostración.</span><span class="sxs-lookup"><span data-stu-id="82558-143">This is just for demonstration purposes.</span></span> <span data-ttu-id="82558-144">Se recomienda establecer el elemento de **BaseShape** a **IdOnly** en producción.</span><span class="sxs-lookup"><span data-stu-id="82558-144">We recommend that you set the **BaseShape** element to **IdOnly** in production.</span></span> 
  
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

## <a name="update-the-client"></a><span data-ttu-id="82558-145">Actualizar el cliente</span><span class="sxs-lookup"><span data-stu-id="82558-145">Update the client</span></span>
<span data-ttu-id="82558-146"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="82558-146"></span></span>

<span data-ttu-id="82558-147">Si está utilizando la API administrada de EWS, después de obtener la lista de carpetas nuevas o modificadas, use el método [Folder.Load](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.folder.load%28v=exchg.80%29.aspx) para obtener las propiedades en los elementos nuevos o modificados, compare las propiedades con los valores locales y actualizar o crear las carpetas en el cliente.</span><span class="sxs-lookup"><span data-stu-id="82558-147">If you're using the EWS Managed API, after you get the list of new or changed folders, use the [Folder.Load](http://msdn.microsoft.com/es-es/library/microsoft.exchange.webservices.data.folder.load%28v=exchg.80%29.aspx) method to get properties on the new or changed items, compare the properties to the local values, and update or create the folders on the client.</span></span> 
  
<span data-ttu-id="82558-148">Si está usando EWS, use la [operación GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) para obtener las propiedades en las carpetas nuevas o modificadas y actualizar o crear las carpetas en el cliente.</span><span class="sxs-lookup"><span data-stu-id="82558-148">If you're using EWS, use the [GetFolder operation](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) to get properties on the new or changed folders and update or create the folders on the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82558-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="82558-149">See also</span></span>

- [<span data-ttu-id="82558-150">Sincronización de buzón de correo y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="82558-150">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)   
- [<span data-ttu-id="82558-151">Sincronizar elementos mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="82558-151">Synchronize items by using EWS in Exchange</span></span>](how-to-synchronize-items-by-using-ews-in-exchange.md)   
- [<span data-ttu-id="82558-152">Tratamiento de errores relacionados con la sincronización en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="82558-152">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    

