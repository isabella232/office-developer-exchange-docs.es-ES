---
title: ItemClasses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemClasses
api_type:
- schema
ms.assetid: f95430cc-2860-47c1-af2d-8c4156c9b281
description: El elemento ItemClasses representa las clases de elementos que se deben estampar en los mensajes entrantes para que se aplique la condición o excepción.
ms.openlocfilehash: 56b99cad2abef0a9953e1793e5b633acca83a9eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460116"
---
# <a name="itemclasses"></a><span data-ttu-id="55353-103">ItemClasses</span><span class="sxs-lookup"><span data-stu-id="55353-103">ItemClasses</span></span>

<span data-ttu-id="55353-104">El elemento **ItemClasses** representa las clases de elementos que se deben estampar en los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="55353-104">The **ItemClasses** element represents the item classes that must be stamped on incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ItemClasses>
    <String/>
</ItemClasses>
```

 <span data-ttu-id="55353-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="55353-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="55353-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="55353-106">Attributes and elements</span></span>

<span data-ttu-id="55353-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="55353-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="55353-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="55353-108">Attributes</span></span>

<span data-ttu-id="55353-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="55353-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="55353-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="55353-110">Child elements</span></span>

|<span data-ttu-id="55353-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="55353-111">**Element**</span></span>|<span data-ttu-id="55353-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55353-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55353-113">String</span><span class="sxs-lookup"><span data-stu-id="55353-113">String</span></span>](string.md) <br/> |<span data-ttu-id="55353-114">Representa una clase de elemento único.</span><span class="sxs-lookup"><span data-stu-id="55353-114">Represents a single item class.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="55353-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="55353-115">Parent elements</span></span>

|<span data-ttu-id="55353-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="55353-116">**Element**</span></span>|<span data-ttu-id="55353-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55353-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55353-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="55353-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="55353-119">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="55353-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="55353-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="55353-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="55353-121">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="55353-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="55353-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="55353-122">Text value</span></span>

<span data-ttu-id="55353-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="55353-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="55353-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="55353-124">Remarks</span></span>

<span data-ttu-id="55353-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="55353-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="55353-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="55353-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55353-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="55353-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="55353-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="55353-128">Schema name</span></span>  <br/> |<span data-ttu-id="55353-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="55353-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="55353-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="55353-130">Validation file</span></span>  <br/> |<span data-ttu-id="55353-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="55353-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="55353-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="55353-132">Can be empty</span></span>  <br/> |<span data-ttu-id="55353-133">Falso</span><span class="sxs-lookup"><span data-stu-id="55353-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55353-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="55353-134">See also</span></span>



- [<span data-ttu-id="55353-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="55353-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

