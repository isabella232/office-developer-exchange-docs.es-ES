---
title: SortOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SortOrder
api_type:
- schema
ms.assetid: c2413f0b-8c03-46ae-9990-13338b3c53a6
description: El elemento SortOrder define cómo se ordenan los elementos en una solicitud FindItem o FindConversation.
ms.openlocfilehash: b520bb3ca6daadc777e7235b2b7420a12e425048
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468372"
---
# <a name="sortorder"></a><span data-ttu-id="cdca0-103">SortOrder</span><span class="sxs-lookup"><span data-stu-id="cdca0-103">SortOrder</span></span>

<span data-ttu-id="cdca0-104">El elemento **SortOrder** define cómo se ordenan los elementos en una solicitud **FindItem** o **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="cdca0-104">The **SortOrder** element defines how items are sorted in a **FindItem** or **FindConversation** request.</span></span> 
  
```xml
<SortOrder>
   <FieldOrder/>
</SortOrder>
```

 <span data-ttu-id="cdca0-105">**NonEmptyArrayOfFieldOrdersType**</span><span class="sxs-lookup"><span data-stu-id="cdca0-105">**NonEmptyArrayOfFieldOrdersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cdca0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cdca0-106">Attributes and elements</span></span>

<span data-ttu-id="cdca0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cdca0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cdca0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cdca0-108">Attributes</span></span>

<span data-ttu-id="cdca0-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cdca0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cdca0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cdca0-110">Child elements</span></span>

|<span data-ttu-id="cdca0-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cdca0-111">**Element**</span></span>|<span data-ttu-id="cdca0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cdca0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cdca0-113">FieldOrder</span><span class="sxs-lookup"><span data-stu-id="cdca0-113">FieldOrder</span></span>](fieldorder.md) <br/> |<span data-ttu-id="cdca0-114">Representa un solo campo por el que se ordenan los resultados e indica la dirección de la ordenación.</span><span class="sxs-lookup"><span data-stu-id="cdca0-114">Represents a single field by which to sort results and indicates the direction for the sort.</span></span> <span data-ttu-id="cdca0-115">Se pueden incluir uno o varios de estos elementos.</span><span class="sxs-lookup"><span data-stu-id="cdca0-115">One or more of these elements may be included.</span></span> <span data-ttu-id="cdca0-116">Los elementos [FieldOrder](fieldorder.md) se aplican en el orden especificado para la ordenación.</span><span class="sxs-lookup"><span data-stu-id="cdca0-116">[FieldOrder](fieldorder.md) elements are applied in the order specified for sorting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cdca0-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cdca0-117">Parent elements</span></span>

|<span data-ttu-id="cdca0-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cdca0-118">**Element**</span></span>|<span data-ttu-id="cdca0-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cdca0-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cdca0-120">FindItem</span><span class="sxs-lookup"><span data-stu-id="cdca0-120">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="cdca0-121">Define una solicitud para buscar elementos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="cdca0-121">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="cdca0-122">La siguiente es la expresión XPath a este elemento:`/FindItem`</span><span class="sxs-lookup"><span data-stu-id="cdca0-122">The following is the XPath expression to this element:  `/FindItem`</span></span> <br/> |
|[<span data-ttu-id="cdca0-123">FindConversation</span><span class="sxs-lookup"><span data-stu-id="cdca0-123">FindConversation</span></span>](findconversation.md) <br/> |<span data-ttu-id="cdca0-124">Define una solicitud para buscar conversaciones en un buzón.</span><span class="sxs-lookup"><span data-stu-id="cdca0-124">Defines a request to find conversations in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cdca0-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cdca0-125">Text value</span></span>

<span data-ttu-id="cdca0-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cdca0-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cdca0-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cdca0-127">Remarks</span></span>

<span data-ttu-id="cdca0-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="cdca0-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cdca0-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cdca0-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cdca0-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="cdca0-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cdca0-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cdca0-131">Schema Name</span></span>  <br/> |<span data-ttu-id="cdca0-132">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="cdca0-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cdca0-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cdca0-133">Validation File</span></span>  <br/> |<span data-ttu-id="cdca0-134">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cdca0-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cdca0-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cdca0-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="cdca0-136">Falso</span><span class="sxs-lookup"><span data-stu-id="cdca0-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cdca0-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdca0-137">See also</span></span>



[<span data-ttu-id="cdca0-138">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="cdca0-138">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="cdca0-139">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="cdca0-139">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="cdca0-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cdca0-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

