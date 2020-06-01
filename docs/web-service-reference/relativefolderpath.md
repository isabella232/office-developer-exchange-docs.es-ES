---
title: RelativeFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54e3ba52-08a6-4d48-8a44-6fd5fdbffb25
description: El elemento RelativeFolderPath contiene una matriz de carpetas que indican la ruta de acceso de la carpeta relativa a la ruta de acceso a la carpeta que se va a crear.
ms.openlocfilehash: 8a0fc0020943afdbe6cd4c79d51d61337f8dd329
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457161"
---
# <a name="relativefolderpath"></a><span data-ttu-id="64023-103">RelativeFolderPath</span><span class="sxs-lookup"><span data-stu-id="64023-103">RelativeFolderPath</span></span>

<span data-ttu-id="64023-104">El elemento **RelativeFolderPath** contiene una matriz de carpetas que indican la ruta de acceso de la carpeta relativa a la ruta de acceso a la carpeta que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="64023-104">The **RelativeFolderPath** element contains an array of folders that indicate the relative folder path of the folder path to be created.</span></span> 
  
```XML
<RelativeFolderPath>
   <Folder/>
   <CalendarFolder/>
   <ContactsFolder/>
   <SearchFolder/>
   <TasksFolder/>
</RelativeFolderPath>
```

 <span data-ttu-id="64023-105">**NonEmptyArrayOfFoldersType**</span><span class="sxs-lookup"><span data-stu-id="64023-105">**NonEmptyArrayOfFoldersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="64023-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="64023-106">Attributes and elements</span></span>

<span data-ttu-id="64023-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="64023-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64023-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="64023-108">Attributes</span></span>

<span data-ttu-id="64023-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="64023-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="64023-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="64023-110">Child elements</span></span>

<span data-ttu-id="64023-111">[Carpeta](folder.md)  |  [Hubiera](calendarfolder.md)  |  [Hubiera](contactsfolder.md)  |  [SearchFolder](searchfolder.md)  |  [Hubiera](tasksfolder.md)</span><span class="sxs-lookup"><span data-stu-id="64023-111">[Folder](folder.md) | [CalendarFolder](calendarfolder.md) | [ContactsFolder](contactsfolder.md) | [SearchFolder](searchfolder.md) | [TasksFolder](tasksfolder.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="64023-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="64023-112">Parent elements</span></span>

[<span data-ttu-id="64023-113">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="64023-113">CreateFolderPath</span></span>](createfolderpath.md)
  
## <a name="remarks"></a><span data-ttu-id="64023-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="64023-114">Remarks</span></span>

<span data-ttu-id="64023-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="64023-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="64023-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="64023-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="64023-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="64023-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64023-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="64023-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="64023-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="64023-119">Schema name</span></span>  <br/> |<span data-ttu-id="64023-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="64023-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="64023-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="64023-121">Validation file</span></span>  <br/> |<span data-ttu-id="64023-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="64023-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="64023-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="64023-123">Can be empty</span></span>  <br/> ||
   

