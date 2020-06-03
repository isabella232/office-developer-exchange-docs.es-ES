---
title: Establecer los permisos de carpeta para otro usuario mediante EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb81676-a780-4c56-b4f2-c4ed2697107d
description: Obtenga información sobre cómo establecer niveles de permisos en una carpeta mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: e25f1a49a430e8c95829d404fa53451b76cab167
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455873"
---
# <a name="set-folder-permissions-for-another-user-by-using-ews-in-exchange"></a><span data-ttu-id="b8f9d-103">Establecer los permisos de carpeta para otro usuario mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b8f9d-103">Set folder permissions for another user by using EWS in Exchange</span></span>

<span data-ttu-id="b8f9d-104">Obtenga información sobre cómo establecer niveles de permisos en una carpeta mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-104">Learn how to set permission levels on a folder by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="b8f9d-105">Los permisos de nivel de carpeta permiten a los usuarios tener acceso a una o más carpetas en el buzón de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-105">Folder-level permissions enable users to access one or more folders in another user's mailbox.</span></span> <span data-ttu-id="b8f9d-106">Los permisos de carpeta son similares a acceso delegado, pero se diferencian en los siguientes aspectos:</span><span class="sxs-lookup"><span data-stu-id="b8f9d-106">Folder permissions are similar to delegate access, but they differ in the following ways:</span></span> 
  
- <span data-ttu-id="b8f9d-107">Los permisos de carpeta no permiten a un usuario "enviar en nombre de" o "enviar como" otro usuario.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-107">Folder permissions do not enable a user to "send on behalf of" or "send as" another user.</span></span> <span data-ttu-id="b8f9d-108">Solo permiten el acceso a las carpetas.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-108">They only enable access to folders.</span></span> <span data-ttu-id="b8f9d-109">Los usuarios pueden crear elementos en esas carpetas, pero no pueden enviarlos.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-109">Users can create items in those folders, but they can't send them.</span></span>
    
- <span data-ttu-id="b8f9d-110">Puede establecer los permisos de carpeta en cualquier carpeta del buzón, pero solo puede Agregar un delegado a las carpetas calendario, contactos, bandeja de entrada, diario, notas y tareas.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-110">You can set folder permissions on any folder in the mailbox, but you can only add a delegate to the Calendar, Contacts, Inbox, Journal, Notes, and Tasks folders.</span></span>
    
- <span data-ttu-id="b8f9d-111">Puede establecer un número de [permisos en una carpeta específica](#bk_folderperms).</span><span class="sxs-lookup"><span data-stu-id="b8f9d-111">You can set a number of [permissions on a specific folder](#bk_folderperms).</span></span> <span data-ttu-id="b8f9d-112">Al agregar un delegado, puede asignar uno de estos [cinco niveles de permisos](delegate-access-and-ews-in-exchange.md#bk_delegateperms).</span><span class="sxs-lookup"><span data-stu-id="b8f9d-112">When you add a delegate, you can assign one of only [five permission levels](delegate-access-and-ews-in-exchange.md#bk_delegateperms).</span></span>
    
- <span data-ttu-id="b8f9d-113">Puede establecer los permisos de carpeta para usuarios anónimos y predeterminados.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-113">You can set folder permissions for anonymous and default users.</span></span> <span data-ttu-id="b8f9d-114">Solo puede conceder acceso delegado a una cuenta habilitada para correo.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-114">You can only grant delegate access to a mail-enabled account.</span></span>
    
<span data-ttu-id="b8f9d-115">Si está familiarizado con las entradas de control de acceso (ACE) y las listas de control de acceso discrecional (DACL), sabrá que un usuario solo puede tener un conjunto de permisos para cada carpeta.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-115">If you're familiar with Access Control Entries (ACEs) and Discretionary Access Control Lists (DACLs), you know that a user can only have one set of permissions for each folder.</span></span> <span data-ttu-id="b8f9d-116">Si intenta agregar un conjunto de permisos para un usuario y ya tienen un conjunto de permisos, recibirá un error.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-116">If you try to add a set of permissions for a user and they already have a set of permissions, you'll get an error.</span></span> <span data-ttu-id="b8f9d-117">Al agregar, quitar o actualizar permisos en una carpeta, se obtiene la DACL actual, se agregan o se quitan todas las ACE y, a continuación, se envía la DACL actualizada.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-117">When you add, remove, or update permissions on a folder, you get the current DACL, add or remove any ACEs, and then send the updated DACL.</span></span> <span data-ttu-id="b8f9d-118">No se pueden agregar varias ACE para el mismo usuario.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-118">You cannot add multiple ACEs for the same user.</span></span> <span data-ttu-id="b8f9d-119">Al actualizar los permisos mediante la API administrada de EWS, debe quitar la ACE actual del usuario y, a continuación, agregar la nueva ACE a la colección.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-119">When you update permissions by using the EWS Managed API, you need to remove the user's current ACE and then add their new ACE to the collection.</span></span> <span data-ttu-id="b8f9d-120">Si está usando EWS, solo tiene que reemplazar el conjunto anterior de ACE por los nuevos.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-120">If you're using EWS, you just replace the previous set of ACEs with the new ones.</span></span>
  
<span data-ttu-id="b8f9d-121">Si está realizando varios cambios de permisos en una sola carpeta, puede realizar adiciones, eliminaciones o actualizaciones por lotes (solo tiene en cuenta que no puede realizar actualizaciones de usuario por lotes en varias carpetas).</span><span class="sxs-lookup"><span data-stu-id="b8f9d-121">If you're making multiple permission changes to a single folder, you can batch additions, removals, or updates —just note that you cannot batch user updates on multiple folders.</span></span> <span data-ttu-id="b8f9d-122">Se necesita una llamada para obtener los permisos en una carpeta única y se necesita una segunda llamada para actualizar los permisos en esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-122">One call is required to get the permissions on a single folder, and a second call is required to update the permissions on that folder.</span></span> <span data-ttu-id="b8f9d-123">Cuando se agregan, quitan o actualizan permisos de usuario, se usan las mismas dos llamadas a métodos u operaciones para cada tarea.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-123">When you add, remove, or update user permissions, you use the same two method calls or operations for each task.</span></span>
  
<span data-ttu-id="b8f9d-124">**Tabla 1. Métodos de API administrada de EWS y operaciones EWS para establecer permisos de carpeta**</span><span class="sxs-lookup"><span data-stu-id="b8f9d-124">**Table 1. EWS Managed API methods and EWS operations for setting folder permissions**</span></span>

|<span data-ttu-id="b8f9d-125">Si quiere...</span><span class="sxs-lookup"><span data-stu-id="b8f9d-125">If you want to…</span></span>|<span data-ttu-id="b8f9d-126">Use este método de API administrada de EWS...</span><span class="sxs-lookup"><span data-stu-id="b8f9d-126">Use this EWS Managed API method…</span></span>|<span data-ttu-id="b8f9d-127">Usar esta operación de EWS...</span><span class="sxs-lookup"><span data-stu-id="b8f9d-127">Use this EWS operation…</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b8f9d-128">Habilitar, quitar o actualizar los permisos de carpeta</span><span class="sxs-lookup"><span data-stu-id="b8f9d-128">Enable, remove, or update folder permissions</span></span>  <br/> |<span data-ttu-id="b8f9d-129">[Folder. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) seguido de [Folder. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8f9d-129">[Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) followed by [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="b8f9d-130">[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) seguida de [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8f9d-130">[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) followed by [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="b8f9d-131">Crear una carpeta y definir los permisos de carpeta</span><span class="sxs-lookup"><span data-stu-id="b8f9d-131">Create a folder and define folder permissions</span></span>  <br/> |[<span data-ttu-id="b8f9d-132">Folder. Save</span><span class="sxs-lookup"><span data-stu-id="b8f9d-132">Folder.Save</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="b8f9d-133">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="b8f9d-133">CreateFolder</span></span>](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
   
## <a name="folder-permissions"></a><span data-ttu-id="b8f9d-134">Permisos de carpeta</span><span class="sxs-lookup"><span data-stu-id="b8f9d-134">Folder permissions</span></span>
<span data-ttu-id="b8f9d-135"><a name="bk_folderperms"> </a></span><span class="sxs-lookup"><span data-stu-id="b8f9d-135"><a name="bk_folderperms"> </a></span></span>

<span data-ttu-id="b8f9d-136">Tiene algunas opciones cuando se trata de establecer los permisos de carpeta en una carpeta específica.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-136">You have quite a few options when it comes to setting folder permissions on a specific folder.</span></span> <span data-ttu-id="b8f9d-137">Puede establecer un nivel de permisos en una carpeta para cada usuario, que agrega un conjunto de permisos individuales predefinidos a la DACL, o puede establecer permisos individuales en una carpeta, pero no puede combinar y hacer coincidir.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-137">You can set a permission level on a folder for each user, which adds a set of predefined individual permissions to the DACL, or you can set individual permissions on a folder — but you can't mix and match.</span></span>
  
<span data-ttu-id="b8f9d-138">Están disponibles los siguientes permisos individuales:</span><span class="sxs-lookup"><span data-stu-id="b8f9d-138">The following individual permissions are available:</span></span>
  
- <span data-ttu-id="b8f9d-139">Puede crear</span><span class="sxs-lookup"><span data-stu-id="b8f9d-139">Can create</span></span>
- <span data-ttu-id="b8f9d-140">Puede crear subcarpetas</span><span class="sxs-lookup"><span data-stu-id="b8f9d-140">Can create subfolders</span></span>    
- <span data-ttu-id="b8f9d-141">Es el propietario de la carpeta</span><span class="sxs-lookup"><span data-stu-id="b8f9d-141">Is folder owner</span></span>    
- <span data-ttu-id="b8f9d-142">La carpeta es visible</span><span class="sxs-lookup"><span data-stu-id="b8f9d-142">Is folder visible</span></span>    
- <span data-ttu-id="b8f9d-143">Es contacto de carpeta</span><span class="sxs-lookup"><span data-stu-id="b8f9d-143">Is folder contact</span></span>    
- <span data-ttu-id="b8f9d-144">Editar elementos</span><span class="sxs-lookup"><span data-stu-id="b8f9d-144">Edit items</span></span>    
- <span data-ttu-id="b8f9d-145">Eliminar elementos</span><span class="sxs-lookup"><span data-stu-id="b8f9d-145">Delete items</span></span>    
- <span data-ttu-id="b8f9d-146">Leer elementos</span><span class="sxs-lookup"><span data-stu-id="b8f9d-146">Read items</span></span>
    
<span data-ttu-id="b8f9d-147">Además, están disponibles los siguientes niveles de permisos, que definen un subconjunto de valores y permisos individuales, como se muestra en la tabla 2:</span><span class="sxs-lookup"><span data-stu-id="b8f9d-147">In addition, the following permission levels are available, which define a subset of individual permissions and values, as shown in Table 2:</span></span>
  
- <span data-ttu-id="b8f9d-148">None</span><span class="sxs-lookup"><span data-stu-id="b8f9d-148">None</span></span>    
- <span data-ttu-id="b8f9d-149">Owner</span><span class="sxs-lookup"><span data-stu-id="b8f9d-149">Owner</span></span>    
- <span data-ttu-id="b8f9d-150">Publishingeditorcreateitems</span><span class="sxs-lookup"><span data-stu-id="b8f9d-150">PublishingEditor</span></span>    
- <span data-ttu-id="b8f9d-151">Editor</span><span class="sxs-lookup"><span data-stu-id="b8f9d-151">Editor</span></span>    
- <span data-ttu-id="b8f9d-152">Publishingauthorcreateitems</span><span class="sxs-lookup"><span data-stu-id="b8f9d-152">PublishingAuthor</span></span>    
- <span data-ttu-id="b8f9d-153">Autor</span><span class="sxs-lookup"><span data-stu-id="b8f9d-153">Author</span></span>    
- <span data-ttu-id="b8f9d-154">Noneditingauthorcreateitems</span><span class="sxs-lookup"><span data-stu-id="b8f9d-154">NoneditingAuthor</span></span>    
- <span data-ttu-id="b8f9d-155">Reviewer</span><span class="sxs-lookup"><span data-stu-id="b8f9d-155">Reviewer</span></span>    
- <span data-ttu-id="b8f9d-156">Colaborador</span><span class="sxs-lookup"><span data-stu-id="b8f9d-156">Contributor</span></span>   
- <span data-ttu-id="b8f9d-157">Custom: la aplicación no puede establecer este valor.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-157">Custom - This value cannot be set by the application.</span></span> <span data-ttu-id="b8f9d-158">El servidor establece este valor si la aplicación incluye una colección personalizada de permisos individuales.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-158">The server sets this value if the application includes a custom collection of individual permissions.</span></span>    
- <span data-ttu-id="b8f9d-159">FreeBusyTimeOnly: solo puede establecerse en las carpetas de calendario.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-159">FreeBusyTimeOnly - This can only be set on Calendar folders.</span></span>   
- <span data-ttu-id="b8f9d-160">FreeBusyTimeAndSubjectAndLocation: solo puede establecerse en las carpetas de calendario.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-160">FreeBusyTimeAndSubjectAndLocation - This can only be set on Calendar folders.</span></span>
    
<span data-ttu-id="b8f9d-161">En la siguiente tabla se muestran los permisos individuales que se aplican de forma predeterminada en función del nivel de permisos.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-161">The following table shows which individual permissions are applied by default based on permission level.</span></span>
  
<span data-ttu-id="b8f9d-162">**Tabla 2. Permisos individuales por nivel de permisos**</span><span class="sxs-lookup"><span data-stu-id="b8f9d-162">**Table 2. Individual permissions by permission level**</span></span>

|<span data-ttu-id="b8f9d-163">Nivel de permisos</span><span class="sxs-lookup"><span data-stu-id="b8f9d-163">Permission level</span></span>|<span data-ttu-id="b8f9d-164">Puede crear elementos</span><span class="sxs-lookup"><span data-stu-id="b8f9d-164">Can create items</span></span>|<span data-ttu-id="b8f9d-165">Puede crear subcarpetas</span><span class="sxs-lookup"><span data-stu-id="b8f9d-165">Can create sub folders</span></span>|<span data-ttu-id="b8f9d-166">Es el propietario de la carpeta</span><span class="sxs-lookup"><span data-stu-id="b8f9d-166">Is folder owner</span></span>|<span data-ttu-id="b8f9d-167">La carpeta es visible</span><span class="sxs-lookup"><span data-stu-id="b8f9d-167">Is folder visible</span></span>|<span data-ttu-id="b8f9d-168">Es contacto de carpeta</span><span class="sxs-lookup"><span data-stu-id="b8f9d-168">Is folder contact</span></span>|<span data-ttu-id="b8f9d-169">Editar elementos</span><span class="sxs-lookup"><span data-stu-id="b8f9d-169">Edit items</span></span>|<span data-ttu-id="b8f9d-170">Eliminar elementos</span><span class="sxs-lookup"><span data-stu-id="b8f9d-170">Delete items</span></span>|<span data-ttu-id="b8f9d-171">Puede leer elementos</span><span class="sxs-lookup"><span data-stu-id="b8f9d-171">Can read items</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b8f9d-172">None</span><span class="sxs-lookup"><span data-stu-id="b8f9d-172">None</span></span>  <br/> |<span data-ttu-id="b8f9d-173">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-173">False</span></span>  <br/> |<span data-ttu-id="b8f9d-174">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-174">False</span></span>  <br/> |<span data-ttu-id="b8f9d-175">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-175">False</span></span>  <br/> |<span data-ttu-id="b8f9d-176">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-176">False</span></span>  <br/> |<span data-ttu-id="b8f9d-177">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-177">False</span></span>  <br/> |<span data-ttu-id="b8f9d-178">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b8f9d-178">None</span></span>  <br/> |<span data-ttu-id="b8f9d-179">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b8f9d-179">None</span></span>  <br/> |<span data-ttu-id="b8f9d-180">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b8f9d-180">None</span></span>  <br/> |
|<span data-ttu-id="b8f9d-181">Owner</span><span class="sxs-lookup"><span data-stu-id="b8f9d-181">Owner</span></span>  <br/> |<span data-ttu-id="b8f9d-182">True</span><span class="sxs-lookup"><span data-stu-id="b8f9d-182">True</span></span>  <br/> |<span data-ttu-id="b8f9d-183">True</span><span class="sxs-lookup"><span data-stu-id="b8f9d-183">True</span></span>  <br/> |<span data-ttu-id="b8f9d-184">True</span><span class="sxs-lookup"><span data-stu-id="b8f9d-184">True</span></span>  <br/> |<span data-ttu-id="b8f9d-185">True</span><span class="sxs-lookup"><span data-stu-id="b8f9d-185">True</span></span>  <br/> |<span data-ttu-id="b8f9d-186">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b8f9d-186">True</span></span>  <br/> |<span data-ttu-id="b8f9d-187">Todo</span><span class="sxs-lookup"><span data-stu-id="b8f9d-187">All</span></span>  <br/> |<span data-ttu-id="b8f9d-188">Todo</span><span class="sxs-lookup"><span data-stu-id="b8f9d-188">All</span></span>  <br/> |<span data-ttu-id="b8f9d-189">FullDetails</span><span class="sxs-lookup"><span data-stu-id="b8f9d-189">FullDetails</span></span>  <br/> |
|<span data-ttu-id="b8f9d-190">Publishingeditorcreateitems</span><span class="sxs-lookup"><span data-stu-id="b8f9d-190">PublishingEditor</span></span>  <br/> |<span data-ttu-id="b8f9d-191">True</span><span class="sxs-lookup"><span data-stu-id="b8f9d-191">True</span></span>  <br/> |<span data-ttu-id="b8f9d-192">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b8f9d-192">True</span></span>  <br/> |<span data-ttu-id="b8f9d-193">False</span><span class="sxs-lookup"><span data-stu-id="b8f9d-193">False</span></span>  <br/> |<span data-ttu-id="b8f9d-194">True</span><span class="sxs-lookup"><span data-stu-id="b8f9d-194">True</span></span>  <br/> |<span data-ttu-id="b8f9d-195">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-195">False</span></span>  <br/> |<span data-ttu-id="b8f9d-196">Todo</span><span class="sxs-lookup"><span data-stu-id="b8f9d-196">All</span></span>  <br/> |<span data-ttu-id="b8f9d-197">Todo</span><span class="sxs-lookup"><span data-stu-id="b8f9d-197">All</span></span>  <br/> |<span data-ttu-id="b8f9d-198">FullDetails</span><span class="sxs-lookup"><span data-stu-id="b8f9d-198">FullDetails</span></span>  <br/> |
|<span data-ttu-id="b8f9d-199">Editor</span><span class="sxs-lookup"><span data-stu-id="b8f9d-199">Editor</span></span>  <br/> |<span data-ttu-id="b8f9d-200">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b8f9d-200">True</span></span>  <br/> |<span data-ttu-id="b8f9d-201">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-201">False</span></span>  <br/> |<span data-ttu-id="b8f9d-202">False</span><span class="sxs-lookup"><span data-stu-id="b8f9d-202">False</span></span>  <br/> |<span data-ttu-id="b8f9d-203">True</span><span class="sxs-lookup"><span data-stu-id="b8f9d-203">True</span></span>  <br/> |<span data-ttu-id="b8f9d-204">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-204">False</span></span>  <br/> |<span data-ttu-id="b8f9d-205">Todo</span><span class="sxs-lookup"><span data-stu-id="b8f9d-205">All</span></span>  <br/> |<span data-ttu-id="b8f9d-206">Todo</span><span class="sxs-lookup"><span data-stu-id="b8f9d-206">All</span></span>  <br/> |<span data-ttu-id="b8f9d-207">FullDetails</span><span class="sxs-lookup"><span data-stu-id="b8f9d-207">FullDetails</span></span>  <br/> |
|<span data-ttu-id="b8f9d-208">Publishingauthorcreateitems</span><span class="sxs-lookup"><span data-stu-id="b8f9d-208">PublishingAuthor</span></span>  <br/> |<span data-ttu-id="b8f9d-209">True</span><span class="sxs-lookup"><span data-stu-id="b8f9d-209">True</span></span>  <br/> |<span data-ttu-id="b8f9d-210">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b8f9d-210">True</span></span>  <br/> |<span data-ttu-id="b8f9d-211">False</span><span class="sxs-lookup"><span data-stu-id="b8f9d-211">False</span></span>  <br/> |<span data-ttu-id="b8f9d-212">True</span><span class="sxs-lookup"><span data-stu-id="b8f9d-212">True</span></span>  <br/> |<span data-ttu-id="b8f9d-213">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-213">False</span></span>  <br/> |<span data-ttu-id="b8f9d-214">Estatal</span><span class="sxs-lookup"><span data-stu-id="b8f9d-214">Owned</span></span>  <br/> |<span data-ttu-id="b8f9d-215">Estatal</span><span class="sxs-lookup"><span data-stu-id="b8f9d-215">Owned</span></span>  <br/> |<span data-ttu-id="b8f9d-216">FullDetails</span><span class="sxs-lookup"><span data-stu-id="b8f9d-216">FullDetails</span></span>  <br/> |
|<span data-ttu-id="b8f9d-217">Autor</span><span class="sxs-lookup"><span data-stu-id="b8f9d-217">Author</span></span>  <br/> |<span data-ttu-id="b8f9d-218">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b8f9d-218">True</span></span>  <br/> |<span data-ttu-id="b8f9d-219">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-219">False</span></span>  <br/> |<span data-ttu-id="b8f9d-220">False</span><span class="sxs-lookup"><span data-stu-id="b8f9d-220">False</span></span>  <br/> |<span data-ttu-id="b8f9d-221">True</span><span class="sxs-lookup"><span data-stu-id="b8f9d-221">True</span></span>  <br/> |<span data-ttu-id="b8f9d-222">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-222">False</span></span>  <br/> |<span data-ttu-id="b8f9d-223">Estatal</span><span class="sxs-lookup"><span data-stu-id="b8f9d-223">Owned</span></span>  <br/> |<span data-ttu-id="b8f9d-224">Estatal</span><span class="sxs-lookup"><span data-stu-id="b8f9d-224">Owned</span></span>  <br/> |<span data-ttu-id="b8f9d-225">FullDetails</span><span class="sxs-lookup"><span data-stu-id="b8f9d-225">FullDetails</span></span>  <br/> |
|<span data-ttu-id="b8f9d-226">Noneditingauthorcreateitems</span><span class="sxs-lookup"><span data-stu-id="b8f9d-226">NoneditingAuthor</span></span>  <br/> |<span data-ttu-id="b8f9d-227">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b8f9d-227">True</span></span>  <br/> |<span data-ttu-id="b8f9d-228">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-228">False</span></span>  <br/> |<span data-ttu-id="b8f9d-229">False</span><span class="sxs-lookup"><span data-stu-id="b8f9d-229">False</span></span>  <br/> |<span data-ttu-id="b8f9d-230">True</span><span class="sxs-lookup"><span data-stu-id="b8f9d-230">True</span></span>  <br/> |<span data-ttu-id="b8f9d-231">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-231">False</span></span>  <br/> |<span data-ttu-id="b8f9d-232">None</span><span class="sxs-lookup"><span data-stu-id="b8f9d-232">None</span></span>  <br/> |<span data-ttu-id="b8f9d-233">Estatal</span><span class="sxs-lookup"><span data-stu-id="b8f9d-233">Owned</span></span>  <br/> |<span data-ttu-id="b8f9d-234">FullDetails</span><span class="sxs-lookup"><span data-stu-id="b8f9d-234">FullDetails</span></span>  <br/> |
|<span data-ttu-id="b8f9d-235">Reviewer</span><span class="sxs-lookup"><span data-stu-id="b8f9d-235">Reviewer</span></span>  <br/> |<span data-ttu-id="b8f9d-236">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-236">False</span></span>  <br/> |<span data-ttu-id="b8f9d-237">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-237">False</span></span>  <br/> |<span data-ttu-id="b8f9d-238">False</span><span class="sxs-lookup"><span data-stu-id="b8f9d-238">False</span></span>  <br/> |<span data-ttu-id="b8f9d-239">True</span><span class="sxs-lookup"><span data-stu-id="b8f9d-239">True</span></span>  <br/> |<span data-ttu-id="b8f9d-240">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-240">False</span></span>  <br/> |<span data-ttu-id="b8f9d-241">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b8f9d-241">None</span></span>  <br/> |<span data-ttu-id="b8f9d-242">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b8f9d-242">None</span></span>  <br/> |<span data-ttu-id="b8f9d-243">FullDetails</span><span class="sxs-lookup"><span data-stu-id="b8f9d-243">FullDetails</span></span>  <br/> |
|<span data-ttu-id="b8f9d-244">Colaborador</span><span class="sxs-lookup"><span data-stu-id="b8f9d-244">Contributor</span></span>  <br/> |<span data-ttu-id="b8f9d-245">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b8f9d-245">True</span></span>  <br/> |<span data-ttu-id="b8f9d-246">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-246">False</span></span>  <br/> |<span data-ttu-id="b8f9d-247">False</span><span class="sxs-lookup"><span data-stu-id="b8f9d-247">False</span></span>  <br/> |<span data-ttu-id="b8f9d-248">True</span><span class="sxs-lookup"><span data-stu-id="b8f9d-248">True</span></span>  <br/> |<span data-ttu-id="b8f9d-249">Falso</span><span class="sxs-lookup"><span data-stu-id="b8f9d-249">False</span></span>  <br/> |<span data-ttu-id="b8f9d-250">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b8f9d-250">None</span></span>  <br/> |<span data-ttu-id="b8f9d-251">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b8f9d-251">None</span></span>  <br/> |<span data-ttu-id="b8f9d-252">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b8f9d-252">None</span></span>  <br/> |
   
<span data-ttu-id="b8f9d-253">Si especifica un nivel de permisos no personalizado en la solicitud de permisos de nivel de carpeta, no es necesario especificar la configuración de permisos individuales.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-253">If you specify a non-custom permission level in the folder-level permissions request, you don't need to specify the individual permission settings.</span></span> <span data-ttu-id="b8f9d-254">Si especifica un permiso individual al establecer un nivel de permisos, se devolverá un error **ErrorInvalidPermissionSettings** en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-254">If you do specify an individual permission when you set a permission level, an **ErrorInvalidPermissionSettings** error will be returned in the response.</span></span> 
  
## <a name="adding-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="b8f9d-255">Adición de permisos de carpeta mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="b8f9d-255">Adding folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="b8f9d-256"><a name="bk_enableewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b8f9d-256"><a name="bk_enableewsma"> </a></span></span>

<span data-ttu-id="b8f9d-257">En el siguiente ejemplo de código se muestra cómo usar la API administrada de EWS para:</span><span class="sxs-lookup"><span data-stu-id="b8f9d-257">The following code example shows how to use the EWS Managed API to:</span></span> 
  
- <span data-ttu-id="b8f9d-258">Cree un nuevo objeto [FolderPermission](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx) para el nuevo usuario.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-258">Create a new [FolderPermission](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx) object for the new user.</span></span> 
    
- <span data-ttu-id="b8f9d-259">Obtener los permisos actuales para una carpeta mediante el método [BIND](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b8f9d-259">Get the current permissions for a folder by using the [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method.</span></span> 
    
- <span data-ttu-id="b8f9d-260">Agregue el nuevo **FolderPermissions** a la propiedad [Folder. Permissions](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b8f9d-260">Add the new **FolderPermissions** to the [Folder.Permissions](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx) property.</span></span> 
    
- <span data-ttu-id="b8f9d-261">Llame al método [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) para guardar los nuevos permisos en el servidor.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-261">Call the [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) method to save the new permissions to the server.</span></span> 
    
<span data-ttu-id="b8f9d-262">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el propietario del buzón y que el usuario se ha autenticado en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-262">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
static void EnableFolderPermissions(ExchangeService service)
{
    // Create a property set to use for folder binding.
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, FolderSchema.Permissions);
    // Specify the SMTP address of the new user and the folder permissions level.
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
    
    // Bind to the folder and get the current permissions. 
    // This call results in a GetFolder call to EWS.
    Folder sentItemsFolder = Folder.Bind(service, WellKnownFolderName.SentItems, propSet);
 
    // Add the permissions for the new user to the Sent Items DACL.
    sentItemsFolder.Permissions.Add(fldperm);
    // This call results in a UpdateFolder call to EWS.
    sentItemsFolder.Update();
}
```

<span data-ttu-id="b8f9d-263">La siguiente línea de código especifica el nivel de permisos.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-263">The following line of code specifies the permission level.</span></span>
  
```cs
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
```

<span data-ttu-id="b8f9d-264">Si desea usar el nivel de permisos personalizado, use este código en su lugar.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-264">If you want to use the custom permission level, use this code instead.</span></span>
  
```cs
FolderPermission fldperm = new FolderPermission();
fldperm.UserId = "sadie@Contoso1000.onmicrosoft.com";
fldperm.CanCreateItems = true;
fldperm.CanCreateSubFolders = true;
…
```

<span data-ttu-id="b8f9d-265">Puede establecer cualquiera o todas las [propiedades FolderPermission](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx) de escritura al crear un objeto **FolderPermission** con un nivel de permisos personalizado.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-265">You can set any or all of the writable [FolderPermission properties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx) when you create a **FolderPermission** object with a custom permission level.</span></span> <span data-ttu-id="b8f9d-266">Sin embargo, tenga en cuenta que [FolderPermissionLevel](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx) nunca se establece de forma explícita en **personalizada** por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-266">Note, however, that the [FolderPermissionLevel](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx) is never explicitly set to **Custom** by the application.</span></span> <span data-ttu-id="b8f9d-267">**FolderPermissionLevel** se establece en personalizado solo cuando se crea un objeto **FolderPermission** y se establecen permisos individuales.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-267">The **FolderPermissionLevel** is set to Custom only when you create a **FolderPermission** object and set individual permissions.</span></span> 
  
## <a name="adding-folder-permissions-by-using-ews"></a><span data-ttu-id="b8f9d-268">Adición de permisos de carpeta mediante EWS</span><span class="sxs-lookup"><span data-stu-id="b8f9d-268">Adding folder permissions by using EWS</span></span>
<span data-ttu-id="b8f9d-269"><a name="bk_enableews"> </a></span><span class="sxs-lookup"><span data-stu-id="b8f9d-269"><a name="bk_enableews"> </a></span></span>

<span data-ttu-id="b8f9d-270">Los siguientes ejemplos de código de EWS muestran cómo agregar permisos a una carpeta específica mediante la recuperación de los permisos actuales y el envío de una lista de nuevos permisos.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-270">The following EWS code examples show how to add permissions to a specific folder by retrieving the current permissions and then submitting a list of new permissions.</span></span>
  
<span data-ttu-id="b8f9d-271">El primer paso es enviar una solicitud [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) , donde el valor [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) especifica la carpeta en la que se van a agregar permisos (la carpeta elementos enviados en este ejemplo) y el valor [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) incluye Folder: PermissionSet.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-271">The first step is to send a [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request, where the [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) value specifies the folder in which to add permissions (the Sent Items folder in this example) and the [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) value includes folder:PermissionSet.</span></span> <span data-ttu-id="b8f9d-272">Esta solicitud recuperará la configuración de permisos para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-272">This request will retrieve the permission settings for the folder specified.</span></span> 
  
<span data-ttu-id="b8f9d-273">También es la solicitud XML que la API administrada de EWS envía cuando se llama al método **BIND** para [Agregar permisos de carpeta](#bk_enableewsma).</span><span class="sxs-lookup"><span data-stu-id="b8f9d-273">This is also the XML request that the EWS Managed API sends when you call the **Bind** method to [add folder permissions](#bk_enableewsma).</span></span>
  
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
      <m:GetFolder>
        <m:FolderShape>
          <t:BaseShape>IdOnly</t:BaseShape>
          <t:AdditionalProperties>
            <t:FieldURI FieldURI="folder:PermissionSet" />
          </t:AdditionalProperties>
        </m:FolderShape>
        <m:FolderIds>
          <t:DistinguishedFolderId Id="sentitems" />
        </m:FolderIds>
      </m:GetFolder>
    </soap:Body>
  </soap:Envelope>
```

<span data-ttu-id="b8f9d-274">El servidor responde a la solicitud **GetFolder** con un mensaje [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la carpeta se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-274">The server responds to the **GetFolder** request with a [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was retrieved successfully.</span></span> <span data-ttu-id="b8f9d-275">Los valores [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) y [ParentFolderId](https://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) se han abreviado por legibilidad.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-275">The [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) and [ParentFolderId](https://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) values have been shortened for readability.</span></span> 
  
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
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="CgAAAA=="
                          ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd1" />
              <t:PermissionSet>
                <t:Permissions>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Default</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                </t:Permissions>
              </t:PermissionSet>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="b8f9d-276">A continuación, use la operación **UpdateFolder** para enviar el [PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx)actualizado, que incluye el [permiso](https://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx) para el nuevo usuario.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-276">Next, use the **UpdateFolder** operation to send the updated [PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx), which includes the [Permission](https://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx) for the new user.</span></span> <span data-ttu-id="b8f9d-277">Tenga en cuenta que, si se incluye el elemento [SetFolderField](https://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx) para la carpeta respectiva en la operación [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) , se sobrescribirá toda la configuración de permisos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-277">Note that including the [SetFolderField](https://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx) element for the respective folder in the [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) operation will overwrite all the permission settings on the folder.</span></span> <span data-ttu-id="b8f9d-278">Del mismo modo, si se incluye la opción [DeleteFolderField](https://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx) de la operación **UpdateFolder** , también se eliminará la configuración de todos los permisos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-278">Likewise, including the [DeleteFolderField](https://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx) option of the **UpdateFolder** operation will also delete all the permission settings on the folder.</span></span> 
  
<span data-ttu-id="b8f9d-279">También es la solicitud XML que la API administrada de EWS envía cuando se llama al método **Update** para [Agregar permisos de carpeta](#bk_enableewsma).</span><span class="sxs-lookup"><span data-stu-id="b8f9d-279">This is also the XML request that the EWS Managed API sends when you call the **Update** method to [add folder permissions](#bk_enableewsma).</span></span>
  
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
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="CgAAAA=="
                      ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd1" />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:PermissionSet" />
              <t:Folder>
                <t:PermissionSet>
                  <t:Permissions>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Default</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
                      </t:UserId>
                      <t:PermissionLevel>Editor</t:PermissionLevel>
                    </t:Permission>
                  </t:Permissions>
                </t:PermissionSet>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b8f9d-280">La siguiente línea de código especifica el nivel de permisos.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-280">The following line of code specifies the permission level.</span></span>
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
    </t:UserId>
    <t:PermissionLevel>Editor</t:PermissionLevel>
</t:Permission>
```

<span data-ttu-id="b8f9d-281">Si desea usar el nivel de permisos personalizado, use este código en su lugar.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-281">If you want to use the custom permission level, use this code instead.</span></span>
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress> sadie@contoso.com </t:PrimarySmtpAddress>
    </t:UserId>
    <t:CanCreateItems>true</t:CanCreateItems>
    <t:CanCreateSubFolders>true</t:CanCreateSubFolders>
    <t:IsFolderOwner>false</t:IsFolderOwner>
    <t:IsFolderVisible>false</t:IsFolderVisible>
    <t:IsFolderContact>false</t:IsFolderContact>
    <t:EditItems>None</t:EditItems>
    <t:DeleteItems>None</t:DeleteItems>
    <t:ReadItems>None</t:ReadItems>
    <t:PermissionLevel>Custom</t:PermissionLevel>
</t:Permission>
```

<span data-ttu-id="b8f9d-282">El servidor responde a la solicitud **UpdateFolder** con un mensaje [UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) que incluye el valor de un elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la carpeta se actualizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-282">The server responds to the **UpdateFolder** request with an [UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was updated successfully.</span></span>
  
## <a name="removing-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="b8f9d-283">Eliminación de los permisos de carpeta mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="b8f9d-283">Removing folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="b8f9d-284"><a name="bk_removeewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b8f9d-284"><a name="bk_removeewsma"> </a></span></span>

<span data-ttu-id="b8f9d-285">En el siguiente ejemplo de código se muestra cómo usar la API administrada de EWS para quitar todos los permisos de usuario en una carpeta específica, excepto para los permisos predeterminados y anónimos, por:</span><span class="sxs-lookup"><span data-stu-id="b8f9d-285">The following code example shows how to use the EWS Managed API to remove all user permissions on a specific folder, except for the default and anonymous permissions, by:</span></span>
  
1. <span data-ttu-id="b8f9d-286">Obtener los permisos actuales para una carpeta mediante el método **BIND** .</span><span class="sxs-lookup"><span data-stu-id="b8f9d-286">Getting the current permissions for a folder by using the **Bind** method.</span></span> 
    
2. <span data-ttu-id="b8f9d-287">Recorrer en iteración la colección de **permisos** y quitar permisos para usuarios individuales.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-287">Iterating through the **Permissions** collection and removing permissions for individual users.</span></span> 
    
3. <span data-ttu-id="b8f9d-288">Llamar al método **Update** para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-288">Calling the **Update** method to save the changes.</span></span> 
    
<span data-ttu-id="b8f9d-289">En este ejemplo se quitan todos los permisos de usuario de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-289">This example removes all user permissions on a folder.</span></span> <span data-ttu-id="b8f9d-290">Si desea modificar este ejemplo para quitar permisos sólo para un usuario específico, cambie la siguiente línea de código para identificar el nombre para mostrar o la dirección SMTP del usuario.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-290">If you want to modify this example to remove permissions only for a specific user, change the following line of code to identify either the display name or SMTP address of the user.</span></span>
  
```cs
if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
```

<span data-ttu-id="b8f9d-291">En este ejemplo se supone que el **servicio** es un objeto [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el propietario del buzón y que el usuario se ha autenticado en un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-291">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
static void RemoveFolderPermissions(ExchangeService service)
{
    // Create a property set to use for folder binding.
    PropertySet propSet = new PropertySet(BasePropertySet.FirstClassProperties, FolderSchema.Permissions);
    // Bind to the folder and get the current permissions. 
    // This call results in a GetFolder call to EWS.
    Folder sentItemsFolder = Folder.Bind(service, new FolderId(WellKnownFolderName.SentItems, "primary@contoso.com"), propSet);
    // Iterate through the collection of permissions and remove permissions for any 
    // user with a display name or SMTP address. This leaves the anonymous and 
    // default user permissions unchanged. 
    if (sentItemsFolder.Permissions.Count != 0)
    {
        for (int t = 0; t < sentItemsFolder.Permissions.Count; t++)
        {
            // Find any permissions associated with the specified user and remove them from the DACL
            if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
            {
                sentItemsFolder.Permissions.Remove(sentItemsFolder.Permissions[t]);
            }
        }
    }
    // This call results in an UpdateFolder call to EWS.
    sentItemsFolder.Update();
}
```

## <a name="removing-folder-permissions-by-using-ews"></a><span data-ttu-id="b8f9d-292">Quitar permisos de carpeta mediante EWS</span><span class="sxs-lookup"><span data-stu-id="b8f9d-292">Removing folder permissions by using EWS</span></span>
<span data-ttu-id="b8f9d-293"><a name="bk_removeews"> </a></span><span class="sxs-lookup"><span data-stu-id="b8f9d-293"><a name="bk_removeews"> </a></span></span>

<span data-ttu-id="b8f9d-294">Los siguientes ejemplos de código de EWS muestran cómo quitar todos los permisos de usuario en una carpeta específica, excepto los permisos predeterminados y anónimos.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-294">The following EWS code examples show how to remove all user permissions on a specific folder, except for the default and anonymous permissions.</span></span>
  
<span data-ttu-id="b8f9d-295">En primer lugar, envíe una solicitud [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) donde el valor [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) especifica la carpeta en la que se van a quitar los permisos (la carpeta elementos enviados en este ejemplo) y el valor [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) incluye Folder: PermissionSet.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-295">First, send a [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request where the [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) value specifies the folder in which to remove permissions (the Sent Items folder in this example) and the [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) value includes folder:PermissionSet.</span></span> <span data-ttu-id="b8f9d-296">Esta solicitud recuperará el [PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx) para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-296">This request will retrieve the [PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx) for the folder specified.</span></span> 
  
<span data-ttu-id="b8f9d-297">También es la solicitud XML que la API administrada de EWS envía cuando se llama al método **BIND** para [quitar permisos de carpeta](#bk_removeewsma).</span><span class="sxs-lookup"><span data-stu-id="b8f9d-297">This is also the XML request that the EWS Managed API sends when you call the **Bind** method to [remove folder permissions](#bk_removeewsma).</span></span>
  
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
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:PermissionSet" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="drafts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b8f9d-298">El servidor responde a la solicitud **GetFolder** con un mensaje [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la carpeta se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-298">The server responds to the **GetFolder** request with a [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was retrieved successfully.</span></span> <span data-ttu-id="b8f9d-299">Los valores de los elementos **FolderId** y **ParentFolderId** se han abreviado para facilitar su lectura.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-299">The values of the **FolderId** and **ParentFolderId** elements have been shortened for readability.</span></span> 
  
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
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="EAAAAA=="
                          ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd5" />
              <t:ParentFolderId Id="CQAAAA=="
                                ChangeKey="AQAAAA==" />
              <t:FolderClass>IPF.Note</t:FolderClass>
              <t:DisplayName>Drafts</t:DisplayName>
              <t:TotalCount>0</t:TotalCount>
              <t:ChildFolderCount>0</t:ChildFolderCount>
              <t:EffectiveRights>
                <t:CreateAssociated>true</t:CreateAssociated>
                <t:CreateContents>true</t:CreateContents>
                <t:CreateHierarchy>true</t:CreateHierarchy>
                <t:Delete>true</t:Delete>
                <t:Modify>true</t:Modify>
                <t:Read>true</t:Read>
                <t:ViewPrivateItems>true</t:ViewPrivateItems>
              </t:EffectiveRights>
              <t:PermissionSet>
                <t:Permissions>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Default</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:SID>S-1-5-21-1337771579-694202782-848329751-1535223</t:SID>
                      <t:PrimarySmtpAddress>sadie@Contoso.com</t:PrimarySmtpAddress>
                      <t:DisplayName>Sadie Daniels</t:DisplayName>
                    </t:UserId>
                    <t:CanCreateItems>true</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>true</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>All</t:EditItems>
                    <t:DeleteItems>All</t:DeleteItems>
                    <t:ReadItems>FullDetails</t:ReadItems>
                    <t:PermissionLevel>Editor</t:PermissionLevel>
                  </t:Permission>
                </t:Permissions>
              </t:PermissionSet>
              <t:UnreadCount>0</t:UnreadCount>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="b8f9d-300">A continuación, use la operación **UpdateFolder** para enviar el **PermissionSet**actualizado, que no incluye el **permiso** para el usuario quitado.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-300">Next, use the **UpdateFolder** operation to send the updated **PermissionSet**, which does not include the **Permission** for the removed user.</span></span> 
  
<span data-ttu-id="b8f9d-301">También es la solicitud XML que la API administrada de EWS envía cuando se llama al método **Update** para [quitar los permisos de carpeta](#bk_removeewsma).</span><span class="sxs-lookup"><span data-stu-id="b8f9d-301">This is also the XML request that the EWS Managed API sends when you call the **Update** method to [remove folder permissions](#bk_removeewsma).</span></span>
  
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
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="EAAAAA=="
                      ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd5" />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:PermissionSet" />
              <t:Folder>
                <t:PermissionSet>
                  <t:Permissions>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Default</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                  </t:Permissions>
                </t:PermissionSet>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b8f9d-302">El servidor responde a la solicitud **UpdateFolder** con un mensaje **UpdateFolderResponse** que incluye un valor de elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la actualización se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-302">The server responds to the **UpdateFolder** request with an **UpdateFolderResponse** message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the update was successful.</span></span>
  
## <a name="updating-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="b8f9d-303">Actualización de permisos de carpeta mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="b8f9d-303">Updating folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="b8f9d-304"><a name="bk_updateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b8f9d-304"><a name="bk_updateewsma"> </a></span></span>

<span data-ttu-id="b8f9d-305">También puede actualizar los permisos de carpeta para una carpeta específica mediante la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-305">You can also update folder permissions for a specific folder by using the EWS Managed API.</span></span> <span data-ttu-id="b8f9d-306">Para actualizar los permisos:</span><span class="sxs-lookup"><span data-stu-id="b8f9d-306">To update the permissions:</span></span> 
  
1. <span data-ttu-id="b8f9d-307">[Quite los permisos de carpeta](#bk_removeewsma) para los permisos obsoletos, pero no llame al método **Update** (todavía).</span><span class="sxs-lookup"><span data-stu-id="b8f9d-307">[Remove the folder permissions](#bk_removeewsma) for the outdated permissions, but do not call the **Update** method (yet).</span></span> 
    
2. <span data-ttu-id="b8f9d-308">[Agregar permisos de carpeta para los usuarios nuevos o modificados](#bk_enableewsma).</span><span class="sxs-lookup"><span data-stu-id="b8f9d-308">[Add folder permissions for the new or changed users](#bk_enableewsma).</span></span>
    
3. <span data-ttu-id="b8f9d-309">Llame al método **Update** para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-309">Call the **Update** method to save the changes.</span></span> 
    
<span data-ttu-id="b8f9d-310">Si intenta agregar dos conjuntos de permisos para el mismo usuario, recibirá un error **ServiceResponseException** con la siguiente descripción: "el conjunto de permisos especificado contiene identificadores de usuario duplicados".</span><span class="sxs-lookup"><span data-stu-id="b8f9d-310">If you try to add two sets of permissions for the same user, you will receive a **ServiceResponseException** error with the following description: "The specified permission set contains duplicate UserIds".</span></span> <span data-ttu-id="b8f9d-311">En ese caso, quite los permisos actuales de la colección **Permission** y, a continuación, agregue los nuevos permisos a la colección **Permission** .</span><span class="sxs-lookup"><span data-stu-id="b8f9d-311">In that case, remove the current permissions from the **Permission** collection, then add the new permissions to the **Permission** collection.</span></span> 
  
## <a name="updating-folder-permissions-by-using-ews"></a><span data-ttu-id="b8f9d-312">Actualización de permisos de carpeta mediante EWS</span><span class="sxs-lookup"><span data-stu-id="b8f9d-312">Updating folder permissions by using EWS</span></span>
<span data-ttu-id="b8f9d-313"><a name="bk_updateews"> </a></span><span class="sxs-lookup"><span data-stu-id="b8f9d-313"><a name="bk_updateews"> </a></span></span>

<span data-ttu-id="b8f9d-314">También puede actualizar los permisos de carpeta para carpetas específicas usando EWS mediante la combinación del proceso de eliminación y adición.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-314">You can also update folder permissions for specific folders by using EWS by combining the removal and addition process.</span></span> <span data-ttu-id="b8f9d-315">Para actualizar los permisos:</span><span class="sxs-lookup"><span data-stu-id="b8f9d-315">To update the permissions:</span></span> 
  
1. <span data-ttu-id="b8f9d-316">Recupere los permisos actuales de la carpeta mediante la operación **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="b8f9d-316">Retrieve the folder's current permissions by using the **GetFolder** operation.</span></span> 
    
2. <span data-ttu-id="b8f9d-317">Envíe una lista actualizada de permisos mediante la operación **UpdateFolder** .</span><span class="sxs-lookup"><span data-stu-id="b8f9d-317">Send an updated list of permissions by using the **UpdateFolder** operation.</span></span> 
    
<span data-ttu-id="b8f9d-318">Estas son las mismas dos operaciones que se usan para [Habilitar](#bk_enableews) o [quitar el acceso](#bk_removeews) mediante EWS.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-318">These are the same two operations you use to [enable](#bk_enableews) or [remove access](#bk_removeews) by using EWS.</span></span> <span data-ttu-id="b8f9d-319">La única diferencia es que, cuando recibe la respuesta **GetFolder** , contendrá un conjunto de **permisos** para User.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-319">The only difference is that when you receive the **GetFolder** response, it will contain a **Permission** set for user.</span></span> <span data-ttu-id="b8f9d-320">Simplemente reemplace el elemento de **permiso** existente con el nuevo elemento **Permission** y, a continuación, envíe la operación **UpdateFolder** con el nuevo valor o valores de **permiso** .</span><span class="sxs-lookup"><span data-stu-id="b8f9d-320">Simply replace that existing **Permission** element with the new **Permission** element, and then send the **UpdateFolder** operation with the new **Permission** value or values.</span></span> 
  
<span data-ttu-id="b8f9d-321">Si intenta agregar dos conjuntos de permisos para el mismo usuario, recibirá un valor **ResponseCode** de **ErrorDuplicateUserIdsSpecified**.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-321">If you try to add two sets of permissions for the same user, you will receive a **ResponseCode** value of **ErrorDuplicateUserIdsSpecified**.</span></span> <span data-ttu-id="b8f9d-322">En ese caso, quite el valor de permiso obsoleto del usuario de la solicitud y, a continuación, vuelva a intentar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-322">In that case, remove the outdated Permission value for the user from the request and then retry the request.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b8f9d-323">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="b8f9d-323">Next steps</span></span>

<span data-ttu-id="b8f9d-324">Después de conceder a un usuario permiso para una carpeta específica, el usuario puede tener acceso a la carpeta como delegado.</span><span class="sxs-lookup"><span data-stu-id="b8f9d-324">After you give a user permission to a specific folder, the user can access the folder as a delegate.</span></span> <span data-ttu-id="b8f9d-325">Para más información, consulte lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b8f9d-325">For more information, see:</span></span>
  
- [<span data-ttu-id="b8f9d-326">Obtener acceso al correo electrónico como delegado mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b8f9d-326">Access email as a delegate by using EWS in Exchange</span></span>](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="b8f9d-327">Obtener acceso a un calendario como delegado mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b8f9d-327">Access a calendar as a delegate by using EWS in Exchange</span></span>](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="b8f9d-328">Obtener acceso a los contactos como un delegado mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b8f9d-328">Access contacts as a delegate by using EWS in Exchange</span></span>](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="b8f9d-329">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8f9d-329">See also</span></span>

- [<span data-ttu-id="b8f9d-330">Acceso delegado y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b8f9d-330">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)   
- [<span data-ttu-id="b8f9d-331">Agregar y quitar delegados mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b8f9d-331">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="b8f9d-332">Carpetas y elementos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b8f9d-332">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    

