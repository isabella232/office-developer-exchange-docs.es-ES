---
title: Configurar la suplantación
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: efcef39f-e26d-4eed-95ac-36a5bf8c089f
description: Este documento puede incluir contenido relacionado con funciones o productos preliminares que pueden cambiar mucho antes del lanzamiento comercial final. Este documento se proporciona "tal cual" solamente con fines informativos y Microsoft no realiza ninguna garantía, explícita ni implícita, en el documento. Aprenda a otorgar el rol de suplantación a una cuenta de servicio usando el Shell de administración de Exchange.
ms.openlocfilehash: 57ccef48a7553bcc06e3b3ae940b376b8555ef84
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763049"
---
# <a name="configure-impersonation"></a><span data-ttu-id="16737-103">Configurar la suplantación</span><span class="sxs-lookup"><span data-stu-id="16737-103">Configure impersonation</span></span>

<span data-ttu-id="16737-104">Este documento puede incluir contenido relacionado con funciones o productos preliminares que pueden cambiar mucho antes del lanzamiento comercial final. Este documento se proporciona "tal cual" solamente con fines informativos y Microsoft no realiza ninguna garantía, explícita ni implícita, en el documento. Aprenda a otorgar el rol de suplantación a una cuenta de servicio usando el Shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="16737-104">Learn how to grant the impersonation role to a service account by using the Exchange Management Shell.</span></span> 
  
<span data-ttu-id="16737-p101">La suplantación permite que un llamador, como una aplicación de servicio, suplante una cuenta de usuario. El llamador puede realizar operaciones usando los permisos asociados a la cuenta de suplantación en lugar de los permisos asociados con la cuenta del llamador.</span><span class="sxs-lookup"><span data-stu-id="16737-p101">Impersonation enables a caller, such as a service application, to impersonate a user account. The caller can perform operations by using the permissions that are associated with the impersonated account instead of the permissions associated with the caller's account.</span></span>
  
<span data-ttu-id="16737-p102">Exchange Online, Exchange Online como parte de Office 365 y las versiones de Exchange a partir de Exchange 2013 usan el control de acceso basado en roles (RBAC) para asignar permisos a las cuentas. El administrador del servidor Exchange deberá conceder a la cuenta de servicio que suplantará a otros usuarios el rol **ApplicationImpersonation** usando el cmdlet [New-ManagementRoleAssignment](http://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx).</span><span class="sxs-lookup"><span data-stu-id="16737-p102">Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013 use role-based access control (RBAC) to assign permissions to accounts. Your Exchange server administrator will need to grant any service account that will be impersonating other users the **ApplicationImpersonation** role by using the [New-ManagementRoleAssignment](http://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx) cmdlet.</span></span> 
  
## <a name="configuring-the-applicationimpersonation-role"></a><span data-ttu-id="16737-109">Configurar el rol ApplicationImpersonation</span><span class="sxs-lookup"><span data-stu-id="16737-109">Configuring the ApplicationImpersonation role</span></span>

<span data-ttu-id="16737-110">Cuando usted o el administrador del servidor Exchanger asigne el rol **ApplicationImpersonation**, use los parámetros siguientes del cmdlet **New-ManagementRoleAssignment**:</span><span class="sxs-lookup"><span data-stu-id="16737-110">When you or your Exchanger server administrator assigns the **ApplicationImpersonation** role, use the following parameters of the **New-ManagementRoleAssignment** cmdlet:</span></span> 
  
-  <span data-ttu-id="16737-111">_Nombre_ &ndash; El nombre descriptivo de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="16737-111">_Name_ &ndash; The friendly name of the role assignment.</span></span> <span data-ttu-id="16737-112">Cada vez que asigna un rol, se realiza una entrada en la lista de roles RBAC.</span><span class="sxs-lookup"><span data-stu-id="16737-112">Each time that you assign a role, an entry is made in the RBAC roles list.</span></span> <span data-ttu-id="16737-113">Puede comprobar las asignaciones de roles mediante el cmdlet [Get-ManagementRoleAssignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx).</span><span class="sxs-lookup"><span data-stu-id="16737-113">You can verify role assignments by using the [Get-ManagementRoleAssignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet.</span></span> 
    
-  <span data-ttu-id="16737-114">_Rol_ &ndash; Un rol RBAC el para asignar.</span><span class="sxs-lookup"><span data-stu-id="16737-114">_Role_ &ndash; The RBAC role to assign.</span></span> <span data-ttu-id="16737-115">Al configurar la suplantación, se asigna el rol **ApplicationImpersonation**.</span><span class="sxs-lookup"><span data-stu-id="16737-115">When you set up impersonation, you assign the **ApplicationImpersonation** role.</span></span> 
    
-  <span data-ttu-id="16737-116">_Usuario_ &ndash; La cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="16737-116">_User_ &ndash; The service account.</span></span> 
    
-  <span data-ttu-id="16737-117">_CustomRecipientScope_ &ndash; El ámbito de los usuarios que puede suplantar la cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="16737-117">_CustomRecipientScope_ &ndash; The scope of users that the service account can impersonate.</span></span> <span data-ttu-id="16737-118">La cuenta de servicio solo tendrá permitido suplantar a otros usuarios dentro del ámbito especificado.</span><span class="sxs-lookup"><span data-stu-id="16737-118">The service account will only be allowed to impersonate other users within the specified scope.</span></span> <span data-ttu-id="16737-119">Si no se especifica ningún ámbito, la cuenta de servicio tiene el rol **ApplicationImpersonation** sobre todos los usuarios de una organización.</span><span class="sxs-lookup"><span data-stu-id="16737-119">If no scope is specified, the service account is granted the **ApplicationImpersonation** role over all users in an organization.</span></span> <span data-ttu-id="16737-120">Puede crear ámbitos de administración personalizada usando el cmdlet [New-ManagementScope](http://msdn.microsoft.com/library/1ea1f474-69d6-48c0-9beb-bfa4442c5dab.aspx).</span><span class="sxs-lookup"><span data-stu-id="16737-120">You can create custom management scopes by using the [New-ManagementScope](http://msdn.microsoft.com/library/1ea1f474-69d6-48c0-9beb-bfa4442c5dab.aspx) cmdlet.</span></span> 
    
<span data-ttu-id="16737-121">Antes de configurar la suplantación, necesita:</span><span class="sxs-lookup"><span data-stu-id="16737-121">Before you can configure impersonation, you need:</span></span>
  
- <span data-ttu-id="16737-122">Credenciales administrativas para el servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="16737-122">Administrative credentials for the Exchange server.</span></span>
    
- <span data-ttu-id="16737-123">Credenciales de administrador de dominio u otras credenciales con permiso para crear y asignar roles y ámbitos.</span><span class="sxs-lookup"><span data-stu-id="16737-123">Domain Administrator credentials, or other credentials with the permission to create and assign roles and scopes.</span></span>
    
- <span data-ttu-id="16737-p106">Herramientas de administración de Exchange. Están instaladas en el equipo desde el que se ejecutan los comandos.</span><span class="sxs-lookup"><span data-stu-id="16737-p106">Exchange management tools. These are installed on the computer from which you will run the commands.</span></span>
    
### <a name="to-configure-impersonation-for-all-users-in-an-organization"></a><span data-ttu-id="16737-126">Para configurar la suplantación para todos los usuarios de una organización</span><span class="sxs-lookup"><span data-stu-id="16737-126">To configure impersonation for all users in an organization</span></span>

1. <span data-ttu-id="16737-p107">Abra el Shell de administración de Exchange. En el menú Inicio, elija **Todos los programas** > **Microsoft Exchange Server 2013**.</span><span class="sxs-lookup"><span data-stu-id="16737-p107">Open the Exchange Management Shell. From the Start menu, choose **All Programs** > **Microsoft Exchange Server 2013**.</span></span> 
    
2. <span data-ttu-id="16737-p108">Ejecute el cmdlet **New-ManagementRoleAssignment** para agregar el permiso de suplantación en el usuario especificado. En el ejemplo siguiente se muestra cómo configurar la suplantación para permitir que una cuenta de servicio suplante a los demás usuarios de una organización.</span><span class="sxs-lookup"><span data-stu-id="16737-p108">Run the **New-ManagementRoleAssignment** cmdlet to add the impersonation permission to the specified user. The following example shows how to configure impersonation to enable a service account to impersonate all other users in an organization.</span></span> 
    
   ```powershell
   New-ManagementRoleAssignment -name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount 
   ```

### <a name="to-configure-impersonation-for-specific-users-or-groups-of-users"></a><span data-ttu-id="16737-131">Para configurar la suplantación de usuarios o grupos de usuarios específicos</span><span class="sxs-lookup"><span data-stu-id="16737-131">To configure impersonation for specific users or groups of users</span></span>

1. <span data-ttu-id="16737-p109">Abra el Shell de administración de Exchange. En el menú Inicio, elija **Todos los programas** > **Microsoft Exchange Server 2013**.</span><span class="sxs-lookup"><span data-stu-id="16737-p109">Open the Exchange Management Shell. From the Start menu, choose **All Programs** > **Microsoft Exchange Server 2013**.</span></span> 
    
2. <span data-ttu-id="16737-p110">Ejecute el cmdlet **New-ManagementScope** para crear un ámbito al que se pueda asignar el rol de suplantación. Si hay un ámbito existente, puede omitir este paso. En el ejemplo siguiente se muestra cómo crear un ámbito de administración para un grupo específico.</span><span class="sxs-lookup"><span data-stu-id="16737-p110">Run the **New-ManagementScope** cmdlet to create a scope to which the impersonation role can be assigned. If an existing scope is available, you can skip this step. The following example shows how to create a management scope for a specific group.</span></span> 
    
   ```powershell
    New-ManagementScope -Name:scopeName -RecipientRestrictionFilter:recipientFilter
   ```

   <span data-ttu-id="16737-137">El parámetro _RecipientRestrictionFilter_ del cmdlet **New-ManagementScope** define a los miembros del ámbito.</span><span class="sxs-lookup"><span data-stu-id="16737-137">The _RecipientRestrictionFilter_ parameter of the **New-ManagementScope** cmdlet defines the members of the scope.</span></span> <span data-ttu-id="16737-138">Puede usar las propiedades del objeto **Identity** para crear el filtro.</span><span class="sxs-lookup"><span data-stu-id="16737-138">You can use the properties of the **Identity** object to create the filter.</span></span> <span data-ttu-id="16737-139">El siguiente ejemplo es un filtro que restringe el resultado a un solo usuario con el usuario nombre de usuario "john".</span><span class="sxs-lookup"><span data-stu-id="16737-139">The following example is a filter that restricts the result to a single user with the user name "john."</span></span> 
    
   ```powershell
   Name -eq "john"
   ```

3. <span data-ttu-id="16737-p112">Ejecute el cmdlet **New-ManagementRoleAssignment** para agregar el permiso para suplantar a los miembros del ámbito especificado. El ejemplo siguiente muestra cómo configurar una cuenta de servicio para suplantar a todos los usuarios de un ámbito.</span><span class="sxs-lookup"><span data-stu-id="16737-p112">Run the **New-ManagementRoleAssignment** cmdlet to add the permission to impersonate the members of the specified scope. The following example shows how to configure a service account to impersonate all users in a scope.</span></span> 
    
   ```powershell
    New-ManagementRoleAssignment -Name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount -CustomRecipientWriteScope:scopeName
    
   ```


<span data-ttu-id="16737-p113">Después de que el administrador conceda los permisos de suplantación, puede usar la cuenta de servicio para realizar llamadas con las cuentas de otros usuarios. Puede comprobar las asignaciones de roles mediante el cmdlet [Get-ManagementRoleAssignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx).</span><span class="sxs-lookup"><span data-stu-id="16737-p113">After your administrator grants impersonation permissions, you can use the service account to make calls against other users' accounts. You can verify role assignments by using the [Get-ManagementRoleAssignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="16737-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="16737-144">See also</span></span>

- [<span data-ttu-id="16737-145">Suplantación y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="16737-145">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
- [<span data-ttu-id="16737-146">Rol ApplicationImpersonation</span><span class="sxs-lookup"><span data-stu-id="16737-146">ApplicationImpersonation role</span></span>](http://technet.microsoft.com/es-es/library/dd776119%28v=exchg.150%29.aspx)   
- [<span data-ttu-id="16737-147">New-ManagementRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="16737-147">New-ManagementRoleAssignment</span></span>](http://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx)    
- [<span data-ttu-id="16737-148">Get-ManagementRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="16737-148">Get-ManagementRoleAssignment</span></span>](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx)
    

