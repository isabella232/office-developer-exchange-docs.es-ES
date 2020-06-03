---
title: Sincronizar elementos mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 886e7d35-9096-480b-8a8c-a7db27da06c2
description: Descubra cómo usar la API administrada de EWS o EWS para obtener una lista de todos los elementos de una carpeta o una lista de cambios que se han producido en una carpeta para sincronizar el cliente.
ms.openlocfilehash: e75f90b2d28d782465de89000796deccdd125e25
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527715"
---
# <a name="synchronize-items-by-using-ews-in-exchange"></a><span data-ttu-id="fdcda-103">Sincronizar elementos mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fdcda-103">Synchronize items by using EWS in Exchange</span></span>

<span data-ttu-id="fdcda-104">Descubra cómo usar la API administrada de EWS o EWS para obtener una lista de todos los elementos de una carpeta o una lista de cambios que se han producido en una carpeta para sincronizar el cliente.</span><span class="sxs-lookup"><span data-stu-id="fdcda-104">Find out how to use the EWS Managed API or EWS to get a list of all items in a folder, or a list of changes that have occurred in a folder, in order to synchronize your client.</span></span>
  
<span data-ttu-id="fdcda-105">EWS en Exchange usa sincronización de elementos y sincronización de carpetas para sincronizar el contenido del buzón entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="fdcda-105">EWS in Exchange uses item synchronization and folder synchronization to sync mailbox content between the client and server.</span></span> <span data-ttu-id="fdcda-106">La sincronización de elementos obtiene la lista inicial de elementos de una carpeta y, a continuación, a lo largo del tiempo, obtiene los cambios realizados en esos elementos y también obtiene los nuevos.</span><span class="sxs-lookup"><span data-stu-id="fdcda-106">Item synchronization gets the initial list of items in a folder and then, over time, gets changes that have been made to those items and gets new items as well.</span></span>
  
<span data-ttu-id="fdcda-107">Tenga en cuenta que antes de poder sincronizar elementos con un cliente, primero tiene que [sincronizar la jerarquía de carpetas](how-to-synchronize-folders-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="fdcda-107">Note that before you can sync items to a client, you first have to [sync the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="fdcda-108">Una vez que la jerarquía de carpetas está en su lugar en el cliente, si va a realizar la sincronización de elementos mediante la API administrada de EWS, primero [obtiene la lista inicial de elementos en la bandeja de entrada](#bk_cesyncongoingewsma) mediante el método [ExchangeService. SyncFolderItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="fdcda-108">After the folder hierarchy is in place on the client, if you're performing item synchronization by using the EWS Managed API, you first [get the initial list of items in the Inbox](#bk_cesyncongoingewsma) by using the [ExchangeService.SyncFolderItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="fdcda-109">A continuación, se actualiza el valor del parámetro _cSyncState_ durante las llamadas posteriores para obtener la lista de elementos modificados en la bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="fdcda-109">You then update the value of the  _cSyncState_ parameter during subsequent calls to get the list of changed items in the Inbox.</span></span> 
  
<span data-ttu-id="fdcda-110">Para realizar la sincronización de elementos mediante EWS, después de [sincronizar la jerarquía de carpetas](how-to-synchronize-folders-by-using-ews-in-exchange.md), debe solicitar la [lista inicial de elementos de la bandeja de entrada](#bk_ewsexamplea) mediante la [operación SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx), analizar la respuesta y, a continuación, en el futuro, [obtener los cambios en los elementos del buzón](#bk_ewsexamplec)y analizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fdcda-110">To perform item synchronization by using EWS, after you [sync the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md), you request the [initial list of items in the Inbox](#bk_ewsexamplea) by using the [SyncFolderItems operation](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx), parse the response, and then at some point in the future [get the changes to the items in the mailbox](#bk_ewsexamplec), and parse the response.</span></span> <span data-ttu-id="fdcda-111">Una vez que el cliente recibe la lista de elementos iniciales o modificados, [realiza las actualizaciones de forma local](#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="fdcda-111">After the client receives the list of initial or changed items, it [makes updates locally](#bk_nextsteps).</span></span> <span data-ttu-id="fdcda-112">Cómo y cuándo se recuperan los cambios en el futuro depende del [modelo de diseño de sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) que use la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fdcda-112">How and when you retrieve changes in the future depends on the [synchronization design pattern](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) your application is using.</span></span> 
  
## <a name="get-the-list-of-all-items-or-changed-items-by-using-the-ews-managed-api"></a><span data-ttu-id="fdcda-113">Obtener la lista de todos los elementos o elementos cambiados mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="fdcda-113">Get the list of all items or changed items by using the EWS Managed API</span></span>
<span data-ttu-id="fdcda-114"><a name="bk_cesyncongoingewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="fdcda-114"><a name="bk_cesyncongoingewsma"> </a></span></span>

<span data-ttu-id="fdcda-115">En el ejemplo de código siguiente se muestra cómo obtener una lista inicial de todos los elementos de la carpeta Bandeja de entrada y, a continuación, obtener una lista de los cambios en los elementos de la carpeta Bandeja de entrada que se han producido desde la última sincronización.</span><span class="sxs-lookup"><span data-stu-id="fdcda-115">The following code example shows how to get an initial list of all items in the Inbox folder and then get a list of changes to items in the Inbox folder that have occurred since the previous synchronization.</span></span> <span data-ttu-id="fdcda-116">Durante la llamada inicial al método [SyncFolderItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) , establezca el valor de _cSyncState_ en NULL.</span><span class="sxs-lookup"><span data-stu-id="fdcda-116">During the initial call to the [SyncFolderItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) method, set the  _cSyncState_ value to null.</span></span> <span data-ttu-id="fdcda-117">Cuando el método finalice, guarde el valor _cSyncState_ localmente para usarlo en la siguiente llamada al método **SyncFolderItems** .</span><span class="sxs-lookup"><span data-stu-id="fdcda-117">When the method completes, save the  _cSyncState_ value locally to use in the next **SyncFolderItems** method call.</span></span> <span data-ttu-id="fdcda-118">Tanto en la llamada inicial como en las llamadas posteriores, los elementos se recuperan en lotes de diez, mediante llamadas sucesivas al método **SyncFolderItems** , hasta que no quedan cambios.</span><span class="sxs-lookup"><span data-stu-id="fdcda-118">In both the initial call and the subsequent calls, the items are retrieved in batches of ten, by using successive calls to the **SyncFolderItems** method, until no more changes remain.</span></span> 
  
<span data-ttu-id="fdcda-119">En este ejemplo se establece el parámetro _propertySet_ en IdOnly para reducir las llamadas a la base de datos de Exchange, que es un [procedimiento recomendado de sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span><span class="sxs-lookup"><span data-stu-id="fdcda-119">This example sets the  _propertySet_ parameter to IdOnly to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="fdcda-120">En este ejemplo, se supone que el **servicio** es un enlace de objeto **ExchangeService** válido y que _cSyncState_ representa el estado de sincronización devuelto por una llamada anterior a **SyncFolderItems**.</span><span class="sxs-lookup"><span data-stu-id="fdcda-120">In this example, we assume that **service** is a valid **ExchangeService** object binding and that  _cSyncState_ represents the sync state that was returned by a prior call to **SyncFolderItems**.</span></span> 
  
```cs
// Track whether there are more items available for download on the server.
bool moreChangesAvailable = false;
do
{
    // Get a list of all items in the Inbox by calling SyncFolderHierarchy repeatedly until no more changes are available.
    // The folderId parameter must be set to the root folder to synchronize,
    // and must be same folder ID as used in previous synchronization calls. 
    // The propertySet parameter is set to IdOnly to reduce calls to the Exchange database,
    // because any additional properties result in additional calls to the Exchange database. 
    // The ignoredItemIds parameter is set to null, so that no items are ignored.
    // The maxChangesReturned parameter is set to return a maximum of 10 items (512 is the maximum).
    // The syncScope parameter is set to Normal items, so that associated items will not be returned.
    // The syncState parameter is set to cSyncState, which should be null in the initial call, 
    // and should be set to the sync state returned by the 
    // previous SyncFolderItems call in subsequent calls.
    ChangeCollection<ItemChange> icc = service.SyncFolderItems(new FolderId(WellKnownFolderName.Inbox), PropertySet.IdOnly, null, 10, SyncFolderItemsScope.NormalItems, cSyncState);
    // If the count of changes is zero, there are no changes to synchronize.
    if (icc.Count == 0)
    {
        Console.WriteLine("There are no item changes to synchronize.");
    }
    // Otherwise, write all the changes included in the response 
    // to the console. 
    else
    {
        foreach (ItemChange ic in icc)
        {
            Console.WriteLine("ChangeType: " + ic.ChangeType.ToString());
            Console.WriteLine("ItemId: " + ic.ItemId);
            Console.WriteLine("===========");
        }
    }
    // Save the sync state for use in future SyncFolderContent requests.
    // The sync state is used by the server to determine what changes to report
    // to the client.
    string sSyncState = icc.SyncState;
   // Determine whether more changes are available on the server.
   moreChangesAvailable = icc.MoreChangesAvailable;
}
while (moreChangesAvailable);

```

El método **SyncFolderItems** es similar al método [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) en el que no puede devolver propiedades como [Body](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx) o [Attachments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx). <span data-ttu-id="fdcda-122">Si necesita propiedades que el método **SyncFolderItems** no puede devolver, especifique la propiedad [IdOnly](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset.idonly%28v=exchg.80%29.aspx) establecida cuando llame a **SyncFolderItems**y, a continuación, use el método [ExchangeService. LoadPropertiesForItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) para obtener las propiedades que necesita para los elementos devueltos por el método **SyncFolderItems** .</span><span class="sxs-lookup"><span data-stu-id="fdcda-122">If you need properties that cannot be returned by the **SyncFolderItems** method, specify the [IdOnly](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset.idonly%28v=exchg.80%29.aspx) property set when you call **SyncFolderItems**, and then use the [ExchangeService.LoadPropertiesForItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) method to get the properties you require for the items that were returned by the **SyncFolderItems** method.</span></span> 
  
<span data-ttu-id="fdcda-123">Después de recuperar la lista de elementos nuevos o modificados en el servidor, [cree o actualice los elementos en el cliente](#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="fdcda-123">After you retrieve the list of new or changed items on the server, [create or update the items on the client](#bk_nextsteps).</span></span>
  
## <a name="get-the-initial-list-of-items-by-using-ews"></a><span data-ttu-id="fdcda-124">Obtener la lista inicial de elementos mediante EWS</span><span class="sxs-lookup"><span data-stu-id="fdcda-124">Get the initial list of items by using EWS</span></span>
<span data-ttu-id="fdcda-125"><a name="bk_ewsexamplea"> </a></span><span class="sxs-lookup"><span data-stu-id="fdcda-125"><a name="bk_ewsexamplea"> </a></span></span>

<span data-ttu-id="fdcda-126">En el ejemplo siguiente se muestra la solicitud XML para obtener la lista inicial de elementos de la bandeja de entrada mediante la [operación SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fdcda-126">The following example shows the XML request to get the initial list of items in the Inbox by using the [SyncFolderItems operation](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx).</span></span> <span data-ttu-id="fdcda-127">También es la solicitud XML que la API administrada de EWS envía al [recuperar la lista de elementos mediante el método SyncFolderItems](#bk_cesyncongoingewsma).</span><span class="sxs-lookup"><span data-stu-id="fdcda-127">This is also the XML request that the EWS Managed API sends when [retrieving the list of items by using the SyncFolderItems method](#bk_cesyncongoingewsma).</span></span> <span data-ttu-id="fdcda-128">El elemento [SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) de la operación **SyncFolderItems** no se incluye porque es la sincronización inicial.</span><span class="sxs-lookup"><span data-stu-id="fdcda-128">The [SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element of the **SyncFolderItems** operation is not included because this is the initial synchronization.</span></span> <span data-ttu-id="fdcda-129">En este ejemplo se establece el elemento [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) en **IdOnly** para reducir las llamadas a la base de datos de Exchange, que es un [procedimiento recomendado de sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span><span class="sxs-lookup"><span data-stu-id="fdcda-129">This example sets the [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span>
  
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
    <m:SyncFolderItems>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </m:ItemShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="inbox" />
      </m:SyncFolderId>
      <m:MaxChangesReturned>10</m:MaxChangesReturned>
      <m:SyncScope>NormalItems</m:SyncScope>
    </m:SyncFolderItems>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="fdcda-130"><a name="bk_responsesyncfolderitems"> </a></span><span class="sxs-lookup"><span data-stu-id="fdcda-130"><a name="bk_responsesyncfolderitems"> </a></span></span>

<span data-ttu-id="fdcda-131">En el ejemplo siguiente se muestra la respuesta XML que devuelve el servidor después de procesar la solicitud de operación **SyncFolderItems** desde el cliente.</span><span class="sxs-lookup"><span data-stu-id="fdcda-131">The following example shows the XML response that is returned by the server after it processes the **SyncFolderItems** operation request from the client.</span></span> <span data-ttu-id="fdcda-132">La respuesta inicial incluye los elementos [Create](https://msdn.microsoft.com/library/cb5e64a2-66a5-4447-921e-7c13efb8f6bf%28Office.15%29.aspx) para cinco elementos, ya que todos los elementos se consideran nuevos durante una sincronización inicial.</span><span class="sxs-lookup"><span data-stu-id="fdcda-132">The initial response includes [Create](https://msdn.microsoft.com/library/cb5e64a2-66a5-4447-921e-7c13efb8f6bf%28Office.15%29.aspx) elements for five items because all items are considered new during an initial synchronization.</span></span> <span data-ttu-id="fdcda-133">Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="fdcda-133">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
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
    <m:SyncFolderItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAA==</m:SyncState>
          <m:IncludesLastItemInRange>true</m:IncludesLastItemInRange>
          <m:Changes>
            <t:Create>
              <t:Message>
                <t:ItemId Id="q04QAAAA=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVdC"/>
              </t:Message>
            </t:Create>
            <t:Create>
              <t:Message>
                <t:ItemId Id="q07AAAAA=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVdB"/>
              </t:Message>
            </t:Create>
            <t:Create>
              <t:Message>
                <t:ItemId Id="q1AwAAAA=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVdA"/>
              </t:Message>
            </t:Create>
            <t:Create>
              <t:Message>
                <t:ItemId Id="AAMkADBh=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVc5"/>
              </t:Message>
            </t:Create>
            <t:Create>
              <t:Message>
                <t:ItemId Id="AAMkADBh=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVc4"/>
              </t:Message>
            </t:Create>
          </m:Changes>
        </m:SyncFolderItemsResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderItemsResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="fdcda-134">Después de recuperar la lista de nuevos elementos en el servidor, [cree los elementos en el cliente](#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="fdcda-134">After you retrieve the list of new items on the server, [create the items on the client](#bk_nextsteps).</span></span>
  
## <a name="get-the-changes-since-the-last-sync-by-using-ews"></a><span data-ttu-id="fdcda-135">Obtener los cambios desde la última sincronización mediante EWS</span><span class="sxs-lookup"><span data-stu-id="fdcda-135">Get the changes since the last sync by using EWS</span></span>
<span data-ttu-id="fdcda-136"><a name="bk_ewsexamplec"> </a></span><span class="sxs-lookup"><span data-stu-id="fdcda-136"><a name="bk_ewsexamplec"> </a></span></span>

<span data-ttu-id="fdcda-137">En el ejemplo siguiente se muestra la solicitud XML para obtener la lista de cambios realizados en los elementos de la bandeja de entrada mediante la operación [SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="fdcda-137">The following example shows the XML request to get the list of changes to items in the Inbox by using the [SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="fdcda-138">También es la solicitud XML que la API administrada de EWS envía al [recuperar la lista de cambios de la bandeja de entrada](#bk_cesyncongoingewsma).</span><span class="sxs-lookup"><span data-stu-id="fdcda-138">This is also the XML request that the EWS Managed API sends when [retrieving the list of changes to the Inbox](#bk_cesyncongoingewsma).</span></span> <span data-ttu-id="fdcda-139">En este ejemplo se establece el valor del elemento [SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) en el valor devuelto en la [respuesta anterior](#bk_responsesyncfolderitems).</span><span class="sxs-lookup"><span data-stu-id="fdcda-139">This example sets the [SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element value to the value returned in the [previous response](#bk_responsesyncfolderitems).</span></span> <span data-ttu-id="fdcda-140">Y con fines de demostración, en este ejemplo se establece el elemento [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) en **AllProperties** en lugar de **IdOnly** para mostrar las propiedades adicionales devueltas.</span><span class="sxs-lookup"><span data-stu-id="fdcda-140">And for demonstration purposes, this example sets the [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **AllProperties** instead of **IdOnly** to show the additional properties returned.</span></span> <span data-ttu-id="fdcda-141">La configuración del elemento [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) en **IdOnly** es un [procedimiento recomendado de sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span><span class="sxs-lookup"><span data-stu-id="fdcda-141">Setting the [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="fdcda-142">El valor de **SyncState** se ha abreviado para facilitar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="fdcda-142">The value of **SyncState** has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
      <t:RequestServerVersion Version="Exchange2010_SP2" />
  </soap:Header>
  <soap:Body>
    <m:SyncFolderItems>
      <m:ItemShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:ItemShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="inbox" />
      </m:SyncFolderId>
      <m:SyncState>H4sIAAA==</m:SyncState>
      <m:MaxChangesReturned>10</m:MaxChangesReturned>
      <m:SyncScope>NormalItems</m:SyncScope>
    </m:SyncFolderItems>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="fdcda-143">En el ejemplo siguiente se muestra la respuesta XML que devuelve el servidor después de procesar la solicitud de operación **SyncFolderItems** desde el cliente.</span><span class="sxs-lookup"><span data-stu-id="fdcda-143">The following example shows the XML response that is returned by the server after it processes the **SyncFolderItems** operation request from the client.</span></span> <span data-ttu-id="fdcda-144">Esta respuesta indica que se ha actualizado un elemento, se han creado dos elementos, se ha cambiado la marca de lectura de un elemento y un elemento se ha eliminado desde la sincronización previa.</span><span class="sxs-lookup"><span data-stu-id="fdcda-144">This response indicates that one item was updated, two items were created, the read flag of one item was changed, and one item was deleted since the prior synchronization.</span></span> <span data-ttu-id="fdcda-145">Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="fdcda-145">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="731" MinorBuildNumber="10" Version="V2_3"
                 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                 xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAAAAAAEAO29B2AcSZY==</m:SyncState>
          <m:IncludesLastItemInRange>true</m:IncludesLastItemInRange>
          <m:Changes>
            <t:Update>
                <t:Message>
                  <t:ItemId Id="q04QAAAA==" ChangeKey="CQAAABYAAADZGACZQpSgSpyNkexYe2b7AAAAird/" />
                  <t:ParentFolderId Id=" AgENAAAA" ChangeKey="AQAAAA==" />
                  <t:ItemClass>IPM.Note</t:ItemClass>
                  <t:Subject>RE: Company Soccer Team</t:Subject>
                  <t:Sensitivity>Normal</t:Sensitivity>
                  <t:DateTimeReceived>2013-08-29T15:22:10Z</t:DateTimeReceived>
                  <t:Size>23110</t:Size>
                  <t:Importance>Normal</t:Importance>
                  <t:InReplyTo>&amp;lt;8e084ea1a5b64f97b95fa8a863a5869d@CH1SR01MB001.namsdf01.sdf.contoso.com&amp;gt;</t:InReplyTo>
                  <t:IsSubmitted>false</t:IsSubmitted>
                  <t:IsDraft>false</t:IsDraft>
                  <t:IsFromMe>false</t:IsFromMe>
                  <t:IsResend>false</t:IsResend>
                  <t:IsUnmodified>false</t:IsUnmodified>
                  <t:DateTimeSent>2013-08-29T15:22:10Z</t:DateTimeSent>
                  <t:DateTimeCreated>2013-08-28T04:07:38Z</t:DateTimeCreated>
                  <t:DisplayCc />
                  <t:DisplayTo>All Employees</t:DisplayTo>
                  <t:HasAttachments>false</t:HasAttachments>
                  <t:Culture>en-US</t:Culture>
                  <t:EffectiveRights>
                    <t:CreateAssociated>false</t:CreateAssociated>
                    <t:CreateContents>false</t:CreateContents>
                    <t:CreateHierarchy>false</t:CreateHierarchy>
                    <t:Delete>true</t:Delete>
                    <t:Modify>true</t:Modify>
                    <t:Read>true</t:Read>
                    <t:ViewPrivateItems>true</t:ViewPrivateItems>
                  </t:EffectiveRights>
                  <t:LastModifiedName>Mara  Whitley</t:LastModifiedName>
                  <t:LastModifiedTime>2013-08-28T16:53:35Z</t:LastModifiedTime>
                  <t:IsAssociated>false</t:IsAssociated>
                  <t:WebClientReadFormQueryString>?ae=Item&amp;amp;a=Open&amp;amp;t=IPM.Note&amp;amp;id=&amp;amp;exvsurl=1</t:WebClientReadFormQueryString>
                  <t:ConversationId Id="AAQkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAQACAi+NTh0F5Eg5YDwpJsXPE=" />
                  <t:Sender>
                    <t:Mailbox>
                      <t:Name>Alfred  Welker </t:Name>
                      <t:EmailAddress>Alfred.Welker@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:Sender>
                  <t:IsReadReceiptRequested>false</t:IsReadReceiptRequested>
                  <t:ConversationIndex>AQHM5V/ZICL41OHQXkSDlgPCkmxc8ZYxA3I4gAAP5UeAANHpbIAAEE+0gAABYhSAACGYTIAAA2+vgAAE81qAkhv0Eg==</t:ConversationIndex>
                  <t:ConversationTopic>Company Soccer Team</t:ConversationTopic>
                  <t:From>
                    <t:Mailbox>
                      <t:Name>Alfred  Welker </t:Name>
                      <t:EmailAddress>Alfred.Welker@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:From>
                  <t:InternetMessageId>&amp;lt;e5919a09c8fc4d64b6ffd3542e194fc3@BY2SR01MB609.contoso.com&amp;gt;</t:InternetMessageId>
                  <t:IsRead>true</t:IsRead>
                  <t:References>namsdf01.sdf.contoso.com&amp;gt;</t:References>
                </t:Message>
            </t:Update>
            <t:Create>
              <t:Message>
                <t:ItemId Id="AQMkAD+" />
                <t:ParentFolderId Id="AQMkA==" ChangeKey="AQAAAA==" />
                <t:ItemClass>IPM.Note</t:ItemClass>
                  <t:Subject>RE: Review Proposal for Contoso</t:Subject>
                  <t:Sensitivity>Normal</t:Sensitivity>
                  <t:DateTimeReceived>2013-08-29T16:20:10Z</t:DateTimeReceived>
                  <t:Size>32515</t:Size>
                  <t:Importance>Normal</t:Importance>
                  <t:InReplyTo>&amp;lt;e52a4de6b98d484887e141da094a2ce6@SN2SR01MB006.contoso.com&amp;gt;</t:InReplyTo>
                  <t:IsSubmitted>false</t:IsSubmitted>
                  <t:IsDraft>false</t:IsDraft>
                  <t:IsFromMe>false</t:IsFromMe>
                  <t:IsResend>false</t:IsResend>
                  <t:IsUnmodified>false</t:IsUnmodified>
                  <t:DateTimeSent>2013-08-29T16:20:10Z</t:DateTimeSent>
                  <t:DateTimeCreated>2013-08-28T04:07:33Z</t:DateTimeCreated>
                  <t:DisplayCc />
                  <t:DisplayTo>Legal Team; Executives</t:DisplayTo>
                  <t:HasAttachments>false</t:HasAttachments>
                  <t:Culture>en-US</t:Culture>
                  <t:EffectiveRights>
                    <t:CreateAssociated>false</t:CreateAssociated>
                    <t:CreateContents>false</t:CreateContents>
                    <t:CreateHierarchy>false</t:CreateHierarchy>
                    <t:Delete>true</t:Delete>
                    <t:Modify>true</t:Modify>
                    <t:Read>true</t:Read>
                    <t:ViewPrivateItems>true</t:ViewPrivateItems>
                  </t:EffectiveRights>
                  <t:LastModifiedName>Mara  Whitley</t:LastModifiedName>
                  <t:LastModifiedTime>2013-08-28T04:07:35Z</t:LastModifiedTime>
                  <t:IsAssociated>false</t:IsAssociated>
                  <t:WebClientReadFormQueryString>?ae=Item&amp;amp;a=Open&amp;amp;t=IPM.Note&amp;amp;id=&amp;amp;exvsurl=1</t:WebClientReadFormQueryString>
                  <t:ConversationId Id="AAQkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAQAIsBEZp25UpElByLLUQFH6Q=" />
                  <t:Sender>
                    <t:Mailbox>
                      <t:Name>Hope Gross</t:Name>
                      <t:EmailAddress>Hope.Gross@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:Sender>
                  <t:IsReadReceiptRequested>false</t:IsReadReceiptRequested>
                  <t:ConversationIndex>AQHM5WBRiwERmnblSkSUHIstRAUfpJYw9fbSgAAAdm2AAAB6koAAAHTDgAADl6+AAAbxCYAABm5PgAACSA+AANx034AAEKGQgAAAfsiAAB7m3IAABG+ngAABPZyAAASUzoAAA2DNgAAAfKE=</t:ConversationIndex>
                  <t:ConversationTopic>Review Proposal for Contoso</t:ConversationTopic>
                  <t:From>
                    <t:Mailbox>
                      <t:Name>Hope Gross</t:Name>
                      <t:EmailAddress>Hope.Gross@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:From>
                  <t:InternetMessageId>&amp;lt;bcdb185495834370a874a1e7ebedbb96@SN2SR01MB005.namsdf01.sdf.contoso.com&amp;gt;</t:InternetMessageId>
                  <t:IsRead>true</t:IsRead>
                  <t:References>&amp;lt;2d4d7d…</t:References>
                </t:Message>
              </t:Create>
              <t:Create>
                <t:Message>
                  <t:ItemId Id="Q04AAAAA==" ChangeKey="AAAirbnd" />
                  <t:ParentFolderId Id="AgENAAAA" ChangeKey="AQAAAA==" />
                  <t:ItemClass>IPM.Note</t:ItemClass>
                  <t:Subject>RE: Review Proposal for Contoso</t:Subject>
                  <t:Sensitivity>Normal</t:Sensitivity>
                  <t:DateTimeReceived>2013-08-29T15:30:10Z</t:DateTimeReceived>
                  <t:Size>29518</t:Size>
                  <t:Importance>Normal</t:Importance>
                  <t:InReplyTo>&amp;lt;f0db3ead01db4fe087d98022149aa16f@SN2SR01MB001.namsdf01.sdf.contoso.com&amp;gt;</t:InReplyTo>
                  <t:IsSubmitted>false</t:IsSubmitted>
                  <t:IsDraft>false</t:IsDraft>
                  <t:IsFromMe>false</t:IsFromMe>
                  <t:IsResend>false</t:IsResend>
                  <t:IsUnmodified>false</t:IsUnmodified>
                  <t:DateTimeSent>2013-08-29T15:30:10Z</t:DateTimeSent>
                  <t:DateTimeCreated>2013-08-28T04:07:36Z</t:DateTimeCreated>
                  <t:DisplayCc />
                  <t:DisplayTo>Legal Team; Executives</t:DisplayTo>
                  <t:HasAttachments>false</t:HasAttachments>
                  <t:Culture>en-US</t:Culture>
                  <t:EffectiveRights>
                    <t:CreateAssociated>false</t:CreateAssociated>
                    <t:CreateContents>false</t:CreateContents>
                    <t:CreateHierarchy>false</t:CreateHierarchy>
                    <t:Delete>true</t:Delete>
                    <t:Modify>true</t:Modify>
                    <t:Read>true</t:Read>
                    <t:ViewPrivateItems>true</t:ViewPrivateItems>
                  </t:EffectiveRights>
                  <t:LastModifiedName>Mara Whitley</t:LastModifiedName>
                  <t:LastModifiedTime>2013-08-28T04:07:38Z</t:LastModifiedTime>
                  <t:IsAssociated>false</t:IsAssociated>
                  <t:WebClientReadFormQueryString>?ae=Item&amp;amp;a=Open&amp;amp;t=IPM.Note&amp;amp;id=&amp;amp;exvsurl=1</t:WebClientReadFormQueryString>
                  <t:ConversationId Id="AAQkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAQAIsBEZp25UpElByLLUQFH6Q=" />
                  <t:Sender>
                    <t:Mailbox>
                      <t:Name>Mack Chaves</t:Name>
                      <t:EmailAddress>Mack.Chaves@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:Sender>
                  <t:IsReadReceiptRequested>false</t:IsReadReceiptRequested>
                  <t:ConversationIndex>AQHM5WBRiwERmnblSkSUHIstRAUfpJYw9fbSgAAAdm2AAAB6koAAAHTDgAADl6+AAAbxCYAABm5PgAACSA+AANx034AAEKGQgAAAfsiAAB7m3IAABG+ngAABPZyAAASUzoAAA2DN</t:ConversationIndex>
                  <t:ConversationTopic>Review Proposal for Contoso</t:ConversationTopic>
                  <t:From>
                    <t:Mailbox>
                      <t:Name>Mack Chaves</t:Name>
                      <t:EmailAddress>Mack.Chaves@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:From>
                  <t:InternetMessageId>&amp;lt;e52a4de6b98d484887e141da094a2ce6@SN2SR01MB006.namsdf01.sdf.contoso.com&amp;gt;</t:InternetMessageId>
                  <t:IsRead>true</t:IsRead>
                  <t:References>namsdf01.sdf.contoso.com&amp;gt;</t:References>
                </t:Message>
              </t:Create>
              <t:ReadFlagChange>
                <t:ItemId Id=" q07AAAAA==" ChangeKey="CQAAAA==" />
                <t:IsRead>true</t:IsRead>
              </t:ReadFlagChange>
              <t:Delete>
                <t:ItemId Id=" q1AwAAAA==" ChangeKey="CQAAAA==" />
              </t:Delete>
          </m:Changes>
        </m:SyncFolderItemsResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderItemsResponse>
  </s:Body>
</s:Envelope>
```

La operación **SyncFolderItems** es similar al método [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) que no puede devolver elementos como el [cuerpo](https://msdn.microsoft.com/library/7851ea9b-9f87-4adc-a26f-7a27df4a9bca%28Office.15%29.aspx) o los elementos [adjuntos](https://msdn.microsoft.com/library/b470e614-34bb-44f0-8790-7ddbdcbbd29d%28Office.15%29.aspx) . <span data-ttu-id="fdcda-147">Si necesita propiedades que la operación **SyncFolderItems** no puede devolver, establezca el valor del elemento [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) en IdOnly cuando llame a **SyncFolderItems**y, a continuación, use la [operación GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) para obtener las propiedades que necesita para los elementos devueltos por la operación **SyncFolderItems** .</span><span class="sxs-lookup"><span data-stu-id="fdcda-147">If you need properties that cannot be returned by the **SyncFolderItems** operation, set the value of the [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to IdOnly when you call **SyncFolderItems**, and then use the [GetItem operation](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) to get the properties you require for the items that were returned by the **SyncFolderItems** operation.</span></span> 
  
<span data-ttu-id="fdcda-148">Después de recuperar la lista de elementos modificados en el servidor, [actualice los elementos en el cliente](#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="fdcda-148">After you retrieve the list of changed items on the server, [update the items on the client](#bk_nextsteps).</span></span>
  
## <a name="update-the-client"></a><span data-ttu-id="fdcda-149">Actualizar el cliente</span><span class="sxs-lookup"><span data-stu-id="fdcda-149">Update the client</span></span>
<span data-ttu-id="fdcda-150"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="fdcda-150"><a name="bk_nextsteps"> </a></span></span>

<span data-ttu-id="fdcda-151">Si está usando la API administrada de EWS, después de obtener la lista de elementos nuevos o modificados, use el método [LoadPropertiesForItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) para obtener las propiedades de los elementos nuevos o modificados, compare las propiedades con los valores locales y actualice los elementos en el cliente.</span><span class="sxs-lookup"><span data-stu-id="fdcda-151">If you're using the EWS Managed API, after you get the list of new or changed items, use the [LoadPropertiesForItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) method to get properties on the new or changed items, compare the properties to the local values, and update the items on the client.</span></span> 
  
<span data-ttu-id="fdcda-152">Si está usando EWS, use la [operación GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) para obtener las propiedades de los elementos nuevos o modificados y actualizar los elementos en el cliente.</span><span class="sxs-lookup"><span data-stu-id="fdcda-152">If you're using EWS, use the [GetItem operation](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) to get properties on the new or changed items and update the items on the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fdcda-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="fdcda-153">See also</span></span>


- [<span data-ttu-id="fdcda-154">Sincronización de buzones de correo y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fdcda-154">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    
- [<span data-ttu-id="fdcda-155">Sincronización de carpetas mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fdcda-155">Synchronize folders by using EWS in Exchange</span></span>](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="fdcda-156">Controlar errores relacionados con la sincronización en EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fdcda-156">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="fdcda-157">Suscripciones de notificación, eventos de buzón y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fdcda-157">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    

