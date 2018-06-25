---
title: Moderadores
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 01057872-4f1a-4246-86ba-73d10ef854a0
description: El elemento de moderadores especifica los moderadores para una reunión en línea.
ms.openlocfilehash: f62b458759e0d8199c98827602d6c3fe16aebeea
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836875"
---
# <a name="presenters"></a><span data-ttu-id="553e7-103">Moderadores</span><span class="sxs-lookup"><span data-stu-id="553e7-103">Presenters</span></span>

<span data-ttu-id="553e7-104">El elemento de **moderadores** especifica los moderadores para una reunión en línea.</span><span class="sxs-lookup"><span data-stu-id="553e7-104">The **Presenters** element specifies the presenters for an online meeting.</span></span> 
  
```XML
<Presenters> Disabled | Internal | Everyone </Presenters>
```

 <span data-ttu-id="553e7-105">**PresentersType**</span><span class="sxs-lookup"><span data-stu-id="553e7-105">**PresentersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="553e7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="553e7-106">Attributes and elements</span></span>

<span data-ttu-id="553e7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="553e7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="553e7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="553e7-108">Attributes</span></span>

<span data-ttu-id="553e7-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="553e7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="553e7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="553e7-110">Child elements</span></span>

<span data-ttu-id="553e7-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="553e7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="553e7-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="553e7-112">Parent elements</span></span>

[<span data-ttu-id="553e7-113">OnlineMeetingSettings</span><span class="sxs-lookup"><span data-stu-id="553e7-113">OnlineMeetingSettings</span></span>](onlinemeetingsettings.md)
  
## <a name="text-value"></a><span data-ttu-id="553e7-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="553e7-114">Text value</span></span>

<span data-ttu-id="553e7-115">El valor de texto del elemento de **moderadores** es el tipo de usuarios que puede ser un moderador para una reunión en línea.</span><span class="sxs-lookup"><span data-stu-id="553e7-115">The text value of **Presenters** element is the type of users that can be a presenter for an online meeting.</span></span> <span data-ttu-id="553e7-116">En la siguiente tabla, se describen los valores de texto para el elemento de **moderadores** .</span><span class="sxs-lookup"><span data-stu-id="553e7-116">The text values for the **Presenters** element are described in the following table.</span></span> 
  
<span data-ttu-id="553e7-117">**Valores de texto del elemento de moderadores**</span><span class="sxs-lookup"><span data-stu-id="553e7-117">**Presenters element text values**</span></span>

|<span data-ttu-id="553e7-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="553e7-118">**Value**</span></span>|<span data-ttu-id="553e7-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="553e7-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="553e7-120">Deshabilitado</span><span class="sxs-lookup"><span data-stu-id="553e7-120">Disabled</span></span>  <br/> |<span data-ttu-id="553e7-121">Se deshabilitan los moderadores.</span><span class="sxs-lookup"><span data-stu-id="553e7-121">Presenters are disabled.</span></span>  <br/> |
|<span data-ttu-id="553e7-122">Interno</span><span class="sxs-lookup"><span data-stu-id="553e7-122">Internal</span></span>  <br/> |<span data-ttu-id="553e7-123">Sólo los participantes internos pueden ser moderadores.</span><span class="sxs-lookup"><span data-stu-id="553e7-123">Only internal participants can be presenters.</span></span>  <br/> |
|<span data-ttu-id="553e7-124">Todos los usuarios</span><span class="sxs-lookup"><span data-stu-id="553e7-124">Everyone</span></span>  <br/> |<span data-ttu-id="553e7-125">Cualquier participante puede ser un moderador.</span><span class="sxs-lookup"><span data-stu-id="553e7-125">Any participant can be a presenter.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="553e7-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="553e7-126">Remarks</span></span>

<span data-ttu-id="553e7-127">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="553e7-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="553e7-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="553e7-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="553e7-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="553e7-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="553e7-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="553e7-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="553e7-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="553e7-131">Schema name</span></span>  <br/> |<span data-ttu-id="553e7-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="553e7-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="553e7-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="553e7-133">Validation file</span></span>  <br/> |<span data-ttu-id="553e7-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="553e7-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="553e7-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="553e7-135">Can be empty</span></span>  <br/> ||
   

