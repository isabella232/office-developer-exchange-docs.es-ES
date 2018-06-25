---
title: MovedItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7d5425ab-1e75-43d1-b801-802ff5139df6
description: El elemento MovedItemId especifica el identificador del elemento que se ha movido por la operación de MarkAsJunk.
ms.openlocfilehash: 17e20e8ca81f97b419fc4a2b413e21322e828ec9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836484"
---
# <a name="moveditemid"></a><span data-ttu-id="e8284-103">MovedItemId</span><span class="sxs-lookup"><span data-stu-id="e8284-103">MovedItemId</span></span>

<span data-ttu-id="e8284-104">El elemento **MovedItemId** especifica el identificador del elemento que se ha movido por la operación de **MarkAsJunk** .</span><span class="sxs-lookup"><span data-stu-id="e8284-104">The **MovedItemId** element specifies the identifier of the item that was moved by the **MarkAsJunk** operation.</span></span> 
  
```XML
<MovedItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="e8284-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="e8284-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e8284-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e8284-106">Attributes and elements</span></span>

<span data-ttu-id="e8284-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e8284-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8284-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e8284-108">Attributes</span></span>

|<span data-ttu-id="e8284-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="e8284-109">**Attribute**</span></span>|<span data-ttu-id="e8284-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8284-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8284-111">Id</span><span class="sxs-lookup"><span data-stu-id="e8284-111">Id</span></span>  <br/> |<span data-ttu-id="e8284-112">El valor del atributo **Id** es el identificador de elemento del elemento que se mueve por la operación de **MarkAsJunk** .</span><span class="sxs-lookup"><span data-stu-id="e8284-112">The value of the **Id** attribute is the item identifier of the item that is moved by the **MarkAsJunk** operation.</span></span> <span data-ttu-id="e8284-113">El identificador del elemento permanecerá igual después del movimiento.</span><span class="sxs-lookup"><span data-stu-id="e8284-113">The item identifier will remain the same after the move.</span></span>  <br/> |
|<span data-ttu-id="e8284-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="e8284-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="e8284-115">El valor del atributo **ChangeKey** es la clave de cambio del elemento que se ha movido.</span><span class="sxs-lookup"><span data-stu-id="e8284-115">The value of the **ChangeKey** attribute is the change key of the moved item.</span></span> <span data-ttu-id="e8284-116">La clave de cambio cambia después de que el elemento se mueve por la operación de **MarkAsJunk** .</span><span class="sxs-lookup"><span data-stu-id="e8284-116">The change key changes after the item is moved by the **MarkAsJunk** operation.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e8284-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e8284-117">Child elements</span></span>

<span data-ttu-id="e8284-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e8284-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e8284-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e8284-119">Parent elements</span></span>

[<span data-ttu-id="e8284-120">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e8284-120">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
  
## <a name="remarks"></a><span data-ttu-id="e8284-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8284-121">Remarks</span></span>

<span data-ttu-id="e8284-122">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e8284-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e8284-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e8284-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8284-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e8284-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8284-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e8284-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e8284-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e8284-126">Schema name</span></span>  <br/> |<span data-ttu-id="e8284-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e8284-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e8284-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e8284-128">Validation file</span></span>  <br/> |<span data-ttu-id="e8284-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e8284-129">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e8284-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e8284-130">Can be empty</span></span>  <br/> ||
   

