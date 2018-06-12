---
title: Condición (RestrictionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4fdb373e-bf1b-4cb0-bbfb-444c6c6cec50
description: El elemento Condition especifica la condición que se usa para identificar el final de una búsqueda para un FindItem o una operación de FindConversation.
ms.openlocfilehash: 513fc21be52a90698f1c292d6d20d7cdaab07371
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763762"
---
# <a name="condition-restrictiontype"></a><span data-ttu-id="3f81d-103">Condición (RestrictionType)</span><span class="sxs-lookup"><span data-stu-id="3f81d-103">Condition (RestrictionType)</span></span>

<span data-ttu-id="3f81d-104">El elemento **Condition** especifica la condición que se usa para identificar el final de una búsqueda para un **FindItem** o una operación de **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="3f81d-104">The **Condition** element specifies the condition that is used to identify the end of a search for a **FindItem** or a **FindConversation** operation.</span></span> 
  
```XML
<Condition>
    <SearchExpression></SearchExpression>
</Condition>
```

 <span data-ttu-id="3f81d-105">**RestrictionType**</span><span class="sxs-lookup"><span data-stu-id="3f81d-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3f81d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3f81d-106">Attributes and elements</span></span>

<span data-ttu-id="3f81d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3f81d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3f81d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3f81d-108">Attributes</span></span>

<span data-ttu-id="3f81d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3f81d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3f81d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3f81d-110">Child elements</span></span>

|<span data-ttu-id="3f81d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f81d-111">**Element**</span></span>|<span data-ttu-id="3f81d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f81d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f81d-113">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="3f81d-113">SearchExpression</span></span>](searchexpression.md) <br/> |<span data-ttu-id="3f81d-114">Elemento abstracta que representa el elemento sustituido dentro de una restricción.</span><span class="sxs-lookup"><span data-stu-id="3f81d-114">Abstract element that represents the substituted element within a restriction.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3f81d-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3f81d-115">Parent elements</span></span>

|<span data-ttu-id="3f81d-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f81d-116">**Element**</span></span>|<span data-ttu-id="3f81d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f81d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3f81d-118">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="3f81d-118">SeekToConditionPageItemView</span></span>](seektoconditionpageitemview.md) <br/> |<span data-ttu-id="3f81d-119">Identifica la condición que se usa para identificar el final de una búsqueda, el índice de inicio de una búsqueda, las entradas máximas para devolver y las instrucciones de búsqueda para un **FindItem** o una operación de **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="3f81d-119">Identifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or a **FindConversation** operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f81d-120">Notas</span><span class="sxs-lookup"><span data-stu-id="3f81d-120">Remarks</span></span>

<span data-ttu-id="3f81d-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3f81d-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3f81d-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3f81d-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3f81d-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3f81d-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f81d-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3f81d-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3f81d-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3f81d-125">Schema Name</span></span>  <br/> |<span data-ttu-id="3f81d-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="3f81d-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="3f81d-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3f81d-127">Validation File</span></span>  <br/> |<span data-ttu-id="3f81d-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3f81d-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3f81d-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3f81d-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3f81d-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="3f81d-130">See also</span></span>



- [<span data-ttu-id="3f81d-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3f81d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

