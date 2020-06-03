---
title: Moderadores
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 01057872-4f1a-4246-86ba-73d10ef854a0
description: El elemento Presenter especifica los moderadores de una reunión en línea.
ms.openlocfilehash: 0236457020dfc4684569e84d3d54e357af00d102
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529913"
---
# <a name="presenters"></a><span data-ttu-id="aa0b0-103">Moderadores</span><span class="sxs-lookup"><span data-stu-id="aa0b0-103">Presenters</span></span>

<span data-ttu-id="aa0b0-104">El elemento **Presenter** especifica los moderadores de una reunión en línea.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-104">The **Presenters** element specifies the presenters for an online meeting.</span></span> 
  
```XML
<Presenters> Disabled | Internal | Everyone </Presenters>
```

 <span data-ttu-id="aa0b0-105">**PresentersType**</span><span class="sxs-lookup"><span data-stu-id="aa0b0-105">**PresentersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa0b0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="aa0b0-106">Attributes and elements</span></span>

<span data-ttu-id="aa0b0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa0b0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="aa0b0-108">Attributes</span></span>

<span data-ttu-id="aa0b0-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa0b0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aa0b0-110">Child elements</span></span>

<span data-ttu-id="aa0b0-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="aa0b0-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="aa0b0-112">Parent elements</span></span>

[<span data-ttu-id="aa0b0-113">OnlineMeetingSettings</span><span class="sxs-lookup"><span data-stu-id="aa0b0-113">OnlineMeetingSettings</span></span>](onlinemeetingsettings.md)
  
## <a name="text-value"></a><span data-ttu-id="aa0b0-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="aa0b0-114">Text value</span></span>

<span data-ttu-id="aa0b0-115">El valor de texto del elemento **presenters** es el tipo de usuario que puede ser un moderador para una reunión en línea.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-115">The text value of **Presenters** element is the type of users that can be a presenter for an online meeting.</span></span> <span data-ttu-id="aa0b0-116">En la tabla siguiente se describen los valores de texto para el elemento **Presenter** .</span><span class="sxs-lookup"><span data-stu-id="aa0b0-116">The text values for the **Presenters** element are described in the following table.</span></span> 
  
<span data-ttu-id="aa0b0-117">**Valores de texto del elemento Presenter**</span><span class="sxs-lookup"><span data-stu-id="aa0b0-117">**Presenters element text values**</span></span>

|<span data-ttu-id="aa0b0-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="aa0b0-118">**Value**</span></span>|<span data-ttu-id="aa0b0-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aa0b0-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aa0b0-120">Deshabilitado</span><span class="sxs-lookup"><span data-stu-id="aa0b0-120">Disabled</span></span>  <br/> |<span data-ttu-id="aa0b0-121">Los moderadores están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-121">Presenters are disabled.</span></span>  <br/> |
|<span data-ttu-id="aa0b0-122">Interno</span><span class="sxs-lookup"><span data-stu-id="aa0b0-122">Internal</span></span>  <br/> |<span data-ttu-id="aa0b0-123">Solo los participantes internos pueden ser moderadores.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-123">Only internal participants can be presenters.</span></span>  <br/> |
|<span data-ttu-id="aa0b0-124">Todos</span><span class="sxs-lookup"><span data-stu-id="aa0b0-124">Everyone</span></span>  <br/> |<span data-ttu-id="aa0b0-125">Cualquier participante puede ser un moderador.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-125">Any participant can be a presenter.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa0b0-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa0b0-126">Remarks</span></span>

<span data-ttu-id="aa0b0-127">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="aa0b0-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aa0b0-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="aa0b0-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa0b0-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa0b0-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aa0b0-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="aa0b0-131">Schema name</span></span>  <br/> |<span data-ttu-id="aa0b0-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="aa0b0-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="aa0b0-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="aa0b0-133">Validation file</span></span>  <br/> |<span data-ttu-id="aa0b0-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="aa0b0-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aa0b0-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="aa0b0-135">Can be empty</span></span>  <br/> ||
   

