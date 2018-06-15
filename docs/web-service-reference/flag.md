---
title: Marca
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b47bc74-a60d-4308-8674-5d52444a1753
description: El elemento de marca especifica una marca en un elemento de buzón de correo.
ms.openlocfilehash: f30f435e8f064d7165ae52de737bbd75b0546206
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764665"
---
# <a name="flag"></a><span data-ttu-id="e077e-103">Marca</span><span class="sxs-lookup"><span data-stu-id="e077e-103">Flag</span></span>

<span data-ttu-id="e077e-104">El elemento de **marca** especifica una marca en un elemento de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e077e-104">The **Flag** element specifies a flag on a mailbox item.</span></span> 
  
```XML
<Flag>
    <FlagStatus/>
    <StartDate/>
    <DueDate/>
    <CompleteDate/>
</Flag>
```

 <span data-ttu-id="e077e-105">**FlagType**</span><span class="sxs-lookup"><span data-stu-id="e077e-105">**FlagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e077e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e077e-106">Attributes and elements</span></span>

<span data-ttu-id="e077e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e077e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e077e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e077e-108">Attributes</span></span>

<span data-ttu-id="e077e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e077e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e077e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e077e-110">Child elements</span></span>

|<span data-ttu-id="e077e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e077e-111">**Element**</span></span>|<span data-ttu-id="e077e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e077e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e077e-113">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="e077e-113">FlagStatus</span></span>](flagstatus.md) <br/> |<span data-ttu-id="e077e-114">Contiene el estado del indicador agregados por los elementos en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="e077e-114">Contains the aggregated flag status for items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="e077e-115">StartDate</span><span class="sxs-lookup"><span data-stu-id="e077e-115">StartDate</span></span>](startdate.md) <br/> |<span data-ttu-id="e077e-116">Representa la fecha de inicio de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e077e-116">Represents the start date of an item.</span></span>  <br/> |
|[<span data-ttu-id="e077e-117">DueDate</span><span class="sxs-lookup"><span data-stu-id="e077e-117">DueDate</span></span>](duedate.md) <br/> |<span data-ttu-id="e077e-118">Representa la fecha de vencimiento de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e077e-118">Represents the date when an item is due.</span></span>  <br/> |
|[<span data-ttu-id="e077e-119">CompleteDate</span><span class="sxs-lookup"><span data-stu-id="e077e-119">CompleteDate</span></span>](completedate.md) <br/> |<span data-ttu-id="e077e-120">Representa la fecha en que se completó un elemento.</span><span class="sxs-lookup"><span data-stu-id="e077e-120">Represents the date on which an item was completed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e077e-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e077e-121">Parent elements</span></span>

|<span data-ttu-id="e077e-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="e077e-122">**Element**</span></span>|<span data-ttu-id="e077e-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e077e-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e077e-124">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="e077e-124">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="e077e-125">Contiene una única acción que se aplicará a una conversación único.</span><span class="sxs-lookup"><span data-stu-id="e077e-125">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="e077e-126">Item</span><span class="sxs-lookup"><span data-stu-id="e077e-126">Item</span></span>](item.md) <br/> |<span data-ttu-id="e077e-127">Representa un elemento genérico en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e077e-127">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e077e-128">Notas</span><span class="sxs-lookup"><span data-stu-id="e077e-128">Remarks</span></span>

<span data-ttu-id="e077e-129">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e077e-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e077e-130">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e077e-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e077e-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e077e-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e077e-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e077e-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e077e-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e077e-133">Schema Name</span></span>  <br/> |<span data-ttu-id="e077e-134">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="e077e-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="e077e-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e077e-135">Validation File</span></span>  <br/> |<span data-ttu-id="e077e-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e077e-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="e077e-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e077e-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e077e-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="e077e-138">See also</span></span>



- [<span data-ttu-id="e077e-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e077e-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
