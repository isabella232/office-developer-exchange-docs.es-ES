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
description: El elemento CreateManagedFolder define una solicitud para agregar carpetas personalizadas administradas a un buzón de correo.
ms.openlocfilehash: 4acc931de2a8665db092c3b309d914f0a3c67558
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763966"
---
# <a name="createmanagedfolder"></a><span data-ttu-id="413df-103">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="413df-103">CreateManagedFolder</span></span>

<span data-ttu-id="413df-104">El elemento **CreateManagedFolder** define una solicitud para agregar carpetas personalizadas administradas a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="413df-104">The **CreateManagedFolder** element defines a request to add managed custom folders to a mailbox.</span></span> 
  
```xml
<CreateManagedFolder>
   <FolderNames/>
   <Mailbox/>
</CreateManagedFolder>
```

 <span data-ttu-id="413df-105">**CreateManagedFolderRequestType**</span><span class="sxs-lookup"><span data-stu-id="413df-105">**CreateManagedFolderRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="413df-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="413df-106">Attributes and elements</span></span>

<span data-ttu-id="413df-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="413df-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="413df-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="413df-108">Attributes</span></span>

<span data-ttu-id="413df-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="413df-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="413df-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="413df-110">Child elements</span></span>

|<span data-ttu-id="413df-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="413df-111">**Element**</span></span>|<span data-ttu-id="413df-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="413df-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="413df-113">Nombres de carpetas</span><span class="sxs-lookup"><span data-stu-id="413df-113">FolderNames</span></span>](foldernames.md) <br/> |<span data-ttu-id="413df-114">Contiene una matriz de las carpetas administradas con nombre para agregar a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="413df-114">Contains an array of named managed folders to add to a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="413df-115">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="413df-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="413df-116">Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="413df-116">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="413df-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="413df-117">Parent elements</span></span>

<span data-ttu-id="413df-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="413df-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="413df-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="413df-119">Remarks</span></span>

<span data-ttu-id="413df-120">La cuenta de la persona que realiza la solicitud debe tener permisos de FullAccess en el buzón de correo donde se crean las carpetas administradas.</span><span class="sxs-lookup"><span data-stu-id="413df-120">The account of the person who is making the request must have FullAccess permissions on the mailbox where the managed folders are created.</span></span> <span data-ttu-id="413df-121">Puede usar el parámetro de _ _ - AccessRights con el cmdlet **Add-MailboxPermission** de Shell de administración de Exchange para asignar el permiso FullAccess.</span><span class="sxs-lookup"><span data-stu-id="413df-121">You can use the _ -AccessRights _ parameter with the Exchange Management Shell **Add-MailboxPermission** cmdlet to assign the FullAccess permission.</span></span> 
  
<span data-ttu-id="413df-122">Aunque puede usar servicios Web de Exchange para agregar las carpetas administradas a un buzón de correo, no puede usar servicios Web de Exchange para tener acceso a la lista de carpetas administradas que están disponibles.</span><span class="sxs-lookup"><span data-stu-id="413df-122">Although you can use Exchange Web Services to add managed folders to a mailbox, you cannot use Exchange Web Services to access the list of managed folders that are available.</span></span> <span data-ttu-id="413df-123">Para obtener una lista de las carpetas administradas disponibles, use el cmdlet del Shell de administración de Exchange de **get-carpeta administrada** .</span><span class="sxs-lookup"><span data-stu-id="413df-123">To obtain a list of available managed folders, use the **get-managedfolder** Exchange Management Shell cmdlet.</span></span> <span data-ttu-id="413df-124">La lista que es devuelto por el **cmdlet get-carpeta administrada** contiene carpetas personalizadas administradas y carpetas predeterminadas administradas.</span><span class="sxs-lookup"><span data-stu-id="413df-124">The list that is returned by the **get-managedfolder cmdlet** will contain both managed custom folders and managed default folders.</span></span> <span data-ttu-id="413df-125">Sólo puede agregar carpetas de tipo **managedcustomfolder** para el buzón de correo mediante el uso de la operación CreateManagedFolder.</span><span class="sxs-lookup"><span data-stu-id="413df-125">You can only add folders of type **managedcustomfolder** to the mailbox by using the CreateManagedFolder operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="413df-126">También puede obtener una lista de las carpetas administradas mediante el uso de la API de DirectoryServices de Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="413df-126">You can also get a list of managed folders by using the DirectoryServices API of the Microsoft .NET Framework.</span></span> 
  
<span data-ttu-id="413df-127">Puede usar la [operación FindFolder](findfolder-operation.md) para buscar las carpetas administradas en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="413df-127">You can use the [FindFolder operation](findfolder-operation.md) to find managed folders in a mailbox.</span></span> <span data-ttu-id="413df-128">Las carpetas administradas se pueden distinguir estableciendo el elemento [BaseShape](baseshape.md) en AllProperties en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="413df-128">Managed folders can be distinguished by setting the [BaseShape](baseshape.md) element to AllProperties in the request.</span></span> <span data-ttu-id="413df-129">La respuesta contendrá un elemento [ManagedFolderInformation](managedfolderinformation.md) para distinguir las carpetas administradas de las carpetas del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="413df-129">The response will contain a [ManagedFolderInformation](managedfolderinformation.md) element to distinguish the managed folders from the Exchange store folders.</span></span> <span data-ttu-id="413df-130">Puede eliminar las carpetas administradas de la misma forma que eliminar otros tipos de carpetas.</span><span class="sxs-lookup"><span data-stu-id="413df-130">You can delete managed folders in the same manner that you delete other folder types.</span></span> 
  
<span data-ttu-id="413df-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="413df-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="413df-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="413df-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="413df-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="413df-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="413df-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="413df-134">Schema Name</span></span>  <br/> |<span data-ttu-id="413df-135">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="413df-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="413df-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="413df-136">Validation File</span></span>  <br/> |<span data-ttu-id="413df-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="413df-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="413df-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="413df-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="413df-139">False</span><span class="sxs-lookup"><span data-stu-id="413df-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="413df-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="413df-140">See also</span></span>



[<span data-ttu-id="413df-141">Operación CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="413df-141">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)
  
[<span data-ttu-id="413df-142">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="413df-142">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="413df-143">Buscar carpetas</span><span class="sxs-lookup"><span data-stu-id="413df-143">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="413df-144">Adición de las carpetas administradas</span><span class="sxs-lookup"><span data-stu-id="413df-144">Adding Managed Folders</span></span>](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

