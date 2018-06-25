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
description: El elemento UnreadCount contiene el recuento de elementos no leídos dentro de una carpeta.
ms.openlocfilehash: fbe887f8f6d83fbcf48ed9593b3d19322a7f48be
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840790"
---
# <a name="unreadcount"></a><span data-ttu-id="30e33-103">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="30e33-103">UnreadCount</span></span>

<span data-ttu-id="30e33-104">El elemento **UnreadCount** contiene el recuento de elementos no leídos dentro de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="30e33-104">The **UnreadCount** element contains the count of unread items within a folder.</span></span> 
  
```XML
<UnreadCount/>
```

 <span data-ttu-id="30e33-105">**xs: int**</span><span class="sxs-lookup"><span data-stu-id="30e33-105">**xs:int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="30e33-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="30e33-106">Attributes and elements</span></span>

<span data-ttu-id="30e33-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="30e33-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="30e33-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="30e33-108">Attributes</span></span>

<span data-ttu-id="30e33-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="30e33-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="30e33-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="30e33-110">Child elements</span></span>

<span data-ttu-id="30e33-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="30e33-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="30e33-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="30e33-112">Parent elements</span></span>

|<span data-ttu-id="30e33-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="30e33-113">**Element**</span></span>|<span data-ttu-id="30e33-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="30e33-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30e33-115">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="30e33-115">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="30e33-116">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="30e33-116">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="30e33-117">Folder</span><span class="sxs-lookup"><span data-stu-id="30e33-117">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="30e33-118">Representa una carpeta en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="30e33-118">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="30e33-119">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="30e33-119">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="30e33-120">Representa un evento que se modifica una carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="30e33-120">Represents an event where an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="30e33-121">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="30e33-121">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="30e33-122">Representa una carpeta de búsqueda en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="30e33-122">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="30e33-123">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="30e33-123">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="30e33-124">Representa una carpeta de tareas en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="30e33-124">Represents a task folder in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="30e33-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="30e33-125">Text value</span></span>

<span data-ttu-id="30e33-126">El valor de texto representa un valor entero.</span><span class="sxs-lookup"><span data-stu-id="30e33-126">The text value represents an integer value.</span></span> <span data-ttu-id="30e33-127">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="30e33-127">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="30e33-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="30e33-128">Remarks</span></span>

<span data-ttu-id="30e33-129">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="30e33-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="30e33-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="30e33-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30e33-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="30e33-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="30e33-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="30e33-132">Schema Name</span></span>  <br/> |<span data-ttu-id="30e33-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="30e33-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="30e33-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="30e33-134">Validation File</span></span>  <br/> |<span data-ttu-id="30e33-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="30e33-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="30e33-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="30e33-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="30e33-137">False</span><span class="sxs-lookup"><span data-stu-id="30e33-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30e33-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="30e33-138">See also</span></span>



- [<span data-ttu-id="30e33-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="30e33-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

