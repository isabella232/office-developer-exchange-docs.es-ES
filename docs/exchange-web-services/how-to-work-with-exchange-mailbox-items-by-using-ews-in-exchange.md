---
title: Trabajar con los elementos del buzón de Exchange mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 721deb84-f85d-45d0-84c1-0ed55f359969
description: Obtenga información sobre cómo crear, obtener, actualizar y eliminar elementos mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: a40cd7ae682c1fb0a8d2f9cfcb10d99d4ab08052
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353969"
---
# <a name="work-with-exchange-mailbox-items-by-using-ews-in-exchange"></a><span data-ttu-id="87ec5-103">Trabajar con los elementos del buzón de Exchange mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="87ec5-103">Work with Exchange mailbox items by using EWS in Exchange</span></span>

<span data-ttu-id="87ec5-104">Obtenga información sobre cómo crear, obtener, actualizar y eliminar elementos mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="87ec5-104">Learn how to create, get, update, and delete items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="87ec5-105">Puede usar la API administrada de EWS o EWS para trabajar con elementos de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="87ec5-105">You can use the EWS Managed API or EWS to work with items in a mailbox.</span></span> <span data-ttu-id="87ec5-106">Puede usar los elementos genéricos: objetos de [elemento](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) de API administrada de EWS o tipos de [elemento](http://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx) EWS: para realizar algunas operaciones (obtención de un elemento o eliminación de un elemento con el identificador del elemento); Sin embargo, la mayor parte de la hora en que tendrá que usar un [elemento con establecimiento inflexible de tipos](folders-and-items-in-ews-in-exchange.md#bk_item) para llevar a cabo una operación get o la operación de actualización debido a que tendrá acceso a las propiedades que son específicas para el elemento fuertemente tipado.</span><span class="sxs-lookup"><span data-stu-id="87ec5-106">You can use generic items — EWS Managed API [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) objects or EWS [Item](http://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx) types — to perform some operations (getting an item or deleting an item by using the item's identifier); however, most of the time you'll have to use a [strongly typed item](folders-and-items-in-ews-in-exchange.md#bk_item) to perform a get or update operation because you'll need access to the properties that are specific to the strongly typed item.</span></span> 

<span data-ttu-id="87ec5-107">Por ejemplo, no puede usar un elemento genérico para recuperar un elemento que contiene un inicio y fecha de finalización: necesita un objeto de la API administrada de EWS [cita](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) o un tipo de EWS [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="87ec5-107">For example, you can't use a generic item to retrieve an item that contains a start and end date - you need an EWS Managed API [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object or an EWS [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) type to do that.</span></span> <span data-ttu-id="87ec5-108">Y si se usa la API administrada de EWS, siempre debe crear elementos fuertemente tipados, porque la clase de **elemento** genérica no tiene un constructor.</span><span class="sxs-lookup"><span data-stu-id="87ec5-108">And if you're using the EWS Managed API, you always have to create strongly typed items, because the generic **Item** class does not have a constructor.</span></span> <span data-ttu-id="87ec5-109">Si está trabajando con un elemento que no está fuertemente tipado, siempre puede usar la clase de **elemento** base para trabajar con el elemento.</span><span class="sxs-lookup"><span data-stu-id="87ec5-109">If you're working with an item that is not strongly typed, you can always use the base **Item** class to work with the item.</span></span> 
  
<span data-ttu-id="87ec5-110">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para trabajar con elementos**</span><span class="sxs-lookup"><span data-stu-id="87ec5-110">**Table 1. EWS Managed API methods and EWS operations for working with items**</span></span>

|<span data-ttu-id="87ec5-111">**Con el fin...**</span><span class="sxs-lookup"><span data-stu-id="87ec5-111">**In order to…**</span></span>|<span data-ttu-id="87ec5-112">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="87ec5-112">**EWS Managed API method**</span></span>|<span data-ttu-id="87ec5-113">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="87ec5-113">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="87ec5-114">Crear un elemento genérico</span><span class="sxs-lookup"><span data-stu-id="87ec5-114">Create a generic item</span></span>  <br/> |<span data-ttu-id="87ec5-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="87ec5-115">None.</span></span> <span data-ttu-id="87ec5-116">Sólo se pueden crear tipos de elemento específico mediante el uso de la API administrada de EWS; no se puede crear los elementos genéricos.</span><span class="sxs-lookup"><span data-stu-id="87ec5-116">You can only create specific item types by using the EWS Managed API; you cannot create generic items.</span></span>  <br/> |[<span data-ttu-id="87ec5-117">CreateItem</span><span class="sxs-lookup"><span data-stu-id="87ec5-117">CreateItem</span></span>](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="87ec5-118">Obtener un elemento</span><span class="sxs-lookup"><span data-stu-id="87ec5-118">Get an item</span></span>  <br/> |[<span data-ttu-id="87ec5-119">Item.Bind</span><span class="sxs-lookup"><span data-stu-id="87ec5-119">Item.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="87ec5-120">GetItem</span><span class="sxs-lookup"><span data-stu-id="87ec5-120">GetItem</span></span>](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="87ec5-121">Actualizar un elemento</span><span class="sxs-lookup"><span data-stu-id="87ec5-121">Update an item</span></span>  <br/> |[<span data-ttu-id="87ec5-122">Item.Update</span><span class="sxs-lookup"><span data-stu-id="87ec5-122">Item.Update</span></span>](http://msdn.microsoft.com/en-us/library/office/dd635915%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="87ec5-123">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="87ec5-123">UpdateItem</span></span>](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="87ec5-124">Eliminar un elemento</span><span class="sxs-lookup"><span data-stu-id="87ec5-124">Delete an item</span></span>  <br/> |[<span data-ttu-id="87ec5-125">Item.Delete</span><span class="sxs-lookup"><span data-stu-id="87ec5-125">Item.Delete</span></span>](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="87ec5-126">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="87ec5-126">DeleteItem</span></span>](../web-service-reference/deleteitem-operation.md) <br/> |
   
<span data-ttu-id="87ec5-127">En este artículo, aprenderá cuándo se puede utilizar la clase base genérica y cuándo debe utilizar un elemento fuertemente tipado para llevar a cabo su tarea.</span><span class="sxs-lookup"><span data-stu-id="87ec5-127">In this article, you'll learn when you can use the generic base class and when you need to use a strongly typed item to complete your task.</span></span> <span data-ttu-id="87ec5-128">Los ejemplos de código muestran cómo usar la clase base y qué hacer cuando no se puede usar la clase base o no ajuste a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="87ec5-128">The code examples will show you how to use the base class, and what to do when you can't use the base class or it doesn't fit your needs.</span></span>
  
## <a name="create-an-item-by-using-the-ews-managed-api"></a><span data-ttu-id="87ec5-129">Crear un elemento mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="87ec5-129">Create an item by using the EWS Managed API</span></span>
<span data-ttu-id="87ec5-130"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="87ec5-130"></span></span>

<span data-ttu-id="87ec5-131">La API administrada de EWS no tiene un constructor públicamente disponible para la clase de [elemento](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) , por lo que debe usar el constructor para el tipo de elemento específico que desea crear con el fin de crear un elemento.</span><span class="sxs-lookup"><span data-stu-id="87ec5-131">The EWS Managed API does not have a publicly available constructor for the [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) class, so you must use the constructor for the specific item type you want to create in order to create an item.</span></span> <span data-ttu-id="87ec5-132">Por ejemplo, use el [constructor de la clase EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) para crear un nuevo mensaje de correo electrónico y [póngase en contacto con el constructor de clase](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) para crear un nuevo contacto.</span><span class="sxs-lookup"><span data-stu-id="87ec5-132">For example, use the [EmailMessage class constructor](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) to create a new email message, and the [Contact class constructor](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) to create a new contact.</span></span> <span data-ttu-id="87ec5-133">Del mismo modo, el servidor nunca devuelve objetos de **elemento** genéricos de respuestas; todos los elementos genéricos se devuelven como objetos **EmailMessage** .</span><span class="sxs-lookup"><span data-stu-id="87ec5-133">Likewise, the server never returns generic **Item** objects in responses; all generic items are returned as **EmailMessage** objects.</span></span> 
  
<span data-ttu-id="87ec5-134">Cuando conoce el tipo de elemento que se va a crear, puede completar la tarea en unos cuantos pasos.</span><span class="sxs-lookup"><span data-stu-id="87ec5-134">When you know the type of item to create, you can complete the task in just a few steps.</span></span> <span data-ttu-id="87ec5-135">Los pasos son similares para todos los tipos de elemento:</span><span class="sxs-lookup"><span data-stu-id="87ec5-135">The steps are similar for all item types:</span></span>
  
1. <span data-ttu-id="87ec5-136">Inicializar una nueva instancia de una de las clases de [elemento](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) con el objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="87ec5-136">Initialize a new instance of one of the [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) classes with the [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object as a parameter.</span></span> 
    
2. <span data-ttu-id="87ec5-137">Establecer propiedades en el elemento.</span><span class="sxs-lookup"><span data-stu-id="87ec5-137">Set properties on the item.</span></span> <span data-ttu-id="87ec5-138">Los esquemas son diferentes para cada tipo de elemento, por lo que distintas propiedades están disponibles para elementos diferentes.</span><span class="sxs-lookup"><span data-stu-id="87ec5-138">The schemas are different for each item type, so different properties are available for different items.</span></span>
    
3. <span data-ttu-id="87ec5-139">Guardar el elemento, o guardar y enviar el elemento.</span><span class="sxs-lookup"><span data-stu-id="87ec5-139">Save the item, or save and send the item.</span></span>
    
<span data-ttu-id="87ec5-140">Por ejemplo, puede crear un objeto [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) , establezca las propiedades de [ToRecipients](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.torecipients%28v=exchg.80%29.aspx) , el [cuerpo](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx)y el [asunto](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.subject%28v=exchg.80%29.aspx)y, a continuación, enviarlo mediante el método [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="87ec5-140">For example, you can create an [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object, set the [Subject](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.subject%28v=exchg.80%29.aspx), [Body](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx), and [ToRecipients](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.torecipients%28v=exchg.80%29.aspx) properties, and then send it by using the [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method.</span></span> 
  
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

<span data-ttu-id="87ec5-141">Para obtener información sobre cómo crear un elemento de cita o reunión mediante el uso de la API administrada de EWS, consulte [crear citas y reuniones mediante el uso de EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span><span class="sxs-lookup"><span data-stu-id="87ec5-141">To learn how to create a meeting or appointment item by using the EWS Managed API, see [Create appointments and meetings by using EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span></span>
  
## <a name="create-an-item-by-using-ews"></a><span data-ttu-id="87ec5-142">Crear un elemento mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="87ec5-142">Create an item by using EWS</span></span>
<span data-ttu-id="87ec5-143"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="87ec5-143"></span></span>

<span data-ttu-id="87ec5-144">Puede crear un elemento genérico o un elemento fuertemente tipado mediante el uso de EWS.</span><span class="sxs-lookup"><span data-stu-id="87ec5-144">You can create a generic item or a strongly typed item by using EWS.</span></span> <span data-ttu-id="87ec5-145">Los pasos son similares para todos los tipos de elemento:</span><span class="sxs-lookup"><span data-stu-id="87ec5-145">The steps are similar for all item types:</span></span>
  
1. <span data-ttu-id="87ec5-146">Use la operación [CreateItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) para crear un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="87ec5-146">Use the [CreateItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) operation to create an item in the Exchange store.</span></span> 
    
2. <span data-ttu-id="87ec5-147">Use el elemento de [los elementos](http://msdn.microsoft.com/library/0811a73e-bf1f-4889-9219-73902dd47639%28Office.15%29.aspx) que contienen uno o más elementos para crear.</span><span class="sxs-lookup"><span data-stu-id="87ec5-147">Use the [Items](http://msdn.microsoft.com/library/0811a73e-bf1f-4889-9219-73902dd47639%28Office.15%29.aspx) element to contain one or more items to create.</span></span> 
    
3. <span data-ttu-id="87ec5-148">Establecer propiedades en el elemento.</span><span class="sxs-lookup"><span data-stu-id="87ec5-148">Set properties on the item.</span></span>
    
<span data-ttu-id="87ec5-149">Por ejemplo, puede crear un mensaje de correo electrónico y enviar mediante el código en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="87ec5-149">For example, you can create an email message and send it by using the code in the following example.</span></span> <span data-ttu-id="87ec5-150">También es la solicitud XML que la API administrada de EWS envía cuando se llama al método [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="87ec5-150">This is also the XML request that the EWS Managed API sends when you call the [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="87ec5-151">El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) **NoError**, lo que indica que el correo electrónico se ha creado correctamente y la [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) de la recientemente mensaje de creación.</span><span class="sxs-lookup"><span data-stu-id="87ec5-151">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
<span data-ttu-id="87ec5-152">Para obtener información sobre cómo crear un elemento de cita o reunión mediante el uso de EWS, consulte [crear citas y reuniones mediante el uso de EWS en Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span><span class="sxs-lookup"><span data-stu-id="87ec5-152">To learn how to create a meeting or appointment item by using EWS, see [Create appointments and meetings by using EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span></span>
  
## <a name="get-an-item-by-using-the-ews-managed-api"></a><span data-ttu-id="87ec5-153">Obtener un elemento mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="87ec5-153">Get an item by using the EWS Managed API</span></span>
<span data-ttu-id="87ec5-154"><a name="bk_getewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="87ec5-154"></span></span>

<span data-ttu-id="87ec5-155">Para usar la API administrada de EWS para obtener un elemento si conoce el [Item.Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento para recuperar, simplemente llama a uno de los métodos de [enlace](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) en el elemento y el elemento se recuperará.</span><span class="sxs-lookup"><span data-stu-id="87ec5-155">To use the EWS Managed API to get an item if you know the [Item.Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to retrieve, you simply call one of the [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) methods on the item, and the item is retrieved.</span></span> <span data-ttu-id="87ec5-156">Como procedimiento recomendado, se recomienda limitar las propiedades devueltas a aquellos que son necesarios.</span><span class="sxs-lookup"><span data-stu-id="87ec5-156">As a best practice, we recommend that you limit the properties returned to only those that are required.</span></span> <span data-ttu-id="87ec5-157">En este ejemplo se devuelve la propiedad de **identificador** de elemento y la propiedad **Subject** .</span><span class="sxs-lookup"><span data-stu-id="87ec5-157">This example returns the item **Id** property and the **Subject** property.</span></span> 
  
<span data-ttu-id="87ec5-158">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="87ec5-158">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="87ec5-159">La variable local *itemId* es el [identificador](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="87ec5-159">The local variable  *itemId*  is the [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to update.</span></span> 
  
```cs
// As a best practice, limit the properties returned to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ItemSchema.Subject);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId, propSet);

```

<span data-ttu-id="87ec5-160">Si está buscando un elemento que cumple determinados criterios, realice lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="87ec5-160">If you're searching for an item that meets specific criteria, do the following:</span></span>
  
1. <span data-ttu-id="87ec5-161">Enlazar a la carpeta que contiene los elementos que desea obtener.</span><span class="sxs-lookup"><span data-stu-id="87ec5-161">Bind to the folder that contains the items to get.</span></span>
    
2. <span data-ttu-id="87ec5-162">Crear una instancia de un [SearchFilter.SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) o un [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) para filtrar los elementos para devolver.</span><span class="sxs-lookup"><span data-stu-id="87ec5-162">Instantiate a [SearchFilter.SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) or a [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) to filter the items to return.</span></span> 
    
3. <span data-ttu-id="87ec5-163">Crear una instancia de un objeto [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) o de [artículoVer](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) para especificar el número de elementos para devolver.</span><span class="sxs-lookup"><span data-stu-id="87ec5-163">Instantiate an [ItemView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) or [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) object to specify the number of items to return.</span></span> 
    
4. <span data-ttu-id="87ec5-164">Llame al método [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) o [ExchangeService.FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="87ec5-164">Call the [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) or [ExchangeService.FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method.</span></span> 
    
<span data-ttu-id="87ec5-165">Por ejemplo, si desea recuperar los mensajes de correo electrónico no leído en la Bandeja de entrada, use el código en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="87ec5-165">For example, if you want to retrieve unread email messages in the Inbox, use the code in the following example.</span></span> <span data-ttu-id="87ec5-166">En este ejemplo se usa un **SearchFilterCollection** para limitar los resultados del método **FindItems** a los mensajes no leídos y se limita el **artículoVer** para limitar los resultados a un elemento.</span><span class="sxs-lookup"><span data-stu-id="87ec5-166">This example uses a **SearchFilterCollection** to limit the results of the **FindItems** method to unread messages, and limits the **ItemView** to limit results to one item.</span></span> <span data-ttu-id="87ec5-167">Este código determinado sólo funciona en objetos [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) debido a que el valor de [EmailMessageSchema.IsRead](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessageschema.isread%28v=exchg.80%29.aspx) es parte de la **SearchFilter**.</span><span class="sxs-lookup"><span data-stu-id="87ec5-167">This particular code only works on [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) objects because the [EmailMessageSchema.IsRead](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessageschema.isread%28v=exchg.80%29.aspx) value is part of the **SearchFilter**.</span></span> 
  
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

<span data-ttu-id="87ec5-168">Como alternativa, puede usar un [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) para limitar los resultados de la búsqueda, tal como se muestra en el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="87ec5-168">Alternatively, you can use a [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) to limit the results of the search as shown in the following code example.</span></span> <span data-ttu-id="87ec5-169">En este ejemplo se usa el método [FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) para recuperar hasta cinco las citas que se producen en los próximos 30 días.</span><span class="sxs-lookup"><span data-stu-id="87ec5-169">This example uses the [FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method to retrieve up to five appointments that occur in the next 30 days.</span></span> <span data-ttu-id="87ec5-170">Evidentemente este código sólo funciona en los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="87ec5-170">This code of course only works on calendar items.</span></span> 
  
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

<span data-ttu-id="87ec5-171">Tenga en cuenta que la información del servidor se devuelve en la respuesta de método **enlazar** es diferente de la información que el servidor devuelve una respuesta de método **FindItem** o **FindAppointment** .</span><span class="sxs-lookup"><span data-stu-id="87ec5-171">Note that the information the server returns in the **Bind** method response is different than the information that the server returns for a **FindItem** or **FindAppointment** method response.</span></span> <span data-ttu-id="87ec5-172">El método **Bind** puede devolver todas las propiedades esquematizadas, mientras que los métodos **FindItem** y **FindAppointment** no devuelven todas las propiedades esquematizadas.</span><span class="sxs-lookup"><span data-stu-id="87ec5-172">The **Bind** method can return all the schematized properties, whereas the **FindItem** and **FindAppointment** methods do not return all the schematized properties.</span></span> <span data-ttu-id="87ec5-173">Por lo que si necesita acceso total al elemento, debe usar el método **Bind** .</span><span class="sxs-lookup"><span data-stu-id="87ec5-173">So if you need full access to the item, you'll have to use the **Bind** method.</span></span> <span data-ttu-id="87ec5-174">Si no tiene el elemento **Id** del elemento que le gustaría recuperar, use los métodos **FindItem** o **FindAppointment** para recuperar el identificador y, a continuación, utilice el método **Bind** para recuperar las propiedades que necesita.</span><span class="sxs-lookup"><span data-stu-id="87ec5-174">If you don't have the item **Id** of the item you'd like to retrieve, use the **FindItem** or **FindAppointment** methods to retrieve the Id, and then use the **Bind** method to retrieve the properties you need.</span></span> 
  
<span data-ttu-id="87ec5-175">Para obtener información sobre cómo obtener un elemento de cita o reunión mediante el uso de la API administrada de EWS, vea [obtener las citas y reuniones mediante el uso de EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="87ec5-175">To learn how to get a meeting or appointment item by using the EWS Managed API, see [Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="get-an-item-by-using-ews"></a><span data-ttu-id="87ec5-176">Obtener un elemento mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="87ec5-176">Get an item by using EWS</span></span>
<span data-ttu-id="87ec5-177"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="87ec5-177"></span></span>

<span data-ttu-id="87ec5-178">Si conoce el [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) del elemento para recuperar, puede obtener el elemento mediante la operación [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="87ec5-178">If you know the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the item to retrieve, you can get the item by using the [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) operation.</span></span> 
  
<span data-ttu-id="87ec5-179">En el ejemplo siguiente se muestra la solicitud XML para obtener el [asunto](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) de un elemento con un determinado **ItemId**.</span><span class="sxs-lookup"><span data-stu-id="87ec5-179">The following example shows the XML request to get the [Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) of an item with a specific **ItemId**.</span></span> <span data-ttu-id="87ec5-180">También es la solicitud XML que la API administrada de EWS envía al llamar al método [enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) en un **ItemId**.</span><span class="sxs-lookup"><span data-stu-id="87ec5-180">This is also the XML request that the EWS Managed API sends when calling the [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method on an **ItemId**.</span></span> <span data-ttu-id="87ec5-181">Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="87ec5-181">The values of some attributes and elements have been shortened for readability.</span></span>
  
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

En el ejemplo siguiente se muestra la respuesta XML que el servidor devuelve una vez que procesa la operación **GetItem** . La respuesta indica que el elemento se recuperó correctamente. <span data-ttu-id="87ec5-184">Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="87ec5-184">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="87ec5-185">Si no conoce el **ItemId** del elemento que desea recuperar, puede usar la operación [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para buscar el elemento.</span><span class="sxs-lookup"><span data-stu-id="87ec5-185">If you do not know the **ItemId** of the item you want to retrieve, you can use the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation to find the item.</span></span> <span data-ttu-id="87ec5-186">Para poder usar la operación **FindItem** , primero debe identificar la carpeta que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="87ec5-186">In order to use the **FindItem** operation, you must first identify the folder that you're searching.</span></span> <span data-ttu-id="87ec5-187">Puede identificar la carpeta mediante el uso de su **DistinguinguishedFolderName** o mediante el [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="87ec5-187">You can identify the folder by using its **DistinguinguishedFolderName** or by using the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx).</span></span> <span data-ttu-id="87ec5-188">Puede usar las operaciones de la [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) o [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) para obtener el **FolderId** necesita.</span><span class="sxs-lookup"><span data-stu-id="87ec5-188">You can use either the [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) or [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operations to get the **FolderId** you need.</span></span> <span data-ttu-id="87ec5-189">A continuación, use la operación **FindItem** para buscar esa carpeta para obtener los resultados que coinciden con el filtro de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="87ec5-189">Then use the **FindItem** operation to search that folder for results that match the search filter.</span></span> <span data-ttu-id="87ec5-190">A diferencia de la API administrada de EWS, EWS no proporciona una operación de búsqueda independiente para las citas.</span><span class="sxs-lookup"><span data-stu-id="87ec5-190">Unlike the EWS Managed API, EWS does not provide a separate find operation for appointments.</span></span> <span data-ttu-id="87ec5-191">La operación **FindItem** recupera los elementos de todos los tipos.</span><span class="sxs-lookup"><span data-stu-id="87ec5-191">The **FindItem** operation retrieves items of all types.</span></span> 
  
<span data-ttu-id="87ec5-192">En el ejemplo siguiente se muestra la solicitud de operación XML **FindItem** que se envía al servidor para buscar citas en la carpeta de calendario que se producen en los próximos 30 días.</span><span class="sxs-lookup"><span data-stu-id="87ec5-192">The following example shows the XML **FindItem** operation request that is sent to the server to find appointments in the Calendar folder that occur in the next 30 days.</span></span> <span data-ttu-id="87ec5-193">Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="87ec5-193">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="87ec5-194">El servidor responde a la solicitud de **FindItem** con un mensaje de [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) que incluye el valor [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la operación que se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="87ec5-194">The server responds to the **FindItem** request with a [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) message that includes the [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the operation completed successfully.</span></span> <span data-ttu-id="87ec5-195">Si los elementos de calendario cumplen los criterios de filtrado, se incluyen en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="87ec5-195">If any calendar items meet the filtering criteria, they are included in the response.</span></span>
  
<span data-ttu-id="87ec5-196">Tenga en cuenta que la información del servidor se devuelve en la respuesta de la operación **GetItem** es diferente de la información que el servidor devuelve en una **FindItem** o una respuesta de la operación de **FindAppointment** .</span><span class="sxs-lookup"><span data-stu-id="87ec5-196">Note that the information the server returns in the **GetItem** operation response is different than the information the server returns in a **FindItem** or **FindAppointment** operation response.</span></span> <span data-ttu-id="87ec5-197">La operación **GetItem** puede devolver todas las propiedades esquematizadas, mientras que las operaciones **FindItem** y **FindAppointment** no devuelven todas las propiedades esquematizadas.</span><span class="sxs-lookup"><span data-stu-id="87ec5-197">The **GetItem** operation can return all the schematized properties, whereas the **FindItem** and **FindAppointment** operations do not return all the schematized properties.</span></span> <span data-ttu-id="87ec5-198">Por lo que si necesita acceso total al elemento, debe usar la operación **GetItem** .</span><span class="sxs-lookup"><span data-stu-id="87ec5-198">So if you need full access to the item, you'll have to use the **GetItem** operation.</span></span> <span data-ttu-id="87ec5-199">Si no dispone de la **ItemId** del elemento que le gustaría recuperar, use las operaciones **FindItem** o **FindAppointment** para recuperar la **ItemId**y, a continuación, use la operación **GetItem** para recuperar los elementos que necesita.</span><span class="sxs-lookup"><span data-stu-id="87ec5-199">If you don't have the **ItemId** of the item you'd like to retrieve, use the **FindItem** or **FindAppointment** operations to retrieve the **ItemId**, and then use the **GetItem** operation to retrieve the elements you need.</span></span> 
  
<span data-ttu-id="87ec5-200">Para obtener información sobre cómo obtener un elemento de cita o reunión mediante el uso de EWS, vea [obtener las citas y reuniones mediante el uso de EWS en Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="87ec5-200">To learn how to get a meeting or appointment item by using EWS, see [Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="update-an-item-by-using-the-ews-managed-api"></a><span data-ttu-id="87ec5-201">Actualizar un elemento mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="87ec5-201">Update an item by using the EWS Managed API</span></span>
<span data-ttu-id="87ec5-202"><a name="bk_updateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="87ec5-202"></span></span>

<span data-ttu-id="87ec5-203">Los pasos para actualizar un elemento mediante la API administrada de EWS son similares para todos los tipos de elemento; Sin embargo, las propiedades de elemento son diferentes para cada tipo de elemento y el método de [actualización](http://msdn.microsoft.com/en-us/library/office/dd635915%28v=exchg.80%29.aspx) tiene muchos métodos sobrecargados para elegir.</span><span class="sxs-lookup"><span data-stu-id="87ec5-203">The steps to update an item by using the EWS Managed API are similar for all item types; however, the item properties are different for each item type, and the [Update](http://msdn.microsoft.com/en-us/library/office/dd635915%28v=exchg.80%29.aspx) method has many overloaded methods to choose from.</span></span> <span data-ttu-id="87ec5-204">Para actualizar un elemento:</span><span class="sxs-lookup"><span data-stu-id="87ec5-204">To update an item:</span></span> 
  
1. <span data-ttu-id="87ec5-205">Utilice el método [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) para obtener la versión más reciente del elemento, a menos que ya tiene.</span><span class="sxs-lookup"><span data-stu-id="87ec5-205">Use the [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method to get the latest version of the item, unless you already have it.</span></span> <span data-ttu-id="87ec5-206">Para actualizar propiedades específicas a un elemento fuertemente tipado, tendrá que enlazar a ese tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="87ec5-206">To update properties specific to a strongly typed item, you'll have to bind to that item type.</span></span> <span data-ttu-id="87ec5-207">Para actualizar las propiedades disponibles en el tipo de elemento genérico, se puede enlazar al objeto de [elemento](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="87ec5-207">To update properties available on the generic item type, you can bind to the [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) object.</span></span> 
    
2. <span data-ttu-id="87ec5-208">Actualizar las propiedades en el elemento.</span><span class="sxs-lookup"><span data-stu-id="87ec5-208">Update the properties on the item.</span></span>
    
3. <span data-ttu-id="87ec5-209">Llame al método **Update** .</span><span class="sxs-lookup"><span data-stu-id="87ec5-209">Call the **Update** method.</span></span> 
    
<span data-ttu-id="87ec5-210">Por ejemplo, puede actualizar al asunto de un correo electrónico con el tipo de elemento genérico, como se muestra en el código en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="87ec5-210">For example, you can update the subject of an email by using the generic item type, as shown in the code in the following example.</span></span>
  
<span data-ttu-id="87ec5-211">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="87ec5-211">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="87ec5-212">La variable local *itemId* es el [identificador](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="87ec5-212">The local variable  *itemId*  is the [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to update.</span></span> 
  
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

<span data-ttu-id="87ec5-213">Para obtener información sobre cómo actualizar un elemento de cita o reunión mediante el uso de la API administrada de EWS, consulte [actualizar las citas y reuniones mediante el uso de EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="87ec5-213">To learn how to update a meeting or appointment item by using the EWS Managed API, see [Update appointments and meetings by using EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="update-an-item-by-using-ews"></a><span data-ttu-id="87ec5-214">Actualizar un elemento mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="87ec5-214">Update an item by using EWS</span></span>
<span data-ttu-id="87ec5-215"><a name="bk_updateews"> </a></span><span class="sxs-lookup"><span data-stu-id="87ec5-215"></span></span>

<span data-ttu-id="87ec5-216">Para actualizar un elemento mediante el uso de EWS, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="87ec5-216">To update an item by using EWS, do the following:</span></span>
  
1. <span data-ttu-id="87ec5-217">Use la operación [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) para obtener la versión más reciente del elemento, a menos que ya tiene.</span><span class="sxs-lookup"><span data-stu-id="87ec5-217">Use the [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) operation to get the latest version of the item, unless you already have it.</span></span> 
    
2. <span data-ttu-id="87ec5-218">Use la operación [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) para especificar campos para actualizar y asignar nuevos valores a esos campos.</span><span class="sxs-lookup"><span data-stu-id="87ec5-218">Use the [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) operation to specify fields to update and assign new values to those fields.</span></span> 
    
<span data-ttu-id="87ec5-219">En el ejemplo siguiente se muestra la solicitud de operación XML **UpdateItem** que se envía al servidor para actualizar el valor de [asunto](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="87ec5-219">The following example shows the XML **UpdateItem** operation request that is sent to the server to update the [Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) value of the email message.</span></span> <span data-ttu-id="87ec5-220">Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="87ec5-220">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="87ec5-221">El servidor responde a la solicitud de **UpdateItem** con un mensaje de [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) que incluye el valor [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) **NoError**, que indica que la actualización de elemento se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="87ec5-221">The server responds to the **UpdateItem** request with a [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) message that includes the a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the item update was successful.</span></span>
  
<span data-ttu-id="87ec5-222">Para obtener información sobre cómo actualizar un elemento de cita o reunión mediante el uso de EWS, consulte [actualizar las citas y reuniones mediante el uso de EWS en Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="87ec5-222">To learn how to update a meeting or appointment item by using EWS, see [Update appointments and meetings by using EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="delete-an-item-by-using-the-ews-managed-api"></a><span data-ttu-id="87ec5-223">Eliminar un elemento mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="87ec5-223">Delete an item by using the EWS Managed API</span></span>
<span data-ttu-id="87ec5-224"><a name="bk_deleteewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="87ec5-224"></span></span>

<span data-ttu-id="87ec5-225">Puede eliminar elementos moviendo a la carpeta Elementos eliminados o al volcado de archivos.</span><span class="sxs-lookup"><span data-stu-id="87ec5-225">You can delete items by moving them to the Deleted Items folder or to the dumpster.</span></span> <span data-ttu-id="87ec5-226">Si conoce el [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento para eliminar, simplemente llame al método [Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) en el elemento.</span><span class="sxs-lookup"><span data-stu-id="87ec5-226">If you know the [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to delete, just call the [Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) method on the item.</span></span> 
  
<span data-ttu-id="87ec5-227">Si necesita buscar el elemento antes de eliminarla, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="87ec5-227">If you need to find the item before deleting it, do the following:</span></span>
  
1. <span data-ttu-id="87ec5-228">Llame al método [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) o [FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) para buscar el elemento que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="87ec5-228">Call the [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) or [FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method to find the item to delete.</span></span> 
    
1. <span data-ttu-id="87ec5-229">Crear una instancia de un [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) y limitar a las propiedades para devolver o utilizar una [SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) para buscar elementos específicos.</span><span class="sxs-lookup"><span data-stu-id="87ec5-229">Instantiate a [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) and limit it to the properties to return, or use a [SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) to find specific items.</span></span> 
    
2. <span data-ttu-id="87ec5-230">Crear una instancia de un [artículoVer](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) o [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) para especificar el número de elementos para devolver.</span><span class="sxs-lookup"><span data-stu-id="87ec5-230">Instantiate an [ItemView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) or [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) to specify the number of items to return.</span></span> 
    
2. <span data-ttu-id="87ec5-231">Llamar al método [Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="87ec5-231">Call the [Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) method.</span></span> 
    
<span data-ttu-id="87ec5-232">Por ejemplo, el código siguiente muestra cómo mover un mensaje de correo electrónico a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="87ec5-232">For example, the following code shows how to move an email message to the Deleted Items folder.</span></span>
  
<span data-ttu-id="87ec5-233">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="87ec5-233">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="87ec5-234">La variable local *itemId* es el [identificador](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) del elemento que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="87ec5-234">The local variable  *itemId*  is the [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to update.</span></span> 
  
```cs
// Bind to the existing item, using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId);
// Delete the item by moving it to the Deleted Items folder.
// This method call results in a DeleteItem call to EWS.
item.Delete(DeleteMode.MoveToDeletedItems);
```

<span data-ttu-id="87ec5-235">Para obtener más información acerca de cómo eliminar elementos, vea [Eliminar elementos mediante el uso de EWS en Exchange](deleting-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="87ec5-235">For more details about deleting items, see [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="87ec5-236">Para obtener información sobre cómo eliminar un elemento de cita o reunión mediante el uso de la API administrada de EWS, vea [Eliminar citas y cancelar reuniones mediante el uso de EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="87ec5-236">To learn how to delete a meeting or appointment item by using the EWS Managed API, see [Delete appointments and cancel meetings by using EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="delete-an-item-by-using-ews"></a><span data-ttu-id="87ec5-237">Eliminar un elemento mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="87ec5-237">Delete an item by using EWS</span></span>
<span data-ttu-id="87ec5-238"><a name="bk_deleteews"> </a></span><span class="sxs-lookup"><span data-stu-id="87ec5-238"></span></span>

<span data-ttu-id="87ec5-239">Puede eliminar un elemento mediante la operación [DeleteItem](../web-service-reference/deleteitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="87ec5-239">You can delete an item by using the [DeleteItem](../web-service-reference/deleteitem-operation.md) operation.</span></span> 
  
<span data-ttu-id="87ec5-240">En el ejemplo siguiente se muestra la solicitud XML que se envía al servidor para mover el mensaje de correo electrónico a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="87ec5-240">The following example shows the XML request that is sent to the server to move the email message to the Deleted Items folder.</span></span> <span data-ttu-id="87ec5-241">Los valores de algunos elementos y atributos se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="87ec5-241">The values of some attributes and elements have been shortened for readability.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="87ec5-242">El servidor responde a la solicitud de **DeleteItem** con un mensaje de [DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) que incluye el valor [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) **NoError**, que indica que la eliminación del elemento se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="87ec5-242">The server responds to the **DeleteItem** request with a [DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) message that includes the a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the item deletion was successful.</span></span>
  
<span data-ttu-id="87ec5-243">Para obtener más información acerca de cómo eliminar elementos, vea [Eliminar elementos mediante el uso de EWS en Exchange](deleting-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="87ec5-243">For more details about deleting items, see [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="87ec5-244">Para obtener información sobre cómo eliminar un elemento de cita o reunión mediante el uso de EWS, vea [Eliminar citas y cancelar reuniones mediante el uso de EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="87ec5-244">To learn how to delete a meeting or appointment item by using EWS, see [Delete appointments and cancel meetings by using EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="move-or-copy-items-to-another-mailbox"></a><span data-ttu-id="87ec5-245">Mover o copiar elementos a otro buzón</span><span class="sxs-lookup"><span data-stu-id="87ec5-245">Move or copy items to another mailbox</span></span>
<span data-ttu-id="87ec5-246"><a name="bk_movecopybtnmailboxes"> </a></span><span class="sxs-lookup"><span data-stu-id="87ec5-246"></span></span>

<span data-ttu-id="87ec5-247">Puede mover o copiar elementos entre buzones de correo mediante el uso de las operaciones de [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) y [UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="87ec5-247">You can move or copy items between mailboxes by using the [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) and [UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) operations.</span></span> <span data-ttu-id="87ec5-248">Para obtener más información, consulte [exportación e importación de elementos mediante el uso de EWS en Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="87ec5-248">To learn more, see [Exporting and importing items by using EWS in Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="87ec5-249">Vea también</span><span class="sxs-lookup"><span data-stu-id="87ec5-249">See also</span></span>

- [<span data-ttu-id="87ec5-250">Las carpetas y elementos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="87ec5-250">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)    
- [<span data-ttu-id="87ec5-251">Trabajar con carpetas mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="87ec5-251">Work with folders by using EWS in Exchange</span></span>](how-to-work-with-folders-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="87ec5-252">Eliminación de elementos con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="87ec5-252">Deleting items by using EWS in Exchange</span></span>](deleting-items-by-using-ews-in-exchange.md)
    

