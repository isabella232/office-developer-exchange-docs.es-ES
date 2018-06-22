---
title: ArchiveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c2172e61-876a-4f76-bc9c-263c8be11429
description: El elemento ArchiveItem contiene el identificador de la carpeta de origen y una matriz de identificadores de elemento para el elemento de archivo asociado.
ms.openlocfilehash: 7f2d79f5a9e6798fafcf64e8b1bb680390800992
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763546"
---
# <a name="archiveitem"></a><span data-ttu-id="c96b4-103">ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="c96b4-103">ArchiveItem</span></span>

<span data-ttu-id="c96b4-104">El elemento **ArchiveItem** contiene el identificador de la carpeta de origen y una matriz de identificadores de elemento para el elemento de archivo asociado.</span><span class="sxs-lookup"><span data-stu-id="c96b4-104">The **ArchiveItem** element contains the source folder Id and an array of item Ids for the associated archive item.</span></span> 
  
```XML
<ArchiveItem>
   <ArchiveSourceFolderId/>
   <ItemIds/>
</ArchiveItem>
```

 <span data-ttu-id="c96b4-105">**ArchiveItemType**</span><span class="sxs-lookup"><span data-stu-id="c96b4-105">**ArchiveItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c96b4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c96b4-106">Attributes and elements</span></span>

<span data-ttu-id="c96b4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c96b4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c96b4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c96b4-108">Attributes</span></span>

<span data-ttu-id="c96b4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c96b4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c96b4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c96b4-110">Child elements</span></span>

<span data-ttu-id="c96b4-111">[ArchiveSourceFolderId](archivesourcefolderid.md) | [ItemID](itemids.md)</span><span class="sxs-lookup"><span data-stu-id="c96b4-111">[ArchiveSourceFolderId](archivesourcefolderid.md) | [ItemIds](itemids.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c96b4-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c96b4-112">Parent elements</span></span>

<span data-ttu-id="c96b4-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c96b4-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c96b4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c96b4-114">Remarks</span></span>

<span data-ttu-id="c96b4-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c96b4-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c96b4-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c96b4-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c96b4-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c96b4-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c96b4-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c96b4-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c96b4-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c96b4-119">Schema name</span></span>  <br/> |<span data-ttu-id="c96b4-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c96b4-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c96b4-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c96b4-121">Validation file</span></span>  <br/> |<span data-ttu-id="c96b4-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c96b4-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c96b4-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c96b4-123">Can be empty</span></span>  <br/> |<span data-ttu-id="c96b4-124">falso</span><span class="sxs-lookup"><span data-stu-id="c96b4-124">false</span></span>  <br/> |
   

