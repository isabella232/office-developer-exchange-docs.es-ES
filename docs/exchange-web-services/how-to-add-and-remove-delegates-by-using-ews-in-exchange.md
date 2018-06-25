---
title: Agregar y quitar delegados mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cc7760bf-633b-483a-84ae-b52f437af2d3
description: Obtenga información sobre cómo agregar delegados a o quitar delegados de buzones de los usuarios mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: d55ef6c5c4e434603d293dbe30c6147ceb73b08b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763028"
---
# <a name="add-and-remove-delegates-by-using-ews-in-exchange"></a><span data-ttu-id="15bce-103">Agregar y quitar delegados mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="15bce-103">Add and remove delegates by using EWS in Exchange</span></span>

<span data-ttu-id="15bce-104">Obtenga información sobre cómo agregar delegados a o quitar delegados de buzones de los usuarios mediante el uso de la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="15bce-104">Learn how to add delegates to or remove delegates from users' mailboxes by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="15bce-105">Puede usar la API administrada de EWS o EWS para habilitar delegados para actuar en nombre de un propietario del buzón o quitar el acceso de un delegado para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="15bce-105">You can use the EWS Managed API or EWS to enable delegates to act on behalf of a mailbox owner or remove a delegate's access to a mailbox.</span></span> <span data-ttu-id="15bce-106">Los usuarios que se agregan como delegado y se les deben conceder permisos, pueden realizar tareas en nombre del propietario del buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="15bce-106">Users who are added as a delegate, and are given permissions, can perform tasks on behalf of the mailbox owner.</span></span> <span data-ttu-id="15bce-107">Por ejemplo, puede crear y enviar invitaciones a reuniones, enviar mensajes de correo electrónico y responder a convocatorias de reunión en nombre del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="15bce-107">For example, they can create and send meeting invitations, send emails, and respond to meeting requests on the mailbox owner's behalf.</span></span> 
  
<span data-ttu-id="15bce-108">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para la adición y eliminación de delegados**</span><span class="sxs-lookup"><span data-stu-id="15bce-108">**Table 1. EWS Managed API methods and EWS operations for adding and removing delegates**</span></span>

|<span data-ttu-id="15bce-109">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="15bce-109">**Task**</span></span>|<span data-ttu-id="15bce-110">**Método de la API administrada de EWS**</span><span class="sxs-lookup"><span data-stu-id="15bce-110">**EWS Managed API method**</span></span>|<span data-ttu-id="15bce-111">**Operación de EWS**</span><span class="sxs-lookup"><span data-stu-id="15bce-111">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="15bce-112">Agregar delegados</span><span class="sxs-lookup"><span data-stu-id="15bce-112">Add delegates</span></span>  <br/> |[<span data-ttu-id="15bce-113">ExchangeService.AddDelegates</span><span class="sxs-lookup"><span data-stu-id="15bce-113">ExchangeService.AddDelegates</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="15bce-114">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="15bce-114">AddDelegate</span></span>](http://msdn.microsoft.com/library/646fb994-229e-4d90-8b95-6541191cb3ae%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="15bce-115">Eliminación de delegados</span><span class="sxs-lookup"><span data-stu-id="15bce-115">Remove delegates</span></span>  <br/> |[<span data-ttu-id="15bce-116">ExchangeService.RemoveDelegates</span><span class="sxs-lookup"><span data-stu-id="15bce-116">ExchangeService.RemoveDelegates</span></span>](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="15bce-117">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="15bce-117">RemoveDelegate</span></span>](http://msdn.microsoft.com/library/f21c5171-62e7-47c8-99b1-22e1ff5883bb%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="15bce-118">Después de un delegado se concede permisos a una carpeta, puede actuar en los elementos de la carpeta y las subcarpetas, según sus [permisos de delegado](delegate-access-and-ews-in-exchange.md#bk_delegateperms).</span><span class="sxs-lookup"><span data-stu-id="15bce-118">After a delegate is granted permissions to a folder, they can act on items in the folder and any subfolders, according to their [delegate permissions](delegate-access-and-ews-in-exchange.md#bk_delegateperms).</span></span> <span data-ttu-id="15bce-119">Permisos para los delegados sólo se aplican a las subcarpetas que se crean después de que se ha concedido el acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="15bce-119">Permissions for delegates only apply to subfolders that are created after the delegate access was granted.</span></span> <span data-ttu-id="15bce-120">Para actualizar los permisos de carpeta para carpetas ya existentes, o en otras carpetas, vea [establecer permisos de carpeta de otro usuario mediante el uso de EWS en Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="15bce-120">To update folder permissions for pre-existing folders, or other folders, see [Set folder permissions for another user by using EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="15bce-121">Tenga en cuenta que sólo se pueden agregar delegados a cuentas con buzón habilitado, incluidos los grupos de seguridad habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="15bce-121">Note that delegates can only be added to mailbox-enabled accounts, including mail-enabled security groups.</span></span> <span data-ttu-id="15bce-122">De forma predeterminada, una única llamada de acceso de delegado EWS puede tener acceso a un máximo de 255 buzones diferentes.</span><span class="sxs-lookup"><span data-stu-id="15bce-122">By default, a single EWS delegate access call can access a maximum of 255 different mailboxes.</span></span>

<span data-ttu-id="15bce-123"><a name="bk_adddelegateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="15bce-123"></span></span>

## <a name="add-delegates-by-using-the-ews-managed-api"></a><span data-ttu-id="15bce-124">Agregar delegados mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="15bce-124">Add delegates by using the EWS Managed API</span></span>

<span data-ttu-id="15bce-125">Puede agregar delegados a un buzón de correo mediante el método de la API administrada de EWS [AddDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="15bce-125">You can add delegates to a mailbox by using the [AddDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) EWS Managed API method.</span></span> <span data-ttu-id="15bce-126">En este ejemplo, un nuevo calendario, contactos y correo electrónico [UsuarioDelegado](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegateuser%28v=exchg.80%29.aspx) se crea el objeto, y cada delegado se les deben conceder [permisos de Editor](delegate-access-and-ews-in-exchange.md#bk_delegateperms) para sus respectivas carpetas.</span><span class="sxs-lookup"><span data-stu-id="15bce-126">In this example, a new calendar, contact, and email [DelegateUser](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegateuser%28v=exchg.80%29.aspx) object is created, and each delegate is given [Editor permissions](delegate-access-and-ews-in-exchange.md#bk_delegateperms) for their respective folder.</span></span> <span data-ttu-id="15bce-127">Puede modificar el ejemplo para agregar a un delegado a cualquiera de las carpetas especificadas por las [Propiedades DelegatePermissions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegatepermissions_properties%28v=exchg.80%29.aspx), y puede establecer los permisos a cualquiera de los valores especificados por la enumeración [DelegateFolderPermissionLevel](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegatefolderpermissionlevel%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="15bce-127">You can modify the example to add a delegate to any of the folders specified by the [DelegatePermissions properties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegatepermissions_properties%28v=exchg.80%29.aspx), and you can set the permissions to any of the values specified by the [DelegateFolderPermissionLevel](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegatefolderpermissionlevel%28v=exchg.80%29.aspx) enumeration.</span></span> 
  
<span data-ttu-id="15bce-128">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el propietario del buzón, y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="15bce-128">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static Collection<DelegateUserResponse> AddDelegates(ExchangeService service)
{
    // Create a list to hold the new delegates to add.
    List<DelegateUser> newDelegates = new System.Collections.Generic.List<DelegateUser>();
    // Create a new delegate that has editor access to the mailbox owner's Calendar folder.
    DelegateUser calendarDelegate = new DelegateUser("calendardelegate@contoso.com");
    calendarDelegate.Permissions.CalendarFolderPermissionLevel = DelegateFolderPermissionLevel.Editor;
    // Add the delegate to the list of new delegates.
    newDelegates.Add(calendarDelegate);
    // Create a new delegate that has editor access to the mailbox owner's Contacts folder.
    DelegateUser contactDelegate = new DelegateUser("contactdelegate@contoso.com");
    contactDelegate.Permissions.ContactsFolderPermissionLevel = DelegateFolderPermissionLevel.Editor;
    // Add the delegate to the list of new delegates.
    newDelegates.Add(contactDelegate);
            
    // Create a new delegate that has editor access to the mailbox owner's Inbox folder.
    DelegateUser emailDelegate = new DelegateUser("emaildelegate@contoso.com");
    emailDelegate.Permissions.InboxFolderPermissionLevel = DelegateFolderPermissionLevel.Editor;
    // Add the delegate to the list of new delegates.
    newDelegates.Add(emailDelegate);
    // Create a mailbox object that represents the mailbox owner.
    Mailbox mailbox = new Mailbox("primary@contoso.com");
    // Call the AddDelegates method to add the delegates to the target mailbox.
    Collection<DelegateUserResponse> response = service.AddDelegates(mailbox, MeetingRequestsDeliveryScope.DelegatesAndSendInformationToMe, newDelegates);
            
    foreach (DelegateUserResponse resp in response)
    {
        // Print out the result and the last eight characters of the item ID.
        Console.WriteLine("For delegate " + resp.DelegateUser.UserId.PrimarySmtpAddress.ToString());
        Console.WriteLine("Result: {0}", resp.Result);
        Console.WriteLine("Error Code: {0}", resp.ErrorCode);
        Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
        Console.WriteLine("\r\n");
    }
    return response;
}
```

<span data-ttu-id="15bce-129"><a name="bk_adddelegateews"> </a></span><span class="sxs-lookup"><span data-stu-id="15bce-129"></span></span>

## <a name="add-delegates-by-using-ews"></a><span data-ttu-id="15bce-130">Agregar delegados mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="15bce-130">Add delegates by using EWS</span></span>

<span data-ttu-id="15bce-131">En el ejemplo de código siguiente se muestra cómo agregar independiente calendario, contactos y delegados de correo electrónico mediante el uso de la operación de EWS [AddDelegate](http://msdn.microsoft.com/library/012d8cc5-648c-4ba0-a155-15c422b1e994%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="15bce-131">The following code example shows how to add separate calendar, contact, and email delegates by using the [AddDelegate](http://msdn.microsoft.com/library/012d8cc5-648c-4ba0-a155-15c422b1e994%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="15bce-132">El buzón de correo para modificar especificada por el elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) , y la configuración de [permisos](delegate-access-and-ews-in-exchange.md#bk_delegateperms) para cada delegado está contenida en el elemento [UsuarioDelegado](http://msdn.microsoft.com/library/aac4e74e-f69b-4c41-a0c9-489610330fbf%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="15bce-132">The mailbox to modify is specified by the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element, and the [permission](delegate-access-and-ews-in-exchange.md#bk_delegateperms) settings for each delegate are contained in the [DelegateUser](http://msdn.microsoft.com/library/aac4e74e-f69b-4c41-a0c9-489610330fbf%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="15bce-133">Cada uno de los delegados se han concedido permisos de Editor para su carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="15bce-133">Each of the delegates has been granted Editor permissions to their target folder.</span></span> 
  
<span data-ttu-id="15bce-134">También es la solicitud XML que la API administrada de EWS envía cuando se utiliza el método **AddDelegates** para [Agregar a los delegados](#bk_adddelegateewsma).</span><span class="sxs-lookup"><span data-stu-id="15bce-134">This is also the XML request that the EWS Managed API sends when you use the **AddDelegates** method to [add delegates](#bk_adddelegateewsma).</span></span>
  
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
    <m:AddDelegate>
      <m:Mailbox>
        <t:EmailAddress>primary@contoso.com</t:EmailAddress>
      </m:Mailbox>
      <m:DelegateUsers>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>calendardelegate@contoso.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:CalendarFolderPermissionLevel>Editor</t:CalendarFolderPermissionLevel>
            <t:TasksFolderPermissionLevel>None</t:TasksFolderPermissionLevel>
            <t:InboxFolderPermissionLevel>None</t:InboxFolderPermissionLevel>
            <t:ContactsFolderPermissionLevel>None</t:ContactsFolderPermissionLevel>
            <t:NotesFolderPermissionLevel>None</t:NotesFolderPermissionLevel>
            <t:JournalFolderPermissionLevel>None</t:JournalFolderPermissionLevel>
          </t:DelegatePermissions>
          <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
          <t:ViewPrivateItems>false</t:ViewPrivateItems>
        </t:DelegateUser>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>contactdelegate@contoso.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:CalendarFolderPermissionLevel>None</t:CalendarFolderPermissionLevel>
            <t:TasksFolderPermissionLevel>None</t:TasksFolderPermissionLevel>
            <t:InboxFolderPermissionLevel>None</t:InboxFolderPermissionLevel>
            <t:ContactsFolderPermissionLevel>Editor</t:ContactsFolderPermissionLevel>
            <t:NotesFolderPermissionLevel>None</t:NotesFolderPermissionLevel>
            <t:JournalFolderPermissionLevel>None</t:JournalFolderPermissionLevel>
          </t:DelegatePermissions>
          <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
          <t:ViewPrivateItems>false</t:ViewPrivateItems>
        </t:DelegateUser>
        <t:DelegateUser>
          <t:UserId>
            <t:PrimarySmtpAddress>emaildelegate@contoso.com</t:PrimarySmtpAddress>
          </t:UserId>
          <t:DelegatePermissions>
            <t:CalendarFolderPermissionLevel>None</t:CalendarFolderPermissionLevel>
            <t:TasksFolderPermissionLevel>None</t:TasksFolderPermissionLevel>
            <t:InboxFolderPermissionLevel>Editor</t:InboxFolderPermissionLevel>
            <t:ContactsFolderPermissionLevel>None</t:ContactsFolderPermissionLevel>
            <t:NotesFolderPermissionLevel>None</t:NotesFolderPermissionLevel>
            <t:JournalFolderPermissionLevel>None</t:JournalFolderPermissionLevel>
          </t:DelegatePermissions>
          <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
          <t:ViewPrivateItems>false</t:ViewPrivateItems>
        </t:DelegateUser>
      </m:DelegateUsers>
      <m:DeliverMeetingRequests>DelegatesAndSendInformationToMe</m:DeliverMeetingRequests>
    </m:AddDelegate>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="15bce-135">El servidor responde a la solicitud de **AddDelegate** con un mensaje de [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que se han creado correctamente los delegados.</span><span class="sxs-lookup"><span data-stu-id="15bce-135">The server responds to the **AddDelegate** request with an [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the delegates were successfully created.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="888"
                         MinorBuildNumber="9"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:AddDelegateResponse ResponseClass="Success"
                           xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:ResponseMessages>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1337771579-694202782-848329751-1535221</t:SID>
              <t:PrimarySmtpAddress>calendardelegate@contoso.com</t:PrimarySmtpAddress>
              <t:DisplayName>calendardelegate</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1337771579-694202782-848329751-1535264</t:SID>
              <t:PrimarySmtpAddress>contactdelegate@contoso.com</t:PrimarySmtpAddress>
              <t:DisplayName>contactdelegate</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
        <m:DelegateUserResponseMessageType ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DelegateUser>
            <t:UserId>
              <t:SID>S-1-5-21-1337771579-694202782-848329751-1535223</t:SID>
              <t:PrimarySmtpAddress>emaildelegate@contoso.com</t:PrimarySmtpAddress>
              <t:DisplayName>emaildelegate</t:DisplayName>
            </t:UserId>
            <t:ReceiveCopiesOfMeetingMessages>false</t:ReceiveCopiesOfMeetingMessages>
            <t:ViewPrivateItems>false</t:ViewPrivateItems>
          </m:DelegateUser>
        </m:DelegateUserResponseMessageType>
      </m:ResponseMessages>
    </m:AddDelegateResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="15bce-136"><a name="bk_removedelegateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="15bce-136"></span></span>

## <a name="remove-delegates-by-using-the-ews-managed-api"></a><span data-ttu-id="15bce-137">Eliminación de delegados mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="15bce-137">Remove delegates by using the EWS Managed API</span></span>

<span data-ttu-id="15bce-138">Puede quitar delegados de un buzón de destino mediante el método de la API administrada de EWS [ExchangeService.RemoveDelegates](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="15bce-138">You can remove delegates from a target mailbox by using the [ExchangeService.RemoveDelegates](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) EWS Managed API method.</span></span> <span data-ttu-id="15bce-139">En este ejemplo, se quitan el conjunto de permisos de delegado en el que se [Agregue un ejemplo de un delegado](#bk_adddelegateewsma) .</span><span class="sxs-lookup"><span data-stu-id="15bce-139">In this example, the delegate permissions set in the [add a delegate example](#bk_adddelegateewsma) are removed.</span></span> 
  
<span data-ttu-id="15bce-140">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el propietario del buzón, y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="15bce-140">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static Collection<DelegateUserResponse> RemoveDelegates(ExchangeService service)
{
    // Create a list to hold the delegates to delete.
    List<UserId> deletedDelegates = new System.Collections.Generic.List<UserId>();
    // Add the delegate to the list of new delegates.
    deletedDelegates.Add("calendardelegate@contoso.com");
    // Add the delegate to the list of new delegates.
    deletedDelegates.Add("contactdelegate@contoso.com");
    // Add the delegate to the list of new delegates.
    deletedDelegates.Add("emaildelegate@contoso.com");
    // Create a mailbox object that represents the mailbox owner.
    Mailbox mailbox = new Mailbox("primary@contoso.com");
    // Call the AddDelegates method to add the delegates to the target mailbox.
    Collection<DelegateUserResponse> response = service.RemoveDelegates(mailbox, deletedDelegates);
    foreach (DelegateUserResponse resp in response)
    {
        // Print out the result and the last eight characters of the item ID.
        Console.WriteLine("Result: {0}", resp.Result);
        Console.WriteLine("Error Code: {0}", resp.ErrorCode);
        Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
    }
    return response;
}
```

<span data-ttu-id="15bce-141"><a name="bk_removedelegateews"> </a></span><span class="sxs-lookup"><span data-stu-id="15bce-141"></span></span>

## <a name="remove-delegates-by-using-ews"></a><span data-ttu-id="15bce-142">Eliminación de delegados mediante EWS</span><span class="sxs-lookup"><span data-stu-id="15bce-142">Remove delegates by using EWS</span></span>

<span data-ttu-id="15bce-143">Puede quitar delegados de un buzón de correo mediante el uso de la operación de EWS [RemoveDelegate](http://msdn.microsoft.com/library/1d42d5ff-8fde-4f8a-b18d-57b1ef7a946a%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="15bce-143">You can remove delegates from a mailbox by using the [RemoveDelegate](http://msdn.microsoft.com/library/1d42d5ff-8fde-4f8a-b18d-57b1ef7a946a%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="15bce-144">En este ejemplo, se quitan el conjunto de permisos de delegado en el que se [Agregue un ejemplo de un delegado](#bk_adddelegateews) .</span><span class="sxs-lookup"><span data-stu-id="15bce-144">In this example, the delegate permissions set in the [add a delegate example](#bk_adddelegateews) are removed.</span></span> 
  
<span data-ttu-id="15bce-145">También es la solicitud XML que la API administrada de EWS envía cuando se utiliza el método **RemoveDelegates** para [quitar a los delegados](#bk_removedelegateewsma).</span><span class="sxs-lookup"><span data-stu-id="15bce-145">This is also the XML request that the EWS Managed API sends when you use the **RemoveDelegates** method to [remove delegates](#bk_removedelegateewsma).</span></span>
  
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
    <m:RemoveDelegate>
      <m:Mailbox>
        <t:EmailAddress>primary@contoso.com</t:EmailAddress>
      </m:Mailbox>
      <m:UserIds>
        <t:UserId>
          <t:PrimarySmtpAddress>calendardelegate@contoso.com</t:PrimarySmtpAddress>
        </t:UserId>
        <t:UserId>
          <t:PrimarySmtpAddress>contactdelegate@contoso.com</t:PrimarySmtpAddress>
        </t:UserId>
        <t:UserId>
          <t:PrimarySmtpAddress>emaildelegate@contoso.com</t:PrimarySmtpAddress>
        </t:UserId>
      </m:UserIds>
    </m:RemoveDelegate>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="15bce-146">El servidor responde a la solicitud de **RemoveDelegate** con un mensaje de [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que los delegados se quitaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="15bce-146">The server responds to the **RemoveDelegate** request with a [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the delegates were successfully removed.</span></span>

<span data-ttu-id="15bce-147"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="15bce-147"></span></span>

## <a name="next-steps"></a><span data-ttu-id="15bce-148">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="15bce-148">Next steps</span></span>

<span data-ttu-id="15bce-149">Después de agregar los delegados a calendario, correo electrónico y carpetas de tareas, el delegado puede tener acceso a los elementos en las carpetas.</span><span class="sxs-lookup"><span data-stu-id="15bce-149">After you add delegates to calendar, email, and task folders, the delegate can access the items in the folders.</span></span> <span data-ttu-id="15bce-150">Para obtener más información, vea los siguientes artículos:</span><span class="sxs-lookup"><span data-stu-id="15bce-150">To learn more, see the following articles:</span></span>
  
- [<span data-ttu-id="15bce-151">Correo electrónico de acceso como delegado mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="15bce-151">Access email as a delegate by using EWS in Exchange</span></span>](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="15bce-152">Obtener acceso a un calendario como delegado mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="15bce-152">Access a calendar as a delegate by using EWS in Exchange</span></span>](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="15bce-153">Contactos de acceso como delegado mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="15bce-153">Access contacts as a delegate by using EWS in Exchange</span></span>](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
<span data-ttu-id="15bce-154">Si las carpetas para la que ha agregado a los delegados incluyen carpetas secundarias que se crearon antes de conceder el acceso de delegado, el delegado no podrá tener acceso a esas carpetas sin permisos adicionales.</span><span class="sxs-lookup"><span data-stu-id="15bce-154">If the folders for which you added delegates include child folders that were created before you granted the delegate access, the delegate will not be able to access those folders without additional permissions.</span></span> <span data-ttu-id="15bce-155">Para agregar estos permisos o modificar los permisos para todas las carpetas, vea [establecer permisos de carpeta de otro usuario mediante el uso de EWS en Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="15bce-155">To add these permissions, or modify permissions for any other folders, see [Set folder permissions for another user by using EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="15bce-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="15bce-156">See also</span></span>

- [<span data-ttu-id="15bce-157">Acceso delegado y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="15bce-157">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
- [<span data-ttu-id="15bce-158">Exchange 2013: Agregar delegar a los usuarios de una cuenta de correo electrónico mediante programación</span><span class="sxs-lookup"><span data-stu-id="15bce-158">Exchange 2013: Add delegate users to an email account programmatically</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Adding-1024511f)   
- [<span data-ttu-id="15bce-159">Exchange 2013: Los delegados de actualización asociados con las cuentas de correo electrónico mediante programación</span><span class="sxs-lookup"><span data-stu-id="15bce-159">Exchange 2013: Update delegates associated with email accounts programmatically</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Update-b40d3bac)   
- [<span data-ttu-id="15bce-160">Exchange 2013: Quitar delegados asociados con cuentas de correo electrónico mediante programación</span><span class="sxs-lookup"><span data-stu-id="15bce-160">Exchange 2013: Remove delegates associated with email accounts programmatically</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Remove-686f7714)
    

