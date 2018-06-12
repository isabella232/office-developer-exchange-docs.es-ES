---
title: Contactos de acceso como delegado mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3cd34c14-18b0-4fe2-a4c2-d884318c88fc
description: Obtenga información sobre cómo obtener acceso a los contactos como delegado mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: a7f695dcbe0693809817de84284294dff872aa9c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763029"
---
# <a name="access-contacts-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="bff9b-103">Contactos de acceso como delegado mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="bff9b-103">Access contacts as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="bff9b-104">Obtenga información sobre cómo obtener acceso a los contactos como delegado mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="bff9b-104">Learn how to access contacts as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="bff9b-105">Puede usar la API administrada de EWS o EWS para otorgar a un usuario acceso a la carpeta de contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bff9b-105">You can use the EWS Managed API or EWS to give a user access to a mailbox owner's Contacts folder.</span></span> <span data-ttu-id="bff9b-106">A continuación, el delegado puede crear contactos en nombre del propietario del buzón de correo y recuperar, actualizar y eliminar los contactos de la carpeta de contactos del propietario del buzón, en función de sus permisos.</span><span class="sxs-lookup"><span data-stu-id="bff9b-106">The delegate can then create contacts on behalf of the mailbox owner, and retrieve, update, and delete contacts from the mailbox owner's Contacts folder, depending on their permissions.</span></span>
  
<span data-ttu-id="bff9b-107">Como delegado, use los mismos métodos y operaciones para tener acceso a la carpeta de contactos del propietario del buzón que usan para tener acceso a su propia carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="bff9b-107">As a delegate, you use the same methods and operations to access a mailbox owner's Contacts folder that you use to access your own Contacts folder.</span></span> <span data-ttu-id="bff9b-108">La diferencia principal es que se debe usar [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicit) para buscar o crear un elemento de contacto y, a continuación, después de identificar el identificador de elemento, puede usar [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit) para obtener, actualizar o eliminar el elemento.</span><span class="sxs-lookup"><span data-stu-id="bff9b-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create a contact item, and then after you identify the item ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="bff9b-109">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para obtener acceso a un contacto como delegado**</span><span class="sxs-lookup"><span data-stu-id="bff9b-109">**Table 1. EWS Managed API methods and EWS operations for accessing a contact as a delegate**</span></span>

|<span data-ttu-id="bff9b-110">**Si quiere...**</span><span class="sxs-lookup"><span data-stu-id="bff9b-110">**If you want to…**</span></span>|<span data-ttu-id="bff9b-111">**Use este método de la API administrada de EWS...**</span><span class="sxs-lookup"><span data-stu-id="bff9b-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="bff9b-112">**Use esta operación de EWS...**</span><span class="sxs-lookup"><span data-stu-id="bff9b-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bff9b-113">Crear un contacto como delegado</span><span class="sxs-lookup"><span data-stu-id="bff9b-113">Create a contact as a delegate</span></span>  <br/> |<span data-ttu-id="bff9b-114">[Item.Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx) donde el parámetro [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de contactos del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="bff9b-114">[Item.Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx) where the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="bff9b-115">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) donde el elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica la [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="bff9b-115">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="bff9b-116">Crear varios contactos como delegado</span><span class="sxs-lookup"><span data-stu-id="bff9b-116">Create multiple contacts as a delegate</span></span>  <br/> |<span data-ttu-id="bff9b-117">[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) donde el parámetro **FolderId** proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de contactos del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="bff9b-117">[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="bff9b-118">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) donde el elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica la [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="bff9b-118">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="bff9b-119">Resolver un contacto como delegado</span><span class="sxs-lookup"><span data-stu-id="bff9b-119">Resolve a contact as a delegate</span></span>  <br/> |<span data-ttu-id="bff9b-120">[ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) donde el parámetro [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de contactos del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="bff9b-120">[ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) where the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="bff9b-121">[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) donde el elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica la [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="bff9b-121">[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="bff9b-122">Buscar o buscar un contacto como delegado</span><span class="sxs-lookup"><span data-stu-id="bff9b-122">Search for or find a contact as a delegate</span></span>  <br/> |<span data-ttu-id="bff9b-123">[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) donde el parámetro **FolderId** proporciona [acceso explícito](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) a la carpeta de contactos del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="bff9b-123">[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder</span></span>  <br/> |<span data-ttu-id="bff9b-124">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) donde el elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) especifica la [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) del propietario del buzón</span><span class="sxs-lookup"><span data-stu-id="bff9b-124">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="bff9b-125">Obtener un contacto como delegado</span><span class="sxs-lookup"><span data-stu-id="bff9b-125">Get a contact as a delegate</span></span>  <br/> |[<span data-ttu-id="bff9b-126">Contact.Bind</span><span class="sxs-lookup"><span data-stu-id="bff9b-126">Contact.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="bff9b-127">GetItem</span><span class="sxs-lookup"><span data-stu-id="bff9b-127">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="bff9b-128">Actualizar un contacto como delegado</span><span class="sxs-lookup"><span data-stu-id="bff9b-128">Update a contact as a delegate</span></span>  <br/> |<span data-ttu-id="bff9b-129">[Contact.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) seguido de [Contact.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bff9b-129">[Contact.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) followed by [Contact.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="bff9b-130">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bff9b-130">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="bff9b-131">Eliminar un contacto como delegado</span><span class="sxs-lookup"><span data-stu-id="bff9b-131">Delete a contact as a delegate</span></span>  <br/> |<span data-ttu-id="bff9b-132">[Contact.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) seguido de [Contact.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bff9b-132">[Contact.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) followed by [Contact.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="bff9b-133">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bff9b-133">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span></span> <br/> |
   
> [!NOTE]
> <span data-ttu-id="bff9b-134">En los ejemplos de código de este artículo, primary@contoso.com es el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bff9b-134">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 

<span data-ttu-id="bff9b-135"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="bff9b-135"></span></span>

## <a name="prerequisite-tasks"></a><span data-ttu-id="bff9b-136">Tareas de requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bff9b-136">Prerequisite tasks</span></span>

<span data-ttu-id="bff9b-137">Antes de que un usuario puede obtener acceso a la carpeta de contactos del propietario del buzón como delegado, el usuario debe ser [agregado como delegado con permisos](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) para la carpeta de contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bff9b-137">Before a user can access the mailbox owner's Contacts folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Contacts folder.</span></span> 

<span data-ttu-id="bff9b-138"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="bff9b-138"></span></span>

## <a name="create-a-contact-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="bff9b-139">Crear un contacto como delegado mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="bff9b-139">Create a contact as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="bff9b-140">La API administrada de EWS le permite usar el objeto de servicio para el usuario delegado para crear contactos para el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bff9b-140">The EWS Managed API enables you to use the service object for the delegate user to create contacts for the mailbox owner.</span></span> <span data-ttu-id="bff9b-141">En este ejemplo se muestra cómo utilizar el método [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) para crear una reunión y enviar convocatorias de reunión a los asistentes.</span><span class="sxs-lookup"><span data-stu-id="bff9b-141">This example shows how to use the [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="bff9b-142">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el delegado y que el delegado se ha concedido los permisos adecuados para la carpeta de contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bff9b-142">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the appropriate permissions for the mailbox owner's Contacts folder.</span></span> 
  
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

<span data-ttu-id="bff9b-143">Tenga en cuenta que cuando se guarda el elemento, la llamada al método [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) debe identificar carpeta de contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bff9b-143">Note that when you save the item, the [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method call must identify the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="bff9b-144">Si no se especifica la carpeta de contactos del propietario del buzón, la convocatoria de reunión obtiene guardan en la carpeta de contactos del delegado y no la carpeta de contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bff9b-144">If the mailbox owner's Contacts folder is not specified, the meeting request gets saved to the delegate's Contacts folder and not the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="bff9b-145">Puede incluir la carpeta de contactos del propietario del buzón en la llamada al método **Guardar** en la forma dos.</span><span class="sxs-lookup"><span data-stu-id="bff9b-145">You can include the mailbox owner's Contacts folder in the **Save** method call in two way.</span></span> <span data-ttu-id="bff9b-146">Se recomienda que se cree una instancia de una nueva instancia del objeto [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) mediante el uso de la [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y la dirección SMTP del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bff9b-146">We recommend that you instantiate a new instance of the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) object by using the [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) and the SMTP address of the mailbox owner.</span></span> 
  
```cs
contact.Save(new FolderId(WellKnownFolderName.Contacts, "primary@contoso.com"));
```

<span data-ttu-id="bff9b-147">Sin embargo, también puede [enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) a la carpeta Contactos en primer lugar y, a continuación, use el identificador de la carpeta en la llamada al método **Save** .</span><span class="sxs-lookup"><span data-stu-id="bff9b-147">However, you can also [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) to the Contacts folder first, and then use the ID of the folder in the **Save** method call.</span></span> <span data-ttu-id="bff9b-148">Tenga en cuenta, sin embargo, esto crea una llamada EWS adicional.</span><span class="sxs-lookup"><span data-stu-id="bff9b-148">Be aware, however, that this creates an extra EWS call.</span></span> 
  
```cs
    // Identify the mailbox owner's SMTP address 
    // and bind to their Contacts folder.
    Mailbox primary = new Mailbox("primary@contoso.com"); 
    Folder primaryContacts = Folder.Bind(service, new FolderId(WellKnownFolderName.Contacts, primary)); 
…
    // Save the contact to the mailbox owner's Contacts folder.
    meeting.Save(primaryContacts.Id);
```

<span data-ttu-id="bff9b-149"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="bff9b-149"></span></span>

## <a name="create-a-contact-as-a-delegate-by-using-ews"></a><span data-ttu-id="bff9b-150">Crear un contacto como delegado mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="bff9b-150">Create a contact as a delegate by using EWS</span></span>

<span data-ttu-id="bff9b-151">EWS le permite usar el objeto de servicio para el usuario delegado para crear elementos de contacto para el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bff9b-151">EWS enables you to use the service object for the delegate user to create contact items for the mailbox owner.</span></span> <span data-ttu-id="bff9b-152">En este ejemplo se muestra cómo usar la operación [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) para crear un contacto.</span><span class="sxs-lookup"><span data-stu-id="bff9b-152">This example shows how to use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a contact.</span></span> 
  
<span data-ttu-id="bff9b-153">También es la solicitud XML que la API administrada de EWS envía cuando se utiliza el método **Save** para [crear un contacto](#bk_createewsma).</span><span class="sxs-lookup"><span data-stu-id="bff9b-153">This is also the XML request that the EWS Managed API sends when you use the **Save** method to [create a contact](#bk_createewsma).</span></span>
  
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

<span data-ttu-id="bff9b-154">El servidor responde a la solicitud **CreateItem** con un mensaje de [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que el contacto se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bff9b-154">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the contact was created successfully.</span></span> <span data-ttu-id="bff9b-155">La respuesta también contiene el identificador de elemento de contacto recientemente creado.</span><span class="sxs-lookup"><span data-stu-id="bff9b-155">The response also contains the item ID of the newly created contact.</span></span>

<span data-ttu-id="bff9b-156"><a name="bk_resolveewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="bff9b-156"></span></span>

## <a name="resolve-a-contact-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="bff9b-157">Resolver un contacto como delegado mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="bff9b-157">Resolve a contact as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="bff9b-158">Para buscar un contacto en función de un nombre ambiguo, posiblemente, o términos, debe usar uno de los métodos de [ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) que incluya un parámetro [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) , por lo que puede especificar la carpeta de contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bff9b-158">To find a contact based on a possibly ambiguous name or term, you must use one of the [ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) methods that includes a [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Contacts folder.</span></span> 
  
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

<span data-ttu-id="bff9b-159">Después de la llamada al método **ResolveNames** devuelve una respuesta con un identificador, se puede [obtener, actualizar o eliminar el contacto](#bk_getewsma) con el identificador y el [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;y no es necesario especificar la dirección de SMTP del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bff9b-159">After the **ResolveNames** method call returns a response with an ID, you can [get, update or delete the contact](#bk_getewsma) using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;and you do not need to specify the mailbox owner's SMTP address.</span></span> 

<span data-ttu-id="bff9b-160"><a name="bk_resolveews"> </a></span><span class="sxs-lookup"><span data-stu-id="bff9b-160"></span></span>

## <a name="resolve-a-contact-as-a-delegate-by-using-ews"></a><span data-ttu-id="bff9b-161">Resolver un contacto como delegado mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="bff9b-161">Resolve a contact as a delegate by using EWS</span></span>

<span data-ttu-id="bff9b-162">EWS le permite usar el objeto de servicio para el usuario delegado para resolver nombres de parciales en la carpeta de contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bff9b-162">EWS enables you to use the service object for the delegate user to resolve partial names in the mailbox owner's Contacts folder.</span></span> <span data-ttu-id="bff9b-163">En este ejemplo se muestra cómo usar la operación [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) para buscar las reuniones en la carpeta de contactos del propietario del buzón que contengan la palabra "García".</span><span class="sxs-lookup"><span data-stu-id="bff9b-163">This example shows how to use the [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) operation to find meetings in the mailbox owner's Contacts folder that contain the word "johnson".</span></span> 
  
<span data-ttu-id="bff9b-164">También es la solicitud XML que la API administrada de EWS envía cuando se utiliza el método **ResolveName** para [resolver un contacto](#bk_resolveewsma).</span><span class="sxs-lookup"><span data-stu-id="bff9b-164">This is also the XML request that the EWS Managed API sends when you use the **ResolveName** method to [resolve a contact](#bk_resolveewsma).</span></span>
  
```xml
 <?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="bff9b-165">El servidor responde a la solicitud de **ResolveNames** con un mensaje de [ResolveNamesResponse](http://msdn.microsoft.com/library/5e7be1e2-44ea-403f-9135-2388d030078c%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la operación se realizó correctamente y que se encuentre una sola resultado, o **ErrorNameResolutionMultipleResults** si se han encontrado varios resultados - que es lo que se muestra en el tercer ejemplo de código basada en el contacto al [crear un contacto como delegado mediante el uso de la API administrada de EWS](#bk_createewsma).</span><span class="sxs-lookup"><span data-stu-id="bff9b-165">The server responds to the **ResolveNames** request with a [ResolveNamesResponse](http://msdn.microsoft.com/library/5e7be1e2-44ea-403f-9135-2388d030078c%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the operation completed successfully and found only one result, or **ErrorNameResolutionMultipleResults** if multiple results were found - which is what's shown in third code example based on the contact [Create a contact as a delegate by using the EWS Managed API](#bk_createewsma).</span></span> <span data-ttu-id="bff9b-166">La respuesta contiene también el [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) de cada resultado.</span><span class="sxs-lookup"><span data-stu-id="bff9b-166">The response also contains the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of each result.</span></span> 
  
<span data-ttu-id="bff9b-167">El valor del elemento **ItemId** se ha acortado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="bff9b-167">The value of the **ItemId** element has been shortened for readability.</span></span> 
  
```XML
 <?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="bff9b-168">Ahora que tiene la **ItemId** para los contactos que coinciden con el nombre ambiguo, se puede [obtener, actualizar o eliminación de elementos de contacto como delegado mediante el uso de EWS](#bk_getews) mediante el [acceso implícito](delegate-access-and-ews-in-exchange.md#bk_implicit)y **ItemId** &mdash;y no es necesario especificar dirección de SMTP del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bff9b-168">Now that you have the **ItemId** for the contacts that match the ambiguous name, you can [Get, update, or delete contact items as a delegate by using EWS](#bk_getews) by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;and you do not need to specify the mailbox owner's SMTP address.</span></span> 

<span data-ttu-id="bff9b-169"><a name="bk_getewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="bff9b-169"></span></span>

## <a name="get-update-or-delete-contact-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="bff9b-170">Obtener, actualizar o eliminar elementos de contacto como delegado mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="bff9b-170">Get, update, or delete contact items as a delegate by using the EWS Managed API</span></span>

<span data-ttu-id="bff9b-171">Puede usar la API administrada de EWS para obtener, actualizar o eliminar un contacto de la misma manera que se realizan estas acciones cuando no está utilizando acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="bff9b-171">You can use the EWS Managed API to get, update, or delete a contact in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="bff9b-172">La única diferencia es que el objeto de servicio para el usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="bff9b-172">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="bff9b-173">El identificador de elemento incluido en la llamada al método **enlazar** de forma única identifica el elemento en el almacén de buzón de correo, en la carpeta de contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bff9b-173">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Contacts folder.</span></span> 
  
<span data-ttu-id="bff9b-174">**Tabla 2. Métodos de API administrada de EWS trabajar con un contacto como delegado**</span><span class="sxs-lookup"><span data-stu-id="bff9b-174">**Table 2. EWS Managed API methods working with a contact as a delegate**</span></span>

|<span data-ttu-id="bff9b-175">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="bff9b-175">**Task**</span></span>|<span data-ttu-id="bff9b-176">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="bff9b-176">**EWS Managed API method**</span></span>|<span data-ttu-id="bff9b-177">**Ejemplo de código**</span><span class="sxs-lookup"><span data-stu-id="bff9b-177">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bff9b-178">Obtener un contacto</span><span class="sxs-lookup"><span data-stu-id="bff9b-178">Get a contact</span></span>  <br/> |[<span data-ttu-id="bff9b-179">Enlazar</span><span class="sxs-lookup"><span data-stu-id="bff9b-179">Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="bff9b-180">Obtener un elemento mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="bff9b-180">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="bff9b-181">Actualizar un contacto</span><span class="sxs-lookup"><span data-stu-id="bff9b-181">Update a contact</span></span>  <br/> |<span data-ttu-id="bff9b-182">[Enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [actualización](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bff9b-182">[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="bff9b-183">Actualizar un elemento mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="bff9b-183">Update an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|<span data-ttu-id="bff9b-184">Eliminar un contacto</span><span class="sxs-lookup"><span data-stu-id="bff9b-184">Delete a contact</span></span>  <br/> |<span data-ttu-id="bff9b-185">[Enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) seguido de [Eliminar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bff9b-185">[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="bff9b-186">Eliminar un elemento mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="bff9b-186">Delete an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |

<span data-ttu-id="bff9b-187"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="bff9b-187"></span></span>

## <a name="get-update-or-delete-contact-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="bff9b-188">Obtener, actualizar o eliminar elementos de contacto como delegado mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="bff9b-188">Get, update, or delete contact items as a delegate by using EWS</span></span>

<span data-ttu-id="bff9b-189">Puede usar EWS para obtener, actualizar o eliminar un contacto de reunión o una cita de la misma manera que se realizan estas acciones cuando no está utilizando acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="bff9b-189">You can use EWS to get, update, or delete a meeting or appointment contact in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="bff9b-190">La única diferencia es que el objeto de servicio para el usuario delegado.</span><span class="sxs-lookup"><span data-stu-id="bff9b-190">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="bff9b-191">El identificador de elemento incluido en la solicitud de [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) identifica de forma exclusiva identifica el elemento en el almacén de buzón de correo, en la carpeta de contactos del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bff9b-191">The item ID included in the [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) request uniquely identifies the item in the mailbox store, in the mailbox owner's Contacts folder.</span></span> 
  
<span data-ttu-id="bff9b-192">**Tabla 3. Operaciones de EWS para trabajar con un contacto como delegado**</span><span class="sxs-lookup"><span data-stu-id="bff9b-192">**Table 3. EWS operations for working with a contact as a delegate**</span></span>

|<span data-ttu-id="bff9b-193">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="bff9b-193">**Task**</span></span>|<span data-ttu-id="bff9b-194">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="bff9b-194">**EWS operation**</span></span>|<span data-ttu-id="bff9b-195">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="bff9b-195">**Sample**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bff9b-196">Obtener un contacto</span><span class="sxs-lookup"><span data-stu-id="bff9b-196">Get a contact</span></span>  <br/> |[<span data-ttu-id="bff9b-197">GetItem</span><span class="sxs-lookup"><span data-stu-id="bff9b-197">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="bff9b-198">Obtener un elemento mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="bff9b-198">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="bff9b-199">Actualizar un contacto</span><span class="sxs-lookup"><span data-stu-id="bff9b-199">Update a contact</span></span>  <br/> |<span data-ttu-id="bff9b-200">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bff9b-200">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="bff9b-201">Actualizar un elemento mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="bff9b-201">Update an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|<span data-ttu-id="bff9b-202">Eliminar un contacto</span><span class="sxs-lookup"><span data-stu-id="bff9b-202">Delete a contact</span></span>  <br/> |<span data-ttu-id="bff9b-203">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) seguido [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bff9b-203">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="bff9b-204">Eliminar un elemento mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="bff9b-204">Delete an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bff9b-205">Ver también</span><span class="sxs-lookup"><span data-stu-id="bff9b-205">See also</span></span>

- [<span data-ttu-id="bff9b-206">Acceso delegado y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="bff9b-206">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
- [<span data-ttu-id="bff9b-207">Agregar y quitar delegados mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="bff9b-207">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [<span data-ttu-id="bff9b-208">Establecer permisos de carpeta de otro usuario mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="bff9b-208">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)
- [<span data-ttu-id="bff9b-209">Las personas y los contactos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="bff9b-209">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)
- [<span data-ttu-id="bff9b-210">Resolver nombres ambiguos mediante el uso de EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="bff9b-210">Resolve ambiguous names by using EWS in Exchange 2013</span></span>](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)
    

