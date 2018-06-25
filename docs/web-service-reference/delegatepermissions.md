---
title: DelegatePermissions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegatePermissions
api_type:
- schema
ms.assetid: 292badc7-bab3-4368-9d7c-9a8b7edb279b
description: El elemento DelegatePermissions contiene la configuración de nivel de permisos de delegado para un usuario. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 319592b6c3386a07b3094115c335c7fb8ffe1130
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764066"
---
# <a name="delegatepermissions"></a><span data-ttu-id="39948-104">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="39948-104">DelegatePermissions</span></span>

<span data-ttu-id="39948-105">El elemento **DelegatePermissions** contiene la configuración de nivel de permisos de delegado para un usuario.</span><span class="sxs-lookup"><span data-stu-id="39948-105">The **DelegatePermissions** element contains the delegate permission-level settings for a user.</span></span> <span data-ttu-id="39948-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="39948-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DelegatePermissions>
   <CalendarFolderPermissionLevel/>
   <TasksFolderPermissionLevel/>
   <InboxFolderPermissionLevel/>
   <ContactsFolderPermissionLevel/>
   <NotesFolderPermissionLevel/>
   <JournalFolderPermissionLevel/>
</DelegatePermissions>
```

<span data-ttu-id="39948-107">**DelegatePermissionsType**</span><span class="sxs-lookup"><span data-stu-id="39948-107">**DelegatePermissionsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="39948-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="39948-108">Attributes and elements</span></span>

<span data-ttu-id="39948-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="39948-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39948-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="39948-110">Attributes</span></span>

<span data-ttu-id="39948-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="39948-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="39948-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="39948-112">Child elements</span></span>

|<span data-ttu-id="39948-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="39948-113">**Element**</span></span>|<span data-ttu-id="39948-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="39948-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39948-115">CalendarFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="39948-115">CalendarFolderPermissionLevel</span></span>](calendarfolderpermissionlevel.md) <br/> |<span data-ttu-id="39948-116">Contiene los permisos para la carpeta Calendario predeterminada.</span><span class="sxs-lookup"><span data-stu-id="39948-116">Contains the permissions for the default Calendar folder.</span></span> <span data-ttu-id="39948-117">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="39948-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="39948-118">TasksFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="39948-118">TasksFolderPermissionLevel</span></span>](tasksfolderpermissionlevel.md) <br/> |<span data-ttu-id="39948-119">Contiene los permisos para la carpeta de tareas predeterminada.</span><span class="sxs-lookup"><span data-stu-id="39948-119">Contains the permissions for the default Task folder.</span></span> <span data-ttu-id="39948-120">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="39948-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="39948-121">InboxFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="39948-121">InboxFolderPermissionLevel</span></span>](inboxfolderpermissionlevel.md) <br/> |<span data-ttu-id="39948-122">Contiene los permisos para la carpeta de la Bandeja de entrada predeterminada.</span><span class="sxs-lookup"><span data-stu-id="39948-122">Contains the permissions for the default Inbox folder.</span></span> <span data-ttu-id="39948-123">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="39948-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="39948-124">ContactsFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="39948-124">ContactsFolderPermissionLevel</span></span>](contactsfolderpermissionlevel.md) <br/> |<span data-ttu-id="39948-125">Contiene los permisos para la carpeta Contactos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="39948-125">Contains the permissions for the default Contacts folder.</span></span> <span data-ttu-id="39948-126">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="39948-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="39948-127">NotesFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="39948-127">NotesFolderPermissionLevel</span></span>](notesfolderpermissionlevel.md) <br/> |<span data-ttu-id="39948-128">Contiene los permisos para la carpeta de notas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="39948-128">Contains the permissions for the default Notes folder.</span></span> <span data-ttu-id="39948-129">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="39948-129">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="39948-130">JournalFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="39948-130">JournalFolderPermissionLevel</span></span>](journalfolderpermissionlevel.md) <br/> |<span data-ttu-id="39948-131">Contiene los permisos para la carpeta de diario predeterminada.</span><span class="sxs-lookup"><span data-stu-id="39948-131">Contains the permissions for the default Journal folder.</span></span> <span data-ttu-id="39948-132">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="39948-132">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="39948-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="39948-133">Parent elements</span></span>

|<span data-ttu-id="39948-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="39948-134">**Element**</span></span>|<span data-ttu-id="39948-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="39948-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39948-136">UsuarioDelegado</span><span class="sxs-lookup"><span data-stu-id="39948-136">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="39948-137">Identifica un único delegado para agregar o actualizar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="39948-137">Identifies a single delegate to add or update in a mailbox.</span></span> <span data-ttu-id="39948-138">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="39948-138">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39948-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="39948-139">Remarks</span></span>

<span data-ttu-id="39948-140">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="39948-140">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39948-141">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="39948-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39948-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="39948-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="39948-143">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="39948-143">Schema Name</span></span>  <br/> |<span data-ttu-id="39948-144">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="39948-144">Types schema</span></span>  <br/> |
|<span data-ttu-id="39948-145">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="39948-145">Validation File</span></span>  <br/> |<span data-ttu-id="39948-146">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="39948-146">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="39948-147">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="39948-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="39948-148">False</span><span class="sxs-lookup"><span data-stu-id="39948-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39948-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="39948-149">See also</span></span>

- [<span data-ttu-id="39948-150">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="39948-150">AddDelegate operation</span></span>](adddelegate-operation.md) 
- [<span data-ttu-id="39948-151">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="39948-151">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="39948-152">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="39948-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="39948-153">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="39948-153">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

