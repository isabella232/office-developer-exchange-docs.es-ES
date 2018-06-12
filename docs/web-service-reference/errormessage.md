---
title: ErrorMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cec33a6-4b10-4259-8ac3-3f39a642b34c
description: El elemento ErrorMessage representa la razón para el error de validación.
ms.openlocfilehash: d1869041254ef7c661fb2acb7c9c2ccaf628b394
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764448"
---
# <a name="errormessage"></a><span data-ttu-id="cc243-103">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="cc243-103">ErrorMessage</span></span>

<span data-ttu-id="cc243-104">El elemento **ErrorMessage** representa la razón para el error de validación.</span><span class="sxs-lookup"><span data-stu-id="cc243-104">The **ErrorMessage** element represents the reason for the validation error.</span></span> 
  
```XML
<ErrorMessage/>
```

 <span data-ttu-id="cc243-105">**String**</span><span class="sxs-lookup"><span data-stu-id="cc243-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cc243-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cc243-106">Attributes and elements</span></span>

<span data-ttu-id="cc243-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cc243-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cc243-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cc243-108">Attributes</span></span>

<span data-ttu-id="cc243-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cc243-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cc243-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cc243-110">Child elements</span></span>

<span data-ttu-id="cc243-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cc243-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cc243-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cc243-112">Parent elements</span></span>

|<span data-ttu-id="cc243-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="cc243-113">**Element**</span></span>|<span data-ttu-id="cc243-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc243-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cc243-115">Error</span><span class="sxs-lookup"><span data-stu-id="cc243-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="cc243-116">Representa un error de validación único en un valor de la propiedad de regla concreto, valor de la propiedad predicado o valor de la propiedad acción.</span><span class="sxs-lookup"><span data-stu-id="cc243-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cc243-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cc243-117">Text value</span></span>

<span data-ttu-id="cc243-118">El mensaje de error asociado al error de validación de regla.</span><span class="sxs-lookup"><span data-stu-id="cc243-118">The error message associated with the rule validation error.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cc243-119">Notas</span><span class="sxs-lookup"><span data-stu-id="cc243-119">Remarks</span></span>

<span data-ttu-id="cc243-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="cc243-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc243-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cc243-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc243-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cc243-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cc243-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cc243-123">Schema Name</span></span>  <br/> |<span data-ttu-id="cc243-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="cc243-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cc243-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cc243-125">Validation File</span></span>  <br/> |<span data-ttu-id="cc243-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cc243-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cc243-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cc243-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="cc243-128">Verdadero</span><span class="sxs-lookup"><span data-stu-id="cc243-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cc243-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="cc243-129">See also</span></span>



- [<span data-ttu-id="cc243-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="cc243-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

