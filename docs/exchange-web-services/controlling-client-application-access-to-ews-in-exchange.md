---
title: Controlar el acceso de la aplicación de cliente para EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60ac3f7b-ba8a-4c93-99f7-c27002caff93
description: Obtenga información sobre las opciones para administrar el acceso de la aplicación de cliente a EWS.
ms.openlocfilehash: e3a0e07b733b4ebc070ab6b3fc73c8aec4b62785
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353066"
---
# <a name="controlling-client-application-access-to-ews-in-exchange"></a><span data-ttu-id="dd4f7-103">Controlar el acceso de la aplicación de cliente para EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="dd4f7-103">Controlling client application access to EWS in Exchange</span></span>

<span data-ttu-id="dd4f7-104">Obtenga información sobre las opciones para administrar el acceso de la aplicación de cliente a EWS.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-104">Learn about the options for managing client application access to EWS.</span></span>
  
<span data-ttu-id="dd4f7-105">Cualquier aplicación de cliente EWS que cree debe tener acceso a Exchange Online, Exchange Online como parte de Office 365, o una versión de Exchange comenzando con Exchange 2013 antes de que pueden llamar a las operaciones de EWS.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-105">Any EWS client application that you create must be granted access to Exchange Online, Exchange Online as part of Office 365, or version of Exchange starting with Exchange 2013 before it can call EWS operations.</span></span> <span data-ttu-id="dd4f7-106">Los administradores de servidores de prueba o de producción pueden usar el Shell de administración de Exchange para limitar el acceso a EWS para todos los usuarios y aplicaciones, para usuarios individuales o para aplicaciones individuales.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-106">Test or production server administrators can use the Exchange Management Shell to limit access to EWS either for all users and applications, for individual users, or for individual applications.</span></span> <span data-ttu-id="dd4f7-107">Control de acceso para EWS se basa en las cuentas de dominio.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-107">Access control for EWS is based on domain accounts.</span></span> <span data-ttu-id="dd4f7-108">Cuando se realiza una conexión con las credenciales que se autentican por la entidad de seguridad local, el servidor devuelve un error que indica que se pueden conectar sólo las cuentas de dominio.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-108">When a connection is made with credentials that are authenticated by the local security authority, the server returns an error that indicates that only domain accounts can connect.</span></span> 
  
## <a name="access-control-for-ews-clients-and-users"></a><span data-ttu-id="dd4f7-109">Control de acceso de los usuarios y los clientes EWS</span><span class="sxs-lookup"><span data-stu-id="dd4f7-109">Access control for EWS clients and users</span></span>
<span data-ttu-id="dd4f7-110"><a name="bk_configure"> </a></span><span class="sxs-lookup"><span data-stu-id="dd4f7-110"></span></span>

<span data-ttu-id="dd4f7-111">El administrador del servidor de prueba o de producción puede configurar el control de acceso para los clientes que se conectan a EWS de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="dd4f7-111">Your test or production server administrator can configure access control for clients that connect to EWS in the following ways:</span></span> 
  
- <span data-ttu-id="dd4f7-112">Mediante el bloqueo de todas las aplicaciones cliente de conexión.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-112">By blocking all client applications from connecting.</span></span>
    
- <span data-ttu-id="dd4f7-113">Al permitir que aplicaciones sólo para conectarse de cliente específico.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-113">By allowing specific client applications only to connect.</span></span>
    
- <span data-ttu-id="dd4f7-114">Al permitir que cualquier aplicación de cliente para conectarse, excepto aquellos que estén bloqueados específicamente.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-114">By allowing any client application to connect except those that are specifically blocked.</span></span>
    
- <span data-ttu-id="dd4f7-115">Al permitir que cualquier aplicación de cliente para conectarse.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-115">By allowing any client application to connect.</span></span>
    
<span data-ttu-id="dd4f7-116">Las aplicaciones se identifican mediante la cadena de agente de usuario que se envían en la solicitud web HTTP.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-116">Applications are identified by the user agent string that they send in the HTTP web request.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="dd4f7-117">Bloqueo de nivel de la aplicación no es una característica de seguridad.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-117">Application-level blocking is not a security feature.</span></span> <span data-ttu-id="dd4f7-118">La cadena de agente de usuario es suplantar fácilmente.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-118">The user agent string is easily spoofed.</span></span> <span data-ttu-id="dd4f7-119">Si se permite el acceso a EWS en una aplicación, la aplicación debe presentar las credenciales que se autentica el servidor antes de la aplicación puede conectarse a EWS.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-119">If an application is allowed access to EWS, the application must still present credentials that the server authenticates before the application can connect to EWS.</span></span> 
  
<span data-ttu-id="dd4f7-120">Los administradores también pueden configurar el control de acceso para los propietarios de buzón de correo que se conectan a EWS de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="dd4f7-120">Administrators can also configure access control for mailbox owners that connect to EWS in the following ways:</span></span> 
  
- <span data-ttu-id="dd4f7-121">Bloquear o permitir que toda la organización.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-121">By blocking or allowing an entire organization.</span></span>
    
- <span data-ttu-id="dd4f7-122">Bloquear o permitir que un grupo de usuarios identificado por un ámbito de autenticación basado en roles que incluye o excluye los propietarios de los buzones de correo que no tienen acceso a EWS.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-122">By blocking or allowing a group of users identified by a role-based authentication scope that includes or excludes mailbox owners that do not have access to EWS.</span></span>
    
- <span data-ttu-id="dd4f7-123">Bloquear o permitir que a un propietario de buzón de correo individuales.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-123">By blocking or allowing an individual mailbox owner.</span></span>
    
<span data-ttu-id="dd4f7-124">Configuración de control de acceso específico invalida la configuración de control de acceso general.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-124">Specific access control settings override general access control settings.</span></span> <span data-ttu-id="dd4f7-125">Por ejemplo, si una organización deniega el acceso EWS pero un propietario del buzón de correo individuales se permitió el acceso de la aplicación, prevalecerá la opción individual y se permite el acceso.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-125">For example, if an organization denies EWS access but an individual mailbox owner is allowed application access, the individual setting prevails and access is allowed.</span></span> 
  
## <a name="delegation-and-ews-access-management"></a><span data-ttu-id="dd4f7-126">Delegación y administración del acceso a EWS</span><span class="sxs-lookup"><span data-stu-id="dd4f7-126">Delegation and EWS access management</span></span>
<span data-ttu-id="dd4f7-127"><a name="bk_delegation"> </a></span><span class="sxs-lookup"><span data-stu-id="dd4f7-127"></span></span>

<span data-ttu-id="dd4f7-128">Cuando los usuarios delegados que no tienen acceso a EWS use la aplicación de cliente, no podrán tener acceso a la entidad de seguridad del buzón del usuario mediante el uso de acceso EWS, incluso si el usuario de entidad de seguridad tiene EWS.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-128">When delegate users who do not have access to EWS use your client application, they will not be able to access the principal user's mailbox by using EWS, even if the principal user has EWS access.</span></span> <span data-ttu-id="dd4f7-129">Si el usuario delegado tiene acceso a EWS, el delegado podrá usar la aplicación de cliente EWS para obtener acceso a la entidad de seguridad del buzón del usuario, incluso si el usuario de entidad de seguridad no tiene EWS acceso.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-129">If the delegate user has EWS access, the delegate will be able to use your EWS client application to access the principal user's mailbox even if the principal user does not have EWS access.</span></span> 
  
## <a name="impersonation-and-ews-access-management"></a><span data-ttu-id="dd4f7-130">Suplantación y administración del acceso a EWS</span><span class="sxs-lookup"><span data-stu-id="dd4f7-130">Impersonation and EWS access management</span></span>
<span data-ttu-id="dd4f7-131"><a name="bk_impersonation"> </a></span><span class="sxs-lookup"><span data-stu-id="dd4f7-131"></span></span>

<span data-ttu-id="dd4f7-132">Es posible que las aplicaciones de cliente que se conectan a EWS en nombre de los propietarios de los buzones de correo no podrá usar la configuración de EWS del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-132">Client applications that connect to EWS on behalf of mailbox owners might not be able to use the EWS settings of the mailbox owner.</span></span> <span data-ttu-id="dd4f7-133">Por ejemplo, una aplicación que archiva los mensajes para una compañía tiene para conectarse a EWS independientemente de la configuración de qué el buzón de correo los usuarios son de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-133">For example, an application that archives email messages for a company has to connect to EWS regardless of what the mailbox users' settings are.</span></span> <span data-ttu-id="dd4f7-134">Otras aplicaciones, como los clientes de correo, es necesario usar la configuración de EWS del propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-134">Other applications, such as mail clients, do have to use the mailbox owner's EWS settings.</span></span> 
  
<span data-ttu-id="dd4f7-135">Los administradores deben crear una cuenta de suplantación para cada aplicación o una clase de aplicación que use en su servidor.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-135">Administrators should create an impersonation account for each application or application class that they use on their server.</span></span> <span data-ttu-id="dd4f7-136">Esto permitirá que el administrador configure el ámbito de control de acceso basado en roles para todos los usuarios que no tienen permisos de EWS.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-136">This will enable the administrator to configure the role-based access control scope for all users that do not have EWS permissions.</span></span> 
  
<span data-ttu-id="dd4f7-137">Para habilitar cuentas de suplantación, el administrador del servidor de prueba o de producción debe realizar una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="dd4f7-137">To enable impersonation accounts, your test or production server administrator should do one of the following:</span></span> 
  
- <span data-ttu-id="dd4f7-138">Agregue el grupo Usuarios autenticados al grupo acceso Compatible Pre-Win2K.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-138">Add the Authenticated Users group to the Pre-Win2K Compatible Access Group.</span></span> 
    
- <span data-ttu-id="dd4f7-139">Agregue el grupo de servidores de Exchange para el grupo de acceso de autorización de Windows.</span><span class="sxs-lookup"><span data-stu-id="dd4f7-139">Add the Exchange Servers group to the Windows Authorization Access group.</span></span> 
    
## <a name="exchange-management-shell-cmdlets-for-access-management"></a><span data-ttu-id="dd4f7-140">Cmdlets del Shell de administración de Exchange para la administración de acceso</span><span class="sxs-lookup"><span data-stu-id="dd4f7-140">Exchange Management Shell cmdlets for access management</span></span>
<span data-ttu-id="dd4f7-141"><a name="bk_cmdlets"> </a></span><span class="sxs-lookup"><span data-stu-id="dd4f7-141"></span></span>

<span data-ttu-id="dd4f7-142">Los administradores usar los siguientes cmdlets del Shell de administración de Exchange para configurar el acceso a controles de EWS:</span><span class="sxs-lookup"><span data-stu-id="dd4f7-142">Administrators use the following Exchange Management Shell cmdlets to configure EWS access controls:</span></span> 
  
- [<span data-ttu-id="dd4f7-143">Get-CASMailbox</span><span class="sxs-lookup"><span data-stu-id="dd4f7-143">Get-CASMailbox</span></span>](http://technet.microsoft.com/en-us/library/bb124754.aspx)   
- [<span data-ttu-id="dd4f7-144">Set-CASMailbox</span><span class="sxs-lookup"><span data-stu-id="dd4f7-144">Set-CASMailbox</span></span>](http://technet.microsoft.com/en-us/library/bb125264.aspx)   
- [<span data-ttu-id="dd4f7-145">Get-OrganizationConfig</span><span class="sxs-lookup"><span data-stu-id="dd4f7-145">Get-OrganizationConfig</span></span>](http://technet.microsoft.com/en-us/library/aa997571.aspx)   
- [<span data-ttu-id="dd4f7-146">Set-OrganizationConfig</span><span class="sxs-lookup"><span data-stu-id="dd4f7-146">Set-OrganizationConfig</span></span>](http://technet.microsoft.com/en-us/library/aa997443.aspx)
    
## <a name="see-also"></a><span data-ttu-id="dd4f7-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd4f7-147">See also</span></span>

- [<span data-ttu-id="dd4f7-148">Empezar a utilizar servicios web de Exchange</span><span class="sxs-lookup"><span data-stu-id="dd4f7-148">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)  
- [<span data-ttu-id="dd4f7-149">Controlar el acceso a EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="dd4f7-149">Control access to EWS in Exchange</span></span>](how-to-control-access-to-ews-in-exchange.md)
- [<span data-ttu-id="dd4f7-150">Exchange Server PowerShell (Shell de administración de Exchange)</span><span class="sxs-lookup"><span data-stu-id="dd4f7-150">Exchange Server PowerShell (Exchange Management Shell)</span></span>](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
- [<span data-ttu-id="dd4f7-151">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dd4f7-151">Windows PowerShell</span></span>](http://msdn.microsoft.com/en-us/library/dd835506%28v=vs.85%29.aspx)
    

