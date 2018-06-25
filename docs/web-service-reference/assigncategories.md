---
title: AssignCategories
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AssignCategories
api_type:
- schema
ms.assetid: f5c73fed-7b00-446d-8296-71a0c86e7fc6
description: El elemento AssignCategories representa las categorías que están marcadas en mensajes de correo electrónico.
ms.openlocfilehash: 96c77306d649677c1be745e8cadc2886e4a84c8a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763557"
---
# <a name="assigncategories"></a><span data-ttu-id="417a7-103">AssignCategories</span><span class="sxs-lookup"><span data-stu-id="417a7-103">AssignCategories</span></span>

<span data-ttu-id="417a7-104">El elemento **AssignCategories** representa las categorías que están marcadas en mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="417a7-104">The **AssignCategories** element represents the categories that are stamped on e-mail messages.</span></span> 
  
- [<span data-ttu-id="417a7-105">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="417a7-105">Rule (RuleType)</span></span>](rule-ruletype.md)
  
- [<span data-ttu-id="417a7-106">Acciones</span><span class="sxs-lookup"><span data-stu-id="417a7-106">Actions</span></span>](actions.md)
  
```XML
<AssignCategories>
   <String/>
</AssignCategories>
```

 <span data-ttu-id="417a7-107">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="417a7-107">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="417a7-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="417a7-108">Attributes and elements</span></span>

<span data-ttu-id="417a7-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="417a7-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="417a7-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="417a7-110">Attributes</span></span>

<span data-ttu-id="417a7-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="417a7-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="417a7-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="417a7-112">Child elements</span></span>

|<span data-ttu-id="417a7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="417a7-113">**Element**</span></span>|<span data-ttu-id="417a7-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="417a7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="417a7-115">String</span><span class="sxs-lookup"><span data-stu-id="417a7-115">String</span></span>](string.md) <br/> |<span data-ttu-id="417a7-116">Contiene una cadena que identifica una única categoría.</span><span class="sxs-lookup"><span data-stu-id="417a7-116">Contains a string that identifies a single category.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="417a7-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="417a7-117">Parent elements</span></span>

|<span data-ttu-id="417a7-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="417a7-118">**Element**</span></span>|<span data-ttu-id="417a7-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="417a7-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="417a7-120">Acciones</span><span class="sxs-lookup"><span data-stu-id="417a7-120">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="417a7-121">Representa el conjunto de acciones que están disponibles para ser tomadas en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="417a7-121">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="417a7-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="417a7-122">Text value</span></span>

<span data-ttu-id="417a7-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="417a7-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="417a7-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="417a7-124">Remarks</span></span>

<span data-ttu-id="417a7-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="417a7-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="417a7-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="417a7-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="417a7-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="417a7-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="417a7-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="417a7-128">Schema Name</span></span>  <br/> |<span data-ttu-id="417a7-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="417a7-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="417a7-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="417a7-130">Validation File</span></span>  <br/> |<span data-ttu-id="417a7-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="417a7-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="417a7-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="417a7-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="417a7-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="417a7-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="417a7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="417a7-134">See also</span></span>

- [<span data-ttu-id="417a7-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="417a7-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

