---
title: UnreadCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnreadCount
api_type:
- schema
ms.assetid: 53b22647-1453-4707-9ea0-6a8369748d56
description: El elemento UnreadCount contiene el número de elementos no leídos dentro de una carpeta.
ms.openlocfilehash: 72e5d47eac7618408e46ad11eb19eaebf9835502
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467224"
---
# <a name="unreadcount"></a><span data-ttu-id="541e1-103">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="541e1-103">UnreadCount</span></span>

<span data-ttu-id="541e1-104">El elemento **UnreadCount** contiene el número de elementos no leídos dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="541e1-104">The **UnreadCount** element contains the count of unread items within a folder.</span></span> 
  
```XML
<UnreadCount/>
```

 <span data-ttu-id="541e1-105">**XS: int**</span><span class="sxs-lookup"><span data-stu-id="541e1-105">**xs:int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="541e1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="541e1-106">Attributes and elements</span></span>

<span data-ttu-id="541e1-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="541e1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="541e1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="541e1-108">Attributes</span></span>

<span data-ttu-id="541e1-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="541e1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="541e1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="541e1-110">Child elements</span></span>

<span data-ttu-id="541e1-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="541e1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="541e1-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="541e1-112">Parent elements</span></span>

|<span data-ttu-id="541e1-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="541e1-113">**Element**</span></span>|<span data-ttu-id="541e1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="541e1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="541e1-115">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="541e1-115">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="541e1-116">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="541e1-116">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="541e1-117">Folder</span><span class="sxs-lookup"><span data-stu-id="541e1-117">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="541e1-118">Representa una carpeta en un buzón.</span><span class="sxs-lookup"><span data-stu-id="541e1-118">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="541e1-119">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="541e1-119">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="541e1-120">Representa un evento en el que se modifica un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="541e1-120">Represents an event where an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="541e1-121">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="541e1-121">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="541e1-122">Representa una carpeta de búsqueda en un buzón.</span><span class="sxs-lookup"><span data-stu-id="541e1-122">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="541e1-123">Hubiera</span><span class="sxs-lookup"><span data-stu-id="541e1-123">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="541e1-124">Representa una carpeta de tareas en un buzón.</span><span class="sxs-lookup"><span data-stu-id="541e1-124">Represents a task folder in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="541e1-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="541e1-125">Text value</span></span>

<span data-ttu-id="541e1-126">El valor de texto representa un valor entero.</span><span class="sxs-lookup"><span data-stu-id="541e1-126">The text value represents an integer value.</span></span> <span data-ttu-id="541e1-127">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="541e1-127">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="541e1-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="541e1-128">Remarks</span></span>

<span data-ttu-id="541e1-129">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="541e1-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="541e1-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="541e1-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="541e1-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="541e1-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="541e1-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="541e1-132">Schema Name</span></span>  <br/> |<span data-ttu-id="541e1-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="541e1-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="541e1-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="541e1-134">Validation File</span></span>  <br/> |<span data-ttu-id="541e1-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="541e1-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="541e1-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="541e1-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="541e1-137">Falso</span><span class="sxs-lookup"><span data-stu-id="541e1-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="541e1-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="541e1-138">See also</span></span>



- [<span data-ttu-id="541e1-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="541e1-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

