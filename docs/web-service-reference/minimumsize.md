---
title: MinimumSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 841d229c-140c-48bd-b3a7-21478fcea2fb
description: El elemento MinimumSize representa el tamaño mínimo que un mensaje debe estar en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: 4f80bac3b9226019ec3d726cd2d6430e02cac423
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836480"
---
# <a name="minimumsize"></a><span data-ttu-id="c7102-103">MinimumSize</span><span class="sxs-lookup"><span data-stu-id="c7102-103">MinimumSize</span></span>

<span data-ttu-id="c7102-104">El elemento **MinimumSize** representa el tamaño mínimo que un mensaje debe estar en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="c7102-104">The **MinimumSize** element represents the minimum size that a message must be in order for the condition or exception to apply.</span></span> 
  
```XML
<MinimumSize/>
```

 <span data-ttu-id="c7102-105">**int**</span><span class="sxs-lookup"><span data-stu-id="c7102-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c7102-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c7102-106">Attributes and elements</span></span>

<span data-ttu-id="c7102-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c7102-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7102-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c7102-108">Attributes</span></span>

<span data-ttu-id="c7102-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c7102-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7102-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c7102-110">Child elements</span></span>

<span data-ttu-id="c7102-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c7102-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c7102-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c7102-112">Parent elements</span></span>

|<span data-ttu-id="c7102-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c7102-113">**Element**</span></span>|<span data-ttu-id="c7102-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7102-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7102-115">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="c7102-115">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="c7102-116">Especifica los tamaños máximos y mínimos que deben ser los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="c7102-116">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c7102-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c7102-117">Text value</span></span>

<span data-ttu-id="c7102-118">El valor de texto es un entero que identifica el tamaño mínimo del mensaje en bytes.</span><span class="sxs-lookup"><span data-stu-id="c7102-118">The text value is an integer that identifies the minimum size of the message in bytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c7102-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c7102-119">Remarks</span></span>

<span data-ttu-id="c7102-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c7102-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7102-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c7102-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7102-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c7102-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c7102-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c7102-123">Schema Name</span></span>  <br/> |<span data-ttu-id="c7102-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c7102-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c7102-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c7102-125">Validation File</span></span>  <br/> |<span data-ttu-id="c7102-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c7102-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c7102-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c7102-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="c7102-128">Verdadero</span><span class="sxs-lookup"><span data-stu-id="c7102-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7102-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7102-129">See also</span></span>



[<span data-ttu-id="c7102-130">MaximumSize</span><span class="sxs-lookup"><span data-stu-id="c7102-130">MaximumSize</span></span>](maximumsize.md)


- [<span data-ttu-id="c7102-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c7102-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

