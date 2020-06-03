---
title: Suplantación y EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: 7e1ea63c-eb29-43d2-827f-2f2b1846483b
description: Obtenga información sobre cómo y Cuándo usar la suplantación en las aplicaciones de servicio de Exchange.
localization_priority: Priority
ms.openlocfilehash: 8151b3d83421786d99ee0c82eaf4f7a5c0721f25
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466615"
---
# <a name="impersonation-and-ews-in-exchange"></a><span data-ttu-id="2ff0a-103">Suplantación y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2ff0a-103">Impersonation and EWS in Exchange</span></span>

<span data-ttu-id="2ff0a-104">Obtenga información sobre cómo y Cuándo usar la suplantación en [las aplicaciones de servicio](ews-application-types.md)de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-104">Learn how and when to use impersonation in your Exchange [service applications](ews-application-types.md).</span></span>
  
<span data-ttu-id="2ff0a-105">Puede habilitar a los usuarios para que tengan acceso a los buzones de otros usuarios de una de estas tres maneras:</span><span class="sxs-lookup"><span data-stu-id="2ff0a-105">You can enable users to access other users' mailboxes in one of three ways:</span></span>
  
- <span data-ttu-id="2ff0a-106">Mediante la adición de delegados y la especificación de permisos para cada delegado.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-106">By adding delegates and specifying permissions for each delegate.</span></span>
    
- <span data-ttu-id="2ff0a-107">Modificando los permisos de carpeta directamente.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-107">By modifying folder permissions directly.</span></span>
    
- <span data-ttu-id="2ff0a-108">Mediante la suplantación.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-108">By using impersonation.</span></span>
    
<span data-ttu-id="2ff0a-109">¿Cuándo debe elegir la suplantación a través de la delegación o los permisos de carpeta?</span><span class="sxs-lookup"><span data-stu-id="2ff0a-109">When should you choose impersonation over delegation or folder permissions?</span></span> <span data-ttu-id="2ff0a-110">Las siguientes instrucciones le ayudarán a decidir:</span><span class="sxs-lookup"><span data-stu-id="2ff0a-110">The following guidelines will help you decide:</span></span>
  
- <span data-ttu-id="2ff0a-111">Use permisos de carpeta cuando desee proporcionar a un usuario acceso a una carpeta pero no desea que el usuario tenga permisos "enviar en nombre de".</span><span class="sxs-lookup"><span data-stu-id="2ff0a-111">Use folder permissions when you want to provide a user access to a folder but do not want the user to have "send on behalf of" permissions.</span></span> 
    
- <span data-ttu-id="2ff0a-112">Use el acceso delegado cuando desee conceder a un usuario permiso para realizar el trabajo en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-112">Use delegate access when you want to give one user permission to perform work on behalf of another user.</span></span> <span data-ttu-id="2ff0a-113">Normalmente se trata de un permiso de uno a uno o de uno a uno reducido, por ejemplo, un único asistente administrativo que administra el calendario de un administrador o un único programador de salas que administra los calendarios de un grupo de salas de reuniones.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-113">Typically, this is a one-to-one or one-to-a-few permission - for example, a single administrative assistant managing the calendar for an administrator, or a single room scheduler managing the calendars for a group of meeting rooms.</span></span>
    
- <span data-ttu-id="2ff0a-114">Use la suplantación cuando tiene una aplicación de servicio que necesita tener acceso a varios buzones de correo y "actuar como" el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-114">Use impersonation when you have a service application that needs to access multiple mailboxes and "act as" the mailbox owner.</span></span>
    
<span data-ttu-id="2ff0a-115">La suplantación es la mejor opción cuando se trabaja con varios buzones, ya que se puede conceder fácilmente un acceso de cuenta de servicio a todos los buzones de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-115">Impersonation is the best choice when you're dealing with multiple mailboxes because you can easily grant one service account access to every mailbox in a database.</span></span> <span data-ttu-id="2ff0a-116">La delegación y los permisos de carpeta son los mejores cuando solo concede acceso a algunos usuarios, porque tiene que agregar permisos individualmente a cada buzón.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-116">Delegation and folder permissions are best when you're only granting access to a few users, because you have to add permissions individually to each mailbox.</span></span> <span data-ttu-id="2ff0a-117">La figura 1 muestra algunas de las diferencias entre cada tipo de acceso.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-117">Figure 1 shows some of the differences between each type of access.</span></span>
  
<span data-ttu-id="2ff0a-118">**Figura 1. Formas de tener acceso a los buzones de otros usuarios**</span><span class="sxs-lookup"><span data-stu-id="2ff0a-118">**Figure 1. Ways to access other users' mailboxes**</span></span>

![Un diagrama que muestra los tipos de acceso a los buzones, la relación entre los propietarios de los buzones y el delegado de cada tipo, y el tipo de permiso. Enviar en nombre de los permisos para delegación y/o permisos de carpeta. Enviar como permisos para suplantación.](media/Ex15_Delegate_Overview.png)
  
<span data-ttu-id="2ff0a-122">La suplantación es ideal para las aplicaciones que se conectan a Exchange Online, Exchange online como parte de Office 365 y las versiones locales de Exchange, y realizan operaciones, como el archivado de correo electrónico, la configuración automática del OOF para los usuarios de vacaciones o cualquier otra tarea que requiera que la aplicación actúe como propietario de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-122">Impersonation is ideal for applications that connect to Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange and perform operations, such as archiving email, setting OOF automatically for users on vacation, or any other task that requires that the application act as the owner of a mailbox.</span></span> <span data-ttu-id="2ff0a-123">Cuando una aplicación utiliza la suplantación para enviar un mensaje, parece que el correo electrónico se envía desde el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-123">When an application uses impersonation to send a message, the email appears to be sent from the mailbox owner.</span></span> <span data-ttu-id="2ff0a-124">No hay forma de que el destinatario sepa que el correo se envió mediante la cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-124">There is no way for the recipient to know the mail was sent by the service account.</span></span> <span data-ttu-id="2ff0a-125">Por otra parte, la delegación da a otro permiso de cuenta de buzón de correo que actúe en nombre de un propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-125">Delegation, on the other hand, gives another mailbox account permission to act on behalf of a mailbox owner.</span></span> <span data-ttu-id="2ff0a-126">Cuando un delegado envía un mensaje de correo electrónico, el valor "de" identifica al propietario del buzón y el valor "Sender" identifica al delegado que envió el correo.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-126">When an email message is sent by a delegate, the "from" value identifies the mailbox owner, and the "sender" value identifies the delegate that sent the mail.</span></span> 
  
## <a name="security-considerations-for-impersonation"></a><span data-ttu-id="2ff0a-127">Consideraciones de seguridad para la suplantación</span><span class="sxs-lookup"><span data-stu-id="2ff0a-127">Security considerations for impersonation</span></span>

<span data-ttu-id="2ff0a-128">La suplantación permite al autor de la llamada suplantar a una cuenta de usuario determinada.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-128">Impersonation enables a caller to impersonate a given user account.</span></span> <span data-ttu-id="2ff0a-129">Esto permite al autor de la llamada realizar operaciones con los permisos asociados con la cuenta suplantada, en lugar de los permisos asociados con la cuenta del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-129">This enables the caller to perform operations by using the permissions that are associated with the impersonated account, instead of the permissions that are associated with the caller's account.</span></span> <span data-ttu-id="2ff0a-130">Por este motivo, debe tener en cuenta las siguientes consideraciones de seguridad:</span><span class="sxs-lookup"><span data-stu-id="2ff0a-130">For this reason, you should be aware of the following security considerations:</span></span>
  
- <span data-ttu-id="2ff0a-131">Solo las cuentas a las que un administrador de Exchange Server ha concedido el rol **ApplicationImpersonation** puede usar la suplantación.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-131">Only accounts that have been granted the **ApplicationImpersonation** role by an Exchange server administrator can use impersonation.</span></span> 
    
- <span data-ttu-id="2ff0a-132">Debe crear un ámbito de administración que limite la suplantación a un grupo de cuentas especificado.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-132">You should create a management scope that limits impersonation to a specified group of accounts.</span></span> <span data-ttu-id="2ff0a-133">Si no crea un ámbito de administración, el rol **ApplicationImpersonation** se concede a todas las cuentas de una organización.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-133">If you do not create a management scope, the **ApplicationImpersonation** role is granted to all accounts in an organization.</span></span> 
    
- <span data-ttu-id="2ff0a-134">Normalmente, el rol **ApplicationImpersonation** se concede a una cuenta de servicio dedicada a una aplicación o grupo de aplicaciones en particular, en lugar de una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-134">Typically, the **ApplicationImpersonation** role is granted to a service account dedicated to a particular application or group of applications, rather than a user account.</span></span> <span data-ttu-id="2ff0a-135">Puede crear tantas o tan pocas cuentas de servicio como necesite.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-135">You can create as many or as few service accounts as you need.</span></span> 
    
<span data-ttu-id="2ff0a-136">Puede obtener más información acerca de la configuración de la [suplantación](how-to-configure-impersonation.md), pero debe colaborar con el administrador de Exchange para asegurarse de que las cuentas de servicio que necesita se crean con los [permisos y el acceso](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx) que cumplen los requisitos de seguridad de su organización.</span><span class="sxs-lookup"><span data-stu-id="2ff0a-136">You can read more about [configuring impersonation](how-to-configure-impersonation.md), but you should work with your Exchange administrator to ensure that the service accounts that you need are created with the [permissions and access](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx) that meet the security requirements of your organization.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="2ff0a-137">En esta sección</span><span class="sxs-lookup"><span data-stu-id="2ff0a-137">In this section</span></span>

- [<span data-ttu-id="2ff0a-138">Configurar la suplantación</span><span class="sxs-lookup"><span data-stu-id="2ff0a-138">Configure impersonation</span></span>](how-to-configure-impersonation.md)
    
- [<span data-ttu-id="2ff0a-139">Identificación de la cuenta que se va a suplantar</span><span class="sxs-lookup"><span data-stu-id="2ff0a-139">Identify the account to impersonate</span></span>](how-to-identify-the-account-to-impersonate.md)
    
- [<span data-ttu-id="2ff0a-140">Adición de citas mediante la suplantación de Exchange</span><span class="sxs-lookup"><span data-stu-id="2ff0a-140">Add appointments by using Exchange impersonation</span></span>](how-to-add-appointments-by-using-exchange-impersonation.md)
    
## <a name="see-also"></a><span data-ttu-id="2ff0a-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ff0a-141">See also</span></span>


- [<span data-ttu-id="2ff0a-142">Desarrollar clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="2ff0a-142">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="2ff0a-143">Acceso delegado y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2ff0a-143">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
    
- [<span data-ttu-id="2ff0a-144">Permisos de Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="2ff0a-144">Exchange 2013 Permissions</span></span>](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx)
    

