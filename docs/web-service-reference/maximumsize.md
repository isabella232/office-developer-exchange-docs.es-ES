---
title: Tamañomáximo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fb7c3ab3-ef97-44c7-83e0-93cfe8c48e84
description: El elemento MaximumSize representa el tamaño máximo que debe tener un mensaje para que se aplique la condición o excepción.
ms.openlocfilehash: 250e0c6aed37b934f5cf6eaed9d93b9f56159d93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461754"
---
# <a name="maximumsize"></a><span data-ttu-id="735ee-103">Tamañomáximo</span><span class="sxs-lookup"><span data-stu-id="735ee-103">MaximumSize</span></span>

<span data-ttu-id="735ee-104">El elemento **MaximumSize** representa el tamaño máximo que debe tener un mensaje para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="735ee-104">The **MaximumSize** element represents the maximum size that a message must be in order for the condition or exception to apply.</span></span> 
  
```XML
<Maximum/>
```

 <span data-ttu-id="735ee-105">**int**</span><span class="sxs-lookup"><span data-stu-id="735ee-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="735ee-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="735ee-106">Attributes and elements</span></span>

<span data-ttu-id="735ee-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="735ee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="735ee-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="735ee-108">Attributes</span></span>

<span data-ttu-id="735ee-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="735ee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="735ee-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="735ee-110">Child elements</span></span>

<span data-ttu-id="735ee-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="735ee-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="735ee-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="735ee-112">Parent elements</span></span>

|<span data-ttu-id="735ee-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="735ee-113">**Element**</span></span>|<span data-ttu-id="735ee-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="735ee-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="735ee-115">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="735ee-115">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="735ee-116">Especifica los tamaños máximos y mínimos que los mensajes entrantes deben tener en orden para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="735ee-116">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="735ee-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="735ee-117">Text value</span></span>

<span data-ttu-id="735ee-118">El valor de texto es un número entero que identifica el tamaño máximo del mensaje en bytes.</span><span class="sxs-lookup"><span data-stu-id="735ee-118">The text value is an integer that identifies the maximum size of the message in bytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="735ee-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="735ee-119">Remarks</span></span>

<span data-ttu-id="735ee-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="735ee-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="735ee-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="735ee-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="735ee-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="735ee-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="735ee-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="735ee-123">Schema Name</span></span>  <br/> |<span data-ttu-id="735ee-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="735ee-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="735ee-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="735ee-125">Validation File</span></span>  <br/> |<span data-ttu-id="735ee-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="735ee-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="735ee-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="735ee-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="735ee-128">Verdadero</span><span class="sxs-lookup"><span data-stu-id="735ee-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="735ee-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="735ee-129">See also</span></span>



[<span data-ttu-id="735ee-130">MinimumSize</span><span class="sxs-lookup"><span data-stu-id="735ee-130">MinimumSize</span></span>](minimumsize.md)


- [<span data-ttu-id="735ee-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="735ee-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

