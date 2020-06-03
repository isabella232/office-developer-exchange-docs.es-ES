---
title: Trabajar con elementos de buzón de Exchange mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 721deb84-f85d-45d0-84c1-0ed55f359969
description: Obtenga información sobre cómo crear, obtener, actualizar y eliminar elementos con la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: e86affbe8efe0dfc312f5ed5fadec2547f1352ea
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527589"
---
# <a name="work-with-exchange-mailbox-items-by-using-ews-in-exchange"></a><span data-ttu-id="27264-103">Trabajar con elementos de buzón de Exchange mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="27264-103">Work with Exchange mailbox items by using EWS in Exchange</span></span>

<span data-ttu-id="27264-104">Obtenga información sobre cómo crear, obtener, actualizar y eliminar elementos con la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="27264-104">Learn how to create, get, update, and delete items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="27264-105">Puede usar la API administrada de EWS o EWS para trabajar con elementos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="27264-105">You can use the EWS Managed API or EWS to work with items in a mailbox.</span></span> <span data-ttu-id="27264-106">Puede usar elementos genéricos (objetos de [elemento](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) de la API administrada de EWS o tipos de [elementos](https://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx) EWS) para realizar algunas operaciones (obtener un elemento o eliminar un elemento mediante el identificador del elemento); sin embargo, la mayoría de las veces tendrá que usar un [elemento con establecimiento inflexible de tipos](folders-and-items-in-ews-in-exchange.md#bk_item) para realizar una operación de obtención o actualización, ya que necesitará tener acceso a las propiedades que son específicas del elemento con establecimiento inflexible de tipos.</span><span class="sxs-lookup"><span data-stu-id="27264-106">You can use generic items — EWS Managed API [Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) objects or EWS [Item](https://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx) types — to perform some operations (getting an item or deleting an item by using the item's identifier); however, most of the time you'll have to use a [strongly typed item](folders-and-items-in-ews-in-exchange.md#bk_item) to perform a get or update operation because you'll need access to the properties that are specific to the strongly typed item.</span></span> 

<span data-ttu-id="27264-107">Por ejemplo, no puede usar un elemento genérico para recuperar un elemento que contenga una fecha de inicio y de finalización, necesita un objeto de [cita](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) de API administrada EWS o un tipo [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) de EWS para ello.</span><span class="sxs-lookup"><span data-stu-id="27264-107">For example, you can't use a generic item to retrieve an item that contains a start and end date - you need an EWS Managed API [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object or an EWS [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) type to do that.</span></span> <span data-ttu-id="27264-108">Y, si usa la API administrada de EWS, siempre tendrá que crear elementos con establecimiento inflexible de tipos, ya que la clase de **elemento** genérico no tiene un constructor.</span><span class="sxs-lookup"><span data-stu-id="27264-108">And if you're using the EWS Managed API, you always have to create strongly typed items, because the generic **Item** class does not have a constructor.</span></span> <span data-ttu-id="27264-109">Si está trabajando con un elemento que no tiene establecimiento inflexible de tipos, puede usar siempre la clase de **elemento** base para trabajar con el elemento.</span><span class="sxs-lookup"><span data-stu-id="27264-109">If you're working with an item that is not strongly typed, you can always use the base **Item** class to work with the item.</span></span> 
  
<span data-ttu-id="27264-110">**Tabla 1. Métodos de API administrada de EWS y operaciones de EWS para trabajar con elementos**</span><span class="sxs-lookup"><span data-stu-id="27264-110">**Table 1. EWS Managed API methods and EWS operations for working with items**</span></span>

|<span data-ttu-id="27264-111">**Para**</span><span class="sxs-lookup"><span data-stu-id="27264-111">**In order to…**</span></span>|<span data-ttu-id="27264-112">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="27264-112">**EWS Managed API method**</span></span>|<span data-ttu-id="27264-113">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="27264-113">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="27264-114">Crear un elemento genérico</span><span class="sxs-lookup"><span data-stu-id="27264-114">Create a generic item</span></span>  <br/> |<span data-ttu-id="27264-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="27264-115">None.</span></span> <span data-ttu-id="27264-116">Solo se pueden crear tipos de elementos específicos mediante la API administrada de EWS; no se pueden crear elementos genéricos.</span><span class="sxs-lookup"><span data-stu-id="27264-116">You can only create specific item types by using the EWS Managed API; you cannot create generic items.</span></span>  <br/> |[<span data-ttu-id="27264-117">CreateItem</span><span class="sxs-lookup"><span data-stu-id="27264-117">CreateItem</span></span>](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="27264-118">Obtener un elemento</span><span class="sxs-lookup"><span data-stu-id="27264-118">Get an item</span></span>  <br/> |[<span data-ttu-id="27264-119">Item. bind</span><span class="sxs-lookup"><span data-stu-id="27264-119">Item.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="27264-120">GetItem</span><span class="sxs-lookup"><span data-stu-id="27264-120">GetItem</span></span>](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="27264-121">Actualizar un elemento</span><span class="sxs-lookup"><span data-stu-id="27264-121">Update an item</span></span>  <br/> |[<span data-ttu-id="27264-122">Item. Update</span><span class="sxs-lookup"><span data-stu-id="27264-122">Item.Update</span></span>](https://msdn.microsoft.com/library/office/dd635915%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="27264-123">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="27264-123">UpdateItem</span></span>](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="27264-124">Eliminar un elemento</span><span class="sxs-lookup"><span data-stu-id="27264-124">Delete an item</span></span>  <br/> |[<span data-ttu-id="27264-125">Item. Delete</span><span class="sxs-lookup"><span data-stu-id="27264-125">Item.Delete</span></span>](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="27264-126">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="27264-126">DeleteItem</span></span>](../web-service-reference/deleteitem-operation.md) <br/> |
   
<span data-ttu-id="27264-127">En este artículo, aprenderá a usar la clase base genérica y cuando necesite usar un elemento con establecimiento inflexible de tipos para completar la tarea.</span><span class="sxs-lookup"><span data-stu-id="27264-127">In this article, you'll learn when you can use the generic base class and when you need to use a strongly typed item to complete your task.</span></span> <span data-ttu-id="27264-128">En los ejemplos de código se muestra cómo usar la clase base y qué hacer cuando no se puede usar la clase base o no se ajusta a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="27264-128">The code examples will show you how to use the base class, and what to do when you can't use the base class or it doesn't fit your needs.</span></span>
  
## <a name="create-an-item-by-using-the-ews-managed-api"></a><span data-ttu-id="27264-129">Crear un elemento mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="27264-129">Create an item by using the EWS Managed API</span></span>
<span data-ttu-id="27264-130"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="27264-130"><a name="bk_createewsma"> </a></span></span>

<span data-ttu-id="27264-131">La API administrada de EWS no tiene un constructor disponible públicamente para la clase de [elemento](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) , por lo que debe usar el constructor para el tipo de elemento específico que desea crear para crear un elemento.</span><span class="sxs-lookup"><span data-stu-id="27264-131">The EWS Managed API does not have a publicly available constructor for the [Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) class, so you must use the constructor for the specific item type you want to create in order to create an item.</span></span> <span data-ttu-id="27264-132">Por ejemplo, use el [constructor de la clase EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) para crear un nuevo mensaje de correo electrónico y el [constructor de clase Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) para crear un contacto nuevo.</span><span class="sxs-lookup"><span data-stu-id="27264-132">For example, use the [EmailMessage class constructor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) to create a new email message, and the [Contact class constructor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) to create a new contact.</span></span> <span data-ttu-id="27264-133">Del mismo modo, el servidor nunca devuelve objetos de **elementos** genéricos en las respuestas; todos los elementos genéricos se devuelven como objetos **EmailMessage** .</span><span class="sxs-lookup"><span data-stu-id="27264-133">Likewise, the server never returns generic **Item** objects in responses; all generic items are returned as **EmailMessage** objects.</span></span> 
  
<span data-ttu-id="27264-134">Cuando conoce el tipo de elemento que se va a crear, puede completar la tarea en tan solo unos pocos pasos.</span><span class="sxs-lookup"><span data-stu-id="27264-134">When you know the type of item to create, you can complete the task in just a few steps.</span></span> <span data-ttu-id="27264-135">Los pasos son similares para todos los tipos de elementos:</span><span class="sxs-lookup"><span data-stu-id="27264-135">The steps are similar for all item types:</span></span>
  
1. <span data-ttu-id="27264-136">Inicialice una nueva instancia de una de las clases de [elemento](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) con el objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) como parámetro.</span><span class="sxs-lookup"><span data-stu-id="27264-136">Initialize a new instance of one of the [Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) classes with the [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object as a parameter.</span></span> 
    
2. <span data-ttu-id="27264-137">Establecer propiedades en el elemento.</span><span class="sxs-lookup"><span data-stu-id="27264-137">Set properties on the item.</span></span> <span data-ttu-id="27264-138">Los esquemas son distintos para cada tipo de elemento, por lo que hay distintas propiedades disponibles para los distintos elementos.</span><span class="sxs-lookup"><span data-stu-id="27264-138">The schemas are different for each item type, so different properties are available for different items.</span></span>
    
3. <span data-ttu-id="27264-139">Guarda el elemento o guarda y envía el elemento.</span><span class="sxs-lookup"><span data-stu-id="27264-139">Save the item, or save and send the item.</span></span>
    
<span data-ttu-id="27264-140">Por ejemplo, puede crear un objeto [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) , establecer las propiedades [Subject](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.subject%28v=exchg.80%29.aspx), [Body](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx)y [ToRecipients](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.torecipients%28v=exchg.80%29.aspx) y, a continuación, enviarlo mediante el método [EmailMessage. SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="27264-140">For example, you can create an [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object, set the [Subject](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.subject%28v=exchg.80%29.aspx), [Body](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx), and [ToRecipients](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.torecipients%28v=exchg.80%29.aspx) properties, and then send it by using the [EmailMessage.SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method.</span></span> 
  
```cs
// Create an email message and provide it with connection 
// configuration information by using an ExchangeService object named service.
EmailMessage message = new EmailMessage(service);
// Set properties on the email message.
message.Subject = "Company Soccer Team";
message.Body = "Are you interested in joining?";
message.ToRecipients.Add("sadie@contoso.com");
// Send the email message and save a copy.
// This method call results in a CreateItem call to EWS.
message.SendAndSaveCopy();
```

<span data-ttu-id="27264-141">Para obtener información sobre cómo crear un elemento de reunión o cita mediante la API administrada de EWS, vea [crear citas y reuniones mediante EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span><span class="sxs-lookup"><span data-stu-id="27264-141">To learn how to create a meeting or appointment item by using the EWS Managed API, see [Create appointments and meetings by using EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span></span>
  
## <a name="create-an-item-by-using-ews"></a><span data-ttu-id="27264-142">Crear un elemento mediante EWS</span><span class="sxs-lookup"><span data-stu-id="27264-142">Create an item by using EWS</span></span>
<span data-ttu-id="27264-143"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="27264-143"><a name="bk_createews"> </a></span></span>

<span data-ttu-id="27264-144">Puede crear un elemento genérico o un elemento con establecimiento inflexible de tipos mediante EWS.</span><span class="sxs-lookup"><span data-stu-id="27264-144">You can create a generic item or a strongly typed item by using EWS.</span></span> <span data-ttu-id="27264-145">Los pasos son similares para todos los tipos de elementos:</span><span class="sxs-lookup"><span data-stu-id="27264-145">The steps are similar for all item types:</span></span>
  
1. <span data-ttu-id="27264-146">Use la operación [CreateItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) para crear un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="27264-146">Use the [CreateItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) operation to create an item in the Exchange store.</span></span> 
    
2. <span data-ttu-id="27264-147">Use el elemento [Items](https://msdn.microsoft.com/library/0811a73e-bf1f-4889-9219-73902dd47639%28Office.15%29.aspx) para contener uno o más elementos que se van a crear.</span><span class="sxs-lookup"><span data-stu-id="27264-147">Use the [Items](https://msdn.microsoft.com/library/0811a73e-bf1f-4889-9219-73902dd47639%28Office.15%29.aspx) element to contain one or more items to create.</span></span> 
    
3. <span data-ttu-id="27264-148">Establecer propiedades en el elemento.</span><span class="sxs-lookup"><span data-stu-id="27264-148">Set properties on the item.</span></span>
    
<span data-ttu-id="27264-149">Por ejemplo, puede crear un mensaje de correo electrónico y enviarlo mediante el código del ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="27264-149">For example, you can create an email message and send it by using the code in the following example.</span></span> <span data-ttu-id="27264-150">También es la solicitud XML que la API administrada de EWS envía cuando se llama al método [SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="27264-150">This is also the XML request that the EWS Managed API sends when you call the [SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com </t:EmailAddress>
              </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="27264-151">El servidor responde a la solicitud **CreateItem** con un mensaje [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) de **NoError**, que indica que el correo electrónico se ha creado correctamente y el [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del mensaje recién creado.</span><span class="sxs-lookup"><span data-stu-id="27264-151">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
<span data-ttu-id="27264-152">Para obtener información sobre cómo crear un elemento de cita o reunión con EWS, vea [crear citas y reuniones mediante EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span><span class="sxs-lookup"><span data-stu-id="27264-152">To learn how to create a meeting or appointment item by using EWS, see [Create appointments and meetings by using EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span></span>
  
## <a name="get-an-item-by-using-the-ews-managed-api"></a><span data-ttu-id="27264-153">Obtener un elemento mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="27264-153">Get an item by using the EWS Managed API</span></span>
<span data-ttu-id="27264-154"><a name="bk_getewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="27264-154"><a name="bk_getewsma"> </a></span></span>

<span data-ttu-id="27264-155">Para usar la API administrada de EWS para obtener un elemento si conoce el [Item.ID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento que se va a recuperar, simplemente debe llamar a uno de los métodos de [enlace](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) en el elemento y se recuperará el elemento.</span><span class="sxs-lookup"><span data-stu-id="27264-155">To use the EWS Managed API to get an item if you know the [Item.Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to retrieve, you simply call one of the [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) methods on the item, and the item is retrieved.</span></span> <span data-ttu-id="27264-156">Como práctica recomendada, le recomendamos que limite las propiedades que se devuelven solo a las que son necesarias.</span><span class="sxs-lookup"><span data-stu-id="27264-156">As a best practice, we recommend that you limit the properties returned to only those that are required.</span></span> <span data-ttu-id="27264-157">En este ejemplo se devuelven la propiedad **ID** del elemento y la propiedad **Subject** .</span><span class="sxs-lookup"><span data-stu-id="27264-157">This example returns the item **Id** property and the **Subject** property.</span></span> 
  
<span data-ttu-id="27264-158">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="27264-158">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="27264-159">La variable local *Itemid* es el [identificador](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="27264-159">The local variable  *itemId*  is the [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to update.</span></span> 
  
```cs
// As a best practice, limit the properties returned to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ItemSchema.Subject);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId, propSet);

```

<span data-ttu-id="27264-160">Si está buscando un elemento que cumpla determinados criterios, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="27264-160">If you're searching for an item that meets specific criteria, do the following:</span></span>
  
1. <span data-ttu-id="27264-161">Enlazar a la carpeta que contiene los elementos que se van a obtener.</span><span class="sxs-lookup"><span data-stu-id="27264-161">Bind to the folder that contains the items to get.</span></span>
    
2. <span data-ttu-id="27264-162">Crea una instancia de [SearchFilter. SearchFilterCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) o un [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) para filtrar los elementos que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="27264-162">Instantiate a [SearchFilter.SearchFilterCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) or a [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) to filter the items to return.</span></span> 
    
3. <span data-ttu-id="27264-163">Cree una instancia de un objeto [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) o [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) para especificar el número de elementos que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="27264-163">Instantiate an [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) or [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) object to specify the number of items to return.</span></span> 
    
4. <span data-ttu-id="27264-164">Llame al método [ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) o [ExchangeService. FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="27264-164">Call the [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) or [ExchangeService.FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method.</span></span> 
    
<span data-ttu-id="27264-165">Por ejemplo, si desea recuperar los mensajes de correo electrónico no leídos en la bandeja de entrada, use el código del ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="27264-165">For example, if you want to retrieve unread email messages in the Inbox, use the code in the following example.</span></span> <span data-ttu-id="27264-166">En este ejemplo se usa un **SearchFilterCollection** para limitar los resultados del método **FindItems** a mensajes no leídos y se limita el **ItemView** para limitar los resultados a un elemento.</span><span class="sxs-lookup"><span data-stu-id="27264-166">This example uses a **SearchFilterCollection** to limit the results of the **FindItems** method to unread messages, and limits the **ItemView** to limit results to one item.</span></span> <span data-ttu-id="27264-167">Este código en concreto solo funciona en objetos [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) porque el valor [EmailMessageSchema. IsRead](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessageschema.isread%28v=exchg.80%29.aspx) forma parte de la **SearchFilter**.</span><span class="sxs-lookup"><span data-stu-id="27264-167">This particular code only works on [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) objects because the [EmailMessageSchema.IsRead](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessageschema.isread%28v=exchg.80%29.aspx) value is part of the **SearchFilter**.</span></span> 
  
```cs
// Bind the Inbox folder to the service object.
Folder inbox = Folder.Bind(service, WellKnownFolderName.Inbox);
// The search filter to get unread email.
SearchFilter sf = new SearchFilter.SearchFilterCollection(LogicalOperator.And, new SearchFilter.IsEqualTo(EmailMessageSchema.IsRead, false));
ItemView view = new ItemView(1);
// Fire the query for the unread items.
// This method call results in a FindItem call to EWS.
FindItemsResults<Item> findResults = service.FindItems(WellKnownFolderName.Inbox, sf, view);
```

<span data-ttu-id="27264-168">Como alternativa, puedes usar un [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) para limitar los resultados de la búsqueda, como se muestra en el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="27264-168">Alternatively, you can use a [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) to limit the results of the search as shown in the following code example.</span></span> <span data-ttu-id="27264-169">En este ejemplo, se usa el método [FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) para recuperar hasta cinco citas que se producen en los próximos 30 días.</span><span class="sxs-lookup"><span data-stu-id="27264-169">This example uses the [FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method to retrieve up to five appointments that occur in the next 30 days.</span></span> <span data-ttu-id="27264-170">Este código de curso solo funciona en los elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="27264-170">This code of course only works on calendar items.</span></span> 
  
```cs
// Initialize values for the start and end times, and the number of appointments to retrieve.
DateTime startDate = DateTime.Now;
DateTime endDate = startDate.AddDays(30);
const int NUM_APPTS = 5;
// Bind the Calendar folder to the service object.
// This method call results in a GetFolder call to EWS.
CalendarFolder calendar = CalendarFolder.Bind(service, WellKnownFolderName.Calendar, new PropertySet());
// Set the start and end time and number of appointments to retrieve.
CalendarView cView = new CalendarView(startDate, endDate, NUM_APPTS);
// Limit the properties returned to the appointment's subject, start time, and end time.
cView.PropertySet = new PropertySet(AppointmentSchema.Subject, AppointmentSchema.Start, AppointmentSchema.End);
// Retrieve a collection of appointments by using the calendar view.
// This method call results in a FindAppointments call to EWS.
FindItemsResults<Appointment> appointments = calendar.FindAppointments(cView);
```

<span data-ttu-id="27264-171">Tenga en cuenta que la información que devuelve el servidor en la respuesta del método de **enlace** es diferente de la información que devuelve el servidor para una respuesta del método **FindItem** o **FindAppointment** .</span><span class="sxs-lookup"><span data-stu-id="27264-171">Note that the information the server returns in the **Bind** method response is different than the information that the server returns for a **FindItem** or **FindAppointment** method response.</span></span> <span data-ttu-id="27264-172">El método **BIND** puede devolver todas las propiedades esquematizado, mientras que los métodos **FindItem** y **FindAppointment** no devuelven todas las propiedades de esquematizado.</span><span class="sxs-lookup"><span data-stu-id="27264-172">The **Bind** method can return all the schematized properties, whereas the **FindItem** and **FindAppointment** methods do not return all the schematized properties.</span></span> <span data-ttu-id="27264-173">Por lo tanto, si necesita acceso total al elemento, tendrá que usar el método **BIND** .</span><span class="sxs-lookup"><span data-stu-id="27264-173">So if you need full access to the item, you'll have to use the **Bind** method.</span></span> <span data-ttu-id="27264-174">Si no tiene el **identificador** de elemento del elemento que le gustaría recuperar, use los métodos **FindItem** o **FindAppointment** para recuperar el identificador y, a continuación, use el método **BIND** para recuperar las propiedades que necesita.</span><span class="sxs-lookup"><span data-stu-id="27264-174">If you don't have the item **Id** of the item you'd like to retrieve, use the **FindItem** or **FindAppointment** methods to retrieve the Id, and then use the **Bind** method to retrieve the properties you need.</span></span> 
  
<span data-ttu-id="27264-175">Para obtener información sobre cómo obtener un elemento de reunión o cita mediante la API administrada de EWS, vea [obtener citas y reuniones mediante EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="27264-175">To learn how to get a meeting or appointment item by using the EWS Managed API, see [Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="get-an-item-by-using-ews"></a><span data-ttu-id="27264-176">Obtener un elemento mediante EWS</span><span class="sxs-lookup"><span data-stu-id="27264-176">Get an item by using EWS</span></span>
<span data-ttu-id="27264-177"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="27264-177"><a name="bk_getews"> </a></span></span>

<span data-ttu-id="27264-178">Si conoce el elemento [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del elemento que se va a recuperar, puede obtener el elemento mediante la operación [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="27264-178">If you know the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the item to retrieve, you can get the item by using the [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) operation.</span></span> 
  
<span data-ttu-id="27264-179">En el ejemplo siguiente se muestra la solicitud XML para obtener el [asunto](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) de un elemento con un **Itemid**específico.</span><span class="sxs-lookup"><span data-stu-id="27264-179">The following example shows the XML request to get the [Subject](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) of an item with a specific **ItemId**.</span></span> <span data-ttu-id="27264-180">También es la solicitud XML que la API administrada de EWS envía cuando llama al método [BIND](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) en un **Itemid**.</span><span class="sxs-lookup"><span data-stu-id="27264-180">This is also the XML request that the EWS Managed API sends when calling the [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method on an **ItemId**.</span></span> <span data-ttu-id="27264-181">Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="27264-181">The values of some attributes and elements have been shortened for readability.</span></span>
  
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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="GJc/NAAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

En el ejemplo siguiente se muestra la respuesta XML que devuelve el servidor después de procesar la operación **GetItem** . La respuesta indica que el elemento se recuperó correctamente. <span data-ttu-id="27264-184">Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="27264-184">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
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
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="GJc/NAAA=" ChangeKey="CQAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAGJd9Z"/>
              <t:Subject>Company Soccer Team</t:Subject>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="27264-185">Si no conoce el elemento **Itemid** del elemento que desea recuperar, puede usar la operación [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para buscar el elemento.</span><span class="sxs-lookup"><span data-stu-id="27264-185">If you do not know the **ItemId** of the item you want to retrieve, you can use the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation to find the item.</span></span> <span data-ttu-id="27264-186">Para poder usar la operación **FindItem** , primero debe identificar la carpeta en la que está buscando.</span><span class="sxs-lookup"><span data-stu-id="27264-186">In order to use the **FindItem** operation, you must first identify the folder that you're searching.</span></span> <span data-ttu-id="27264-187">Puede identificar la carpeta con su **DistinguinguishedFolderName** o con el [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="27264-187">You can identify the folder by using its **DistinguinguishedFolderName** or by using the [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx).</span></span> <span data-ttu-id="27264-188">Puede usar las operaciones [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) o [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) para obtener la **FolderId** que necesita.</span><span class="sxs-lookup"><span data-stu-id="27264-188">You can use either the [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) or [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operations to get the **FolderId** you need.</span></span> <span data-ttu-id="27264-189">A continuación, use la operación **FindItem** para buscar en esa carpeta los resultados que coinciden con el filtro de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="27264-189">Then use the **FindItem** operation to search that folder for results that match the search filter.</span></span> <span data-ttu-id="27264-190">A diferencia de la API administrada de EWS, EWS no proporciona una operación de búsqueda independiente para las citas.</span><span class="sxs-lookup"><span data-stu-id="27264-190">Unlike the EWS Managed API, EWS does not provide a separate find operation for appointments.</span></span> <span data-ttu-id="27264-191">La operación **FindItem** recupera elementos de todos los tipos.</span><span class="sxs-lookup"><span data-stu-id="27264-191">The **FindItem** operation retrieves items of all types.</span></span> 
  
<span data-ttu-id="27264-192">En el siguiente ejemplo se muestra la solicitud de operación de **FINDITEM** XML que se envía al servidor para buscar citas en la carpeta calendario que se producen en los próximos 30 días.</span><span class="sxs-lookup"><span data-stu-id="27264-192">The following example shows the XML **FindItem** operation request that is sent to the server to find appointments in the Calendar folder that occur in the next 30 days.</span></span> <span data-ttu-id="27264-193">Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="27264-193">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView MaxEntriesReturned="5" StartDate="2013-10-16T17:04:28.722Z" EndDate="2013-11-15T18:04:28.722Z" />
      <m:ParentFolderIds>
        <t:FolderId Id="AAAEOAAA=" ChangeKey="AgAAABYAAAAqRr3mNdNMSasqx/o9J13UAAAAAAA3" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="27264-194">El servidor responde a la solicitud **FindItem** con un mensaje [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) que incluye el valor [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que la operación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="27264-194">The server responds to the **FindItem** request with a [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) message that includes the [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the operation completed successfully.</span></span> <span data-ttu-id="27264-195">Si alguno de los elementos del calendario cumple los criterios de filtrado, se incluyen en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27264-195">If any calendar items meet the filtering criteria, they are included in the response.</span></span>
  
<span data-ttu-id="27264-196">Tenga en cuenta que la información que devuelve el servidor en la respuesta de la operación **GetItem** es diferente de la información que devuelve el servidor en una respuesta de operación **FindItem** o **FindAppointment** .</span><span class="sxs-lookup"><span data-stu-id="27264-196">Note that the information the server returns in the **GetItem** operation response is different than the information the server returns in a **FindItem** or **FindAppointment** operation response.</span></span> <span data-ttu-id="27264-197">La operación **GetItem** puede devolver todas las propiedades esquematizado, mientras que las operaciones **FindItem** y **FindAppointment** no devuelven todas las propiedades de esquematizado.</span><span class="sxs-lookup"><span data-stu-id="27264-197">The **GetItem** operation can return all the schematized properties, whereas the **FindItem** and **FindAppointment** operations do not return all the schematized properties.</span></span> <span data-ttu-id="27264-198">Por lo tanto, si necesita acceso total al elemento, tendrá que usar la operación **GetItem** .</span><span class="sxs-lookup"><span data-stu-id="27264-198">So if you need full access to the item, you'll have to use the **GetItem** operation.</span></span> <span data-ttu-id="27264-199">Si no tiene el elemento **Itemid** del elemento que quiere recuperar, use las operaciones **FindItem** o **FindAppointment** para recuperar el **Itemid**y, a continuación, use la operación **GetItem** para recuperar los elementos que necesita.</span><span class="sxs-lookup"><span data-stu-id="27264-199">If you don't have the **ItemId** of the item you'd like to retrieve, use the **FindItem** or **FindAppointment** operations to retrieve the **ItemId**, and then use the **GetItem** operation to retrieve the elements you need.</span></span> 
  
<span data-ttu-id="27264-200">Para obtener información sobre cómo obtener un elemento de reunión o cita con EWS, vea [obtener citas y reuniones mediante EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="27264-200">To learn how to get a meeting or appointment item by using EWS, see [Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="update-an-item-by-using-the-ews-managed-api"></a><span data-ttu-id="27264-201">Actualizar un elemento mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="27264-201">Update an item by using the EWS Managed API</span></span>
<span data-ttu-id="27264-202"><a name="bk_updateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="27264-202"><a name="bk_updateewsma"> </a></span></span>

<span data-ttu-id="27264-203">Los pasos para actualizar un elemento mediante la API administrada de EWS son similares para todos los tipos de elementos; sin embargo, las propiedades de elemento son diferentes para cada tipo de elemento y el método [Update](https://msdn.microsoft.com/library/office/dd635915%28v=exchg.80%29.aspx) tiene muchos métodos sobrecargados para elegir.</span><span class="sxs-lookup"><span data-stu-id="27264-203">The steps to update an item by using the EWS Managed API are similar for all item types; however, the item properties are different for each item type, and the [Update](https://msdn.microsoft.com/library/office/dd635915%28v=exchg.80%29.aspx) method has many overloaded methods to choose from.</span></span> <span data-ttu-id="27264-204">Para actualizar un elemento:</span><span class="sxs-lookup"><span data-stu-id="27264-204">To update an item:</span></span> 
  
1. <span data-ttu-id="27264-205">Use el método [BIND](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) para obtener la versión más reciente del elemento, a menos que ya la tenga.</span><span class="sxs-lookup"><span data-stu-id="27264-205">Use the [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method to get the latest version of the item, unless you already have it.</span></span> <span data-ttu-id="27264-206">Para actualizar las propiedades específicas de un elemento con establecimiento inflexible de tipos, tendrá que enlazar a ese tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="27264-206">To update properties specific to a strongly typed item, you'll have to bind to that item type.</span></span> <span data-ttu-id="27264-207">Para actualizar las propiedades disponibles en el tipo de elemento genérico, puede enlazar al objeto de [elemento](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="27264-207">To update properties available on the generic item type, you can bind to the [Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) object.</span></span> 
    
2. <span data-ttu-id="27264-208">Actualice las propiedades del elemento.</span><span class="sxs-lookup"><span data-stu-id="27264-208">Update the properties on the item.</span></span>
    
3. <span data-ttu-id="27264-209">Llamar al método **Update** .</span><span class="sxs-lookup"><span data-stu-id="27264-209">Call the **Update** method.</span></span> 
    
<span data-ttu-id="27264-210">Por ejemplo, puede actualizar el asunto de un mensaje de correo electrónico usando el tipo de elemento genérico, como se muestra en el código del siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="27264-210">For example, you can update the subject of an email by using the generic item type, as shown in the code in the following example.</span></span>
  
<span data-ttu-id="27264-211">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="27264-211">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="27264-212">La variable local *Itemid* es el [identificador](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="27264-212">The local variable  *itemId*  is the [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to update.</span></span> 
  
```cs
// Bind to the existing item, using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId);
// Update the Subject of the email.
item.Subject = "New subject";
// Save the updated email.
// This method call results in an UpdateItem call to EWS.
item.Update(ConflictResolutionMode.AlwaysOverwrite);
```

<span data-ttu-id="27264-213">Para obtener información sobre cómo actualizar un elemento de reunión o cita mediante la API administrada de EWS, vea [actualizar citas y reuniones mediante EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="27264-213">To learn how to update a meeting or appointment item by using the EWS Managed API, see [Update appointments and meetings by using EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="update-an-item-by-using-ews"></a><span data-ttu-id="27264-214">Actualizar un elemento mediante EWS</span><span class="sxs-lookup"><span data-stu-id="27264-214">Update an item by using EWS</span></span>
<span data-ttu-id="27264-215"><a name="bk_updateews"> </a></span><span class="sxs-lookup"><span data-stu-id="27264-215"><a name="bk_updateews"> </a></span></span>

<span data-ttu-id="27264-216">Para actualizar un elemento mediante EWS, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="27264-216">To update an item by using EWS, do the following:</span></span>
  
1. <span data-ttu-id="27264-217">Use la operación [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) para obtener la versión más reciente del elemento, a menos que ya la tenga.</span><span class="sxs-lookup"><span data-stu-id="27264-217">Use the [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) operation to get the latest version of the item, unless you already have it.</span></span> 
    
2. <span data-ttu-id="27264-218">Use la operación [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) para especificar los campos que se actualizarán y asigne nuevos valores a esos campos.</span><span class="sxs-lookup"><span data-stu-id="27264-218">Use the [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) operation to specify fields to update and assign new values to those fields.</span></span> 
    
<span data-ttu-id="27264-219">En el ejemplo siguiente se muestra la solicitud de operación XML **UpdateItem** que se envía al servidor para actualizar el valor de [asunto](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="27264-219">The following example shows the XML **UpdateItem** operation request that is sent to the server to update the [Subject](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) value of the email message.</span></span> <span data-ttu-id="27264-220">Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="27264-220">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AlwaysOverwrite">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="APdZjAAA=" ChangeKey="CQAAABYAAAAqRr3mNdNMSasqx/o9J13UAAAAPdgr" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>New subject</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="27264-221">El servidor responde a la solicitud **UpdateItem** con un mensaje [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) que incluye el valor [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) de **NoError**, que indica que la actualización del elemento se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="27264-221">The server responds to the **UpdateItem** request with a [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) message that includes the a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the item update was successful.</span></span>
  
<span data-ttu-id="27264-222">Para obtener información sobre cómo actualizar un elemento de reunión o cita mediante EWS, consulte [actualizar citas y reuniones mediante EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="27264-222">To learn how to update a meeting or appointment item by using EWS, see [Update appointments and meetings by using EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="delete-an-item-by-using-the-ews-managed-api"></a><span data-ttu-id="27264-223">Eliminar un elemento mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="27264-223">Delete an item by using the EWS Managed API</span></span>
<span data-ttu-id="27264-224"><a name="bk_deleteewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="27264-224"><a name="bk_deleteewsma"> </a></span></span>

<span data-ttu-id="27264-225">Puede eliminar elementos moviéndolos a la carpeta elementos eliminados o al contenedor.</span><span class="sxs-lookup"><span data-stu-id="27264-225">You can delete items by moving them to the Deleted Items folder or to the dumpster.</span></span> <span data-ttu-id="27264-226">Si conoce el elemento [Itemid](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento que se va a eliminar, solo tiene que llamar al método [Delete](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx) en el elemento.</span><span class="sxs-lookup"><span data-stu-id="27264-226">If you know the [ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to delete, just call the [Delete](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx) method on the item.</span></span> 
  
<span data-ttu-id="27264-227">Si necesita buscar el elemento antes de eliminarlo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="27264-227">If you need to find the item before deleting it, do the following:</span></span>
  
1. <span data-ttu-id="27264-228">Llame al método [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) o [FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) para buscar el elemento que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="27264-228">Call the [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) or [FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method to find the item to delete.</span></span> 
    
1. <span data-ttu-id="27264-229">Crea una instancia de una [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) y la limita a las propiedades que se van a devolver, o usa una [SearchFilterCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) para buscar elementos específicos.</span><span class="sxs-lookup"><span data-stu-id="27264-229">Instantiate a [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) and limit it to the properties to return, or use a [SearchFilterCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) to find specific items.</span></span> 
    
2. <span data-ttu-id="27264-230">Cree una instancia de [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) o [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) para especificar el número de elementos que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="27264-230">Instantiate an [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) or [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) to specify the number of items to return.</span></span> 
    
2. <span data-ttu-id="27264-231">Llamar al método [Delete](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="27264-231">Call the [Delete](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx) method.</span></span> 
    
<span data-ttu-id="27264-232">Por ejemplo, el siguiente código muestra cómo mover un mensaje de correo electrónico a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="27264-232">For example, the following code shows how to move an email message to the Deleted Items folder.</span></span>
  
<span data-ttu-id="27264-233">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que el usuario se ha autenticado en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="27264-233">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="27264-234">La variable local *Itemid* es el [identificador](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="27264-234">The local variable  *itemId*  is the [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to update.</span></span> 
  
```cs
// Bind to the existing item, using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId);
// Delete the item by moving it to the Deleted Items folder.
// This method call results in a DeleteItem call to EWS.
item.Delete(DeleteMode.MoveToDeletedItems);
```

<span data-ttu-id="27264-235">Para obtener más información sobre cómo eliminar elementos, vea [eliminar elementos mediante EWS en Exchange](deleting-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="27264-235">For more details about deleting items, see [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="27264-236">Para obtener información sobre cómo eliminar una reunión o un elemento de cita mediante la API administrada de EWS, vea [eliminar citas y cancelar reuniones mediante EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="27264-236">To learn how to delete a meeting or appointment item by using the EWS Managed API, see [Delete appointments and cancel meetings by using EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="delete-an-item-by-using-ews"></a><span data-ttu-id="27264-237">Eliminar un elemento mediante EWS</span><span class="sxs-lookup"><span data-stu-id="27264-237">Delete an item by using EWS</span></span>
<span data-ttu-id="27264-238"><a name="bk_deleteews"> </a></span><span class="sxs-lookup"><span data-stu-id="27264-238"><a name="bk_deleteews"> </a></span></span>

<span data-ttu-id="27264-239">Puede eliminar un elemento mediante la operación [DeleteItem](../web-service-reference/deleteitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="27264-239">You can delete an item by using the [DeleteItem](../web-service-reference/deleteitem-operation.md) operation.</span></span> 
  
<span data-ttu-id="27264-240">En el ejemplo siguiente se muestra la solicitud XML que se envía al servidor para mover el mensaje de correo electrónico a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="27264-240">The following example shows the XML request that is sent to the server to move the email message to the Deleted Items folder.</span></span> <span data-ttu-id="27264-241">Los valores de algunos atributos y elementos se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="27264-241">The values of some attributes and elements have been shortened for readability.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:DeleteItem DeleteType="MoveToDeletedItems">
      <m:ItemIds>
        <t:ItemId Id="APdZjAAA=" ChangeKey="CQAAABYAAAAqRr3mNdNMSasqx/o9J13UAAANIFzC" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="27264-242">El servidor responde a la solicitud **DeleteItem** con un mensaje [DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) que incluye el valor [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) de **NoError**, lo que indica que la eliminación del elemento se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="27264-242">The server responds to the **DeleteItem** request with a [DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) message that includes the a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the item deletion was successful.</span></span>
  
<span data-ttu-id="27264-243">Para obtener más información sobre cómo eliminar elementos, vea [eliminar elementos mediante EWS en Exchange](deleting-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="27264-243">For more details about deleting items, see [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="27264-244">Para obtener información sobre cómo eliminar una reunión o un elemento de cita mediante EWS, vea [eliminar citas y cancelar reuniones mediante EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="27264-244">To learn how to delete a meeting or appointment item by using EWS, see [Delete appointments and cancel meetings by using EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="move-or-copy-items-to-another-mailbox"></a><span data-ttu-id="27264-245">Mover o copiar elementos a otro buzón</span><span class="sxs-lookup"><span data-stu-id="27264-245">Move or copy items to another mailbox</span></span>
<span data-ttu-id="27264-246"><a name="bk_movecopybtnmailboxes"> </a></span><span class="sxs-lookup"><span data-stu-id="27264-246"><a name="bk_movecopybtnmailboxes"> </a></span></span>

<span data-ttu-id="27264-247">Puede mover o copiar elementos entre buzones de correo mediante el uso de las operaciones [ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) y [UploadItems](https://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="27264-247">You can move or copy items between mailboxes by using the [ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) and [UploadItems](https://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) operations.</span></span> <span data-ttu-id="27264-248">Para obtener más información, vea [exportar e importar elementos mediante EWS en Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="27264-248">To learn more, see [Exporting and importing items by using EWS in Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="27264-249">Vea también</span><span class="sxs-lookup"><span data-stu-id="27264-249">See also</span></span>

- [<span data-ttu-id="27264-250">Carpetas y elementos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="27264-250">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)    
- [<span data-ttu-id="27264-251">Trabajar con carpetas mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="27264-251">Work with folders by using EWS in Exchange</span></span>](how-to-work-with-folders-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="27264-252">Eliminación de elementos mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="27264-252">Deleting items by using EWS in Exchange</span></span>](deleting-items-by-using-ews-in-exchange.md)
    

