---
title: CreateManagedFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateManagedFolder
api_type:
- schema
ms.assetid: cfdf01a9-0191-47c7-a7ad-5254d8bdee4a
description: El elemento CreateManagedFolder define una solicitud para agregar carpetas administradas personalizadas a un buzón de correo.
ms.openlocfilehash: 01fe8b7341c38ad33089c56271434ad3f9a4e5f0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458365"
---
# <a name="createmanagedfolder"></a><span data-ttu-id="bc568-103">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="bc568-103">CreateManagedFolder</span></span>

<span data-ttu-id="bc568-104">El elemento **CreateManagedFolder** define una solicitud para agregar carpetas administradas personalizadas a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="bc568-104">The **CreateManagedFolder** element defines a request to add managed custom folders to a mailbox.</span></span> 
  
```xml
<CreateManagedFolder>
   <FolderNames/>
   <Mailbox/>
</CreateManagedFolder>
```

 <span data-ttu-id="bc568-105">**CreateManagedFolderRequestType**</span><span class="sxs-lookup"><span data-stu-id="bc568-105">**CreateManagedFolderRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bc568-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bc568-106">Attributes and elements</span></span>

<span data-ttu-id="bc568-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bc568-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bc568-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="bc568-108">Attributes</span></span>

<span data-ttu-id="bc568-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="bc568-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bc568-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bc568-110">Child elements</span></span>

|<span data-ttu-id="bc568-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bc568-111">**Element**</span></span>|<span data-ttu-id="bc568-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bc568-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc568-113">FolderNames</span><span class="sxs-lookup"><span data-stu-id="bc568-113">FolderNames</span></span>](foldernames.md) <br/> |<span data-ttu-id="bc568-114">Contiene una matriz de carpetas administradas con nombre para agregar a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="bc568-114">Contains an array of named managed folders to add to a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="bc568-115">Buzón</span><span class="sxs-lookup"><span data-stu-id="bc568-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="bc568-116">Identifica un objeto de servicio de directorio de Active Directory habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="bc568-116">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bc568-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bc568-117">Parent elements</span></span>

<span data-ttu-id="bc568-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bc568-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bc568-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bc568-119">Remarks</span></span>

<span data-ttu-id="bc568-120">La cuenta de la persona que realiza la solicitud debe tener permisos FullAccess en el buzón de correo en el que se crean las carpetas administradas.</span><span class="sxs-lookup"><span data-stu-id="bc568-120">The account of the person who is making the request must have FullAccess permissions on the mailbox where the managed folders are created.</span></span> <span data-ttu-id="bc568-121">Puede usar el parámetro _-AccessRights _ con el cmdlet **Add-MailboxPermission** del shell de administración de Exchange para asignar el permiso FullAccess.</span><span class="sxs-lookup"><span data-stu-id="bc568-121">You can use the _ -AccessRights _ parameter with the Exchange Management Shell **Add-MailboxPermission** cmdlet to assign the FullAccess permission.</span></span> 
  
<span data-ttu-id="bc568-122">Aunque puede usar los servicios Web de Exchange para agregar carpetas administradas a un buzón de correo, no puede usar los servicios web Exchange para tener acceso a la lista de carpetas administradas que están disponibles.</span><span class="sxs-lookup"><span data-stu-id="bc568-122">Although you can use Exchange Web Services to add managed folders to a mailbox, you cannot use Exchange Web Services to access the list of managed folders that are available.</span></span> <span data-ttu-id="bc568-123">Para obtener una lista de las carpetas administradas disponibles, use el cmdlet **Get-managedfolder de** Shell de administración de Exchange.</span><span class="sxs-lookup"><span data-stu-id="bc568-123">To obtain a list of available managed folders, use the **get-managedfolder** Exchange Management Shell cmdlet.</span></span> <span data-ttu-id="bc568-124">La lista que devuelve el **cmdlet Get-managedfolder** contendrá tanto las carpetas personalizadas administradas como las carpetas predeterminadas administradas.</span><span class="sxs-lookup"><span data-stu-id="bc568-124">The list that is returned by the **get-managedfolder cmdlet** will contain both managed custom folders and managed default folders.</span></span> <span data-ttu-id="bc568-125">Solo se pueden agregar carpetas de tipo **managedcustomfolder** al buzón mediante la operación CreateManagedFolder.</span><span class="sxs-lookup"><span data-stu-id="bc568-125">You can only add folders of type **managedcustomfolder** to the mailbox by using the CreateManagedFolder operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bc568-126">También puede obtener una lista de carpetas administradas mediante la API de DirectoryServices de Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="bc568-126">You can also get a list of managed folders by using the DirectoryServices API of the Microsoft .NET Framework.</span></span> 
  
<span data-ttu-id="bc568-127">Puede usar la [operación FindFolder](findfolder-operation.md) para buscar carpetas administradas en un buzón.</span><span class="sxs-lookup"><span data-stu-id="bc568-127">You can use the [FindFolder operation](findfolder-operation.md) to find managed folders in a mailbox.</span></span> <span data-ttu-id="bc568-128">Las carpetas administradas se pueden distinguir estableciendo el elemento [BaseShape](baseshape.md) en AllProperties en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bc568-128">Managed folders can be distinguished by setting the [BaseShape](baseshape.md) element to AllProperties in the request.</span></span> <span data-ttu-id="bc568-129">La respuesta contendrá un elemento [ManagedFolderInformation](managedfolderinformation.md) para distinguir las carpetas administradas de las carpetas de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="bc568-129">The response will contain a [ManagedFolderInformation](managedfolderinformation.md) element to distinguish the managed folders from the Exchange store folders.</span></span> <span data-ttu-id="bc568-130">Las carpetas administradas se pueden eliminar de la misma manera que se eliminan otros tipos de carpetas.</span><span class="sxs-lookup"><span data-stu-id="bc568-130">You can delete managed folders in the same manner that you delete other folder types.</span></span> 
  
<span data-ttu-id="bc568-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="bc568-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bc568-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bc568-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bc568-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc568-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bc568-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bc568-134">Schema Name</span></span>  <br/> |<span data-ttu-id="bc568-135">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="bc568-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bc568-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bc568-136">Validation File</span></span>  <br/> |<span data-ttu-id="bc568-137">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="bc568-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bc568-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bc568-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="bc568-139">Falso</span><span class="sxs-lookup"><span data-stu-id="bc568-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bc568-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc568-140">See also</span></span>



[<span data-ttu-id="bc568-141">Operación CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="bc568-141">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)
  
[<span data-ttu-id="bc568-142">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="bc568-142">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="bc568-143">Buscar carpetas</span><span class="sxs-lookup"><span data-stu-id="bc568-143">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="bc568-144">Adición de carpetas administradas</span><span class="sxs-lookup"><span data-stu-id="bc568-144">Adding Managed Folders</span></span>](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

