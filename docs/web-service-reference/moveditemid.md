---
title: MovedItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7d5425ab-1e75-43d1-b801-802ff5139df6
description: El elemento MovedItemId especifica el identificador del elemento movido por la operación MarkAsJunk.
ms.openlocfilehash: 5cf8800ec672278691348bbcd8c6c8cc7a12905b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468617"
---
# <a name="moveditemid"></a><span data-ttu-id="5ea94-103">MovedItemId</span><span class="sxs-lookup"><span data-stu-id="5ea94-103">MovedItemId</span></span>

<span data-ttu-id="5ea94-104">El elemento **MovedItemId** especifica el identificador del elemento movido por la operación **MarkAsJunk** .</span><span class="sxs-lookup"><span data-stu-id="5ea94-104">The **MovedItemId** element specifies the identifier of the item that was moved by the **MarkAsJunk** operation.</span></span> 
  
```XML
<MovedItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="5ea94-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="5ea94-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5ea94-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5ea94-106">Attributes and elements</span></span>

<span data-ttu-id="5ea94-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5ea94-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5ea94-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5ea94-108">Attributes</span></span>

|<span data-ttu-id="5ea94-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="5ea94-109">**Attribute**</span></span>|<span data-ttu-id="5ea94-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5ea94-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5ea94-111">Id</span><span class="sxs-lookup"><span data-stu-id="5ea94-111">Id</span></span>  <br/> |<span data-ttu-id="5ea94-112">El valor del atributo **ID** es el identificador de elemento del elemento que se mueve mediante la operación **MarkAsJunk** .</span><span class="sxs-lookup"><span data-stu-id="5ea94-112">The value of the **Id** attribute is the item identifier of the item that is moved by the **MarkAsJunk** operation.</span></span> <span data-ttu-id="5ea94-113">El identificador de elemento permanecerá igual después del movimiento.</span><span class="sxs-lookup"><span data-stu-id="5ea94-113">The item identifier will remain the same after the move.</span></span>  <br/> |
|<span data-ttu-id="5ea94-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="5ea94-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="5ea94-115">El valor del atributo **changekey** es la clave de cambio del elemento que se ha movido.</span><span class="sxs-lookup"><span data-stu-id="5ea94-115">The value of the **ChangeKey** attribute is the change key of the moved item.</span></span> <span data-ttu-id="5ea94-116">La clave de cambio cambia después de que la operación **MarkAsJunk** mueva el elemento.</span><span class="sxs-lookup"><span data-stu-id="5ea94-116">The change key changes after the item is moved by the **MarkAsJunk** operation.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5ea94-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5ea94-117">Child elements</span></span>

<span data-ttu-id="5ea94-118">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5ea94-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5ea94-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5ea94-119">Parent elements</span></span>

[<span data-ttu-id="5ea94-120">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5ea94-120">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
  
## <a name="remarks"></a><span data-ttu-id="5ea94-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5ea94-121">Remarks</span></span>

<span data-ttu-id="5ea94-122">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5ea94-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5ea94-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5ea94-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5ea94-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5ea94-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5ea94-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ea94-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5ea94-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5ea94-126">Schema name</span></span>  <br/> |<span data-ttu-id="5ea94-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5ea94-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5ea94-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5ea94-128">Validation file</span></span>  <br/> |<span data-ttu-id="5ea94-129">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5ea94-129">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5ea94-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5ea94-130">Can be empty</span></span>  <br/> ||
   

