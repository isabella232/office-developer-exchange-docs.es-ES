---
title: Condición (RestrictionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4fdb373e-bf1b-4cb0-bbfb-444c6c6cec50
description: El elemento Condition especifica la condición que se usa para identificar el final de una búsqueda de una operación FindItem o FindConversation.
ms.openlocfilehash: 00c5b5e615ed9b253c79dae9dc2b89c797853089
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463940"
---
# <a name="condition-restrictiontype"></a><span data-ttu-id="ef0b0-103">Condición (RestrictionType)</span><span class="sxs-lookup"><span data-stu-id="ef0b0-103">Condition (RestrictionType)</span></span>

<span data-ttu-id="ef0b0-104">El elemento **Condition** especifica la condición que se usa para identificar el final de una búsqueda de una operación **FindItem** o **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="ef0b0-104">The **Condition** element specifies the condition that is used to identify the end of a search for a **FindItem** or a **FindConversation** operation.</span></span> 
  
```XML
<Condition>
    <SearchExpression></SearchExpression>
</Condition>
```

 <span data-ttu-id="ef0b0-105">**RestrictionType**</span><span class="sxs-lookup"><span data-stu-id="ef0b0-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef0b0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ef0b0-106">Attributes and elements</span></span>

<span data-ttu-id="ef0b0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ef0b0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef0b0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ef0b0-108">Attributes</span></span>

<span data-ttu-id="ef0b0-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ef0b0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef0b0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ef0b0-110">Child elements</span></span>

|<span data-ttu-id="ef0b0-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ef0b0-111">**Element**</span></span>|<span data-ttu-id="ef0b0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef0b0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef0b0-113">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="ef0b0-113">SearchExpression</span></span>](searchexpression.md) <br/> |<span data-ttu-id="ef0b0-114">Elemento abstracto que representa el elemento sustituido dentro de una restricción.</span><span class="sxs-lookup"><span data-stu-id="ef0b0-114">Abstract element that represents the substituted element within a restriction.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ef0b0-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ef0b0-115">Parent elements</span></span>

|<span data-ttu-id="ef0b0-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ef0b0-116">**Element**</span></span>|<span data-ttu-id="ef0b0-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef0b0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef0b0-118">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="ef0b0-118">SeekToConditionPageItemView</span></span>](seektoconditionpageitemview.md) <br/> |<span data-ttu-id="ef0b0-119">Identifica la condición que se usa para identificar el final de una búsqueda, el índice inicial de una búsqueda, las entradas máximas que se devolverán y las direcciones de búsqueda de una operación **FindItem** o **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="ef0b0-119">Identifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or a **FindConversation** operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef0b0-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ef0b0-120">Remarks</span></span>

<span data-ttu-id="ef0b0-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ef0b0-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ef0b0-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef0b0-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef0b0-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ef0b0-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef0b0-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef0b0-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ef0b0-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ef0b0-125">Schema Name</span></span>  <br/> |<span data-ttu-id="ef0b0-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="ef0b0-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="ef0b0-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ef0b0-127">Validation File</span></span>  <br/> |<span data-ttu-id="ef0b0-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ef0b0-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="ef0b0-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ef0b0-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ef0b0-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef0b0-130">See also</span></span>



- [<span data-ttu-id="ef0b0-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ef0b0-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

