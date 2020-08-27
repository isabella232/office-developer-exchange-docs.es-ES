---
title: Suplantación y EWS en Exchange
manager: sethgros
ms.date: 08/24/2020
ms.audience: Developer
ms.assetid: 7e1ea63c-eb29-43d2-827f-2f2b1846483b
description: Obtenga información acerca de cómo y cuándo usar la suplantación en las aplicaciones de servicio de Exchange.
localization_priority: Priority
ms.openlocfilehash: da35fb04f316c21a1c85c71b789b7f1485653466
ms.sourcegitcommit: 636c05a929279812c6ef87d75b01c166a4a05584
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2020
ms.locfileid: "47254975"
---
# <a name="impersonation-and-ews-in-exchange"></a><span data-ttu-id="bd8fa-103">Suplantación y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="bd8fa-103">Impersonation and EWS in Exchange</span></span>

<span data-ttu-id="bd8fa-104">Obtenga información acerca de cómo y cuándo usar la suplantación en las [aplicaciones de servicio de Exchange](ews-application-types.md).</span><span class="sxs-lookup"><span data-stu-id="bd8fa-104">Learn how and when to use impersonation in your Exchange [service applications](ews-application-types.md).</span></span>
  
<span data-ttu-id="bd8fa-105">Para permitir a los usuarios acceder a los buzones de otros usuarios, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bd8fa-105">You can enable users to access other users' mailboxes in one of three ways:</span></span>
  
- <span data-ttu-id="bd8fa-106">Agregar delegados y especificar permisos para cada uno.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-106">By adding delegates and specifying permissions for each delegate.</span></span>
    
- <span data-ttu-id="bd8fa-107">Modificar los permisos de carpeta directamente.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-107">By modifying folder permissions directly.</span></span>
    
- <span data-ttu-id="bd8fa-108">Utilizar la suplantación.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-108">By using impersonation.</span></span>
    
<span data-ttu-id="bd8fa-109">¿Cuándo debería elegir la suplantación en lugar de la delegación o de modificar los permisos de carpeta?</span><span class="sxs-lookup"><span data-stu-id="bd8fa-109">When should you choose impersonation over delegation or folder permissions?</span></span> <span data-ttu-id="bd8fa-110">Las siguientes instrucciones le ayudarán a decidir:</span><span class="sxs-lookup"><span data-stu-id="bd8fa-110">The following guidelines will help you decide:</span></span>
  
- <span data-ttu-id="bd8fa-111">Utilice los permisos de carpeta cuando quiera proporcionar a un usuario acceso a una carpeta sin que dicho usuario tenga permisos para "Enviar en nombre de".</span><span class="sxs-lookup"><span data-stu-id="bd8fa-111">Use folder permissions when you want to provide a user access to a folder but do not want the user to have "send on behalf of" permissions.</span></span> 
    
- <span data-ttu-id="bd8fa-112">Use el acceso delegado cuando quiera conceder permiso a un usuario para realizar trabajo en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-112">Use delegate access when you want to give one user permission to perform work on behalf of another user.</span></span> <span data-ttu-id="bd8fa-113">Por lo general, se trata de un permiso que se da a uno o a pocos usuarios; por ejemplo, un único asistente administrativo que administra el calendario en nombre de un administrador o un único programador de sala que administra los calendarios de un grupo de salas de reuniones.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-113">Typically, this is a one-to-one or one-to-a-few permission - for example, a single administrative assistant managing the calendar for an administrator, or a single room scheduler managing the calendars for a group of meeting rooms.</span></span>
    
- <span data-ttu-id="bd8fa-114">Emplee la suplantación cuando tenga una aplicación de servicio que necesite tener acceso a varios buzones de correo y "actuar como" el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-114">Use impersonation when you have a service application that needs to access multiple mailboxes and "act as" the mailbox owner.</span></span>
    
<span data-ttu-id="bd8fa-115">La suplantación es la mejor opción cuando se utilizan varios buzones, ya que permite conceder fácilmente acceso de cuenta de servicio a cada buzón de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-115">Impersonation is the best choice when you're dealing with multiple mailboxes because you can easily grant one service account access to every mailbox in a database.</span></span> <span data-ttu-id="bd8fa-116">Los permisos de carpeta y delegación son óptimos cuando solo concede acceso a unos pocos usuarios, porque tiene que agregar permisos de forma individual para cada buzón.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-116">Delegation and folder permissions are best when you're only granting access to a few users, because you have to add permissions individually to each mailbox.</span></span> <span data-ttu-id="bd8fa-117">En la figura 1 se muestran algunas de las diferencias entre cada tipo de acceso.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-117">Figure 1 shows some of the differences between each type of access.</span></span>
  
<span data-ttu-id="bd8fa-118">**Ilustración 1. Formas de acceder a los buzones de otros usuarios**</span><span class="sxs-lookup"><span data-stu-id="bd8fa-118">**Figure 1. Ways to access other users' mailboxes**</span></span>

![Un diagrama que muestra los tipos de acceso a los buzones, la relación entre los propietarios de los buzones y el delegado de cada tipo, y el tipo de permiso. Enviar en nombre de los permisos para delegación y/o permisos de carpeta. Enviar como permisos para suplantación.](media/Ex15_Delegate_Overview.png)
  
<span data-ttu-id="bd8fa-122">La suplantación es ideal para aplicaciones que se conectan a Exchange Online, Exchange Online como parte de Office 365 y a las versiones locales de Exchange y que realizan operaciones como archivar correo electrónico, establecer automáticamente acciones de fuera de la oficina para los usuarios de vacaciones, o realizar cualquier otra tarea que requiera que la aplicación actúe como propietario de un buzón.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-122">Impersonation is ideal for applications that connect to Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange and perform operations, such as archiving email, setting OOF automatically for users on vacation, or any other task that requires that the application act as the owner of a mailbox.</span></span> <span data-ttu-id="bd8fa-123">Cuando una aplicación usa la suplantación para enviar un mensaje, el correo electrónico aparece como si se hubiera enviado desde el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-123">When an application uses impersonation to send a message, the email appears to be sent from the mailbox owner.</span></span> <span data-ttu-id="bd8fa-124">Al destinatario le resulta imposible saber que el correo lo envió la cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-124">There is no way for the recipient to know the mail was sent by the service account.</span></span> <span data-ttu-id="bd8fa-125">Por otra parte, la delegación concede a otra cuenta de buzón permiso para actuar en nombre del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-125">Delegation, on the other hand, gives another mailbox account permission to act on behalf of a mailbox owner.</span></span> <span data-ttu-id="bd8fa-126">Cuando un delegado envía un mensaje de correo electrónico, el valor "de" identifica al propietario del buzón y el valor "remitente" identifica al delegado que envió el correo.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-126">When an email message is sent by a delegate, the "from" value identifies the mailbox owner, and the "sender" value identifies the delegate that sent the mail.</span></span> 
  
## <a name="security-considerations-for-impersonation"></a><span data-ttu-id="bd8fa-127">Consideraciones de seguridad para la suplantación</span><span class="sxs-lookup"><span data-stu-id="bd8fa-127">Security considerations for impersonation</span></span>

<span data-ttu-id="bd8fa-128">La suplantación permite a un autor de llamada suplantar una cuenta de usuario determinada.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-128">Impersonation enables a caller to impersonate a given user account.</span></span> <span data-ttu-id="bd8fa-129">Esto permite al autor de llamada realizar operaciones mediante los permisos asociados a la cuenta suplantada, en lugar de los permisos asociados con la cuenta del autor de llamada.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-129">This enables the caller to perform operations by using the permissions that are associated with the impersonated account, instead of the permissions that are associated with the caller's account.</span></span> <span data-ttu-id="bd8fa-130">Por este motivo, debe tener en cuenta las siguientes consideraciones de seguridad:</span><span class="sxs-lookup"><span data-stu-id="bd8fa-130">For this reason, you should be aware of the following security considerations:</span></span>
  
- <span data-ttu-id="bd8fa-131">Solo las cuentas a las que un administrador de Exchange Server ha concedido el rol **ApplicationImpersonation** pueden usar la suplantación.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-131">Only accounts that have been granted the **ApplicationImpersonation** role by an Exchange server administrator can use impersonation.</span></span> 
    
- <span data-ttu-id="bd8fa-132">Debe crear un ámbito de administración que limite la suplantación a un grupo específico de cuentas.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-132">You should create a management scope that limits impersonation to a specified group of accounts.</span></span> <span data-ttu-id="bd8fa-133">Si no crea un ámbito de administración, el rol **ApplicationImpersonation** se concederá a todas las cuentas de la organización.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-133">If you do not create a management scope, the **ApplicationImpersonation** role is granted to all accounts in an organization.</span></span> 
    
- <span data-ttu-id="bd8fa-134">Por lo general, el rol **ApplicationImpersonation** se otorga a una cuenta de servicio dedicada a una aplicación o a un grupo de aplicaciones en particular, en lugar de a una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-134">Typically, the **ApplicationImpersonation** role is granted to a service account dedicated to a particular application or group of applications, rather than a user account.</span></span> <span data-ttu-id="bd8fa-135">Puede crear todas las cuentas de servicio que necesite.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-135">You can create as many or as few service accounts as you need.</span></span> 
    
<span data-ttu-id="bd8fa-136">Puede obtener más información acerca de la [configuración de la suplantación](how-to-configure-impersonation.md), pero debe trabajar con su administrador de Exchange para asegurarse de que las cuentas de servicio que necesita se creen con los [permisos y el acceso](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx) que cumplan los requisitos de seguridad de su organización.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-136">You can read more about [configuring impersonation](how-to-configure-impersonation.md), but you should work with your Exchange administrator to ensure that the service accounts that you need are created with the [permissions and access](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx) that meet the security requirements of your organization.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="bd8fa-137">En esta sección</span><span class="sxs-lookup"><span data-stu-id="bd8fa-137">In this section</span></span>

- [<span data-ttu-id="bd8fa-138">Configurar la suplantación</span><span class="sxs-lookup"><span data-stu-id="bd8fa-138">Configure impersonation</span></span>](how-to-configure-impersonation.md)
    
- [<span data-ttu-id="bd8fa-139">Identificar la cuenta a suplantar</span><span class="sxs-lookup"><span data-stu-id="bd8fa-139">Identify the account to impersonate</span></span>](how-to-identify-the-account-to-impersonate.md)
    
- [<span data-ttu-id="bd8fa-140">Agregar citas mediante la suplantación de Exchange</span><span class="sxs-lookup"><span data-stu-id="bd8fa-140">Add appointments by using Exchange impersonation</span></span>](how-to-add-appointments-by-using-exchange-impersonation.md)

## <a name="performance-considerations-for-ews-impersonation"></a><span data-ttu-id="bd8fa-141">Consideraciones de rendimiento para la suplantación de EWS</span><span class="sxs-lookup"><span data-stu-id="bd8fa-141">Performance considerations for EWS impersonation</span></span>

<span data-ttu-id="bd8fa-142">Cuando se usa la suplantación de EWS, X-AnchorMailbox siempre debe establecerse correctamente.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-142">When EWS Impersonation is used, the X-AnchorMailbox should always be correctly set.</span></span>  <span data-ttu-id="bd8fa-143">De lo contrario, es posible que reciba los mensajes de error 500 o 503 en ocasiones.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-143">Otherwise, you may get error messages 500 or 503 at times.</span></span> <span data-ttu-id="bd8fa-144">Resulta fundamental para el rendimiento y las notificaciones de Exchange Online y Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-144">It is critical for performance and also for notifications with Exchange Online/Exchange 2013.</span></span>  <span data-ttu-id="bd8fa-145">Si no lo establece, puede que se tarde el doble o más en completar la llamada.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-145">Not setting it can double or more the time it takes to complete the call.</span></span> <span data-ttu-id="bd8fa-146">En algunos casos, puede recibir también tiempos de espera.</span><span class="sxs-lookup"><span data-stu-id="bd8fa-146">In some cases, you can also get timeouts.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="bd8fa-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd8fa-147">See also</span></span>


- [<span data-ttu-id="bd8fa-148">Desarrollo de clientes de servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="bd8fa-148">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="bd8fa-149">Acceso delegado y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="bd8fa-149">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
    
- [<span data-ttu-id="bd8fa-150">Permisos de Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="bd8fa-150">Exchange 2013 Permissions</span></span>](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx)
    

