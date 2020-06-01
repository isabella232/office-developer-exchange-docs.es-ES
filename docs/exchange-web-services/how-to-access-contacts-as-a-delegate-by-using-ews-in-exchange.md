---
title: Obtener acceso a los contactos como un delegado mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3cd34c14-18b0-4fe2-a4c2-d884318c88fc
description: Obtenga información sobre cómo obtener acceso a contactos como un delegado mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 06faf7dd7459b14792abbea21761e909c8eb9fb6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455348"
---
# <a name="access-contacts-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="f5d9e-103">Obtener acceso a los contactos como un delegado mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f5d9e-103">Access contacts as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="f5d9e-104">Obtenga información sobre cómo obtener acceso a contactos como un delegado mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-104">Learn how to access contacts as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="f5d9e-105">Puede usar la API administrada de EWS o EWS para conceder a un usuario acceso a la carpeta de contactos de un propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-105">You can use the EWS Managed API or EWS to give a user access to a mailbox owner's Contacts folder.</span></span> <span data-ttu-id="f5d9e-106">A continuación, el delegado puede crear contactos en nombre del propietario del buzón y recuperar, actualizar y eliminar contactos de la carpeta de contactos del propietario del buzón, en función de sus permisos.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-106">The delegate can then create contacts on behalf of the mailbox owner, and retrieve, update, and delete contacts from the mailbox owner's Contacts folder, depending on their permissions.</span></span>
  
<span data-ttu-id="f5d9e-107">Como delegado, se usan los mismos métodos y operaciones para tener acceso a la carpeta de contactos de un propietario del buzón que se usa para tener acceso a su propia carpeta contactos.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-107">As a delegate, you use the same methods and operations to access a mailbox owner's Contacts folder that you use to access your own Contacts folder.</span></span> <span data-ttu-id="f5d9e-108">La principal diferencia es que tiene que usar el [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicit) para buscar o crear un elemento de contacto y, después, después de identificar el identificador de elemento, puede usar el [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) para obtener, actualizar o eliminar el elemento.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create a contact item, and then after you identify the item ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="f5d9e-109">**Tabla 1. Métodos de la API administrada de EWS y operaciones EWS para tener acceso a un contacto como delegado**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-109">**Table 1. EWS Managed API methods and EWS operations for accessing a contact as a delegate**</span></span>

|<span data-ttu-id="f5d9e-110">**Si quiere...**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-110">**If you want to…**</span></span>|<span data-ttu-id="f5d9e-111">**Use este método de API administrada de EWS...**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="f5d9e-112">**Usar esta operación de EWS...**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f5d9e-113">Crear un contacto como delegado</span><span class="sxs-lookup"><span data-stu-id="f5d9e-113">Create a contact as a delegate</span></span>  <br/> |<span data-ttu-id="f5d9e-114">[Item. Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) donde el parámetro [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de contactos del propietario del buzón de correo</span><span class="sxs-lookup"><span data-stu-id="f5d9e-114">[Item.Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) where the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="f5d9e-115">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) donde el elemento [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica el [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón de correo</span><span class="sxs-lookup"><span data-stu-id="f5d9e-115">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="f5d9e-116">Crear varios contactos como un delegado</span><span class="sxs-lookup"><span data-stu-id="f5d9e-116">Create multiple contacts as a delegate</span></span>  <br/> |<span data-ttu-id="f5d9e-117">[ExchangeService. CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) donde el parámetro **FolderId** proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de contactos del propietario del buzón de correo</span><span class="sxs-lookup"><span data-stu-id="f5d9e-117">[ExchangeService.CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="f5d9e-118">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) donde el elemento [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica el [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón de correo</span><span class="sxs-lookup"><span data-stu-id="f5d9e-118">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="f5d9e-119">Resolver un contacto como delegado</span><span class="sxs-lookup"><span data-stu-id="f5d9e-119">Resolve a contact as a delegate</span></span>  <br/> |<span data-ttu-id="f5d9e-120">[ExchangeService. ResolveName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) donde el parámetro [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de contactos del propietario del buzón de correo</span><span class="sxs-lookup"><span data-stu-id="f5d9e-120">[ExchangeService.ResolveName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) where the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="f5d9e-121">[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) donde el elemento [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica el [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="f5d9e-121">[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="f5d9e-122">Buscar o buscar un contacto como delegado</span><span class="sxs-lookup"><span data-stu-id="f5d9e-122">Search for or find a contact as a delegate</span></span>  <br/> |<span data-ttu-id="f5d9e-123">[ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) donde el parámetro **FolderId** proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de contactos del propietario del buzón de correo</span><span class="sxs-lookup"><span data-stu-id="f5d9e-123">[ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="f5d9e-124">[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) donde el elemento [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica el [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-124">[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="f5d9e-125">Obtener un contacto como delegado</span><span class="sxs-lookup"><span data-stu-id="f5d9e-125">Get a contact as a delegate</span></span>  <br/> |[<span data-ttu-id="f5d9e-126">Contact. bind</span><span class="sxs-lookup"><span data-stu-id="f5d9e-126">Contact.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="f5d9e-127">GetItem</span><span class="sxs-lookup"><span data-stu-id="f5d9e-127">GetItem</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="f5d9e-128">Actualizar un contacto como delegado</span><span class="sxs-lookup"><span data-stu-id="f5d9e-128">Update a contact as a delegate</span></span>  <br/> |<span data-ttu-id="f5d9e-129">[Contact. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) seguido por [Contact. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-129">[Contact.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) followed by [Contact.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="f5d9e-130">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido de [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-130">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="f5d9e-131">Eliminar un contacto como delegado</span><span class="sxs-lookup"><span data-stu-id="f5d9e-131">Delete a contact as a delegate</span></span>  <br/> |<span data-ttu-id="f5d9e-132">[Contact. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) seguido por [Contact. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-132">[Contact.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) followed by [Contact.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="f5d9e-133">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido de [DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-133">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |
   
> [!NOTE]
> <span data-ttu-id="f5d9e-134">En los ejemplos de código de este artículo, primary@contoso.com es el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-134">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 

<span data-ttu-id="f5d9e-135"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="f5d9e-135"><a name="bk_prereq"> </a></span></span>

## <a name="prerequisite-tasks"></a><span data-ttu-id="f5d9e-136">Tareas de requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f5d9e-136">Prerequisite tasks</span></span>

<span data-ttu-id="f5d9e-137">Para que un usuario pueda tener acceso a la carpeta de contactos del propietario del buzón como delegado, el usuario debe [agregarse como delegado con permisos](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) para la carpeta de contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-137">Before a user can access the mailbox owner's Contacts folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Contacts folder.</span></span> 

<span data-ttu-id="f5d9e-138"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="f5d9e-138"><a name="bk_createewsma"> </a></span></span>

## <a name="create-a-contact-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="f5d9e-139">Crear un contacto como delegado mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="f5d9e-139">Create a contact as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="f5d9e-140">La API administrada de EWS permite usar el objeto de servicio para que el usuario delegado cree contactos para el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-140">The EWS Managed API enables you to use the service object for the delegate user to create contacts for the mailbox owner.</span></span> <span data-ttu-id="f5d9e-141">En este ejemplo se muestra cómo usar el método [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) para crear una reunión y enviar las convocatorias de reunión a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-141">This example shows how to use the [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="f5d9e-142">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el delegado y que se han concedido al delegado los permisos adecuados para la carpeta de contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-142">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the appropriate permissions for the mailbox owner's Contacts folder.</span></span> 
  
```cs
 public static void DelegateAccessCreateContact(ExchangeService service)
{
    // Create the contact.
    Contact contact = new Contact(service);
    // Specify the name and how the contact should be filed.
    contact.GivenName = "Brian";
    contact.MiddleName = "David";
    contact.Surname = "Johnson";
    contact.FileAsMapping = FileAsMapping.SurnameCommaGivenName;
    // Specify the company name.
    contact.CompanyName = "Contoso";
    // Specify the business, home, and car phone numbers.
    contact.PhoneNumbers[PhoneNumberKey.BusinessPhone] = "425-555-0110";
    contact.PhoneNumbers[PhoneNumberKey.HomePhone] = "425-555-0120";
    contact.PhoneNumbers[PhoneNumberKey.CarPhone] = "425-555-0130";
    // Specify two email addresses.
    contact.EmailAddresses[EmailAddressKey.EmailAddress1] = 
        new EmailAddress("brian_1@contoso.com");
    contact.EmailAddresses[EmailAddressKey.EmailAddress2] = 
        new EmailAddress("brian_2@contoso.com");
    // Save the contact in the mailbox owner's Contacts folder.
    // This method call results in a CreateItem call to EWS. 
    // The contact identifier contains the context for the mailbox owner's 
    // Contact folder. Any additional actions take on this contact will 
    // be performed in the mailbox owner's mailbox. 
    contact.Save(new FolderId(WellKnownFolderName.Contacts, 
        "primary@contoso.com"));
    // Verify that the contact was created.
    // This method call results in a GetItem call to EWS
    // to load the display name property on the contact. 
    contact.Load(new PropertySet (ContactSchema.DisplayName));
    Console.WriteLine("\nContact created: " + contact.DisplayName + "\n");
}
```

<span data-ttu-id="f5d9e-143">Tenga en cuenta que, al guardar el elemento, la llamada al método [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) debe identificar la carpeta de contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-143">Note that when you save the item, the [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method call must identify the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="f5d9e-144">Si no se especifica la carpeta de contactos del propietario del buzón, la convocatoria de reunión se guarda en la carpeta contactos del delegado y no en la carpeta contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-144">If the mailbox owner's Contacts folder is not specified, the meeting request gets saved to the delegate's Contacts folder and not the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="f5d9e-145">Puede incluir la carpeta contactos del propietario del buzón en la llamada al método **Save** de dos maneras.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-145">You can include the mailbox owner's Contacts folder in the **Save** method call in two way.</span></span> <span data-ttu-id="f5d9e-146">Se recomienda crear una instancia de una nueva instancia del objeto [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) con el [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y la dirección SMTP del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-146">We recommend that you instantiate a new instance of the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) object by using the [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) and the SMTP address of the mailbox owner.</span></span> 
  
```cs
contact.Save(new FolderId(WellKnownFolderName.Contacts, "primary@contoso.com"));
```

<span data-ttu-id="f5d9e-147">Sin embargo, también puede [enlazar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) a la carpeta de contactos y, a continuación, usar el identificador de la carpeta en la llamada al método **Save** .</span><span class="sxs-lookup"><span data-stu-id="f5d9e-147">However, you can also [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) to the Contacts folder first, and then use the ID of the folder in the **Save** method call.</span></span> <span data-ttu-id="f5d9e-148">Sin embargo, tenga en cuenta que esto crea una llamada a EWS adicional.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-148">Be aware, however, that this creates an extra EWS call.</span></span> 
  
```cs
    // Identify the mailbox owner's SMTP address 
    // and bind to their Contacts folder.
    Mailbox primary = new Mailbox("primary@contoso.com"); 
    Folder primaryContacts = Folder.Bind(service, new FolderId(WellKnownFolderName.Contacts, primary)); 
…
    // Save the contact to the mailbox owner's Contacts folder.
    meeting.Save(primaryContacts.Id);
```

<span data-ttu-id="f5d9e-149"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="f5d9e-149"><a name="bk_createews"> </a></span></span>

## <a name="create-a-contact-as-a-delegate-by-using-ews"></a><span data-ttu-id="f5d9e-150">Crear un contacto como delegado mediante EWS</span><span class="sxs-lookup"><span data-stu-id="f5d9e-150">Create a contact as a delegate by using EWS</span></span>

<span data-ttu-id="f5d9e-151">EWS permite usar el objeto de servicio para que el usuario delegado cree elementos de contacto para el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-151">EWS enables you to use the service object for the delegate user to create contact items for the mailbox owner.</span></span> <span data-ttu-id="f5d9e-152">En este ejemplo se muestra cómo utilizar la operación [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para crear un contacto.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-152">This example shows how to use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a contact.</span></span> 
  
<span data-ttu-id="f5d9e-153">También es la solicitud XML que la API administrada de EWS envía cuando se usa el método **Save** para [crear un contacto](#bk_createewsma).</span><span class="sxs-lookup"><span data-stu-id="f5d9e-153">This is also the XML request that the EWS Managed API sends when you use the **Save** method to [create a contact](#bk_createewsma).</span></span>
  
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
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="contacts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:Contact>
          <t:FileAsMapping>LastCommaFirst</t:FileAsMapping>
          <t:GivenName>Brian</t:GivenName>
          <t:MiddleName>David</t:MiddleName>
          <t:CompanyName>Contoso</t:CompanyName>
          <t:EmailAddresses>
            <t:Entry Key="EmailAddress1">brian_1@contoso.com</t:Entry>
            <t:Entry Key="EmailAddress2">brian_2@contoso.com</t:Entry>
          </t:EmailAddresses>
          <t:PhoneNumbers>
            <t:Entry Key="BusinessPhone">425-555-0110</t:Entry>
            <t:Entry Key="HomePhone">425-555-0120</t:Entry>
            <t:Entry Key="CarPhone">425-555-0130</t:Entry>
          </t:PhoneNumbers>
          <t:Surname>Johnson</t:Surname>
        </t:Contact>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="f5d9e-154">El servidor responde a la solicitud **CreateItem** con un mensaje [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que el contacto se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-154">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the contact was created successfully.</span></span> <span data-ttu-id="f5d9e-155">La respuesta también contiene el identificador de elemento del contacto recién creado.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-155">The response also contains the item ID of the newly created contact.</span></span>

<span data-ttu-id="f5d9e-156"><a name="bk_resolveewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="f5d9e-156"><a name="bk_resolveewsma"> </a></span></span>

## <a name="resolve-a-contact-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="f5d9e-157">Resolver un contacto como delegado mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="f5d9e-157">Resolve a contact as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="f5d9e-158">Para buscar un contacto basándose en un nombre o término posiblemente ambiguo, debe usar uno de los métodos [ExchangeService. ResolveName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) que incluya un parámetro [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) , de modo que pueda especificar la carpeta de contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-158">To find a contact based on a possibly ambiguous name or term, you must use one of the [ExchangeService.ResolveName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) methods that includes a [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Contacts folder.</span></span> 
  
```cs
private static void DelegateAccessResolveContacts(ExchangeService service)
{
    // Create a list to store folders to search.
    List<FolderId> folders = new List<FolderId>();
   
    // Add the mailbox owner's folder to the list.
    folders.Add(new FolderId(WellKnownFolderName.Contacts, 
        "primary@contoso.com"));
    
    // Resolve the ambiguous name "Johnson".
    // This method call results in a ResolveNames call to EWS.
    NameResolutionCollection resolvedNames = service.ResolveName(
        "johnson", folders, ResolveNameSearchLocation.ContactsOnly, true);
    // Output the list of candidate email addresses and contact names.
    foreach (NameResolution nameRes in resolvedNames)
    {
        Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
        Console.WriteLine("Contact ID: " + nameRes.Mailbox.Id);
    }
}
```

<span data-ttu-id="f5d9e-159">Una vez que la llamada al método **ResolveNames** devuelve una respuesta con un identificador, puede [obtener, actualizar o eliminar el contacto](#bk_getewsma) mediante el uso del identificador y el [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit), &mdash; y no es necesario especificar la dirección SMTP del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-159">After the **ResolveNames** method call returns a response with an ID, you can [get, update or delete the contact](#bk_getewsma) using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;and you do not need to specify the mailbox owner's SMTP address.</span></span> 

<span data-ttu-id="f5d9e-160"><a name="bk_resolveews"> </a></span><span class="sxs-lookup"><span data-stu-id="f5d9e-160"><a name="bk_resolveews"> </a></span></span>

## <a name="resolve-a-contact-as-a-delegate-by-using-ews"></a><span data-ttu-id="f5d9e-161">Resolver un contacto como delegado mediante EWS</span><span class="sxs-lookup"><span data-stu-id="f5d9e-161">Resolve a contact as a delegate by using EWS</span></span>

<span data-ttu-id="f5d9e-162">EWS permite usar el objeto de servicio para que el usuario delegado resuelva los nombres parciales en la carpeta de contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-162">EWS enables you to use the service object for the delegate user to resolve partial names in the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="f5d9e-163">En este ejemplo se muestra cómo usar la operación [ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) para buscar reuniones en la carpeta de contactos del propietario del buzón de correo que contengan la palabra "Johnson".</span><span class="sxs-lookup"><span data-stu-id="f5d9e-163">This example shows how to use the [ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) operation to find meetings in the mailbox owner's Contacts folder that contain the word "johnson".</span></span> 
  
<span data-ttu-id="f5d9e-164">También es la solicitud XML que la API administrada de EWS envía cuando usa el método **ResolveName** para [resolver un contacto](#bk_resolveewsma).</span><span class="sxs-lookup"><span data-stu-id="f5d9e-164">This is also the XML request that the EWS Managed API sends when you use the **ResolveName** method to [resolve a contact](#bk_resolveewsma).</span></span>
  
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
    <m:ResolveNames ReturnFullContactData="true"
                    SearchScope="Contacts">
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="contacts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
      <m:UnresolvedEntry>johnson</m:UnresolvedEntry>
    </m:ResolveNames>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="f5d9e-165">El servidor responde a la solicitud **ResolveNames** con un mensaje [ResolveNamesResponse](https://msdn.microsoft.com/library/5e7be1e2-44ea-403f-9135-2388d030078c%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la operación se completó correctamente y encontró solo un resultado, o **ErrorNameResolutionMultipleResults** si se encontraron varios resultados, que es lo que se muestra en el tercer ejemplo de código en función del contacto [cree un contacto como delegado mediante la API administrada de EWS](#bk_createewsma).</span><span class="sxs-lookup"><span data-stu-id="f5d9e-165">The server responds to the **ResolveNames** request with a [ResolveNamesResponse](https://msdn.microsoft.com/library/5e7be1e2-44ea-403f-9135-2388d030078c%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the operation completed successfully and found only one result, or **ErrorNameResolutionMultipleResults** if multiple results were found - which is what's shown in third code example based on the contact [Create a contact as a delegate by using the EWS Managed API](#bk_createewsma).</span></span> <span data-ttu-id="f5d9e-166">La respuesta también contiene el [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) de cada resultado.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-166">The response also contains the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of each result.</span></span> 
  
<span data-ttu-id="f5d9e-167">El valor del elemento **Itemid** se ha abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-167">The value of the **ItemId** element has been shortened for readability.</span></span> 
  
```XML
 <?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Warning">
          <m:MessageText>Multiple results were found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionMultipleResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:ResolutionSet TotalItemsInView="2"
                           IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>brian_1@contoso.com</t:Name>
                <t:EmailAddress>brian_1@contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Contact</t:MailboxType>
                <t:ItemId Id="iMihAAA="
                          ChangeKey="EQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiPQo" />
              </t:Mailbox>
            </t:Resolution>
            <t:Resolution>
              <t:Mailbox>
                <t:Name>brian_2@contoso.com</t:Name>
                <t:EmailAddress>brian_2@contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Contact</t:MailboxType>
                <t:ItemId Id="iMihAAA="
                          ChangeKey="EQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiPQo" />
              </t:Mailbox>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </m:ResolveNamesResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="f5d9e-168">Ahora que tiene el **Itemid** para los contactos que coinciden con el nombre ambiguo, puede [obtener, actualizar o eliminar los elementos de contacto como delegado mediante EWS](#bk_getews) mediante el uso de **Itemid** y el [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) &mdash; y no es necesario especificar la dirección SMTP del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-168">Now that you have the **ItemId** for the contacts that match the ambiguous name, you can [Get, update, or delete contact items as a delegate by using EWS](#bk_getews) by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;and you do not need to specify the mailbox owner's SMTP address.</span></span> 

<span data-ttu-id="f5d9e-169"><a name="bk_getewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="f5d9e-169"><a name="bk_getewsma"> </a></span></span>

## <a name="get-update-or-delete-contact-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="f5d9e-170">Obtener, actualizar o eliminar elementos de contacto como un delegado mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="f5d9e-170">Get, update, or delete contact items as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="f5d9e-171">Puede usar la API administrada de EWS para obtener, actualizar o eliminar un contacto de la misma manera que realiza estas acciones cuando no está usando acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-171">You can use the EWS Managed API to get, update, or delete a contact in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="f5d9e-172">La única diferencia es que el objeto de servicio es para el usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-172">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="f5d9e-173">El identificador de elemento incluido en la llamada al método **BIND** identifica de forma única el elemento en el almacén de buzones, en la carpeta de contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-173">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Contacts folder.</span></span> 
  
<span data-ttu-id="f5d9e-174">**Tabla 2. Métodos de la API administrada de EWS trabajar con un contacto como delegado**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-174">**Table 2. EWS Managed API methods working with a contact as a delegate**</span></span>

|<span data-ttu-id="f5d9e-175">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-175">**Task**</span></span>|<span data-ttu-id="f5d9e-176">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-176">**EWS Managed API method**</span></span>|<span data-ttu-id="f5d9e-177">**Ejemplo de código**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-177">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f5d9e-178">Obtener un contacto</span><span class="sxs-lookup"><span data-stu-id="f5d9e-178">Get a contact</span></span>  <br/> |[<span data-ttu-id="f5d9e-179">BIND</span><span class="sxs-lookup"><span data-stu-id="f5d9e-179">Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="f5d9e-180">Obtener un elemento mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="f5d9e-180">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="f5d9e-181">Actualizar un contacto</span><span class="sxs-lookup"><span data-stu-id="f5d9e-181">Update a contact</span></span>  <br/> |<span data-ttu-id="f5d9e-182">[Enlazar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-182">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="f5d9e-183">Actualizar un elemento mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="f5d9e-183">Update an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|<span data-ttu-id="f5d9e-184">Eliminar un contacto</span><span class="sxs-lookup"><span data-stu-id="f5d9e-184">Delete a contact</span></span>  <br/> |<span data-ttu-id="f5d9e-185">[Enlazar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguida de [eliminar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-185">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="f5d9e-186">Eliminar un elemento mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="f5d9e-186">Delete an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |

<span data-ttu-id="f5d9e-187"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="f5d9e-187"><a name="bk_getews"> </a></span></span>

## <a name="get-update-or-delete-contact-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="f5d9e-188">Obtener, actualizar o eliminar elementos de contacto como un delegado mediante EWS</span><span class="sxs-lookup"><span data-stu-id="f5d9e-188">Get, update, or delete contact items as a delegate by using EWS</span></span>

<span data-ttu-id="f5d9e-189">Puede usar EWS para obtener, actualizar o eliminar un contacto de reunión o cita de la misma manera que realiza estas acciones cuando no está usando acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-189">You can use EWS to get, update, or delete a meeting or appointment contact in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="f5d9e-190">La única diferencia es que el objeto de servicio es para el usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-190">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="f5d9e-191">El identificador de elemento incluido en la solicitud [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) identifica de forma única el elemento en el almacén de buzones, en la carpeta de contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="f5d9e-191">The item ID included in the [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) request uniquely identifies the item in the mailbox store, in the mailbox owner's Contacts folder.</span></span> 
  
<span data-ttu-id="f5d9e-192">**Tabla 3. Operaciones de EWS para trabajar con un contacto como delegado**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-192">**Table 3. EWS operations for working with a contact as a delegate**</span></span>

|<span data-ttu-id="f5d9e-193">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-193">**Task**</span></span>|<span data-ttu-id="f5d9e-194">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-194">**EWS operation**</span></span>|<span data-ttu-id="f5d9e-195">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="f5d9e-195">**Sample**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f5d9e-196">Obtener un contacto</span><span class="sxs-lookup"><span data-stu-id="f5d9e-196">Get a contact</span></span>  <br/> |[<span data-ttu-id="f5d9e-197">GetItem</span><span class="sxs-lookup"><span data-stu-id="f5d9e-197">GetItem</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="f5d9e-198">Obtener un elemento mediante EWS</span><span class="sxs-lookup"><span data-stu-id="f5d9e-198">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="f5d9e-199">Actualizar un contacto</span><span class="sxs-lookup"><span data-stu-id="f5d9e-199">Update a contact</span></span>  <br/> |<span data-ttu-id="f5d9e-200">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido de [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-200">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="f5d9e-201">Actualizar un elemento mediante EWS</span><span class="sxs-lookup"><span data-stu-id="f5d9e-201">Update an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|<span data-ttu-id="f5d9e-202">Eliminar un contacto</span><span class="sxs-lookup"><span data-stu-id="f5d9e-202">Delete a contact</span></span>  <br/> |<span data-ttu-id="f5d9e-203">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido de [DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="f5d9e-203">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |[<span data-ttu-id="f5d9e-204">Eliminar un elemento mediante EWS</span><span class="sxs-lookup"><span data-stu-id="f5d9e-204">Delete an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f5d9e-205">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5d9e-205">See also</span></span>

- [<span data-ttu-id="f5d9e-206">Acceso delegado y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f5d9e-206">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
- [<span data-ttu-id="f5d9e-207">Agregar y quitar delegados mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f5d9e-207">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [<span data-ttu-id="f5d9e-208">Establecer los permisos de carpeta para otro usuario mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f5d9e-208">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)
- [<span data-ttu-id="f5d9e-209">Personas y contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f5d9e-209">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)
- [<span data-ttu-id="f5d9e-210">Resolver nombres ambiguos mediante EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="f5d9e-210">Resolve ambiguous names by using EWS in Exchange 2013</span></span>](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)
    

