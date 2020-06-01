---
title: FolderName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderName
api_type:
- schema
ms.assetid: c5a2cd55-ac47-43bf-94b5-3ab3a4c28a62
description: El elemento nombreDeCarpeta identifica una única carpeta administrada administrada que se va a agregar a un buzón.
ms.openlocfilehash: 1bb63e50c06e81337d1142a6624213fb2db12457
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461355"
---
# <a name="foldername"></a><span data-ttu-id="5d171-103">FolderName</span><span class="sxs-lookup"><span data-stu-id="5d171-103">FolderName</span></span>

<span data-ttu-id="5d171-104">El elemento **nombreDeCarpeta** identifica una única carpeta administrada administrada que se va a agregar a un buzón.</span><span class="sxs-lookup"><span data-stu-id="5d171-104">The **FolderName** element identifies a single managed custom folder to add to a mailbox.</span></span> 
  
[<span data-ttu-id="5d171-105">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="5d171-105">CreateManagedFolder</span></span>](createmanagedfolder.md)
  
[<span data-ttu-id="5d171-106">FolderNames</span><span class="sxs-lookup"><span data-stu-id="5d171-106">FolderNames</span></span>](foldernames.md)
  
[<span data-ttu-id="5d171-107">FolderName</span><span class="sxs-lookup"><span data-stu-id="5d171-107">FolderName</span></span>](foldername.md)
  
```xml
<FolderName>...</FolderName>
```

 <span data-ttu-id="5d171-108">**string**</span><span class="sxs-lookup"><span data-stu-id="5d171-108">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5d171-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5d171-109">Attributes and elements</span></span>

<span data-ttu-id="5d171-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5d171-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d171-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="5d171-111">Attributes</span></span>

<span data-ttu-id="5d171-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5d171-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5d171-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5d171-113">Child elements</span></span>

<span data-ttu-id="5d171-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5d171-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5d171-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5d171-115">Parent elements</span></span>

|<span data-ttu-id="5d171-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5d171-116">**Element**</span></span>|<span data-ttu-id="5d171-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d171-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d171-118">FolderNames</span><span class="sxs-lookup"><span data-stu-id="5d171-118">FolderNames</span></span>](foldernames.md) <br/> |<span data-ttu-id="5d171-119">Contiene una matriz de carpetas personalizadas administradas con nombre para agregar a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="5d171-119">Contains an array of named managed custom folders to add to a mailbox.</span></span>  <br/> <span data-ttu-id="5d171-120">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="5d171-120">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateManagedFolder/FolderNames` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5d171-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5d171-121">Text value</span></span>

<span data-ttu-id="5d171-122">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="5d171-122">A text value is required.</span></span> <span data-ttu-id="5d171-123">El valor de texto representa un nombre de carpeta.</span><span class="sxs-lookup"><span data-stu-id="5d171-123">The text value represents a folder name.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5d171-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d171-124">Remarks</span></span>

<span data-ttu-id="5d171-125">Aunque puede usar los servicios Web de Exchange para agregar carpetas personalizadas administradas a un buzón de correo, no puede usar la misma tecnología para tener acceso a la lista de carpetas personalizadas administradas disponibles.</span><span class="sxs-lookup"><span data-stu-id="5d171-125">Although you can use Exchange Web Services to add managed custom folders to a mailbox, you cannot use the same technology to access the list of available managed custom folders.</span></span> <span data-ttu-id="5d171-126">Puede obtener una lista de las carpetas personalizadas administradas mediante un comando del shell de administración de Exchange o mediante una API que interactúa con el servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5d171-126">You can obtain a list of managed custom folders by using an Exchange Management Shell command or by using an API that interfaces with the Active Directory directory service.</span></span> <span data-ttu-id="5d171-127">El nombre de la carpeta es el nombre del objeto de Active Directory correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5d171-127">The folder name is the name of the corresponding Active Directory object.</span></span>
  
<span data-ttu-id="5d171-128">Puede usar la [operación FindFolder](findfolder-operation.md) para buscar carpetas personalizadas administradas.</span><span class="sxs-lookup"><span data-stu-id="5d171-128">You can use the [FindFolder operation](findfolder-operation.md) to find managed custom folders.</span></span> <span data-ttu-id="5d171-129">Use la [operación DeleteFolder](deletefolder-operation.md) para eliminar las carpetas personalizadas administradas.</span><span class="sxs-lookup"><span data-stu-id="5d171-129">Use the [DeleteFolder operation](deletefolder-operation.md) to delete managed custom folders.</span></span> 
  
<span data-ttu-id="5d171-130">Es importante tener en cuenta que **nombreDeCarpeta** es el nombre de una carpeta personalizada administrada existente en la organización.</span><span class="sxs-lookup"><span data-stu-id="5d171-130">It is important to note that **FolderName** is the name of an existing managed custom folder in the organization.</span></span> <span data-ttu-id="5d171-131">Si se intenta agregar una carpeta que no está en la organización, se producirá una respuesta de error.</span><span class="sxs-lookup"><span data-stu-id="5d171-131">An attempt to add a folder that is not in the organization will result in an error response.</span></span> 
  
<span data-ttu-id="5d171-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="5d171-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5d171-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5d171-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d171-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d171-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5d171-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5d171-135">Schema Name</span></span>  <br/> |<span data-ttu-id="5d171-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5d171-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="5d171-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5d171-137">Validation File</span></span>  <br/> |<span data-ttu-id="5d171-138">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5d171-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5d171-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5d171-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="5d171-140">Falso</span><span class="sxs-lookup"><span data-stu-id="5d171-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d171-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d171-141">See also</span></span>



[<span data-ttu-id="5d171-142">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="5d171-142">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="5d171-143">Buscar carpetas</span><span class="sxs-lookup"><span data-stu-id="5d171-143">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="5d171-144">Adición de carpetas administradas</span><span class="sxs-lookup"><span data-stu-id="5d171-144">Adding Managed Folders</span></span>](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

