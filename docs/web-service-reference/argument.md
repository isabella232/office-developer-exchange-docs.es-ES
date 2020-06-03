---
title: Argumento
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Argument
api_type:
- schema
ms.assetid: 15b0bfb8-2448-4ceb-aeac-965115e0fb72
description: El elemento argument especifica los argumentos de la acción.
ms.openlocfilehash: 41e3b1d891610669b0cc93f3daf6e8ee98c48396
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464759"
---
# <a name="argument"></a><span data-ttu-id="0c1e0-103">Argumento</span><span class="sxs-lookup"><span data-stu-id="0c1e0-103">Argument</span></span>

<span data-ttu-id="0c1e0-104">El elemento **argument** especifica los argumentos de la acción.</span><span class="sxs-lookup"><span data-stu-id="0c1e0-104">The **Argument** element specifies arguments to the action.</span></span> 
  
```xml
<Argument Value=""/>
```

 <span data-ttu-id="0c1e0-105">**ProtectionRuleArgumentType**</span><span class="sxs-lookup"><span data-stu-id="0c1e0-105">**ProtectionRuleArgumentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0c1e0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0c1e0-106">Attributes and elements</span></span>

<span data-ttu-id="0c1e0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0c1e0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c1e0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0c1e0-108">Attributes</span></span>

|<span data-ttu-id="0c1e0-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="0c1e0-109">**Attribute**</span></span>|<span data-ttu-id="0c1e0-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0c1e0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0c1e0-111">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0c1e0-111">**Value**</span></span> <br/> |<span data-ttu-id="0c1e0-112">Un valor de tipo String que no está vacío que representa el valor de un argumento para la parte de acción de una regla de protección.</span><span class="sxs-lookup"><span data-stu-id="0c1e0-112">A non-empty string value that represents the value of an argument to the action part of a protection rule.</span></span> <span data-ttu-id="0c1e0-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0c1e0-113">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0c1e0-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0c1e0-114">Child elements</span></span>

<span data-ttu-id="0c1e0-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0c1e0-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0c1e0-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0c1e0-116">Parent elements</span></span>

|<span data-ttu-id="0c1e0-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0c1e0-117">**Element**</span></span>|<span data-ttu-id="0c1e0-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0c1e0-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c1e0-119">Acción (ProtectionRuleActionType)</span><span class="sxs-lookup"><span data-stu-id="0c1e0-119">Action (ProtectionRuleActionType)</span></span>](action-protectionruleactiontype.md) <br/> |<span data-ttu-id="0c1e0-120">Identifica qué acción debe ejecutarse si la parte de condición de la regla coincide.</span><span class="sxs-lookup"><span data-stu-id="0c1e0-120">Identifies what action must be executed if the condition part of the rule matches.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0c1e0-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0c1e0-121">Text value</span></span>

<span data-ttu-id="0c1e0-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0c1e0-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0c1e0-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0c1e0-123">Remarks</span></span>

<span data-ttu-id="0c1e0-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0c1e0-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0c1e0-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0c1e0-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c1e0-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c1e0-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0c1e0-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0c1e0-127">Schema Name</span></span>  <br/> |<span data-ttu-id="0c1e0-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0c1e0-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="0c1e0-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0c1e0-129">Validation File</span></span>  <br/> |<span data-ttu-id="0c1e0-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="0c1e0-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0c1e0-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0c1e0-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="0c1e0-132">Falso</span><span class="sxs-lookup"><span data-stu-id="0c1e0-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c1e0-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c1e0-133">See also</span></span>

- [<span data-ttu-id="0c1e0-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0c1e0-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

