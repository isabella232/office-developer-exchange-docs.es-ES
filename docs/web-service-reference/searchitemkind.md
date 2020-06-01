---
title: SearchItemKind
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89513c26-b751-4619-a300-0ed8f55b0102
description: El elemento SearchItemKind indica el tipo de elementos que se buscan en una operación de FindMailboxStatisticsByKeyword.
ms.openlocfilehash: e0625ac169c3083702494c094da15d38d220fe67
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464003"
---
# <a name="searchitemkind"></a><span data-ttu-id="b1714-103">SearchItemKind</span><span class="sxs-lookup"><span data-stu-id="b1714-103">SearchItemKind</span></span>

<span data-ttu-id="b1714-104">El elemento **SearchItemKind** indica el tipo de elementos que se buscan en una operación de **FindMailboxStatisticsByKeyword** .</span><span class="sxs-lookup"><span data-stu-id="b1714-104">The **SearchItemKind** element indicates the type of items that are searched for a **FindMailboxStatisticsByKeyword** operation.</span></span> 
  
```XML
<SearchItemKind>Email | Meetings | Tasks | Notes | Docs | Journals | Contacts | Im | Voicemail | Faxes | Posts | Rssfeeds</SearchItemKind>
```

 <span data-ttu-id="b1714-105">**SearchItemKindType**</span><span class="sxs-lookup"><span data-stu-id="b1714-105">**SearchItemKindType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b1714-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b1714-106">Attributes and elements</span></span>

<span data-ttu-id="b1714-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b1714-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1714-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b1714-108">Attributes</span></span>

<span data-ttu-id="b1714-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b1714-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1714-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b1714-110">Child elements</span></span>

<span data-ttu-id="b1714-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b1714-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b1714-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b1714-112">Parent elements</span></span>

[<span data-ttu-id="b1714-113">MessageTypes</span><span class="sxs-lookup"><span data-stu-id="b1714-113">MessageTypes</span></span>](messagetypes.md)
  
## <a name="text-value"></a><span data-ttu-id="b1714-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b1714-114">Text value</span></span>

<span data-ttu-id="b1714-115">El valor de texto del elemento **SearchItemKind** es el tipo de elemento en el que se buscan palabras clave.</span><span class="sxs-lookup"><span data-stu-id="b1714-115">The text value of the **SearchItemKind** element is the type of item that is searched for keywords.</span></span> <span data-ttu-id="b1714-116">La lista siguiente contiene los valores de texto que se pueden usar en el elemento **SearchItemKind** .</span><span class="sxs-lookup"><span data-stu-id="b1714-116">The following list contains the text values that can be used in the **SearchItemKind** element.</span></span> 
  
- <span data-ttu-id="b1714-117">**Email** -indica que se buscan palabras clave en los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b1714-117">**Email** - Indicates that email messages are searched for keywords.</span></span> 
    
- <span data-ttu-id="b1714-118">**Reuniones** : indica que se buscan palabras clave en las reuniones.</span><span class="sxs-lookup"><span data-stu-id="b1714-118">**Meetings** - Indicates that meetings are searched for keywords.</span></span> 
    
- <span data-ttu-id="b1714-119">**Tareas** : indica que se buscan palabras clave en las tareas.</span><span class="sxs-lookup"><span data-stu-id="b1714-119">**Tasks** - Indicates that tasks are searched for keywords.</span></span> 
    
- <span data-ttu-id="b1714-120">**Notas** : indica que se buscan palabras clave en las notas.</span><span class="sxs-lookup"><span data-stu-id="b1714-120">**Notes** - Indicates that notes are searched for keywords.</span></span> 
    
- <span data-ttu-id="b1714-121">**Docs** : indica que se buscan palabras clave en los documentos.</span><span class="sxs-lookup"><span data-stu-id="b1714-121">**Docs** - Indicates that documents are searched for keywords.</span></span> 
    
- <span data-ttu-id="b1714-122">**Diarios** : indica que se buscan palabras clave en los diarios.</span><span class="sxs-lookup"><span data-stu-id="b1714-122">**Journals** - Indicates that journals are searched for keywords.</span></span> 
    
- <span data-ttu-id="b1714-123">**Contacts** : indica que se buscan palabras clave en los contactos.</span><span class="sxs-lookup"><span data-stu-id="b1714-123">**Contacts** - Indicates that contacts are searched for keywords.</span></span> 
    
- <span data-ttu-id="b1714-124">**Mi** : indica que se buscan palabras clave en los mensajes instantáneos.</span><span class="sxs-lookup"><span data-stu-id="b1714-124">**Im** - Indicates that instant messages are searched for keywords.</span></span> 
    
- <span data-ttu-id="b1714-125">Correo **de voz: indica** que se buscan palabras clave en los correos de voz.</span><span class="sxs-lookup"><span data-stu-id="b1714-125">**Voicemail** - Indicates that voice mails are searched for keywords.</span></span> 
    
- <span data-ttu-id="b1714-126">**Faxes** : indica que se buscan palabras clave en los faxes.</span><span class="sxs-lookup"><span data-stu-id="b1714-126">**Faxes** - Indicates that faxes are searched for keywords.</span></span> 
    
- <span data-ttu-id="b1714-127">**Postes** : indica que se buscan palabras clave en las publicaciones.</span><span class="sxs-lookup"><span data-stu-id="b1714-127">**Posts** - Indicates that posts are searched for keywords.</span></span> 
    
- <span data-ttu-id="b1714-128">**RSSFeeds** : indica que se buscan palabras clave en las fuentes RSS.</span><span class="sxs-lookup"><span data-stu-id="b1714-128">**Rssfeeds** - Indicates that RSS feeds are searched for keywords.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b1714-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1714-129">Remarks</span></span>

<span data-ttu-id="b1714-130">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b1714-130">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b1714-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b1714-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b1714-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b1714-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1714-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1714-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b1714-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b1714-134">Schema name</span></span>  <br/> |<span data-ttu-id="b1714-135">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b1714-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="b1714-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b1714-136">Validation file</span></span>  <br/> |<span data-ttu-id="b1714-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b1714-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b1714-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b1714-138">Can be empty</span></span>  <br/> ||
   

