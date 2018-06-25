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
ms.openlocfilehash: e20e5eab7972616c90079786abd78a0f7fedfebe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837519"
---
# <a name="sortorder"></a><span data-ttu-id="e3cdc-103">SortOrder</span><span class="sxs-lookup"><span data-stu-id="e3cdc-103">SortOrder</span></span>

<span data-ttu-id="e3cdc-104">El elemento **SortOrder** define cómo se ordenan los elementos en una solicitud **FindItem** o **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="e3cdc-104">The **SortOrder** element defines how items are sorted in a **FindItem** or **FindConversation** request.</span></span> 
  
```xml
<SortOrder>
   <FieldOrder/>
</SortOrder>
```

 <span data-ttu-id="e3cdc-105">**NonEmptyArrayOfFieldOrdersType**</span><span class="sxs-lookup"><span data-stu-id="e3cdc-105">**NonEmptyArrayOfFieldOrdersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3cdc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e3cdc-106">Attributes and elements</span></span>

<span data-ttu-id="e3cdc-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e3cdc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3cdc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e3cdc-108">Attributes</span></span>

<span data-ttu-id="e3cdc-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e3cdc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3cdc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e3cdc-110">Child elements</span></span>

|<span data-ttu-id="e3cdc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e3cdc-111">**Element**</span></span>|<span data-ttu-id="e3cdc-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e3cdc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3cdc-113">FieldOrder</span><span class="sxs-lookup"><span data-stu-id="e3cdc-113">FieldOrder</span></span>](fieldorder.md) <br/> |<span data-ttu-id="e3cdc-114">Representa un solo campo por el que se va a ordenar los resultados y se indica la dirección para la ordenación.</span><span class="sxs-lookup"><span data-stu-id="e3cdc-114">Represents a single field by which to sort results and indicates the direction for the sort.</span></span> <span data-ttu-id="e3cdc-115">Pueden incluir uno o varios de estos elementos.</span><span class="sxs-lookup"><span data-stu-id="e3cdc-115">One or more of these elements may be included.</span></span> <span data-ttu-id="e3cdc-116">[FieldOrder](fieldorder.md) elementos se aplican en el orden especificado para la ordenación.</span><span class="sxs-lookup"><span data-stu-id="e3cdc-116">[FieldOrder](fieldorder.md) elements are applied in the order specified for sorting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e3cdc-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e3cdc-117">Parent elements</span></span>

|<span data-ttu-id="e3cdc-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="e3cdc-118">**Element**</span></span>|<span data-ttu-id="e3cdc-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e3cdc-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3cdc-120">FindItem</span><span class="sxs-lookup"><span data-stu-id="e3cdc-120">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="e3cdc-121">Define una solicitud para buscar elementos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e3cdc-121">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="e3cdc-122">La siguiente es la expresión de XPath para este elemento:`/FindItem`</span><span class="sxs-lookup"><span data-stu-id="e3cdc-122">The following is the XPath expression to this element:  `/FindItem`</span></span> <br/> |
|[<span data-ttu-id="e3cdc-123">FindConversation</span><span class="sxs-lookup"><span data-stu-id="e3cdc-123">FindConversation</span></span>](findconversation.md) <br/> |<span data-ttu-id="e3cdc-124">Define una solicitud para buscar las conversaciones en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e3cdc-124">Defines a request to find conversations in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e3cdc-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e3cdc-125">Text value</span></span>

<span data-ttu-id="e3cdc-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e3cdc-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e3cdc-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e3cdc-127">Remarks</span></span>

<span data-ttu-id="e3cdc-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e3cdc-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3cdc-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e3cdc-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3cdc-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e3cdc-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e3cdc-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e3cdc-131">Schema Name</span></span>  <br/> |<span data-ttu-id="e3cdc-132">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e3cdc-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e3cdc-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e3cdc-133">Validation File</span></span>  <br/> |<span data-ttu-id="e3cdc-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e3cdc-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e3cdc-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e3cdc-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="e3cdc-136">False</span><span class="sxs-lookup"><span data-stu-id="e3cdc-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3cdc-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3cdc-137">See also</span></span>



[<span data-ttu-id="e3cdc-138">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="e3cdc-138">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="e3cdc-139">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="e3cdc-139">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="e3cdc-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e3cdc-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

