---
title: RelativeFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54e3ba52-08a6-4d48-8a44-6fd5fdbffb25
description: El elemento RelativeFolderPath contiene una matriz de las carpetas que indique la ruta de acceso relativa de la ruta de acceso de la carpeta que se creará.
ms.openlocfilehash: f568d282e47a41c0aaf6d70ef383e5ef3e2b54bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837051"
---
# <a name="relativefolderpath"></a><span data-ttu-id="3f7d3-103">RelativeFolderPath</span><span class="sxs-lookup"><span data-stu-id="3f7d3-103">RelativeFolderPath</span></span>

<span data-ttu-id="3f7d3-104">El elemento **RelativeFolderPath** contiene una matriz de las carpetas que indique la ruta de acceso relativa de la ruta de acceso de la carpeta que se creará.</span><span class="sxs-lookup"><span data-stu-id="3f7d3-104">The **RelativeFolderPath** element contains an array of folders that indicate the relative folder path of the folder path to be created.</span></span> 
  
```XML
<RelativeFolderPath>
   <Folder/>
   <CalendarFolder/>
   <ContactsFolder/>
   <SearchFolder/>
   <TasksFolder/>
</RelativeFolderPath>
```

 <span data-ttu-id="3f7d3-105">**NonEmptyArrayOfFoldersType**</span><span class="sxs-lookup"><span data-stu-id="3f7d3-105">**NonEmptyArrayOfFoldersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3f7d3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3f7d3-106">Attributes and elements</span></span>

<span data-ttu-id="3f7d3-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3f7d3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3f7d3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3f7d3-108">Attributes</span></span>

<span data-ttu-id="3f7d3-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3f7d3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3f7d3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3f7d3-110">Child elements</span></span>

<span data-ttu-id="3f7d3-111">[Carpeta](folder.md) | [CalendarFolder](calendarfolder.md) | [ContactsFolder](contactsfolder.md) | [SearchFolder](searchfolder.md) | [TasksFolder](tasksfolder.md)</span><span class="sxs-lookup"><span data-stu-id="3f7d3-111">[Folder](folder.md) | [CalendarFolder](calendarfolder.md) | [ContactsFolder](contactsfolder.md) | [SearchFolder](searchfolder.md) | [TasksFolder](tasksfolder.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3f7d3-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3f7d3-112">Parent elements</span></span>

[<span data-ttu-id="3f7d3-113">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="3f7d3-113">CreateFolderPath</span></span>](createfolderpath.md)
  
## <a name="remarks"></a><span data-ttu-id="3f7d3-114">Notas</span><span class="sxs-lookup"><span data-stu-id="3f7d3-114">Remarks</span></span>

<span data-ttu-id="3f7d3-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3f7d3-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3f7d3-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3f7d3-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3f7d3-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3f7d3-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f7d3-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3f7d3-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3f7d3-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3f7d3-119">Schema name</span></span>  <br/> |<span data-ttu-id="3f7d3-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3f7d3-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3f7d3-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3f7d3-121">Validation file</span></span>  <br/> |<span data-ttu-id="3f7d3-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3f7d3-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3f7d3-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3f7d3-123">Can be empty</span></span>  <br/> ||
   

