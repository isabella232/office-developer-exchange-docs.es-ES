---
title: MarkAllItemsAsRead
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22244afb-99ec-41b4-8f73-3fbccd56d1ab
description: El elemento MarkAllItemsAsRead contiene la solicitud para marcar todos los elementos de una carpeta como leídos.
ms.openlocfilehash: 9d7eb8eb7194cb5d77e909dc08abfb70e2385d56
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836346"
---
# <a name="markallitemsasread"></a><span data-ttu-id="14c2e-103">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="14c2e-103">MarkAllItemsAsRead</span></span>

<span data-ttu-id="14c2e-104">El elemento **MarkAllItemsAsRead** contiene la solicitud para marcar todos los elementos de una carpeta como leídos.</span><span class="sxs-lookup"><span data-stu-id="14c2e-104">The **MarkAllItemsAsRead** element contains the request to mark all the items in a folder as read.</span></span> 
  
```XML
<MarkAllItemsAsRead>
   <ReadFlag/>
   <SuppressReadReceipts/>
   <FolderIds/>
</MarkAllItemsAsRead>
```

 <span data-ttu-id="14c2e-105">**MarkAllItemsAsReadType**</span><span class="sxs-lookup"><span data-stu-id="14c2e-105">**MarkAllItemsAsReadType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="14c2e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="14c2e-106">Attributes and elements</span></span>

<span data-ttu-id="14c2e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="14c2e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="14c2e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="14c2e-108">Attributes</span></span>

<span data-ttu-id="14c2e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="14c2e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="14c2e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="14c2e-110">Child elements</span></span>

<span data-ttu-id="14c2e-111">[ReadFlag](readflag.md) | [SuppressReadReceipts](suppressreadreceipts.md) | [FolderIds](folderids.md)</span><span class="sxs-lookup"><span data-stu-id="14c2e-111">[ReadFlag](readflag.md) | [SuppressReadReceipts](suppressreadreceipts.md) | [FolderIds](folderids.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="14c2e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="14c2e-112">Parent elements</span></span>

<span data-ttu-id="14c2e-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="14c2e-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="14c2e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="14c2e-114">Remarks</span></span>

<span data-ttu-id="14c2e-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="14c2e-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="14c2e-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="14c2e-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="14c2e-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="14c2e-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14c2e-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="14c2e-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="14c2e-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="14c2e-119">Schema name</span></span>  <br/> |<span data-ttu-id="14c2e-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="14c2e-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="14c2e-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="14c2e-121">Validation file</span></span>  <br/> |<span data-ttu-id="14c2e-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="14c2e-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="14c2e-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="14c2e-123">Can be empty</span></span>  <br/> ||
   

