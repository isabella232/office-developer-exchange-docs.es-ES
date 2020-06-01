---
title: WithinSizeRange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WithinSizeRange
api_type:
- schema
ms.assetid: 6f98650e-3399-4f87-9b7f-40bf20cdb821
description: El elemento WithinSizeRange especifica los tamaños máximo y mínimo que los mensajes entrantes deben tener en orden para que se aplique la condición o excepción.
ms.openlocfilehash: 31da5815b70e20c47594da89b0b7ccab87eaf8f3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459745"
---
# <a name="withinsizerange"></a><span data-ttu-id="b8d0c-103">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="b8d0c-103">WithinSizeRange</span></span>

<span data-ttu-id="b8d0c-104">El elemento **WithinSizeRange** especifica los tamaños máximo y mínimo que los mensajes entrantes deben tener en orden para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="b8d0c-104">The **WithinSizeRange** element specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span> 
  
```XML
<WithinSizeRange>
     <MinimumSize/>
     <MaximumSize/>
</WithinSizeRange>
```

 <span data-ttu-id="b8d0c-105">**RulePredicateSizeRangeType**</span><span class="sxs-lookup"><span data-stu-id="b8d0c-105">**RulePredicateSizeRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b8d0c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b8d0c-106">Attributes and elements</span></span>

<span data-ttu-id="b8d0c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b8d0c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8d0c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b8d0c-108">Attributes</span></span>

<span data-ttu-id="b8d0c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b8d0c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b8d0c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b8d0c-110">Child elements</span></span>

|<span data-ttu-id="b8d0c-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b8d0c-111">**Element**</span></span>|<span data-ttu-id="b8d0c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8d0c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8d0c-113">MinimumSize</span><span class="sxs-lookup"><span data-stu-id="b8d0c-113">MinimumSize</span></span>](minimumsize.md) <br/> |<span data-ttu-id="b8d0c-114">Especifica el tamaño mínimo que debe tener un mensaje para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="b8d0c-114">Specifies the minimum size that a message must be in order for the condition or exception to apply.</span></span>  <br/> |
|[<span data-ttu-id="b8d0c-115">Tamañomáximo</span><span class="sxs-lookup"><span data-stu-id="b8d0c-115">MaximumSize</span></span>](maximumsize.md) <br/> |<span data-ttu-id="b8d0c-116">Especifica el tamaño máximo que debe tener un mensaje para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="b8d0c-116">Specifies the maximum size that a message must be in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b8d0c-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b8d0c-117">Parent elements</span></span>

|<span data-ttu-id="b8d0c-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b8d0c-118">**Element**</span></span>|<span data-ttu-id="b8d0c-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8d0c-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8d0c-120">Condiciones</span><span class="sxs-lookup"><span data-stu-id="b8d0c-120">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="b8d0c-121">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="b8d0c-121">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="b8d0c-122">Excepciones</span><span class="sxs-lookup"><span data-stu-id="b8d0c-122">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="b8d0c-123">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="b8d0c-123">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b8d0c-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b8d0c-124">Text value</span></span>

<span data-ttu-id="b8d0c-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b8d0c-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b8d0c-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b8d0c-126">Remarks</span></span>

<span data-ttu-id="b8d0c-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b8d0c-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8d0c-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b8d0c-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8d0c-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8d0c-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b8d0c-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b8d0c-130">Schema Name</span></span>  <br/> |<span data-ttu-id="b8d0c-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b8d0c-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b8d0c-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b8d0c-132">Validation File</span></span>  <br/> |<span data-ttu-id="b8d0c-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b8d0c-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b8d0c-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b8d0c-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="b8d0c-135">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b8d0c-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8d0c-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8d0c-136">See also</span></span>



- [<span data-ttu-id="b8d0c-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b8d0c-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

