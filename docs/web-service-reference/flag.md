---
title: Anotación
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b47bc74-a60d-4308-8674-5d52444a1753
description: El elemento Flag especifica una marca en un elemento de buzón.
ms.openlocfilehash: 7229a26181ee9baf80be5c32c0ef99483310ccb3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466265"
---
# <a name="flag"></a><span data-ttu-id="0ae30-103">Anotación</span><span class="sxs-lookup"><span data-stu-id="0ae30-103">Flag</span></span>

<span data-ttu-id="0ae30-104">El elemento **Flag** especifica una marca en un elemento de buzón.</span><span class="sxs-lookup"><span data-stu-id="0ae30-104">The **Flag** element specifies a flag on a mailbox item.</span></span> 
  
```XML
<Flag>
    <FlagStatus/>
    <StartDate/>
    <DueDate/>
    <CompleteDate/>
</Flag>
```

 <span data-ttu-id="0ae30-105">**FlagType**</span><span class="sxs-lookup"><span data-stu-id="0ae30-105">**FlagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0ae30-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0ae30-106">Attributes and elements</span></span>

<span data-ttu-id="0ae30-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0ae30-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0ae30-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0ae30-108">Attributes</span></span>

<span data-ttu-id="0ae30-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0ae30-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0ae30-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0ae30-110">Child elements</span></span>

|<span data-ttu-id="0ae30-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0ae30-111">**Element**</span></span>|<span data-ttu-id="0ae30-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ae30-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ae30-113">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="0ae30-113">FlagStatus</span></span>](flagstatus.md) <br/> |<span data-ttu-id="0ae30-114">Contiene el estado de marca agregada para los elementos de la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="0ae30-114">Contains the aggregated flag status for items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="0ae30-115">StartDate</span><span class="sxs-lookup"><span data-stu-id="0ae30-115">StartDate</span></span>](startdate.md) <br/> |<span data-ttu-id="0ae30-116">Representa la fecha de inicio de un elemento.</span><span class="sxs-lookup"><span data-stu-id="0ae30-116">Represents the start date of an item.</span></span>  <br/> |
|[<span data-ttu-id="0ae30-117">DueDate</span><span class="sxs-lookup"><span data-stu-id="0ae30-117">DueDate</span></span>](duedate.md) <br/> |<span data-ttu-id="0ae30-118">Representa la fecha en que vence un elemento.</span><span class="sxs-lookup"><span data-stu-id="0ae30-118">Represents the date when an item is due.</span></span>  <br/> |
|[<span data-ttu-id="0ae30-119">CompleteDate</span><span class="sxs-lookup"><span data-stu-id="0ae30-119">CompleteDate</span></span>](completedate.md) <br/> |<span data-ttu-id="0ae30-120">Representa la fecha en que se completó un elemento.</span><span class="sxs-lookup"><span data-stu-id="0ae30-120">Represents the date on which an item was completed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0ae30-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0ae30-121">Parent elements</span></span>

|<span data-ttu-id="0ae30-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0ae30-122">**Element**</span></span>|<span data-ttu-id="0ae30-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ae30-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ae30-124">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="0ae30-124">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="0ae30-125">Contiene una sola acción que se aplicará a una única conversación.</span><span class="sxs-lookup"><span data-stu-id="0ae30-125">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="0ae30-126">Elemento</span><span class="sxs-lookup"><span data-stu-id="0ae30-126">Item</span></span>](item.md) <br/> |<span data-ttu-id="0ae30-127">Representa un elemento genérico del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ae30-127">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ae30-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0ae30-128">Remarks</span></span>

<span data-ttu-id="0ae30-129">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0ae30-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0ae30-130">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ae30-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ae30-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0ae30-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ae30-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ae30-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0ae30-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0ae30-133">Schema Name</span></span>  <br/> |<span data-ttu-id="0ae30-134">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="0ae30-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="0ae30-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0ae30-135">Validation File</span></span>  <br/> |<span data-ttu-id="0ae30-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="0ae30-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="0ae30-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0ae30-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0ae30-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ae30-138">See also</span></span>



- [<span data-ttu-id="0ae30-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0ae30-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

