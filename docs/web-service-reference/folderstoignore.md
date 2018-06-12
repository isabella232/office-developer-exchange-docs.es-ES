---
title: FoldersToIgnore
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b5d18516-a617-4daf-8baf-c7ce29c76f6b
description: El elemento FoldersToIgnore identifica una lista de carpetas que se pasan por alto al obtener elementos en una conversación. Todos los elementos de conversación de las carpetas omitidos no se devuelven en una respuesta de GetConversationItems.
ms.openlocfilehash: 96c094996c601e685dc1c7e6b869a790ce7d74a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764696"
---
# <a name="folderstoignore"></a><span data-ttu-id="261a1-104">FoldersToIgnore</span><span class="sxs-lookup"><span data-stu-id="261a1-104">FoldersToIgnore</span></span>

<span data-ttu-id="261a1-105">El elemento **FoldersToIgnore** identifica una lista de carpetas que se pasan por alto al obtener elementos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="261a1-105">The **FoldersToIgnore** element identifies a list of folders that are ignored when getting items in a conversation.</span></span> <span data-ttu-id="261a1-106">Todos los elementos de conversación de las carpetas omitidos no se devuelven en una respuesta de **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="261a1-106">All conversation items in the ignored folders are not returned in a **GetConversationItems** response.</span></span> 
  
```XML
<FoldersToIgnore>
   <FolderId/>
   <DistinguishedFolderId/>
</FoldersToIgnore>
```

 <span data-ttu-id="261a1-107">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="261a1-107">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="261a1-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="261a1-108">Attributes and elements</span></span>

<span data-ttu-id="261a1-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="261a1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="261a1-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="261a1-110">Attributes</span></span>

<span data-ttu-id="261a1-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="261a1-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="261a1-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="261a1-112">Child elements</span></span>

<span data-ttu-id="261a1-113">[FolderId](folderid.md) | [DistinguishedFolderId](distinguishedfolderid.md)</span><span class="sxs-lookup"><span data-stu-id="261a1-113">[FolderId](folderid.md) | [DistinguishedFolderId](distinguishedfolderid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="261a1-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="261a1-114">Parent elements</span></span>

[<span data-ttu-id="261a1-115">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="261a1-115">GetConversationItems</span></span>](getconversationitems.md)
  
## <a name="remarks"></a><span data-ttu-id="261a1-116">Notas</span><span class="sxs-lookup"><span data-stu-id="261a1-116">Remarks</span></span>

<span data-ttu-id="261a1-117">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="261a1-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="261a1-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="261a1-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="261a1-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="261a1-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="261a1-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="261a1-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="261a1-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="261a1-121">Schema name</span></span>  <br/> |<span data-ttu-id="261a1-122">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="261a1-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="261a1-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="261a1-123">Validation file</span></span>  <br/> |<span data-ttu-id="261a1-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="261a1-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="261a1-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="261a1-125">Can be empty</span></span>  <br/> |<span data-ttu-id="261a1-126">falso</span><span class="sxs-lookup"><span data-stu-id="261a1-126">false</span></span>  <br/> |
   

