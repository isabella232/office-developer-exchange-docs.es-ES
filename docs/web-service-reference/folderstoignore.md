---
title: FoldersToIgnore
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b5d18516-a617-4daf-8baf-c7ce29c76f6b
description: El elemento FoldersToIgnore identifica una lista de carpetas que se ignoran al obtener elementos en una conversación. No se devuelven todos los elementos de conversación en las carpetas omitidas en una respuesta GetConversationItems.
ms.openlocfilehash: 07813a54a9a3afa3de23ae94f1c9b191d1cb6fac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44453360"
---
# <a name="folderstoignore"></a><span data-ttu-id="d43db-104">FoldersToIgnore</span><span class="sxs-lookup"><span data-stu-id="d43db-104">FoldersToIgnore</span></span>

<span data-ttu-id="d43db-105">El elemento **FoldersToIgnore** identifica una lista de carpetas que se ignoran al obtener elementos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="d43db-105">The **FoldersToIgnore** element identifies a list of folders that are ignored when getting items in a conversation.</span></span> <span data-ttu-id="d43db-106">No se devuelven todos los elementos de conversación en las carpetas omitidas en una respuesta **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="d43db-106">All conversation items in the ignored folders are not returned in a **GetConversationItems** response.</span></span> 
  
```XML
<FoldersToIgnore>
   <FolderId/>
   <DistinguishedFolderId/>
</FoldersToIgnore>
```

 <span data-ttu-id="d43db-107">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="d43db-107">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d43db-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d43db-108">Attributes and elements</span></span>

<span data-ttu-id="d43db-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d43db-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d43db-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="d43db-110">Attributes</span></span>

<span data-ttu-id="d43db-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d43db-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d43db-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d43db-112">Child elements</span></span>

<span data-ttu-id="d43db-113">[FolderId](folderid.md)  |  [DistinguishedFolderId](distinguishedfolderid.md)</span><span class="sxs-lookup"><span data-stu-id="d43db-113">[FolderId](folderid.md) | [DistinguishedFolderId](distinguishedfolderid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d43db-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d43db-114">Parent elements</span></span>

[<span data-ttu-id="d43db-115">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="d43db-115">GetConversationItems</span></span>](getconversationitems.md)
  
## <a name="remarks"></a><span data-ttu-id="d43db-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d43db-116">Remarks</span></span>

<span data-ttu-id="d43db-117">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d43db-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d43db-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d43db-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d43db-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d43db-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d43db-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="d43db-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d43db-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d43db-121">Schema name</span></span>  <br/> |<span data-ttu-id="d43db-122">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d43db-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="d43db-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d43db-123">Validation file</span></span>  <br/> |<span data-ttu-id="d43db-124">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d43db-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d43db-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d43db-125">Can be empty</span></span>  <br/> |<span data-ttu-id="d43db-126">false</span><span class="sxs-lookup"><span data-stu-id="d43db-126">false</span></span>  <br/> |
   

