---
title: EffectiveRights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EffectiveRights
api_type:
- schema
ms.assetid: bf5278eb-3a1a-4d27-9d16-b8be043bb023
description: El elemento EffectiveRights contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta. Este elemento es de sólo lectura.
ms.openlocfilehash: 3055eb73056750508b48ead29136b56e7ce97ee9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459247"
---
# <a name="effectiverights"></a><span data-ttu-id="e0c4f-104">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="e0c4f-104">EffectiveRights</span></span>

<span data-ttu-id="e0c4f-105">El elemento **EffectiveRights** contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-105">The **EffectiveRights** element contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="e0c4f-106">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-106">This element is read-only.</span></span> 
  
```XML
<EffectiveRights>
   <CreateAssociated/>
   <CreateContents/>
   <CreateHierarchy/>
   <Delete/>
   <Modify/>
   <Read/>
   <ViewPrivateItems/>
</EffectiveRights>
```

 <span data-ttu-id="e0c4f-107">**EffectiveRightsType**</span><span class="sxs-lookup"><span data-stu-id="e0c4f-107">**EffectiveRightsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0c4f-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e0c4f-108">Attributes and elements</span></span>

<span data-ttu-id="e0c4f-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0c4f-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="e0c4f-110">Attributes</span></span>

<span data-ttu-id="e0c4f-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0c4f-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e0c4f-112">Child elements</span></span>

|<span data-ttu-id="e0c4f-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e0c4f-113">**Element**</span></span>|<span data-ttu-id="e0c4f-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0c4f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0c4f-115">CreateAssociated</span><span class="sxs-lookup"><span data-stu-id="e0c4f-115">CreateAssociated</span></span>](createassociated.md) <br/> |<span data-ttu-id="e0c4f-116">Indica si un cliente puede crear una tabla de contenido asociada.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-116">Indicates whether a client can create an associated contents table.</span></span> <span data-ttu-id="e0c4f-117">Esta propiedad solo se usa en objetos Folder.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-117">This property is only used on folder objects.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-118">CreateContents</span><span class="sxs-lookup"><span data-stu-id="e0c4f-118">CreateContents</span></span>](createcontents.md) <br/> |<span data-ttu-id="e0c4f-119">Indica si un cliente puede crear una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-119">Indicates whether a client can create a contents table.</span></span> <span data-ttu-id="e0c4f-120">Esta propiedad solo se usa en objetos Folder.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-120">This property is only used on folder objects.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-121">CreateHierarchy</span><span class="sxs-lookup"><span data-stu-id="e0c4f-121">CreateHierarchy</span></span>](createhierarchy.md) <br/> |<span data-ttu-id="e0c4f-122">Indica si un cliente puede crear una tabla de jerarquías.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-122">Indicates whether a client can create a hierarchy table.</span></span> <span data-ttu-id="e0c4f-123">Esta propiedad solo se usa en objetos Folder.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-123">This property is only used on folder objects.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-124">Eliminar</span><span class="sxs-lookup"><span data-stu-id="e0c4f-124">Delete</span></span>](delete.md) <br/> |<span data-ttu-id="e0c4f-125">Indica si un cliente puede eliminar una carpeta o un elemento.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-125">Indicates whether a client can delete a folder or item.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-126">Modify</span><span class="sxs-lookup"><span data-stu-id="e0c4f-126">Modify</span></span>](modify.md) <br/> |<span data-ttu-id="e0c4f-127">Indica si un cliente puede modificar una carpeta o un elemento.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-127">Indicates whether a client can modify a folder or item.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-128">Read</span><span class="sxs-lookup"><span data-stu-id="e0c4f-128">Read</span></span>](read.md) <br/> |<span data-ttu-id="e0c4f-129">Indica si un cliente puede leer una carpeta o un elemento.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-129">Indicates whether a client can read a folder or item.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-130">ViewPrivateItems</span><span class="sxs-lookup"><span data-stu-id="e0c4f-130">ViewPrivateItems</span></span>](viewprivateitems.md) <br/> |<span data-ttu-id="e0c4f-131">Indica si se puede ver un elemento privado.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-131">Indicates whether a private item can be viewed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e0c4f-132">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e0c4f-132">Parent elements</span></span>

|<span data-ttu-id="e0c4f-133">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e0c4f-133">**Element**</span></span>|<span data-ttu-id="e0c4f-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0c4f-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0c4f-135">Folder</span><span class="sxs-lookup"><span data-stu-id="e0c4f-135">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="e0c4f-136">Representa una carpeta en un buzón.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-136">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-137">Hubiera</span><span class="sxs-lookup"><span data-stu-id="e0c4f-137">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="e0c4f-138">Representa una carpeta de tareas en un buzón.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-138">Represents a tasks folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-139">Hubiera</span><span class="sxs-lookup"><span data-stu-id="e0c4f-139">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="e0c4f-140">Representa una carpeta de contactos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-140">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-141">Hubiera</span><span class="sxs-lookup"><span data-stu-id="e0c4f-141">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="e0c4f-142">Representa una carpeta de calendario en un buzón.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-142">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-143">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="e0c4f-143">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="e0c4f-144">Representa una carpeta de búsqueda en un buzón.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-144">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-145">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="e0c4f-145">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="e0c4f-146">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-146">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-147">Contacto</span><span class="sxs-lookup"><span data-stu-id="e0c4f-147">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="e0c4f-148">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-148">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-149">DistributionList</span><span class="sxs-lookup"><span data-stu-id="e0c4f-149">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="e0c4f-150">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-150">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-151">Elemento</span><span class="sxs-lookup"><span data-stu-id="e0c4f-151">Item</span></span>](item.md) <br/> |<span data-ttu-id="e0c4f-152">Representa un elemento de Exchange genérico.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-152">Represents a generic Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-153">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="e0c4f-153">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="e0c4f-154">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-154">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-155">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="e0c4f-155">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="e0c4f-156">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-156">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-157">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e0c4f-157">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="e0c4f-158">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-158">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-159">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="e0c4f-159">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="e0c4f-160">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-160">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-161">Mensaje</span><span class="sxs-lookup"><span data-stu-id="e0c4f-161">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e0c4f-162">Representa un mensaje de correo electrónico de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-162">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-163">Tarea</span><span class="sxs-lookup"><span data-stu-id="e0c4f-163">Task</span></span>](task.md) <br/> |<span data-ttu-id="e0c4f-164">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-164">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e0c4f-165">PostItem</span><span class="sxs-lookup"><span data-stu-id="e0c4f-165">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="e0c4f-166">Representa un elemento post en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-166">Represents a post item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e0c4f-167">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e0c4f-167">Text value</span></span>

<span data-ttu-id="e0c4f-168">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-168">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0c4f-169">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0c4f-169">Remarks</span></span>

<span data-ttu-id="e0c4f-170">**EffectiveRights** se admite en las respuestas GetFolder, GetItem, FindFolder, FindItem, SyncFolderHierarchy y SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-170">**EffectiveRights** is supported in the GetFolder, GetItem, FindFolder, FindItem, SyncFolderHierarchy, and SyncFolderItems responses.</span></span> <span data-ttu-id="e0c4f-171">La propiedad **EffectiveRights** se expone en la forma **AllProperties** para carpetas y elementos.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-171">The **EffectiveRights** property is exposed in the **AllProperties** shape for folders and items.</span></span> 
  
<span data-ttu-id="e0c4f-172">Esta propiedad **EffectiveRights** proporciona acceso a la misma información que se proporciona en la propiedad **MAPI PR_ACCESS** .</span><span class="sxs-lookup"><span data-stu-id="e0c4f-172">This **EffectiveRights** property provides access to the same information that is provided in the **PR_ACCESS MAPI** property.</span></span> 
  
<span data-ttu-id="e0c4f-173">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0c4f-173">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0c4f-174">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e0c4f-174">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0c4f-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0c4f-175">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e0c4f-176">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e0c4f-176">Schema Name</span></span>  <br/> |<span data-ttu-id="e0c4f-177">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e0c4f-177">Types schema</span></span>  <br/> |
|<span data-ttu-id="e0c4f-178">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e0c4f-178">Validation File</span></span>  <br/> |<span data-ttu-id="e0c4f-179">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e0c4f-179">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e0c4f-180">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e0c4f-180">Can be Empty</span></span>  <br/> |<span data-ttu-id="e0c4f-181">Falso</span><span class="sxs-lookup"><span data-stu-id="e0c4f-181">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0c4f-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0c4f-182">See also</span></span>

- [<span data-ttu-id="e0c4f-183">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e0c4f-183">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="e0c4f-184">Configuración de permisos de nivel de carpeta</span><span class="sxs-lookup"><span data-stu-id="e0c4f-184">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

