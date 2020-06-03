---
title: Controlar el acceso de la aplicación cliente a EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 60ac3f7b-ba8a-4c93-99f7-c27002caff93
description: Obtenga información sobre las opciones para administrar el acceso de aplicaciones cliente a EWS.
localization_priority: Priority
ms.openlocfilehash: b887b8167e3d38946b1d6caffe12655ded89569f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528464"
---
# <a name="controlling-client-application-access-to-ews-in-exchange"></a><span data-ttu-id="bc3d0-103">Controlar el acceso de la aplicación cliente a EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="bc3d0-103">Controlling client application access to EWS in Exchange</span></span>

<span data-ttu-id="bc3d0-104">Obtenga información sobre las opciones para administrar el acceso de aplicaciones cliente a EWS.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-104">Learn about the options for managing client application access to EWS.</span></span>
  
<span data-ttu-id="bc3d0-105">Todas las aplicaciones de cliente de EWS que cree deben tener acceso a Exchange Online, Exchange online como parte de Office 365 o a la versión de Exchange que comienza con Exchange 2013 antes de que pueda llamar a operaciones de EWS.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-105">Any EWS client application that you create must be granted access to Exchange Online, Exchange Online as part of Office 365, or version of Exchange starting with Exchange 2013 before it can call EWS operations.</span></span> <span data-ttu-id="bc3d0-106">Los administradores de servidores de prueba o de producción pueden usar el shell de administración de Exchange para limitar el acceso a EWS para todos los usuarios y aplicaciones, para los usuarios individuales o para las aplicaciones individuales.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-106">Test or production server administrators can use the Exchange Management Shell to limit access to EWS either for all users and applications, for individual users, or for individual applications.</span></span> <span data-ttu-id="bc3d0-107">El control de acceso para EWS se basa en las cuentas de dominio.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-107">Access control for EWS is based on domain accounts.</span></span> <span data-ttu-id="bc3d0-108">Cuando se realiza una conexión con credenciales que se autentican mediante la autoridad de seguridad local, el servidor devuelve un error que indica que solo se pueden conectar cuentas de dominio.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-108">When a connection is made with credentials that are authenticated by the local security authority, the server returns an error that indicates that only domain accounts can connect.</span></span> 
  
## <a name="access-control-for-ews-clients-and-users"></a><span data-ttu-id="bc3d0-109">Control de acceso para clientes y usuarios de EWS</span><span class="sxs-lookup"><span data-stu-id="bc3d0-109">Access control for EWS clients and users</span></span>
<span data-ttu-id="bc3d0-110"><a name="bk_configure"> </a></span><span class="sxs-lookup"><span data-stu-id="bc3d0-110"><a name="bk_configure"> </a></span></span>

<span data-ttu-id="bc3d0-111">El administrador del servidor de prueba o de producción puede configurar el control de acceso para clientes que se conectan a EWS de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="bc3d0-111">Your test or production server administrator can configure access control for clients that connect to EWS in the following ways:</span></span> 
  
- <span data-ttu-id="bc3d0-112">Al impedir que se conecten todas las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-112">By blocking all client applications from connecting.</span></span>
    
- <span data-ttu-id="bc3d0-113">Al permitir que las aplicaciones cliente específicas solo se conecten.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-113">By allowing specific client applications only to connect.</span></span>
    
- <span data-ttu-id="bc3d0-114">Al permitir que cualquier aplicación cliente se conecte excepto la que esté bloqueada específicamente.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-114">By allowing any client application to connect except those that are specifically blocked.</span></span>
    
- <span data-ttu-id="bc3d0-115">Al permitir que cualquier aplicación cliente se conecte.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-115">By allowing any client application to connect.</span></span>
    
<span data-ttu-id="bc3d0-116">Las aplicaciones se identifican por la cadena de agente de usuario que envían en la solicitud Web HTTP.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-116">Applications are identified by the user agent string that they send in the HTTP web request.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="bc3d0-117">El bloqueo en el nivel de aplicación no es una característica de seguridad.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-117">Application-level blocking is not a security feature.</span></span> <span data-ttu-id="bc3d0-118">La cadena de agente de usuario se falsifica fácilmente.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-118">The user agent string is easily spoofed.</span></span> <span data-ttu-id="bc3d0-119">Si se permite el acceso de una aplicación a EWS, la aplicación debe seguir presentando credenciales que el servidor autentica antes de que la aplicación pueda conectarse a EWS.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-119">If an application is allowed access to EWS, the application must still present credentials that the server authenticates before the application can connect to EWS.</span></span> 
  
<span data-ttu-id="bc3d0-120">Los administradores también pueden configurar el control de acceso para los propietarios de buzones que se conectan a EWS de las maneras siguientes:</span><span class="sxs-lookup"><span data-stu-id="bc3d0-120">Administrators can also configure access control for mailbox owners that connect to EWS in the following ways:</span></span> 
  
- <span data-ttu-id="bc3d0-121">Al bloquear o permitir a toda la organización.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-121">By blocking or allowing an entire organization.</span></span>
    
- <span data-ttu-id="bc3d0-122">Al bloquear o permitir a un grupo de usuarios identificado por un ámbito de autenticación basado en roles que incluya o excluya los propietarios de buzones que no tienen acceso a EWS.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-122">By blocking or allowing a group of users identified by a role-based authentication scope that includes or excludes mailbox owners that do not have access to EWS.</span></span>
    
- <span data-ttu-id="bc3d0-123">Bloqueando o permitiendo el propietario de un buzón de correo individual.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-123">By blocking or allowing an individual mailbox owner.</span></span>
    
<span data-ttu-id="bc3d0-124">La configuración de control de acceso específica invalida la configuración de control de acceso general.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-124">Specific access control settings override general access control settings.</span></span> <span data-ttu-id="bc3d0-125">Por ejemplo, si una organización deniega el acceso a EWS, pero el propietario de un buzón individual permite el acceso a la aplicación, prevalecerá la configuración individual y se permitirá el acceso.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-125">For example, if an organization denies EWS access but an individual mailbox owner is allowed application access, the individual setting prevails and access is allowed.</span></span> 
  
## <a name="delegation-and-ews-access-management"></a><span data-ttu-id="bc3d0-126">Delegación y administración del acceso a EWS</span><span class="sxs-lookup"><span data-stu-id="bc3d0-126">Delegation and EWS access management</span></span>
<span data-ttu-id="bc3d0-127"><a name="bk_delegation"> </a></span><span class="sxs-lookup"><span data-stu-id="bc3d0-127"><a name="bk_delegation"> </a></span></span>

<span data-ttu-id="bc3d0-128">Cuando los usuarios delegados que no tienen acceso a EWS usan la aplicación cliente, no podrán acceder al buzón de correo del usuario principal mediante EWS, incluso si el usuario principal tiene acceso a EWS.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-128">When delegate users who do not have access to EWS use your client application, they will not be able to access the principal user's mailbox by using EWS, even if the principal user has EWS access.</span></span> <span data-ttu-id="bc3d0-129">Si el usuario delegado tiene acceso a EWS, el delegado podrá usar la aplicación cliente de EWS para tener acceso al buzón de correo del usuario principal incluso si el usuario principal no tiene acceso a EWS.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-129">If the delegate user has EWS access, the delegate will be able to use your EWS client application to access the principal user's mailbox even if the principal user does not have EWS access.</span></span> 
  
## <a name="impersonation-and-ews-access-management"></a><span data-ttu-id="bc3d0-130">Suplantación y administración del acceso a EWS</span><span class="sxs-lookup"><span data-stu-id="bc3d0-130">Impersonation and EWS access management</span></span>
<span data-ttu-id="bc3d0-131"><a name="bk_impersonation"> </a></span><span class="sxs-lookup"><span data-stu-id="bc3d0-131"><a name="bk_impersonation"> </a></span></span>

<span data-ttu-id="bc3d0-132">Es posible que las aplicaciones cliente que se conectan a EWS en nombre de propietarios de buzones de correo no puedan usar la configuración de EWS del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-132">Client applications that connect to EWS on behalf of mailbox owners might not be able to use the EWS settings of the mailbox owner.</span></span> <span data-ttu-id="bc3d0-133">Por ejemplo, una aplicación que archiva mensajes de correo electrónico para una compañía tiene que conectarse a EWS independientemente de la configuración de los usuarios del buzón.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-133">For example, an application that archives email messages for a company has to connect to EWS regardless of what the mailbox users' settings are.</span></span> <span data-ttu-id="bc3d0-134">Otras aplicaciones, como los clientes de correo, tienen que usar la configuración de EWS del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-134">Other applications, such as mail clients, do have to use the mailbox owner's EWS settings.</span></span> 
  
<span data-ttu-id="bc3d0-135">Los administradores deben crear una cuenta de suplantación para cada aplicación o clase de aplicación que usen en su servidor.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-135">Administrators should create an impersonation account for each application or application class that they use on their server.</span></span> <span data-ttu-id="bc3d0-136">Esto permitirá que el Administrador configure el ámbito de control de acceso basado en roles para todos los usuarios que no tengan permisos EWS.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-136">This will enable the administrator to configure the role-based access control scope for all users that do not have EWS permissions.</span></span> 
  
<span data-ttu-id="bc3d0-137">Para habilitar las cuentas de suplantación, el administrador del servidor de prueba o de producción debe realizar una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="bc3d0-137">To enable impersonation accounts, your test or production server administrator should do one of the following:</span></span> 
  
- <span data-ttu-id="bc3d0-138">Agregue el grupo usuarios autenticados al grupo acceso compatible con versiones anteriores a Win2K.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-138">Add the Authenticated Users group to the Pre-Win2K Compatible Access Group.</span></span> 
    
- <span data-ttu-id="bc3d0-139">Agregue el grupo servidores de Exchange al grupo de acceso de autorización de Windows.</span><span class="sxs-lookup"><span data-stu-id="bc3d0-139">Add the Exchange Servers group to the Windows Authorization Access group.</span></span> 
    
## <a name="exchange-management-shell-cmdlets-for-access-management"></a><span data-ttu-id="bc3d0-140">Cmdlets del shell de administración de Exchange para la administración de acceso</span><span class="sxs-lookup"><span data-stu-id="bc3d0-140">Exchange Management Shell cmdlets for access management</span></span>
<span data-ttu-id="bc3d0-141"><a name="bk_cmdlets"> </a></span><span class="sxs-lookup"><span data-stu-id="bc3d0-141"><a name="bk_cmdlets"> </a></span></span>

<span data-ttu-id="bc3d0-142">Los administradores usan los siguientes cmdlets del shell de administración de Exchange para configurar los controles de acceso de EWS:</span><span class="sxs-lookup"><span data-stu-id="bc3d0-142">Administrators use the following Exchange Management Shell cmdlets to configure EWS access controls:</span></span> 
  
- [<span data-ttu-id="bc3d0-143">Get-CASMailbox</span><span class="sxs-lookup"><span data-stu-id="bc3d0-143">Get-CASMailbox</span></span>](https://technet.microsoft.com/library/bb124754.aspx)   
- [<span data-ttu-id="bc3d0-144">Set-CASMailbox</span><span class="sxs-lookup"><span data-stu-id="bc3d0-144">Set-CASMailbox</span></span>](https://technet.microsoft.com/library/bb125264.aspx)   
- [<span data-ttu-id="bc3d0-145">Get-OrganizationConfig</span><span class="sxs-lookup"><span data-stu-id="bc3d0-145">Get-OrganizationConfig</span></span>](https://technet.microsoft.com/library/aa997571.aspx)   
- [<span data-ttu-id="bc3d0-146">Set-OrganizationConfig</span><span class="sxs-lookup"><span data-stu-id="bc3d0-146">Set-OrganizationConfig</span></span>](https://technet.microsoft.com/library/aa997443.aspx)
    
## <a name="see-also"></a><span data-ttu-id="bc3d0-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc3d0-147">See also</span></span>

- [<span data-ttu-id="bc3d0-148">Empezar a usar los servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="bc3d0-148">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)  
- [<span data-ttu-id="bc3d0-149">Controlar el acceso a EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="bc3d0-149">Control access to EWS in Exchange</span></span>](how-to-control-access-to-ews-in-exchange.md)
- [<span data-ttu-id="bc3d0-150">PowerShell de Exchange Server (Shell de administración de Exchange)</span><span class="sxs-lookup"><span data-stu-id="bc3d0-150">Exchange Server PowerShell (Exchange Management Shell)</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
- [<span data-ttu-id="bc3d0-151">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc3d0-151">Windows PowerShell</span></span>](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

