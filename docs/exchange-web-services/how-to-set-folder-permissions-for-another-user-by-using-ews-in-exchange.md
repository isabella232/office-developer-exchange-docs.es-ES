---
title: Establecer permisos de carpeta de otro usuario mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb81676-a780-4c56-b4f2-c4ed2697107d
description: Obtenga información sobre cómo establecer los niveles de permisos en una carpeta mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 5bf570612d6349628e7f3abf858daa33daa13745
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763178"
---
# <a name="set-folder-permissions-for-another-user-by-using-ews-in-exchange"></a><span data-ttu-id="1734b-103">Establecer permisos de carpeta de otro usuario mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1734b-103">Set folder permissions for another user by using EWS in Exchange</span></span>

<span data-ttu-id="1734b-104">Obtenga información sobre cómo establecer los niveles de permisos en una carpeta mediante el uso de la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="1734b-104">Learn how to set permission levels on a folder by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="1734b-105">Permisos de nivel de carpeta permiten a los usuarios tener acceso a una o varias carpetas en el buzón de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="1734b-105">Folder-level permissions enable users to access one or more folders in another user's mailbox.</span></span> <span data-ttu-id="1734b-106">Permisos de carpeta son similares a la delegación de acceso, pero se diferencian de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="1734b-106">Folder permissions are similar to delegate access, but they differ in the following ways:</span></span> 
  
- <span data-ttu-id="1734b-107">Permisos de carpeta no habilitar a un usuario para "enviar en nombre de" o "Enviar como" otro usuario.</span><span class="sxs-lookup"><span data-stu-id="1734b-107">Folder permissions do not enable a user to "send on behalf of" or "send as" another user.</span></span> <span data-ttu-id="1734b-108">Sólo permiten el acceso a las carpetas.</span><span class="sxs-lookup"><span data-stu-id="1734b-108">They only enable access to folders.</span></span> <span data-ttu-id="1734b-109">Los usuarios pueden crear elementos en esas carpetas, pero no puede enviarlos.</span><span class="sxs-lookup"><span data-stu-id="1734b-109">Users can create items in those folders, but they can't send them.</span></span>
    
- <span data-ttu-id="1734b-110">Puede establecer permisos de carpetas en cualquier carpeta en el buzón de correo, pero sólo se puede agregar a un delegado a las carpetas de calendario, contactos, Bandeja de entrada, diario, notas y tareas.</span><span class="sxs-lookup"><span data-stu-id="1734b-110">You can set folder permissions on any folder in the mailbox, but you can only add a delegate to the Calendar, Contacts, Inbox, Journal, Notes, and Tasks folders.</span></span>
    
- <span data-ttu-id="1734b-111">Puede establecer un número de [permisos en una carpeta específica](#bk_folderperms).</span><span class="sxs-lookup"><span data-stu-id="1734b-111">You can set a number of [permissions on a specific folder](#bk_folderperms).</span></span> <span data-ttu-id="1734b-112">Cuando se agrega un delegado, puede asignar uno de sólo [cinco niveles de permisos](delegate-access-and-ews-in-exchange.md#bk_delegateperms).</span><span class="sxs-lookup"><span data-stu-id="1734b-112">When you add a delegate, you can assign one of only [five permission levels](delegate-access-and-ews-in-exchange.md#bk_delegateperms).</span></span>
    
- <span data-ttu-id="1734b-113">Puede establecer los permisos de carpeta anónimo y establecer como predeterminado a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="1734b-113">You can set folder permissions for anonymous and default users.</span></span> <span data-ttu-id="1734b-114">Sólo puede conceder acceso de delegado a una cuenta habilitada para correo.</span><span class="sxs-lookup"><span data-stu-id="1734b-114">You can only grant delegate access to a mail-enabled account.</span></span>
    
<span data-ttu-id="1734b-115">Si está familiarizado con entradas de Control de acceso (ACE) y listas de Control de acceso discrecional (DACL), sabrá que un usuario sólo puede tener un conjunto de permisos para cada carpeta.</span><span class="sxs-lookup"><span data-stu-id="1734b-115">If you're familiar with Access Control Entries (ACEs) and Discretionary Access Control Lists (DACLs), you know that a user can only have one set of permissions for each folder.</span></span> <span data-ttu-id="1734b-116">Si intenta agregar un conjunto de permisos para un usuario y ya tienen un conjunto de permisos, obtendrá un error.</span><span class="sxs-lookup"><span data-stu-id="1734b-116">If you try to add a set of permissions for a user and they already have a set of permissions, you'll get an error.</span></span> <span data-ttu-id="1734b-117">Al agregar, quitar o actualizar los permisos en una carpeta, que obtener la DACL actual, agrega o quita cualquier ACE y, a continuación, enviar la DACL actualizada.</span><span class="sxs-lookup"><span data-stu-id="1734b-117">When you add, remove, or update permissions on a folder, you get the current DACL, add or remove any ACEs, and then send the updated DACL.</span></span> <span data-ttu-id="1734b-118">No se puede agregar varias entradas ACE para el mismo usuario.</span><span class="sxs-lookup"><span data-stu-id="1734b-118">You cannot add multiple ACEs for the same user.</span></span> <span data-ttu-id="1734b-119">Al actualizar los permisos mediante el uso de la API administrada de EWS, debe quitar la ACE actual del usuario y, a continuación, agregar su nueva ACE a la colección.</span><span class="sxs-lookup"><span data-stu-id="1734b-119">When you update permissions by using the EWS Managed API, you need to remove the user's current ACE and then add their new ACE to the collection.</span></span> <span data-ttu-id="1734b-120">Si está usando EWS, solo tendrá que cambiar el conjunto de las entradas ACE anterior con los nuevos.</span><span class="sxs-lookup"><span data-stu-id="1734b-120">If you're using EWS, you just replace the previous set of ACEs with the new ones.</span></span>
  
<span data-ttu-id="1734b-121">Si está realizando varios cambios en los permisos para una sola carpeta, puede procesar por lotes las adiciones, eliminaciones o actualizaciones, tenga en cuenta que no se puede procesar por lotes las actualizaciones del usuario en varias carpetas.</span><span class="sxs-lookup"><span data-stu-id="1734b-121">If you're making multiple permission changes to a single folder, you can batch additions, removals, or updates —just note that you cannot batch user updates on multiple folders.</span></span> <span data-ttu-id="1734b-122">Es necesaria una llamada para obtener los permisos en una sola carpeta, y una segunda llamada es necesario para actualizar los permisos en esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="1734b-122">One call is required to get the permissions on a single folder, and a second call is required to update the permissions on that folder.</span></span> <span data-ttu-id="1734b-123">Al agregar, quitar o actualizar los permisos de usuario, se utiliza el mismo dos llamadas al método u operaciones para cada tarea.</span><span class="sxs-lookup"><span data-stu-id="1734b-123">When you add, remove, or update user permissions, you use the same two method calls or operations for each task.</span></span>
  
<span data-ttu-id="1734b-124">**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para establecer los permisos de carpeta**</span><span class="sxs-lookup"><span data-stu-id="1734b-124">**Table 1. EWS Managed API methods and EWS operations for setting folder permissions**</span></span>

|<span data-ttu-id="1734b-125">Si quiere...</span><span class="sxs-lookup"><span data-stu-id="1734b-125">If you want to…</span></span>|<span data-ttu-id="1734b-126">Use este método de la API administrada de EWS...</span><span class="sxs-lookup"><span data-stu-id="1734b-126">Use this EWS Managed API method…</span></span>|<span data-ttu-id="1734b-127">Use esta operación de EWS...</span><span class="sxs-lookup"><span data-stu-id="1734b-127">Use this EWS operation…</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1734b-128">Habilitar, quitar o actualizar los permisos de carpeta</span><span class="sxs-lookup"><span data-stu-id="1734b-128">Enable, remove, or update folder permissions</span></span>  <br/> |<span data-ttu-id="1734b-129">[Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) seguido de [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1734b-129">[Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) followed by [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="1734b-130">[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) seguido [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1734b-130">[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) followed by [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="1734b-131">Cree una carpeta y definir los permisos de carpeta</span><span class="sxs-lookup"><span data-stu-id="1734b-131">Create a folder and define folder permissions</span></span>  <br/> |[<span data-ttu-id="1734b-132">Folder.Save</span><span class="sxs-lookup"><span data-stu-id="1734b-132">Folder.Save</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="1734b-133">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="1734b-133">CreateFolder</span></span>](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
   
## <a name="folder-permissions"></a><span data-ttu-id="1734b-134">Permisos de carpeta</span><span class="sxs-lookup"><span data-stu-id="1734b-134">Folder permissions</span></span>
<span data-ttu-id="1734b-135"><a name="bk_folderperms"> </a></span><span class="sxs-lookup"><span data-stu-id="1734b-135"></span></span>

<span data-ttu-id="1734b-136">Tener unas cuantas opciones cuando se trata de establecer los permisos de carpeta en una carpeta específica.</span><span class="sxs-lookup"><span data-stu-id="1734b-136">You have quite a few options when it comes to setting folder permissions on a specific folder.</span></span> <span data-ttu-id="1734b-137">Puede establecer un nivel de permisos en una carpeta para cada usuario, que agrega un conjunto de permisos individuales predefinidos a la DACL, o puede establecer los permisos individuales en una carpeta, pero no puede mezclar y match.</span><span class="sxs-lookup"><span data-stu-id="1734b-137">You can set a permission level on a folder for each user, which adds a set of predefined individual permissions to the DACL, or you can set individual permissions on a folder — but you can't mix and match.</span></span>
  
<span data-ttu-id="1734b-138">Los siguientes permisos individuales están disponibles:</span><span class="sxs-lookup"><span data-stu-id="1734b-138">The following individual permissions are available:</span></span>
  
- <span data-ttu-id="1734b-139">Puede crear</span><span class="sxs-lookup"><span data-stu-id="1734b-139">Can create</span></span>
- <span data-ttu-id="1734b-140">Puede crear subcarpetas</span><span class="sxs-lookup"><span data-stu-id="1734b-140">Can create subfolders</span></span>    
- <span data-ttu-id="1734b-141">Es propietario de la carpeta</span><span class="sxs-lookup"><span data-stu-id="1734b-141">Is folder owner</span></span>    
- <span data-ttu-id="1734b-142">Es la carpeta visible</span><span class="sxs-lookup"><span data-stu-id="1734b-142">Is folder visible</span></span>    
- <span data-ttu-id="1734b-143">Es el contacto de carpeta</span><span class="sxs-lookup"><span data-stu-id="1734b-143">Is folder contact</span></span>    
- <span data-ttu-id="1734b-144">Editar elementos</span><span class="sxs-lookup"><span data-stu-id="1734b-144">Edit items</span></span>    
- <span data-ttu-id="1734b-145">Eliminar elementos</span><span class="sxs-lookup"><span data-stu-id="1734b-145">Delete items</span></span>    
- <span data-ttu-id="1734b-146">Leer elementos</span><span class="sxs-lookup"><span data-stu-id="1734b-146">Read items</span></span>
    
<span data-ttu-id="1734b-147">Además, los siguientes niveles de permisos están disponibles, que definen un subconjunto de permisos individuales y los valores, como se muestra en la tabla 2:</span><span class="sxs-lookup"><span data-stu-id="1734b-147">In addition, the following permission levels are available, which define a subset of individual permissions and values, as shown in Table 2:</span></span>
  
- <span data-ttu-id="1734b-148">None</span><span class="sxs-lookup"><span data-stu-id="1734b-148">None</span></span>    
- <span data-ttu-id="1734b-149">Owner</span><span class="sxs-lookup"><span data-stu-id="1734b-149">Owner</span></span>    
- <span data-ttu-id="1734b-150">PublishingEditor</span><span class="sxs-lookup"><span data-stu-id="1734b-150">PublishingEditor</span></span>    
- <span data-ttu-id="1734b-151">Editor</span><span class="sxs-lookup"><span data-stu-id="1734b-151">Editor</span></span>    
- <span data-ttu-id="1734b-152">PublishingAuthor</span><span class="sxs-lookup"><span data-stu-id="1734b-152">PublishingAuthor</span></span>    
- <span data-ttu-id="1734b-153">Autor</span><span class="sxs-lookup"><span data-stu-id="1734b-153">Author</span></span>    
- <span data-ttu-id="1734b-154">NoneditingAuthor</span><span class="sxs-lookup"><span data-stu-id="1734b-154">NoneditingAuthor</span></span>    
- <span data-ttu-id="1734b-155">Reviewer</span><span class="sxs-lookup"><span data-stu-id="1734b-155">Reviewer</span></span>    
- <span data-ttu-id="1734b-156">Colaborador</span><span class="sxs-lookup"><span data-stu-id="1734b-156">Contributor</span></span>   
- <span data-ttu-id="1734b-157">Personalizado - no se puede establecer este valor por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1734b-157">Custom - This value cannot be set by the application.</span></span> <span data-ttu-id="1734b-158">El servidor establece este valor si la aplicación incluye una colección personalizada de permisos individuales.</span><span class="sxs-lookup"><span data-stu-id="1734b-158">The server sets this value if the application includes a custom collection of individual permissions.</span></span>    
- <span data-ttu-id="1734b-159">FreeBusyTimeOnly - esto sólo se puede establecer en las carpetas de calendario.</span><span class="sxs-lookup"><span data-stu-id="1734b-159">FreeBusyTimeOnly - This can only be set on Calendar folders.</span></span>   
- <span data-ttu-id="1734b-160">FreeBusyTimeAndSubjectAndLocation - esto sólo se puede establecer en las carpetas de calendario.</span><span class="sxs-lookup"><span data-stu-id="1734b-160">FreeBusyTimeAndSubjectAndLocation - This can only be set on Calendar folders.</span></span>
    
<span data-ttu-id="1734b-161">En la siguiente tabla muestra qué permisos individuales se aplican de forma predeterminada según el nivel de permisos.</span><span class="sxs-lookup"><span data-stu-id="1734b-161">The following table shows which individual permissions are applied by default based on permission level.</span></span>
  
<span data-ttu-id="1734b-162">**Tabla 2. Permisos individuales por nivel de permisos**</span><span class="sxs-lookup"><span data-stu-id="1734b-162">**Table 2. Individual permissions by permission level**</span></span>

|<span data-ttu-id="1734b-163">Nivel de permisos</span><span class="sxs-lookup"><span data-stu-id="1734b-163">Permission level</span></span>|<span data-ttu-id="1734b-164">Puede crear los elementos</span><span class="sxs-lookup"><span data-stu-id="1734b-164">Can create items</span></span>|<span data-ttu-id="1734b-165">Puede crear carpetas de sub</span><span class="sxs-lookup"><span data-stu-id="1734b-165">Can create sub folders</span></span>|<span data-ttu-id="1734b-166">Es propietario de la carpeta</span><span class="sxs-lookup"><span data-stu-id="1734b-166">Is folder owner</span></span>|<span data-ttu-id="1734b-167">Es la carpeta visible</span><span class="sxs-lookup"><span data-stu-id="1734b-167">Is folder visible</span></span>|<span data-ttu-id="1734b-168">Es el contacto de carpeta</span><span class="sxs-lookup"><span data-stu-id="1734b-168">Is folder contact</span></span>|<span data-ttu-id="1734b-169">Editar elementos</span><span class="sxs-lookup"><span data-stu-id="1734b-169">Edit items</span></span>|<span data-ttu-id="1734b-170">Eliminar elementos</span><span class="sxs-lookup"><span data-stu-id="1734b-170">Delete items</span></span>|<span data-ttu-id="1734b-171">Puede leer elementos</span><span class="sxs-lookup"><span data-stu-id="1734b-171">Can read items</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1734b-172">None</span><span class="sxs-lookup"><span data-stu-id="1734b-172">None</span></span>  <br/> |<span data-ttu-id="1734b-173">False</span><span class="sxs-lookup"><span data-stu-id="1734b-173">False</span></span>  <br/> |<span data-ttu-id="1734b-174">False</span><span class="sxs-lookup"><span data-stu-id="1734b-174">False</span></span>  <br/> |<span data-ttu-id="1734b-175">False</span><span class="sxs-lookup"><span data-stu-id="1734b-175">False</span></span>  <br/> |<span data-ttu-id="1734b-176">False</span><span class="sxs-lookup"><span data-stu-id="1734b-176">False</span></span>  <br/> |<span data-ttu-id="1734b-177">False</span><span class="sxs-lookup"><span data-stu-id="1734b-177">False</span></span>  <br/> |<span data-ttu-id="1734b-178">None</span><span class="sxs-lookup"><span data-stu-id="1734b-178">None</span></span>  <br/> |<span data-ttu-id="1734b-179">None</span><span class="sxs-lookup"><span data-stu-id="1734b-179">None</span></span>  <br/> |<span data-ttu-id="1734b-180">None</span><span class="sxs-lookup"><span data-stu-id="1734b-180">None</span></span>  <br/> |
|<span data-ttu-id="1734b-181">Owner</span><span class="sxs-lookup"><span data-stu-id="1734b-181">Owner</span></span>  <br/> |<span data-ttu-id="1734b-182">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-182">True</span></span>  <br/> |<span data-ttu-id="1734b-183">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-183">True</span></span>  <br/> |<span data-ttu-id="1734b-184">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-184">True</span></span>  <br/> |<span data-ttu-id="1734b-185">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-185">True</span></span>  <br/> |<span data-ttu-id="1734b-186">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-186">True</span></span>  <br/> |<span data-ttu-id="1734b-187">Todos</span><span class="sxs-lookup"><span data-stu-id="1734b-187">All</span></span>  <br/> |<span data-ttu-id="1734b-188">Todos</span><span class="sxs-lookup"><span data-stu-id="1734b-188">All</span></span>  <br/> |<span data-ttu-id="1734b-189">FullDetails</span><span class="sxs-lookup"><span data-stu-id="1734b-189">FullDetails</span></span>  <br/> |
|<span data-ttu-id="1734b-190">PublishingEditor</span><span class="sxs-lookup"><span data-stu-id="1734b-190">PublishingEditor</span></span>  <br/> |<span data-ttu-id="1734b-191">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-191">True</span></span>  <br/> |<span data-ttu-id="1734b-192">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-192">True</span></span>  <br/> |<span data-ttu-id="1734b-193">False</span><span class="sxs-lookup"><span data-stu-id="1734b-193">False</span></span>  <br/> |<span data-ttu-id="1734b-194">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-194">True</span></span>  <br/> |<span data-ttu-id="1734b-195">False</span><span class="sxs-lookup"><span data-stu-id="1734b-195">False</span></span>  <br/> |<span data-ttu-id="1734b-196">Todos</span><span class="sxs-lookup"><span data-stu-id="1734b-196">All</span></span>  <br/> |<span data-ttu-id="1734b-197">Todos</span><span class="sxs-lookup"><span data-stu-id="1734b-197">All</span></span>  <br/> |<span data-ttu-id="1734b-198">FullDetails</span><span class="sxs-lookup"><span data-stu-id="1734b-198">FullDetails</span></span>  <br/> |
|<span data-ttu-id="1734b-199">Editor</span><span class="sxs-lookup"><span data-stu-id="1734b-199">Editor</span></span>  <br/> |<span data-ttu-id="1734b-200">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-200">True</span></span>  <br/> |<span data-ttu-id="1734b-201">False</span><span class="sxs-lookup"><span data-stu-id="1734b-201">False</span></span>  <br/> |<span data-ttu-id="1734b-202">False</span><span class="sxs-lookup"><span data-stu-id="1734b-202">False</span></span>  <br/> |<span data-ttu-id="1734b-203">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-203">True</span></span>  <br/> |<span data-ttu-id="1734b-204">False</span><span class="sxs-lookup"><span data-stu-id="1734b-204">False</span></span>  <br/> |<span data-ttu-id="1734b-205">Todos</span><span class="sxs-lookup"><span data-stu-id="1734b-205">All</span></span>  <br/> |<span data-ttu-id="1734b-206">Todos</span><span class="sxs-lookup"><span data-stu-id="1734b-206">All</span></span>  <br/> |<span data-ttu-id="1734b-207">FullDetails</span><span class="sxs-lookup"><span data-stu-id="1734b-207">FullDetails</span></span>  <br/> |
|<span data-ttu-id="1734b-208">PublishingAuthor</span><span class="sxs-lookup"><span data-stu-id="1734b-208">PublishingAuthor</span></span>  <br/> |<span data-ttu-id="1734b-209">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-209">True</span></span>  <br/> |<span data-ttu-id="1734b-210">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-210">True</span></span>  <br/> |<span data-ttu-id="1734b-211">False</span><span class="sxs-lookup"><span data-stu-id="1734b-211">False</span></span>  <br/> |<span data-ttu-id="1734b-212">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-212">True</span></span>  <br/> |<span data-ttu-id="1734b-213">False</span><span class="sxs-lookup"><span data-stu-id="1734b-213">False</span></span>  <br/> |<span data-ttu-id="1734b-214">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1734b-214">Owned</span></span>  <br/> |<span data-ttu-id="1734b-215">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1734b-215">Owned</span></span>  <br/> |<span data-ttu-id="1734b-216">FullDetails</span><span class="sxs-lookup"><span data-stu-id="1734b-216">FullDetails</span></span>  <br/> |
|<span data-ttu-id="1734b-217">Autor</span><span class="sxs-lookup"><span data-stu-id="1734b-217">Author</span></span>  <br/> |<span data-ttu-id="1734b-218">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-218">True</span></span>  <br/> |<span data-ttu-id="1734b-219">False</span><span class="sxs-lookup"><span data-stu-id="1734b-219">False</span></span>  <br/> |<span data-ttu-id="1734b-220">False</span><span class="sxs-lookup"><span data-stu-id="1734b-220">False</span></span>  <br/> |<span data-ttu-id="1734b-221">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-221">True</span></span>  <br/> |<span data-ttu-id="1734b-222">False</span><span class="sxs-lookup"><span data-stu-id="1734b-222">False</span></span>  <br/> |<span data-ttu-id="1734b-223">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1734b-223">Owned</span></span>  <br/> |<span data-ttu-id="1734b-224">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1734b-224">Owned</span></span>  <br/> |<span data-ttu-id="1734b-225">FullDetails</span><span class="sxs-lookup"><span data-stu-id="1734b-225">FullDetails</span></span>  <br/> |
|<span data-ttu-id="1734b-226">NoneditingAuthor</span><span class="sxs-lookup"><span data-stu-id="1734b-226">NoneditingAuthor</span></span>  <br/> |<span data-ttu-id="1734b-227">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-227">True</span></span>  <br/> |<span data-ttu-id="1734b-228">False</span><span class="sxs-lookup"><span data-stu-id="1734b-228">False</span></span>  <br/> |<span data-ttu-id="1734b-229">False</span><span class="sxs-lookup"><span data-stu-id="1734b-229">False</span></span>  <br/> |<span data-ttu-id="1734b-230">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-230">True</span></span>  <br/> |<span data-ttu-id="1734b-231">False</span><span class="sxs-lookup"><span data-stu-id="1734b-231">False</span></span>  <br/> |<span data-ttu-id="1734b-232">None</span><span class="sxs-lookup"><span data-stu-id="1734b-232">None</span></span>  <br/> |<span data-ttu-id="1734b-233">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1734b-233">Owned</span></span>  <br/> |<span data-ttu-id="1734b-234">FullDetails</span><span class="sxs-lookup"><span data-stu-id="1734b-234">FullDetails</span></span>  <br/> |
|<span data-ttu-id="1734b-235">Reviewer</span><span class="sxs-lookup"><span data-stu-id="1734b-235">Reviewer</span></span>  <br/> |<span data-ttu-id="1734b-236">False</span><span class="sxs-lookup"><span data-stu-id="1734b-236">False</span></span>  <br/> |<span data-ttu-id="1734b-237">False</span><span class="sxs-lookup"><span data-stu-id="1734b-237">False</span></span>  <br/> |<span data-ttu-id="1734b-238">False</span><span class="sxs-lookup"><span data-stu-id="1734b-238">False</span></span>  <br/> |<span data-ttu-id="1734b-239">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-239">True</span></span>  <br/> |<span data-ttu-id="1734b-240">False</span><span class="sxs-lookup"><span data-stu-id="1734b-240">False</span></span>  <br/> |<span data-ttu-id="1734b-241">None</span><span class="sxs-lookup"><span data-stu-id="1734b-241">None</span></span>  <br/> |<span data-ttu-id="1734b-242">None</span><span class="sxs-lookup"><span data-stu-id="1734b-242">None</span></span>  <br/> |<span data-ttu-id="1734b-243">FullDetails</span><span class="sxs-lookup"><span data-stu-id="1734b-243">FullDetails</span></span>  <br/> |
|<span data-ttu-id="1734b-244">Colaborador</span><span class="sxs-lookup"><span data-stu-id="1734b-244">Contributor</span></span>  <br/> |<span data-ttu-id="1734b-245">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-245">True</span></span>  <br/> |<span data-ttu-id="1734b-246">False</span><span class="sxs-lookup"><span data-stu-id="1734b-246">False</span></span>  <br/> |<span data-ttu-id="1734b-247">False</span><span class="sxs-lookup"><span data-stu-id="1734b-247">False</span></span>  <br/> |<span data-ttu-id="1734b-248">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1734b-248">True</span></span>  <br/> |<span data-ttu-id="1734b-249">False</span><span class="sxs-lookup"><span data-stu-id="1734b-249">False</span></span>  <br/> |<span data-ttu-id="1734b-250">None</span><span class="sxs-lookup"><span data-stu-id="1734b-250">None</span></span>  <br/> |<span data-ttu-id="1734b-251">None</span><span class="sxs-lookup"><span data-stu-id="1734b-251">None</span></span>  <br/> |<span data-ttu-id="1734b-252">None</span><span class="sxs-lookup"><span data-stu-id="1734b-252">None</span></span>  <br/> |
   
<span data-ttu-id="1734b-253">Si especifica un nivel de permisos no personalizada en la solicitud de permisos de nivel de carpeta, no es necesario especificar la configuración de permisos individuales.</span><span class="sxs-lookup"><span data-stu-id="1734b-253">If you specify a non-custom permission level in the folder-level permissions request, you don't need to specify the individual permission settings.</span></span> <span data-ttu-id="1734b-254">Si especifica un permiso individual cuando se establece un nivel de permisos, se devolverá un error de **ErrorInvalidPermissionSettings** en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1734b-254">If you do specify an individual permission when you set a permission level, an **ErrorInvalidPermissionSettings** error will be returned in the response.</span></span> 
  
## <a name="adding-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="1734b-255">Adición de permisos de carpeta mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="1734b-255">Adding folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="1734b-256"><a name="bk_enableewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="1734b-256"></span></span>

<span data-ttu-id="1734b-257">En el ejemplo de código siguiente se muestra cómo usar la API administrada de EWS para:</span><span class="sxs-lookup"><span data-stu-id="1734b-257">The following code example shows how to use the EWS Managed API to:</span></span> 
  
- <span data-ttu-id="1734b-258">Crear un nuevo objeto [FolderPermission](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx) para el nuevo usuario.</span><span class="sxs-lookup"><span data-stu-id="1734b-258">Create a new [FolderPermission](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx) object for the new user.</span></span> 
    
- <span data-ttu-id="1734b-259">Obtenga los permisos para una carpeta actuales mediante el método [enlazar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1734b-259">Get the current permissions for a folder by using the [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method.</span></span> 
    
- <span data-ttu-id="1734b-260">Agregue el nuevo **FolderPermissions** a la propiedad [Folder.Permissions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1734b-260">Add the new **FolderPermissions** to the [Folder.Permissions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx) property.</span></span> 
    
- <span data-ttu-id="1734b-261">Llame al método [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) para guardar los nuevos permisos en el servidor.</span><span class="sxs-lookup"><span data-stu-id="1734b-261">Call the [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) method to save the new permissions to the server.</span></span> 
    
<span data-ttu-id="1734b-262">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el propietario del buzón y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1734b-262">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner and that the user has been authenticated to an Exchange server.</span></span> 
  
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

<span data-ttu-id="1734b-263">La siguiente línea de código, especifica el nivel de permisos.</span><span class="sxs-lookup"><span data-stu-id="1734b-263">The following line of code specifies the permission level.</span></span>
  
```cs
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
```

<span data-ttu-id="1734b-264">Si desea usar el nivel de permisos personalizados, use este código en su lugar.</span><span class="sxs-lookup"><span data-stu-id="1734b-264">If you want to use the custom permission level, use this code instead.</span></span>
  
```cs
FolderPermission fldperm = new FolderPermission();
fldperm.UserId = "sadie@Contoso1000.onmicrosoft.com";
fldperm.CanCreateItems = true;
fldperm.CanCreateSubFolders = true;
…
```

<span data-ttu-id="1734b-265">Puede establecer cualquiera o todas las [Propiedades FolderPermission](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx) de escritura cuando se crea un objeto **FolderPermission** con un nivel de permisos personalizados.</span><span class="sxs-lookup"><span data-stu-id="1734b-265">You can set any or all of the writable [FolderPermission properties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx) when you create a **FolderPermission** object with a custom permission level.</span></span> <span data-ttu-id="1734b-266">Sin embargo, tenga en cuenta que el [FolderPermissionLevel](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx) nunca de forma explícita está establecida en **Custom** por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1734b-266">Note, however, that the [FolderPermissionLevel](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx) is never explicitly set to **Custom** by the application.</span></span> <span data-ttu-id="1734b-267">El **FolderPermissionLevel** está establecida en Custom sólo cuando cree un objeto **FolderPermission** y establecer permisos individuales.</span><span class="sxs-lookup"><span data-stu-id="1734b-267">The **FolderPermissionLevel** is set to Custom only when you create a **FolderPermission** object and set individual permissions.</span></span> 
  
## <a name="adding-folder-permissions-by-using-ews"></a><span data-ttu-id="1734b-268">Adición de permisos de carpeta mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="1734b-268">Adding folder permissions by using EWS</span></span>
<span data-ttu-id="1734b-269"><a name="bk_enableews"> </a></span><span class="sxs-lookup"><span data-stu-id="1734b-269"></span></span>

<span data-ttu-id="1734b-270">Los siguientes ejemplos de código EWS muestran cómo agregar permisos a una carpeta específica por recuperar los permisos actuales y, a continuación, enviar una lista de nuevos permisos.</span><span class="sxs-lookup"><span data-stu-id="1734b-270">The following EWS code examples show how to add permissions to a specific folder by retrieving the current permissions and then submitting a list of new permissions.</span></span>
  
<span data-ttu-id="1734b-271">El primer paso es enviar una solicitud de [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) , donde el valor [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) especifica la carpeta en la que se va a agregar permisos (la carpeta Elementos enviados en este ejemplo) y el valor de [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) incluye: conjunto de permisos de carpeta.</span><span class="sxs-lookup"><span data-stu-id="1734b-271">The first step is to send a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request, where the [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) value specifies the folder in which to add permissions (the Sent Items folder in this example) and the [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) value includes folder:PermissionSet.</span></span> <span data-ttu-id="1734b-272">Esta solicitud recupera la configuración de permisos para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="1734b-272">This request will retrieve the permission settings for the folder specified.</span></span> 
  
<span data-ttu-id="1734b-273">También es la solicitud XML que la API administrada de EWS envía cuando se llama al método **enlazar** para [Agregar permisos de carpeta](#bk_enableewsma).</span><span class="sxs-lookup"><span data-stu-id="1734b-273">This is also the XML request that the EWS Managed API sends when you call the **Bind** method to [add folder permissions](#bk_enableewsma).</span></span>
  
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

<span data-ttu-id="1734b-274">El servidor responde a la solicitud de **GetFolder** con un mensaje de [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la carpeta se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1734b-274">The server responds to the **GetFolder** request with a [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was retrieved successfully.</span></span> <span data-ttu-id="1734b-275">Los valores de [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) e [ID](http://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="1734b-275">The [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) and [ParentFolderId](http://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) values have been shortened for readability.</span></span> 
  
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
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="1734b-276">A continuación, use la operación **UpdateFolder** para enviar el actualizado [PermissionSet](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx), que incluye el [permiso](http://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx) para el nuevo usuario.</span><span class="sxs-lookup"><span data-stu-id="1734b-276">Next, use the **UpdateFolder** operation to send the updated [PermissionSet](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx), which includes the [Permission](http://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx) for the new user.</span></span> <span data-ttu-id="1734b-277">Tenga en cuenta que incluido el elemento [SetFolderField](http://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx) para la carpeta respectivo en la operación de [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) sobrescribirá todas las configuraciones de permisos en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="1734b-277">Note that including the [SetFolderField](http://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx) element for the respective folder in the [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) operation will overwrite all the permission settings on the folder.</span></span> <span data-ttu-id="1734b-278">Del mismo modo, incluida la opción [DeleteFolderField](http://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx) de la operación **UpdateFolder** , se eliminan también todas las configuraciones de permisos en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="1734b-278">Likewise, including the [DeleteFolderField](http://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx) option of the **UpdateFolder** operation will also delete all the permission settings on the folder.</span></span> 
  
<span data-ttu-id="1734b-279">También es la solicitud XML que la API administrada de EWS envía al llamar al método **Update** para [Agregar permisos de carpeta](#bk_enableewsma).</span><span class="sxs-lookup"><span data-stu-id="1734b-279">This is also the XML request that the EWS Managed API sends when you call the **Update** method to [add folder permissions](#bk_enableewsma).</span></span>
  
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

<span data-ttu-id="1734b-280">La siguiente línea de código, especifica el nivel de permisos.</span><span class="sxs-lookup"><span data-stu-id="1734b-280">The following line of code specifies the permission level.</span></span>
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
    </t:UserId>
    <t:PermissionLevel>Editor</t:PermissionLevel>
</t:Permission>
```

<span data-ttu-id="1734b-281">Si desea usar el nivel de permisos personalizados, use este código en su lugar.</span><span class="sxs-lookup"><span data-stu-id="1734b-281">If you want to use the custom permission level, use this code instead.</span></span>
  
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

<span data-ttu-id="1734b-282">El servidor responde a la solicitud de **UpdateFolder** con un mensaje de [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la carpeta se ha actualizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1734b-282">The server responds to the **UpdateFolder** request with an [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was updated successfully.</span></span>
  
## <a name="removing-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="1734b-283">Eliminación de permisos de carpeta mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="1734b-283">Removing folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="1734b-284"><a name="bk_removeewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="1734b-284"></span></span>

<span data-ttu-id="1734b-285">En el ejemplo de código siguiente se muestra cómo utilizar la API administrada de EWS para quitar todos los permisos de usuario en una carpeta específica, excepto los permisos predeterminado y anónimo, mediante:</span><span class="sxs-lookup"><span data-stu-id="1734b-285">The following code example shows how to use the EWS Managed API to remove all user permissions on a specific folder, except for the default and anonymous permissions, by:</span></span>
  
1. <span data-ttu-id="1734b-286">Obtener los permisos para una carpeta actuales mediante el método **Bind** .</span><span class="sxs-lookup"><span data-stu-id="1734b-286">Getting the current permissions for a folder by using the **Bind** method.</span></span> 
    
2. <span data-ttu-id="1734b-287">Recorrer en iteración la colección de **permisos** y quitar permisos para usuarios individuales.</span><span class="sxs-lookup"><span data-stu-id="1734b-287">Iterating through the **Permissions** collection and removing permissions for individual users.</span></span> 
    
3. <span data-ttu-id="1734b-288">Llamar al método **Update** para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="1734b-288">Calling the **Update** method to save the changes.</span></span> 
    
<span data-ttu-id="1734b-289">En este ejemplo se quitan todos los permisos de usuario en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="1734b-289">This example removes all user permissions on a folder.</span></span> <span data-ttu-id="1734b-290">Si desea modificar este ejemplo para quitar los permisos sólo para un usuario específico, cambie la siguiente línea de código para identificar el nombre para mostrar o la dirección SMTP del usuario.</span><span class="sxs-lookup"><span data-stu-id="1734b-290">If you want to modify this example to remove permissions only for a specific user, change the following line of code to identify either the display name or SMTP address of the user.</span></span>
  
```cs
if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
```

<span data-ttu-id="1734b-291">En este ejemplo se da por supuesto que **servicio** es un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) válido para el propietario del buzón y que se ha autenticado el usuario a un servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1734b-291">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="removing-folder-permissions-by-using-ews"></a><span data-ttu-id="1734b-292">Eliminación de permisos de carpeta mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="1734b-292">Removing folder permissions by using EWS</span></span>
<span data-ttu-id="1734b-293"><a name="bk_removeews"> </a></span><span class="sxs-lookup"><span data-stu-id="1734b-293"></span></span>

<span data-ttu-id="1734b-294">Los siguientes ejemplos de código EWS muestran cómo quitar todos los permisos de usuario en una carpeta específica, excepto los permisos predeterminado y anónimo.</span><span class="sxs-lookup"><span data-stu-id="1734b-294">The following EWS code examples show how to remove all user permissions on a specific folder, except for the default and anonymous permissions.</span></span>
  
<span data-ttu-id="1734b-295">En primer lugar, envíe una solicitud de [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) donde el valor de [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) especifica la carpeta en la que se va a quitar los permisos (la carpeta Elementos enviados en este ejemplo) y el valor de [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) incluye: conjunto de permisos de carpeta.</span><span class="sxs-lookup"><span data-stu-id="1734b-295">First, send a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request where the [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) value specifies the folder in which to remove permissions (the Sent Items folder in this example) and the [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) value includes folder:PermissionSet.</span></span> <span data-ttu-id="1734b-296">Esta solicitud, recuperará el [conjunto de permisos](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx) para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="1734b-296">This request will retrieve the [PermissionSet](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx) for the folder specified.</span></span> 
  
<span data-ttu-id="1734b-297">También es la solicitud XML que la API administrada de EWS envía cuando se llama al método **enlazar** para [quitar permisos de carpeta](#bk_removeewsma).</span><span class="sxs-lookup"><span data-stu-id="1734b-297">This is also the XML request that the EWS Managed API sends when you call the **Bind** method to [remove folder permissions](#bk_removeewsma).</span></span>
  
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

<span data-ttu-id="1734b-298">El servidor responde a la solicitud de **GetFolder** con un mensaje de [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, lo que indica que la carpeta se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1734b-298">The server responds to the **GetFolder** request with a [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was retrieved successfully.</span></span> <span data-ttu-id="1734b-299">Los valores de los elementos **FolderId** e **ID** se han abreviado para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="1734b-299">The values of the **FolderId** and **ParentFolderId** elements have been shortened for readability.</span></span> 
  
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
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="1734b-300">A continuación, use la operación **UpdateFolder** para enviar el actualizado **PermissionSet**, que no incluye el **permiso** para el usuario se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="1734b-300">Next, use the **UpdateFolder** operation to send the updated **PermissionSet**, which does not include the **Permission** for the removed user.</span></span> 
  
<span data-ttu-id="1734b-301">También es la solicitud XML que la API administrada de EWS envía al llamar al método **Update** para [quitar permisos de carpeta](#bk_removeewsma).</span><span class="sxs-lookup"><span data-stu-id="1734b-301">This is also the XML request that the EWS Managed API sends when you call the **Update** method to [remove folder permissions](#bk_removeewsma).</span></span>
  
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

<span data-ttu-id="1734b-302">El servidor responde a la solicitud de **UpdateFolder** con un mensaje de **UpdateFolderResponse** que incluye un valor de elemento [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de **NoError**, que indica que la actualización se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1734b-302">The server responds to the **UpdateFolder** request with an **UpdateFolderResponse** message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the update was successful.</span></span>
  
## <a name="updating-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="1734b-303">Actualización de permisos de carpeta mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="1734b-303">Updating folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="1734b-304"><a name="bk_updateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="1734b-304"></span></span>

<span data-ttu-id="1734b-305">También puede actualizar los permisos de carpeta para una carpeta específica mediante el uso de la API administrada de EWS.</span><span class="sxs-lookup"><span data-stu-id="1734b-305">You can also update folder permissions for a specific folder by using the EWS Managed API.</span></span> <span data-ttu-id="1734b-306">Para actualizar los permisos:</span><span class="sxs-lookup"><span data-stu-id="1734b-306">To update the permissions:</span></span> 
  
1. <span data-ttu-id="1734b-307">[Quitar los permisos de carpeta](#bk_removeewsma) para los permisos no actualizados, pero no se llama al método **Update** (todavía).</span><span class="sxs-lookup"><span data-stu-id="1734b-307">[Remove the folder permissions](#bk_removeewsma) for the outdated permissions, but do not call the **Update** method (yet).</span></span> 
    
2. <span data-ttu-id="1734b-308">[Agregar permisos de carpeta para los usuarios nuevos o modificados](#bk_enableewsma).</span><span class="sxs-lookup"><span data-stu-id="1734b-308">[Add folder permissions for the new or changed users](#bk_enableewsma).</span></span>
    
3. <span data-ttu-id="1734b-309">Llame al método **Update** para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="1734b-309">Call the **Update** method to save the changes.</span></span> 
    
<span data-ttu-id="1734b-310">Si se intenta agregar dos conjuntos de permisos para el mismo usuario, recibirá un error de **ServiceResponseException** con la siguiente descripción: "el conjunto de permisos especificado contiene identificadores de usuario duplicados".</span><span class="sxs-lookup"><span data-stu-id="1734b-310">If you try to add two sets of permissions for the same user, you will receive a **ServiceResponseException** error with the following description: "The specified permission set contains duplicate UserIds".</span></span> <span data-ttu-id="1734b-311">En ese caso, quitar los permisos actuales de la colección **Permission** , a continuación, agregar los nuevos permisos a la colección **Permission** .</span><span class="sxs-lookup"><span data-stu-id="1734b-311">In that case, remove the current permissions from the **Permission** collection, then add the new permissions to the **Permission** collection.</span></span> 
  
## <a name="updating-folder-permissions-by-using-ews"></a><span data-ttu-id="1734b-312">Actualización de permisos de carpeta mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="1734b-312">Updating folder permissions by using EWS</span></span>
<span data-ttu-id="1734b-313"><a name="bk_updateews"> </a></span><span class="sxs-lookup"><span data-stu-id="1734b-313"></span></span>

<span data-ttu-id="1734b-314">También puede actualizar los permisos de carpeta para carpetas específicas mediante el uso de EWS combinando el proceso de adición y eliminación.</span><span class="sxs-lookup"><span data-stu-id="1734b-314">You can also update folder permissions for specific folders by using EWS by combining the removal and addition process.</span></span> <span data-ttu-id="1734b-315">Para actualizar los permisos:</span><span class="sxs-lookup"><span data-stu-id="1734b-315">To update the permissions:</span></span> 
  
1. <span data-ttu-id="1734b-316">Recuperar los permisos de la carpeta actual mediante el uso de la operación **GetFolder** .</span><span class="sxs-lookup"><span data-stu-id="1734b-316">Retrieve the folder's current permissions by using the **GetFolder** operation.</span></span> 
    
2. <span data-ttu-id="1734b-317">Enviar una lista actualizada de permisos mediante la operación **UpdateFolder** .</span><span class="sxs-lookup"><span data-stu-id="1734b-317">Send an updated list of permissions by using the **UpdateFolder** operation.</span></span> 
    
<span data-ttu-id="1734b-318">Estos son las mismas dos operaciones que se usa para [Habilitar](#bk_enableews) o [quitar el acceso](#bk_removeews) mediante el uso de EWS.</span><span class="sxs-lookup"><span data-stu-id="1734b-318">These are the same two operations you use to [enable](#bk_enableews) or [remove access](#bk_removeews) by using EWS.</span></span> <span data-ttu-id="1734b-319">La única diferencia es que cuando se recibe la respuesta **GetFolder** , contendrá un conjunto de **permisos** de usuario.</span><span class="sxs-lookup"><span data-stu-id="1734b-319">The only difference is that when you receive the **GetFolder** response, it will contain a **Permission** set for user.</span></span> <span data-ttu-id="1734b-320">Simplemente reemplace ese elemento de **permiso** existente con el nuevo elemento de **permiso** y, a continuación, envíe la operación **UpdateFolder** con el nuevo valor de **permiso** o los valores.</span><span class="sxs-lookup"><span data-stu-id="1734b-320">Simply replace that existing **Permission** element with the new **Permission** element, and then send the **UpdateFolder** operation with the new **Permission** value or values.</span></span> 
  
<span data-ttu-id="1734b-321">Si se intenta agregar dos conjuntos de permisos para el mismo usuario, recibirá un valor **ResponseCode** de **ErrorDuplicateUserIdsSpecified**.</span><span class="sxs-lookup"><span data-stu-id="1734b-321">If you try to add two sets of permissions for the same user, you will receive a **ResponseCode** value of **ErrorDuplicateUserIdsSpecified**.</span></span> <span data-ttu-id="1734b-322">En ese caso, quite el valor de permiso no actualizado para el usuario de la solicitud y, a continuación, vuelva a intentar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1734b-322">In that case, remove the outdated Permission value for the user from the request and then retry the request.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1734b-323">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="1734b-323">Next steps</span></span>

<span data-ttu-id="1734b-324">Después de conceder permisos de usuario para una carpeta específica, el usuario puede tener acceso a la carpeta como un delegado.</span><span class="sxs-lookup"><span data-stu-id="1734b-324">After you give a user permission to a specific folder, the user can access the folder as a delegate.</span></span> <span data-ttu-id="1734b-325">Para obtener m?s informaci?n, vea:</span><span class="sxs-lookup"><span data-stu-id="1734b-325">For more information, see:</span></span>
  
- [<span data-ttu-id="1734b-326">Correo electrónico de acceso como delegado mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1734b-326">Access email as a delegate by using EWS in Exchange</span></span>](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="1734b-327">Obtener acceso a un calendario como delegado mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1734b-327">Access a calendar as a delegate by using EWS in Exchange</span></span>](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="1734b-328">Contactos de acceso como delegado mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1734b-328">Access contacts as a delegate by using EWS in Exchange</span></span>](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="1734b-329">Vea también</span><span class="sxs-lookup"><span data-stu-id="1734b-329">See also</span></span>

- [<span data-ttu-id="1734b-330">Acceso delegado y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1734b-330">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)   
- [<span data-ttu-id="1734b-331">Agregar y quitar delegados mediante EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1734b-331">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="1734b-332">Las carpetas y elementos de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1734b-332">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    

