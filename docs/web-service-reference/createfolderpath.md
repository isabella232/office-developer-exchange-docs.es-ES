---
title: CreateFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282576cb-a921-49f7-8748-64158fd50c41
description: El elemento CreateFolderPath se usa para crear una ruta de acceso de carpeta e incluye un identificador de carpeta principal y una ruta de acceso de carpeta relativa.
ms.openlocfilehash: e6ce6c9b6e12a6a0fb6792b63368a79c87d06f07
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457539"
---
# <a name="createfolderpath"></a><span data-ttu-id="8f959-103">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="8f959-103">CreateFolderPath</span></span>

<span data-ttu-id="8f959-104">El elemento **CreateFolderPath** se usa para crear una ruta de acceso de carpeta e incluye un identificador de carpeta principal y una ruta de acceso de carpeta relativa.</span><span class="sxs-lookup"><span data-stu-id="8f959-104">The **CreateFolderPath** element is used to create a folder path and includes a parent folder Id and a relative folder path.</span></span> 
  
```XML
<CreateFolderPath>
   <ParentFolderId/>
   <RelativeFolderPath/>
</CreateFolderPath>
```

 <span data-ttu-id="8f959-105">**CreateFolderPathType**</span><span class="sxs-lookup"><span data-stu-id="8f959-105">**CreateFolderPathType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8f959-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8f959-106">Attributes and elements</span></span>

<span data-ttu-id="8f959-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8f959-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8f959-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8f959-108">Attributes</span></span>

<span data-ttu-id="8f959-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8f959-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8f959-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8f959-110">Child elements</span></span>

<span data-ttu-id="8f959-111">[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)  |  [RelativeFolderPath](relativefolderpath.md)</span><span class="sxs-lookup"><span data-stu-id="8f959-111">[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) | [RelativeFolderPath](relativefolderpath.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8f959-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8f959-112">Parent elements</span></span>

<span data-ttu-id="8f959-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8f959-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8f959-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8f959-114">Remarks</span></span>

<span data-ttu-id="8f959-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8f959-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8f959-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="8f959-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8f959-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8f959-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8f959-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f959-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8f959-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8f959-119">Schema name</span></span>  <br/> |<span data-ttu-id="8f959-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="8f959-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8f959-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8f959-121">Validation file</span></span>  <br/> |<span data-ttu-id="8f959-122">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="8f959-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8f959-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8f959-123">Can be empty</span></span>  <br/> |<span data-ttu-id="8f959-124">false</span><span class="sxs-lookup"><span data-stu-id="8f959-124">false</span></span>  <br/> |
   

