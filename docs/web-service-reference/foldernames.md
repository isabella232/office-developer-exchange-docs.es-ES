---
title: Nombres de carpetas
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderNames
api_type:
- schema
ms.assetid: 6cbe4083-5705-4695-a54e-8dab3e472662
description: El elemento de los nombres de carpetas contiene una matriz de las carpetas administradas con nombre para agregar a un buzón de correo.
ms.openlocfilehash: 819b3c2df1cfcae3a5d4a48539e369a00b1f7229
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764684"
---
# <a name="foldernames"></a><span data-ttu-id="7b30e-103">Nombres de carpetas</span><span class="sxs-lookup"><span data-stu-id="7b30e-103">FolderNames</span></span>

<span data-ttu-id="7b30e-104">El elemento de **los nombres de carpetas** contiene una matriz de las carpetas administradas con nombre para agregar a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="7b30e-104">The **FolderNames** element contains an array of named managed folders to add to a mailbox.</span></span> 
  
[<span data-ttu-id="7b30e-105">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="7b30e-105">CreateManagedFolder</span></span>](createmanagedfolder.md)
  
[<span data-ttu-id="7b30e-106">Nombres de carpetas</span><span class="sxs-lookup"><span data-stu-id="7b30e-106">FolderNames</span></span>](foldernames.md)
  
```xml
<FolderNames>
   <FolderName/>
</FolderNames>
```

 <span data-ttu-id="7b30e-107">**NonEmptyArrayOfFolderNamesType**</span><span class="sxs-lookup"><span data-stu-id="7b30e-107">**NonEmptyArrayOfFolderNamesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7b30e-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7b30e-108">Attributes and elements</span></span>

<span data-ttu-id="7b30e-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7b30e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b30e-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="7b30e-110">Attributes</span></span>

<span data-ttu-id="7b30e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7b30e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7b30e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7b30e-112">Child elements</span></span>

|<span data-ttu-id="7b30e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7b30e-113">**Element**</span></span>|<span data-ttu-id="7b30e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7b30e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b30e-115">FolderName</span><span class="sxs-lookup"><span data-stu-id="7b30e-115">FolderName</span></span>](foldername.md) <br/> |<span data-ttu-id="7b30e-116">Identifica una sola carpeta administrada para agregar al buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="7b30e-116">Identifies a single managed folder to add to mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7b30e-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7b30e-117">Parent elements</span></span>

|<span data-ttu-id="7b30e-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="7b30e-118">**Element**</span></span>|<span data-ttu-id="7b30e-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7b30e-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b30e-120">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="7b30e-120">CreateManagedFolder</span></span>](createmanagedfolder.md) <br/> |<span data-ttu-id="7b30e-121">El elemento raíz en una solicitud para agregar una carpeta administrada a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="7b30e-121">The root element in a request to add a managed folder to a mailbox.</span></span>  <br/> <span data-ttu-id="7b30e-122">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="7b30e-122">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateManagedFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b30e-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b30e-123">Remarks</span></span>

<span data-ttu-id="7b30e-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="7b30e-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7b30e-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7b30e-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b30e-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7b30e-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7b30e-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7b30e-127">Schema Name</span></span>  <br/> |<span data-ttu-id="7b30e-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7b30e-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7b30e-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7b30e-129">Validation File</span></span>  <br/> |<span data-ttu-id="7b30e-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7b30e-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7b30e-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7b30e-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="7b30e-132">False</span><span class="sxs-lookup"><span data-stu-id="7b30e-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b30e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b30e-133">See also</span></span>



[<span data-ttu-id="7b30e-134">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="7b30e-134">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="7b30e-135">Buscar carpetas</span><span class="sxs-lookup"><span data-stu-id="7b30e-135">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="7b30e-136">Adición de las carpetas administradas</span><span class="sxs-lookup"><span data-stu-id="7b30e-136">Adding Managed Folders</span></span>](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

