---
title: Suplantación y EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7e1ea63c-eb29-43d2-827f-2f2b1846483b
description: Obtenga información sobre cómo y cuándo utilizar la representación en las aplicaciones de servicio de Exchange.
ms.openlocfilehash: f8a215874475034f0d147b80a05cae414e6438f9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763189"
---
# <a name="impersonation-and-ews-in-exchange"></a><span data-ttu-id="d0331-103">Suplantación y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d0331-103">Impersonation and EWS in Exchange</span></span>

<span data-ttu-id="d0331-104">Obtenga información sobre cómo y cuándo utilizar la representación en las [aplicaciones de servicio](ews-application-types.md)de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d0331-104">Learn how and when to use impersonation in your Exchange [service applications](ews-application-types.md).</span></span>
  
<span data-ttu-id="d0331-105">Puede habilitar a los usuarios tener acceso a los buzones de otros usuarios en uno de tres maneras:</span><span class="sxs-lookup"><span data-stu-id="d0331-105">You can enable users to access other users' mailboxes in one of three ways:</span></span>
  
- <span data-ttu-id="d0331-106">Adición de delegados y especificando los permisos para cada delegado.</span><span class="sxs-lookup"><span data-stu-id="d0331-106">By adding delegates and specifying permissions for each delegate.</span></span>
    
- <span data-ttu-id="d0331-107">Mediante la modificación de permisos de carpeta directamente.</span><span class="sxs-lookup"><span data-stu-id="d0331-107">By modifying folder permissions directly.</span></span>
    
- <span data-ttu-id="d0331-108">Mediante el uso de suplantación.</span><span class="sxs-lookup"><span data-stu-id="d0331-108">By using impersonation.</span></span>
    
<span data-ttu-id="d0331-109">¿Cuándo debería elegir suplantación a través de los permisos de delegación o carpeta?</span><span class="sxs-lookup"><span data-stu-id="d0331-109">When should you choose impersonation over delegation or folder permissions?</span></span> <span data-ttu-id="d0331-110">Las siguientes instrucciones le ayudará a decidir:</span><span class="sxs-lookup"><span data-stu-id="d0331-110">The following guidelines will help you decide:</span></span>
  
- <span data-ttu-id="d0331-111">Use los permisos de carpeta cuando desee proporcionar un acceso de usuario a una carpeta, pero no desea que el usuario tenga permisos "enviar en nombre de".</span><span class="sxs-lookup"><span data-stu-id="d0331-111">Use folder permissions when you want to provide a user access to a folder but do not want the user to have "send on behalf of" permissions.</span></span> 
    
- <span data-ttu-id="d0331-112">Usar acceso de delegado al que desea conceder permiso a un usuario para llevar a cabo el trabajo en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="d0331-112">Use delegate access when you want to give one user permission to perform work on behalf of another user.</span></span> <span data-ttu-id="d0331-113">Normalmente, se trata de un permiso de uno a uno o uno a algunos - por ejemplo, un auxiliar administrativo único administrar el calendario de un administrador o un programador de habitación individual administrar los calendarios para un grupo de las salas de reuniones.</span><span class="sxs-lookup"><span data-stu-id="d0331-113">Typically, this is a one-to-one or one-to-a-few permission - for example, a single administrative assistant managing the calendar for an administrator, or a single room scheduler managing the calendars for a group of meeting rooms.</span></span>
    
- <span data-ttu-id="d0331-114">Usar suplantación cuando tiene una aplicación de servicio que necesita tener acceso a varios buzones de correo y "actuar como" propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="d0331-114">Use impersonation when you have a service application that needs to access multiple mailboxes and "act as" the mailbox owner.</span></span>
    
<span data-ttu-id="d0331-115">Suplantación de es la mejor opción cuando se trata con varios buzones porque fácilmente puede otorgar un acceso de cuenta de servicio para cada buzón de correo en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="d0331-115">Impersonation is the best choice when you're dealing with multiple mailboxes because you can easily grant one service account access to every mailbox in a database.</span></span> <span data-ttu-id="d0331-116">Permisos de delegación y carpeta están mejor cuando solo va a conceder acceso a unos pocos usuarios, debido a que se debe agregar permisos individualmente a cada buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d0331-116">Delegation and folder permissions are best when you're only granting access to a few users, because you have to add permissions individually to each mailbox.</span></span> <span data-ttu-id="d0331-117">La figura 1 muestra algunas de las diferencias entre cada tipo de acceso.</span><span class="sxs-lookup"><span data-stu-id="d0331-117">Figure 1 shows some of the differences between each type of access.</span></span>
  
<span data-ttu-id="d0331-118">**En la figura 1. Formas de acceso a los buzones de otros usuarios**</span><span class="sxs-lookup"><span data-stu-id="d0331-118">**Figure 1. Ways to access other users' mailboxes**</span></span>

![Un diagrama que muestra los tipos de acceso a los buzones, la relación entre los propietarios de los buzones y el delegado de cada tipo, y el tipo de permiso. Enviar en nombre de los permisos para delegación y/o permisos de carpeta. Enviar como permisos para suplantación.](media/Ex15_Delegate_Overview.png)
  
<span data-ttu-id="d0331-122">Suplantación es ideal para aplicaciones que se conectan a Exchange Online, Exchange Online como parte de Office 365, y las versiones de Exchange local y realiza operaciones, como el archivado de correo electrónico, configuración OOF automáticamente para los usuarios de vacaciones o cualquier otra tarea que requiere que la aplicación que actúe como el propietario de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d0331-122">Impersonation is ideal for applications that connect to Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange and perform operations, such as archiving email, setting OOF automatically for users on vacation, or any other task that requires that the application act as the owner of a mailbox.</span></span> <span data-ttu-id="d0331-123">Cuando una aplicación utiliza la suplantación para enviar un mensaje, aparece el correo electrónico que se envíen desde el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="d0331-123">When an application uses impersonation to send a message, the email appears to be sent from the mailbox owner.</span></span> <span data-ttu-id="d0331-124">No hay ninguna forma para el destinatario que debe conocer que el correo se ha enviado por la cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="d0331-124">There is no way for the recipient to know the mail was sent by the service account.</span></span> <span data-ttu-id="d0331-125">La delegación, por otro lado, da a otro permiso de cuenta de buzón de correo para que actúe en nombre de un propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="d0331-125">Delegation, on the other hand, gives another mailbox account permission to act on behalf of a mailbox owner.</span></span> <span data-ttu-id="d0331-126">Cuando se envía un mensaje de correo electrónico por parte de un delegado, el valor "desde" identifica el propietario del buzón y el valor de "sender" identifica al delegado que envía el correo.</span><span class="sxs-lookup"><span data-stu-id="d0331-126">When an email message is sent by a delegate, the "from" value identifies the mailbox owner, and the "sender" value identifies the delegate that sent the mail.</span></span> 
  
## <a name="security-considerations-for-impersonation"></a><span data-ttu-id="d0331-127">Consideraciones de seguridad para la suplantación</span><span class="sxs-lookup"><span data-stu-id="d0331-127">Security considerations for impersonation</span></span>

<span data-ttu-id="d0331-128">Suplantación permite a un autor de la llamada suplantar una cuenta de usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="d0331-128">Impersonation enables a caller to impersonate a given user account.</span></span> <span data-ttu-id="d0331-129">Esto permite que el autor de la llamada realizar operaciones con los permisos que están asociados con la cuenta suplantada, en lugar de los permisos que están asociados con la cuenta del llamador.</span><span class="sxs-lookup"><span data-stu-id="d0331-129">This enables the caller to perform operations by using the permissions that are associated with the impersonated account, instead of the permissions that are associated with the caller's account.</span></span> <span data-ttu-id="d0331-130">Por este motivo, debe tener en cuenta las siguientes consideraciones de seguridad:</span><span class="sxs-lookup"><span data-stu-id="d0331-130">For this reason, you should be aware of the following security considerations:</span></span>
  
- <span data-ttu-id="d0331-131">Sólo las cuentas que se han concedido la función **ApplicationImpersonation** por un administrador de Exchange server pueden utilizar suplantación.</span><span class="sxs-lookup"><span data-stu-id="d0331-131">Only accounts that have been granted the **ApplicationImpersonation** role by an Exchange server administrator can use impersonation.</span></span> 
    
- <span data-ttu-id="d0331-132">Debe crear un ámbito de administración que limita la suplantación de un grupo de cuentas especificado.</span><span class="sxs-lookup"><span data-stu-id="d0331-132">You should create a management scope that limits impersonation to a specified group of accounts.</span></span> <span data-ttu-id="d0331-133">Si no se crea un ámbito de administración, se concede a la función **ApplicationImpersonation** a todas las cuentas de una organización.</span><span class="sxs-lookup"><span data-stu-id="d0331-133">If you do not create a management scope, the **ApplicationImpersonation** role is granted to all accounts in an organization.</span></span> 
    
- <span data-ttu-id="d0331-134">Normalmente, la función **ApplicationImpersonation** se concede a una cuenta de servicio dedicada a una aplicación en particular o el grupo de aplicaciones, en lugar de una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="d0331-134">Typically, the **ApplicationImpersonation** role is granted to a service account dedicated to a particular application or group of applications, rather than a user account.</span></span> <span data-ttu-id="d0331-135">Puede crear tantas o tan solo cuentas de servicio que necesite.</span><span class="sxs-lookup"><span data-stu-id="d0331-135">You can create as many or as few service accounts as you need.</span></span> 
    
<span data-ttu-id="d0331-136">Puede leer más información acerca de la [configuración de suplantación](how-to-configure-impersonation.md), pero se debe trabajar con el Administrador de Exchange para asegurarse de que las cuentas de servicio que necesita se crean con el [acceso y los permisos](http://technet.microsoft.com/en-us/library/dd351175%28v=exchg.150%29.aspx) que cumplen los requisitos de seguridad de su organización.</span><span class="sxs-lookup"><span data-stu-id="d0331-136">You can read more about [configuring impersonation](how-to-configure-impersonation.md), but you should work with your Exchange administrator to ensure that the service accounts that you need are created with the [permissions and access](http://technet.microsoft.com/en-us/library/dd351175%28v=exchg.150%29.aspx) that meet the security requirements of your organization.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="d0331-137">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d0331-137">In this section</span></span>

- [<span data-ttu-id="d0331-138">Configurar la suplantación</span><span class="sxs-lookup"><span data-stu-id="d0331-138">Configure impersonation</span></span>](how-to-configure-impersonation.md)
    
- [<span data-ttu-id="d0331-139">Identificación de la cuenta para suplantar a</span><span class="sxs-lookup"><span data-stu-id="d0331-139">Identify the account to impersonate</span></span>](how-to-identify-the-account-to-impersonate.md)
    
- [<span data-ttu-id="d0331-140">Agregar citas mediante el uso de la suplantación de Exchange</span><span class="sxs-lookup"><span data-stu-id="d0331-140">Add appointments by using Exchange impersonation</span></span>](how-to-add-appointments-by-using-exchange-impersonation.md)
    
## <a name="see-also"></a><span data-ttu-id="d0331-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="d0331-141">See also</span></span>


- [<span data-ttu-id="d0331-142">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="d0331-142">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="d0331-143">Acceso delegado y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d0331-143">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
    
- [<span data-ttu-id="d0331-144">Permisos de Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="d0331-144">Exchange 2013 Permissions</span></span>](http://technet.microsoft.com/en-us/library/dd351175%28v=exchg.150%29.aspx)
    

