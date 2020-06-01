---
title: MinimumSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 841d229c-140c-48bd-b3a7-21478fcea2fb
description: El elemento MinimumSize representa el tamaño mínimo que debe tener un mensaje para que se aplique la condición o excepción.
ms.openlocfilehash: b43a8b5916747c4e3e4ca9b66cf8b9d73f5f8942
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44464206"
---
# <a name="minimumsize"></a><span data-ttu-id="91dc4-103">MinimumSize</span><span class="sxs-lookup"><span data-stu-id="91dc4-103">MinimumSize</span></span>

<span data-ttu-id="91dc4-104">El elemento **MinimumSize** representa el tamaño mínimo que debe tener un mensaje para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="91dc4-104">The **MinimumSize** element represents the minimum size that a message must be in order for the condition or exception to apply.</span></span> 
  
```XML
<MinimumSize/>
```

 <span data-ttu-id="91dc4-105">**int**</span><span class="sxs-lookup"><span data-stu-id="91dc4-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="91dc4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="91dc4-106">Attributes and elements</span></span>

<span data-ttu-id="91dc4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="91dc4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91dc4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="91dc4-108">Attributes</span></span>

<span data-ttu-id="91dc4-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="91dc4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="91dc4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="91dc4-110">Child elements</span></span>

<span data-ttu-id="91dc4-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="91dc4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="91dc4-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="91dc4-112">Parent elements</span></span>

|<span data-ttu-id="91dc4-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="91dc4-113">**Element**</span></span>|<span data-ttu-id="91dc4-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="91dc4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91dc4-115">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="91dc4-115">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="91dc4-116">Especifica los tamaños máximos y mínimos que los mensajes entrantes deben tener en orden para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="91dc4-116">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="91dc4-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="91dc4-117">Text value</span></span>

<span data-ttu-id="91dc4-118">El valor de texto es un número entero que identifica el tamaño mínimo del mensaje en bytes.</span><span class="sxs-lookup"><span data-stu-id="91dc4-118">The text value is an integer that identifies the minimum size of the message in bytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="91dc4-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="91dc4-119">Remarks</span></span>

<span data-ttu-id="91dc4-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="91dc4-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="91dc4-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="91dc4-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91dc4-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="91dc4-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="91dc4-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="91dc4-123">Schema Name</span></span>  <br/> |<span data-ttu-id="91dc4-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="91dc4-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="91dc4-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="91dc4-125">Validation File</span></span>  <br/> |<span data-ttu-id="91dc4-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="91dc4-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="91dc4-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="91dc4-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="91dc4-128">Verdadero</span><span class="sxs-lookup"><span data-stu-id="91dc4-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91dc4-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="91dc4-129">See also</span></span>



[<span data-ttu-id="91dc4-130">Tamañomáximo</span><span class="sxs-lookup"><span data-stu-id="91dc4-130">MaximumSize</span></span>](maximumsize.md)


- [<span data-ttu-id="91dc4-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="91dc4-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

