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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764066"
---
# <a name="delegatepermissions"></a><span data-ttu-id="17e17-104">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="17e17-104">DelegatePermissions</span></span>

<span data-ttu-id="17e17-105">El elemento **DelegatePermissions** contiene la configuración de nivel de permisos de delegado para un usuario.</span><span class="sxs-lookup"><span data-stu-id="17e17-105">The **DelegatePermissions** element contains the delegate permission-level settings for a user.</span></span> <span data-ttu-id="17e17-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="17e17-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
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

<span data-ttu-id="17e17-107">**DelegatePermissionsType**</span><span class="sxs-lookup"><span data-stu-id="17e17-107">**DelegatePermissionsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="17e17-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="17e17-108">Attributes and elements</span></span>

<span data-ttu-id="17e17-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="17e17-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17e17-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="17e17-110">Attributes</span></span>

<span data-ttu-id="17e17-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="17e17-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="17e17-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="17e17-112">Child elements</span></span>

|<span data-ttu-id="17e17-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="17e17-113">**Element**</span></span>|<span data-ttu-id="17e17-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="17e17-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17e17-115">CalendarFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="17e17-115">CalendarFolderPermissionLevel</span></span>](calendarfolderpermissionlevel.md) <br/> |<span data-ttu-id="17e17-116">Contiene los permisos para la carpeta Calendario predeterminada.</span><span class="sxs-lookup"><span data-stu-id="17e17-116">Contains the permissions for the default Calendar folder.</span></span> <span data-ttu-id="17e17-117">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="17e17-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="17e17-118">TasksFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="17e17-118">TasksFolderPermissionLevel</span></span>](tasksfolderpermissionlevel.md) <br/> |<span data-ttu-id="17e17-119">Contiene los permisos para la carpeta de tareas predeterminada.</span><span class="sxs-lookup"><span data-stu-id="17e17-119">Contains the permissions for the default Task folder.</span></span> <span data-ttu-id="17e17-120">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="17e17-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="17e17-121">InboxFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="17e17-121">InboxFolderPermissionLevel</span></span>](inboxfolderpermissionlevel.md) <br/> |<span data-ttu-id="17e17-122">Contiene los permisos para la carpeta de la Bandeja de entrada predeterminada.</span><span class="sxs-lookup"><span data-stu-id="17e17-122">Contains the permissions for the default Inbox folder.</span></span> <span data-ttu-id="17e17-123">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="17e17-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="17e17-124">ContactsFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="17e17-124">ContactsFolderPermissionLevel</span></span>](contactsfolderpermissionlevel.md) <br/> |<span data-ttu-id="17e17-125">Contiene los permisos para la carpeta Contactos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="17e17-125">Contains the permissions for the default Contacts folder.</span></span> <span data-ttu-id="17e17-126">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="17e17-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="17e17-127">NotesFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="17e17-127">NotesFolderPermissionLevel</span></span>](notesfolderpermissionlevel.md) <br/> |<span data-ttu-id="17e17-128">Contiene los permisos para la carpeta de notas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="17e17-128">Contains the permissions for the default Notes folder.</span></span> <span data-ttu-id="17e17-129">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="17e17-129">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="17e17-130">JournalFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="17e17-130">JournalFolderPermissionLevel</span></span>](journalfolderpermissionlevel.md) <br/> |<span data-ttu-id="17e17-131">Contiene los permisos para la carpeta de diario predeterminada.</span><span class="sxs-lookup"><span data-stu-id="17e17-131">Contains the permissions for the default Journal folder.</span></span> <span data-ttu-id="17e17-132">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="17e17-132">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="17e17-133">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="17e17-133">Parent elements</span></span>

|<span data-ttu-id="17e17-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="17e17-134">**Element**</span></span>|<span data-ttu-id="17e17-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="17e17-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17e17-136">UsuarioDelegado</span><span class="sxs-lookup"><span data-stu-id="17e17-136">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="17e17-137">Identifica un único delegado para agregar o actualizar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="17e17-137">Identifies a single delegate to add or update in a mailbox.</span></span> <span data-ttu-id="17e17-138">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="17e17-138">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17e17-139">Notas</span><span class="sxs-lookup"><span data-stu-id="17e17-139">Remarks</span></span>

<span data-ttu-id="17e17-140">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="17e17-140">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17e17-141">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="17e17-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17e17-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="17e17-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="17e17-143">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="17e17-143">Schema Name</span></span>  <br/> |<span data-ttu-id="17e17-144">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="17e17-144">Types schema</span></span>  <br/> |
|<span data-ttu-id="17e17-145">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="17e17-145">Validation File</span></span>  <br/> |<span data-ttu-id="17e17-146">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="17e17-146">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="17e17-147">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="17e17-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="17e17-148">False</span><span class="sxs-lookup"><span data-stu-id="17e17-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="17e17-149">Ver también</span><span class="sxs-lookup"><span data-stu-id="17e17-149">See also</span></span>

- [<span data-ttu-id="17e17-150">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="17e17-150">AddDelegate operation</span></span>](adddelegate-operation.md) 
- [<span data-ttu-id="17e17-151">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="17e17-151">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="17e17-152">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="17e17-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="17e17-153">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="17e17-153">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

